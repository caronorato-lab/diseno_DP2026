🎨 DataDesign DP - Panel de Análisis de Tráfico de Diseño 2026

¡Bienvenido al proyecto DataDesign DP!

Si estás leyendo esto, es porque probablemente te diste cuenta de que llevar el control de cientos de piezas gráficas, flyers, carruseles y masacres de requerimientos en un Excel crudo no era vida para nadie. Este proyecto nace de la necesidad de tener visibilidad real sobre el rendimiento del equipo de diseño, los tiempos de entrega y, seamos honestos, para saber qué cliente interno nos está reventando a punta de solicitudes.

🚀 ¿Qué es esta belleza?

Es un Dashboard interactivo construido en React que se alimenta (idealmente) de los datos exportados de la matriz de "Cargas laborales diseño". Toma esa sábana de datos llena de fechas de recepción, asignación y entrega, y la transforma en gráficos y métricas que cualquier humano (incluso los coordinadores y "Karen Jefe") puede entender en 5 segundos sin que les dé migraña.

⚙️ Características Principales

El aplicativo está dividido en 4 módulos principales:

📊 Dashboard General: La vista de águila. Te muestra el total de solicitudes procesadas, cuántas salieron a tiempo, cuántas están con retraso y cuántas están en el limbo (pendientes).

🔍 Buscador en Tiempo Real: Un filtro poderoso. Escribe "flyer", "Lina" o "Pipo" y la tabla filtrará instantáneamente los requerimientos asociados sin tener que usar el odioso Ctrl+B de Excel.

👨‍🎨 Desempeño por Diseñador: Aquí no hay dónde esconderse. Muestra una barra de progreso visual por cada miembro del equipo indicando su volumen de trabajo y su ratio de cumplimiento (A Tiempo vs. Retrasos).

🏢 Top Solicitantes: El ranking de los clientes internos. Muestra quiénes son los que más carga laboral generan y cómo les estamos respondiendo. Útil para justificar contrataciones o poner límites.

🛠️ Stack Tecnológico

Para que no te digan que esto es magia negra, aquí está lo que usamos bajo el capó:

Frontend UI: React.js (con Hooks como useState y useMemo para que vuele).

Estilos: Tailwind CSS (por eso se ve tan moderno, con bordes redondeados y colores pastel sin tener que escribir un millón de líneas de CSS).

Íconos: Lucide React.

Procesamiento de Datos (Pre-limpieza): Python y Pandas (usado inicialmente para estandarizar las hojas del Excel, limpiar espacios basura y castear las fechas).

⚠️ La Cruda Verdad (Disclaimer de Datos)

Atención a quien mantenga este proyecto: La calidad de este dashboard depende 100% de la calidad de los datos que le metan. La lógica actual toma la fecha solicitada de entrega y la resta con la fecha entrega final. Si la diferencia es <= 0, es un éxito. Si es > 0, es un retraso.
PERO, si el equipo olvida llenar la columna de "fecha entrega final" (como pasó casi todo el mes de mayo de 2026 en los datos originales), el sistema automáticamente lo marcará como "Pendiente / Sin dato".

Si ves muchos amarillos en el dashboard, no es que el código falle, es que hay que ir a apretar tuercas con el equipo para que documenten cuando terminen una tarea.

💻 ¿Cómo correr esto localmente?

Si quieres sacar este código del Canvas interactivo y correrlo en tu máquina local, sigue estos pasos:

Asegúrate de tener Node.js instalado.

Crea un proyecto nuevo con Vite: npm create vite@latest datadesign-dp -- --template react

Entra a la carpeta: cd datadesign-dp

Instala las dependencias principales y las de íconos: npm install && npm install lucide-react

Instala Tailwind CSS siguiendo su guía oficial para Vite.

Copia el código del archivo app.jsx y pégalo en tu src/App.jsx.

Levanta el servidor: npm run dev.

¡Abre tu navegador y disfruta!

Hecho con sangre, sudor, lágrimas y mucho café para sobrevivir al cierre de mes.