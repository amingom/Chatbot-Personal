# Chatbot Personal

## 🧠 Chatbot Inteligente con n8n, Telegram, Google Calendar y Gemini AI

Este proyecto consiste en el desarrollo de un **chatbot automatizado**, utilizando **Inteligencia Artificial (Google Gemini)** para comprender el lenguaje natural. Está implementado en **n8n**, permitiendo interactuar con el usuario a través de **Telegram** de una forma mucho más fluida y humana.

El bot gestiona eventos en **Google Calendar** (crear, ver, modificar y eliminar) y consulta información meteorológica mediante la **API de OpenWeather**, interpretando las peticiones del usuario.

---

### 🧩 Flujo actual del proyecto

<img width="1846" height="1160" alt="image" src="https://github.com/user-attachments/assets/b8983fda-e1a1-423e-8cbc-567d9b0d07d5" />

---

El flujo se compone de los siguientes elementos clave:

1. **Telegram Trigger**  
   Recibe cualquier mensaje de texto del usuario.

2. **Clasificador con IA (Google Gemini)**  
   Un modelo de lenguaje analiza el mensaje y determina la intención del usuario entre:
   - **Crear**: Agendar nuevos eventos.
   - **Ver**: Consultar la agenda.
   - **Eliminar**: Borrar eventos existentes.
   - **Modificar**: Cambiar detalles de un evento.
   - **Clima**: Consultar el tiempo.

3. **Procesamiento Inteligente (Nodos IA)**  
   Dependiendo de la intención, otros modelos de IA extraen los datos necesarios:
   - *Fechas y horas*.
   - *Resúmenes y descripciones*.
   - *Ciudades* para el clima.

4. **Integración con Google Calendar**  
   - **Crear evento:** Añade tareas con título, fecha, hora y recordatorios.
   - **Ver eventos:** Busca eventos en rangos de tiempo.
   - **Eliminar evento:** Busca y elimina eventos por nombre.
   - **Modificar evento:** Permite cambiar hora, fecha o título de eventos existentes.

5. **Consulta del clima**  
   Detecta automáticamente la ciudad mencionada o muestra el clima de la ciudad por defecto, que es Madrid, y consulta la API de OpenWeather.

6. **Respuestas Naturales**  
   El bot confirma las acciones o responde a las consultas con mensajes formateados en Markdown/HTML.

---

### 🚀 Funcionalidades implementadas

- **Procesamiento de Lenguaje Natural (NLP):** Entiende frases como "Cena con Paco el viernes a las 9" sin usar comandos como `/crear`.
- **Gestión Completa de Calendario:**
  - Creación inteligente de eventos.
  - Consulta de agenda.
  - Modificación de eventos existentes.
  - Eliminación de eventos.
- **Consulta Meteorológica Inteligente:** Detecta la ciudad dentro de la frase.
- **Interacción Fluida:** Respuestas contextuales y manejo de errores.

---

### 🛠️ Tecnologías utilizadas

- [**n8n**][n8nurl] – Orquestador de flujos de trabajo.
- [**Google Gemini API**][geminiurl] – Motor de Inteligencia Artificial para comprensión del lenguaje.
- [**Telegram Bot**][telegramboturl] – Interfaz de usuario.
- [**Google Calendar API**][googlecalendarurl] – Gestión de agenda. 
- [**OpenWeather API**][openweatherurl] – Datos meteorológicos.

[n8nurl]: https://n8n.io/
[geminiurl]: https://aistudio.google.com/
[telegramboturl]: https://core.telegram.org/bots
[googlecalendarurl]: https://developers.google.com/workspace/calendar/api/guides/overview?hl=es_419
[openweatherurl]: https://openweathermap.org/api

---

### 📋 Ejemplos de uso

#### 🗓️ Evento creado en Google Calendar
<img src="https://github.com/user-attachments/assets/20d7e3f8-184a-4996-90e6-b08bf23f56e4" width="380" />

#### 📅 Lista de eventos
<img src="https://github.com/user-attachments/assets/8c6795a8-6140-416d-b9f5-4113f18cba48" width="300" />

#### 🧭 Google Calendar
<img src="https://github.com/user-attachments/assets/2c8e065e-5cb0-4bbc-b81b-ff296e7492a3" width="340" />

#### ☀️ Muestra de datos del clima
<img src="https://github.com/user-attachments/assets/a67de7f9-074a-465d-93b2-ea13bef8c0cb" width="250" />

---
