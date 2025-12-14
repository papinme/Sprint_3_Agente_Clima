# Sprint_3_Agente_Clima
🤖 Descripción del Agente Propuesto
Es un agente de software que tiene la tarea de interactuar con el mundo exterior (internet) para obtener información específica (el pronóstico del tiempo) y presentarla al usuario.


# 🧠 Explicación Conceptual de la Lógica
La lógica de este código sigue un proceso de entrada, procesamiento, decisión y salida, actuando como un traductor entre el usuario y un servicio de clima en internet via API.


# Flujo Lógico Paso a Paso:
Preparación (Identidad): El programa primero se prepara estableciendo su identidad secreta (api_key) para poder hablar con el servicio de clima en la web.

Consulta al Usuario (Entrada): Le pide al usuario que ingrese el nombre de la ciudad que le interesa.

Comunicación Externa (Procesamiento): Usando la ciudad ingresada, el programa envía un mensaje al servicio de clima y espera una respuesta.

Evaluación (Decisión): Al recibir la respuesta, el programa realiza una pregunta crucial: "¿He recibido datos de clima válidos?"

Resultado (Salida):

Si la respuesta es SÍ (es exitosa): El programa extrae la temperatura y la descripción del clima y las muestra de forma clara.

Si la respuesta es NO (hubo un error, como una ciudad mal escrita): El programa muestra un mensaje de error.

La lógica se basa en garantizar que la comunicación con el servicio externo haya sido exitosa antes de intentar mostrar cualquier información.


# 💻 Fundamentos de Programación (Lenguaje Natural)
Aquí están los conceptos básicos de programación presentes en el código, explicados sin términos técnicos complejos:

a) Variables: Las Cajas de Información
Imagina que una variable es una caja etiquetada donde el programa puede guardar un pedazo de información para usarlo más tarde.

api_key: Guarda la clave secreta que sirve como "pase de acceso" para usar el servicio de clima.

city: Guarda el nombre de la ciudad que el usuario escribe.

weather_data: Guarda toda la información del clima (temperatura, humedad, descripción, etc.) que se trae de internet.

b) Funciones: Las Recetas de Tareas
Una función es como una receta o un procedimiento que agrupa una serie de pasos para lograr una tarea específica.

main(): Esta es la receta principal del programa. Cuando el programa se inicia, sigue todos los pasos listados dentro de esta función.

weather_api.get_weather(city): Esta es una función especializada cuya única tarea es comunicarse con internet para obtener los datos del clima de la ciudad especificada.

c) Estructura de Decisión (if/else): La Bifurcación
Esta es la forma en que el programa toma decisiones para reaccionar a diferentes situaciones.

La Pregunta (if weather_data:): El programa pregunta: "¿La caja de weather_data contiene información del clima útil?"

Si la respuesta es "VERDADERA" (Éxito): Se ejecuta el código que está dentro del if, y muestra la temperatura y descripción.

Si la respuesta es "FALSA" (Fracaso): Se ejecuta el código que está dentro del else, y muestra el mensaje de error.

d) ¿Qué Función Cumple la Respuesta del Agente?
En este programa, la "respuesta del agente" es lo que el servicio de clima en internet le devuelve al código, guardado en la variable weather_data.

Función Principal: La respuesta sirve como la fuente de datos que el programa necesita para ser útil. Contiene todos los detalles del clima.

Función de Control: También sirve como indicador de éxito o fracaso. Si el servicio de internet no puede encontrar la ciudad o tiene un problema, la respuesta le indica al código que no hay datos útiles, lo que activa inmediatamente la lógica de decisión (if/else) para mostrar el error al usuario.
