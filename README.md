# Sprint_3_Agente_Clima
🤖 **DESCRIPCIÓN DEL AGENTE PROPUESTO**

Es un agente de software que tiene la tarea de interactuar con el mundo exterior (internet) para obtener información específica (el pronóstico del tiempo) y presentarla al usuario.


🧠 **EXPLICACIÓN CONCPETUAL DE LA LOGICA**

La lógica de este código sigue un proceso de entrada, procesamiento, decisión y salida, actuando como un traductor entre el usuario y un servicio de clima en internet via API.


**Flujo Lógico Paso a Paso**

Preparación (Identidad): El programa primero se prepara estableciendo su identidad secreta (api_key) para poder hablar con el servicio de clima en la web.

Consulta al Usuario (Entrada): Le pide al usuario que ingrese el nombre de la ciudad que le interesa.

Comunicación Externa (Procesamiento): Usando la ciudad ingresada, el programa envía un mensaje al servicio de clima y espera una respuesta.

Evaluación (Decisión): Al recibir la respuesta, el programa realiza una pregunta crucial: "¿He recibido datos de clima válidos?"

Resultado (Salida):

Si la respuesta es SÍ (es exitosa): El programa extrae la temperatura y la descripción del clima y las muestra de forma clara.

Si la respuesta es NO (hubo un error, como una ciudad mal escrita): El programa muestra un mensaje de error.

La lógica se basa en garantizar que la comunicación con el servicio externo haya sido exitosa antes de intentar mostrar cualquier información.


**💻 FUNDAMENTOS DE PROGRAMACIÓN EN EL EJEMPLO**
Este código es un programa simple en Python diseñado para obtener el clima de una ciudad que el usuario especifique, utilizando un servicio en internet (una "API" de clima).

**Variables = Es una caja etiquetada donde puedes guardar diferentes tipos de información.**

Asignación de Valores: El código usa variables para recordar datos importantes:

api_key: Guarda la clave secreta necesaria para que el programa pueda comunicarse con el servicio de clima en internet.

city: Guarda el nombre de la ciudad que el usuario escribe.

weather_data: Guarda toda la información del clima (temperatura, descripción, etc.) que se trae de internet.

Ejemplo: Cuando el usuario ingresa "Madrid", el valor "Madrid" se guarda en la caja etiquetada como city.

**Funciones (Bloques de Tareas) = Una función es como una receta o un procedimiento al que le das un nombre. Contiene una secuencia de pasos para realizar una tarea específica.**

main(): Esta es la función principal del programa. Es la "receta" que contiene todos los pasos que el programa debe seguir: preparar la conexión al clima, pedir la ciudad, obtener los datos y mostrarlos.

weather_api.get_weather(city): Esta es una función especializada que está dentro de otra parte del programa (WeatherAPI). Su trabajo es ir a internet (usando la api_key y el nombre de la city) y traer la información del clima.

**Entrada y Salida de Datos = Entrada (input()): Permite que el programa reciba información de una fuente externa, en este caso, del usuario.**

city = input("Ingrese el nombre de la ciudad: ") le pide al usuario que escriba algo y guarda lo que escribió en la variable city.

Salida (print()): Permite que el programa muestre información al usuario.

Las líneas con print() son las que muestran los mensajes en la pantalla, como "Clima en Madrid:" o la temperatura.

**Estructura de Decisión (if/else) = Esta estructura es el mecanismo para tomar decisiones en el código. Es como preguntar: "Si se cumple esta condición, haz esto; si no se cumple, haz esto otro."**

La Condición: if weather_data:

El programa pregunta: "¿Pudimos obtener la información del clima (weather_data) exitosamente?" Si la información se obtuvo (la variable no está vacía), la condición es verdadera.

Si es Verdadera (Bloque if):

Si sí se obtuvieron los datos, el programa ejecuta el bloque if y muestra la información del clima (temperatura y descripción).

Si es Falsa (Bloque else):

Si no se obtuvieron los datos (por ejemplo, si la ciudad no existe o hubo un error de conexión), el programa ejecuta el bloque else y muestra el mensaje de error: "No se pudo obtener el clima para la ciudad ingresada."

**¿QUÉ FUNCIÓN CUMPLE LA RESPUESTA DEL AGENTE?**

En este programa, la "respuesta del agente" es lo que el servicio de clima en internet le devuelve al código, guardado en la variable weather_data.

Función Principal: La respuesta sirve como la fuente de datos que el programa necesita para ser útil. Contiene todos los detalles del clima.

Función de Control: También sirve como indicador de éxito o fracaso. Si el servicio de internet no puede encontrar la ciudad o tiene un problema, la respuesta le indica al código que no hay datos útiles, lo que activa inmediatamente la lógica de decisión (if/else) para mostrar el error al usuario.

<img width="1470" height="901" alt="Screenshot 2025-12-14 at 4 24 07 PM" src="https://github.com/user-attachments/assets/500ad311-9e5a-47de-8515-9fc757b86d2f" />

 



