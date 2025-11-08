# Chatbot-Personal

## 🧠 Chatbot Automatizado con n8n, Telegram y Google Calendar

Este proyecto consiste en el desarrollo de un **chatbot automatizado** implementado en **n8n**, que permite interactuar con el usuario a través de **Telegram**.  

El bot está diseñado para gestionar eventos en **Google Calendar** y consultar información meteorológica mediante la **API de OpenWeather**.

---

### 🧩 Flujo actual del proyecto

A continuación se muestra el flujo principal actualmente implementado en **n8n**:

<img width="2048" height="1067" alt="image" src="https://github.com/user-attachments/assets/e7ef2070-4e62-43c3-93e1-7c878e2671af" />

---

El flujo se compone de los siguientes elementos y conexiones:

1. **Telegram Trigger**  
   El flujo comienza cuando el bot recibe un mensaje del usuario en Telegram. Este mensaje actúa para iniciar la ejecución del proceso.

2. **Switch**  
   Este nodo analiza el contenido del mensaje y redirige la ejecución según el comando introducido por el usuario:  
   - `/añadir_tarea`: crea un nuevo evento en Google Calendar.  
   - `/ver_tareas`: muestra la lista de eventos pendientes en el calendario.  
   - `/clima`: consulta la información meteorológica actual de una ciudad específica.  

3. **Integración con Google Calendar**  
   - **Crear evento:** añade una nueva tarea en el calendario configurado.  
   - **Ver eventos:** obtiene y lista todos los eventos próximos del calendario.  

4. **Consulta del clima (HTTP Request)**  
   A través de una petición a la **API de OpenWeather**, el bot recupera los datos meteorológicos de la ciudad indicada por el usuario, en caso de que no se especifique, de manera predeterminada se mostrará el clima de Madrid.
   
   Los parámetros de la solicitud incluyen el nombre de la ciudad, la clave de API y las unidades de medida.  

6. **Mensajes formateados y respuesta a Telegram**  
   Cada acción del bot genera un mensaje de respuesta estructurado, usando HTML, que se envía de vuelta al chat de Telegram.  
   Por último, el usuario recibe información sobre el evento creado, la lista de tareas o las condiciones climáticas actuales.  

---

### 🚀 Funcionalidades implementadas

- Creación automática de eventos en Google Calendar.  
- Visualización de los eventos próximos del calendario.  
- Consulta del estado del clima mediante la API de OpenWeather.  
- Comunicación interactiva con el usuario a través de Telegram.  

---

### 🛠️ Tecnologías utilizadas

- [**n8n**][n8nurl] – herramienta de automatización sin código.
- [**Telegram Bot**][telegramboturl] – comunicación con el usuario.
- [**Google Calendar API**][googlecalendarurl] – gestión de eventos. 
- [**OpenWeather API**][openweatherurl] – consulta de datos meteorológicos.

[n8nurl]: https://n8n.io/
[telegramboturl]: https://core.telegram.org/bots
[googlecalendarurl]: https://developers.google.com/workspace/calendar/api/guides/overview?hl=es_419
[openweatherurl]: https://openweathermap.org/api

---

### 📋 Ejemplo de datos mostrados en Telegram

---

