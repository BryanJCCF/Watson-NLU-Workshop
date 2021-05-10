# Watson-NLU-Workshop
Natural-language understanding (NLU) es un subtema del procesamiento de lenguaje natural en la inteligencia artificial que se ocupa de la comprensión de lectura automática. En este laboratorio vamos a usar Watson Natural Language Understanding (WNLU) para extraer palabras clave de un conjunto de datos y poder analizarlas para conocer el sentimiento que expresa. Esto lo haremos con un Jupyter Notebook y utilizando las APIs de Python, posteriormente usaremos Pandas, Matlib y Seaborn para poder visualizar la información y extraer más datos importantes de la información.

En este taller aprenderas a:
- Crear y usar una instancia de Watson Natural Understanding 
- Conectarte a Watson NLU por medio de APIs de Python
- Realizar un análisis de texto para sacar palabras clave, sentimientos y emociones
- Mostrar la información de manera gráfica para entender mejor los datos.

## Crear una instancia de Watson NLU
1. Haga click en el menú de navegación en la esquina superior izquierda de su instancia de Cloud Pak for Data y haga click en Services -> Services catalog

//Aquí va una imagen de eso 

2. En la barra de busqueda ponga "Natural Language Understanding" y de click en Natural Langua Understanding:

//Aquí va una imagen

3. Escoga el plan gratuito Lite (solo puede tener una instancia Lite en su cuenta, si ya cuenta con otra tendrá que borrarla para que esta sea nueva o bien pagar por tener otra instancia). Pongale un nombre con el que pueda identificar la instancia:

//Aquí va una imagen

4. Usted podrá ver su nueva instancia de NLU en la página de "Services instances". De click en el nombre para abrir la página de su nueva instancia:

// Aquí va otra imagen

5. Haga click en la pestaña de Credenciales o haga click en "Ver credenciales del servicio" para navegar a la página de credenciales:

//Aqui va otra imagen

6. De click en Crear credenciales. Después dar click en la flecha hacia abajo para ver las nuevas credenciales creadas. De los datos que que se muestran necesitarás la "api key" y el "url" por lo que se recomienda que las copies en un lugar seguro o bien dejes la pestaña abierta:

//Aquí va una imagen

Tenga en cuenta que puede acceder al tutorial "Getting Started" y a la referencia de la API desde su isntancia de NLU en la pestaña de "Overview". Tal vez quiera echarles un vistazo para investigar más a fondo de Watson NLU.

## Demostración de Watson NLU y Análisis de Sentimientos

1. Visite https://www.ibm.com/demos/live/natural-language-understanding/self-service/home. De click en el botón "Analyze Text"
//IMAGEN
2. De click en las pestañas "Etxraction", "Classification", "Linguistics" y en "Custom". Puede notar que hay sub-pestañas en cada una donde se muestra información más detallada.

//Imagen

3. De click en la pestaña "Classification" y en la sub-pestaña "Emotion". Aquí puede ver como NLU extra información sobre la emocion que tiene el texto.

Puede ver las puntuaciones de confianza para cada una de las diversas frase objetivo que se extrajeron en el análisis, siendo "Tristeza", "Alegría", "Miedo", "Desagrado" y "Enojo".

Ahora que ha visto como trabaja NLU y el Análisis de Sentimientos, usaremos las APIs de Python en un cuaderno de Jupyter junto con herramientas para graficar y visualizar los datos.

## Cargar y Ejecutar un cuaderno

1. Vaya a su proyecto en Cloud Pak for Data 
//imagen
2. En su proyecto, de click en "Add to project" y escoja "Notebook":
//imagen
3. Seleccione "New Notebook from URL". Copie y pege el siguient URL: 
https://github.com/ibmdevelopermx/Watson-NLU-Workshop/blob/9392b702ec018ad32b6276170e07043efcd67c0d/Notebook/Watson_NLU.ipynb
De click en "Create":

//imagen

Dedique tiempo a examinar las secciones del cuaderno para obtener una descripción general. Un cuaderno se compone de celdas de texto (markdown o heading) y celdas de código. Las celdas de markdown proporcionan comentarios sobre para qué está diseñado el código.

Ejecutará celdas individualmente resaltando cada celda, luego haga clic en el botón Ejecutar en la parte superior del cuaderno o presione el atajo de teclado para ejecutar la celda (Shift + Enter, pero puede variar según la plataforma). Mientras la celda se está ejecutando, aparecerá un asterisco ([*]) a la izquierda de la celda. Cuando esa celda haya terminado de ejecutarse, aparecerá un número secuencial (es decir, [17]).
