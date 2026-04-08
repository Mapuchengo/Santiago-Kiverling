Público Objetivo

* Rango etario: 15 a 60 años.
* Nacionalidad: Argentina.
* Ubicación geográfica: Entorno urbano principalmente, enfcado inicialmente en estudiantes de Fontana, provincia del Chaco, y la región circundante. A ser posible siempre se busca llegar a ser internacional, pero me enfoque en un punto de partida.
* Variables adiicionales: Estudiantes de escuelas técnicas (como la E.E.T N°24) y programadores junior. Tienen un nivel de alfabetización digital alto, acceden al contenido principalmente desde computadoras de escritorio en laboratorios de informática y desde teléfonos móviles. Buscan información directa, sin distracciones y valoran el rendimiento rápido de las páginas web ( en resumen nenes adictos al tikitoko).
* Extra: El plan a futuro seria crear una pagina bastante mas profesional y seria ( por eso estoy definiendo todo esto lo mas groso posible). aunque no quiero perder la originalidad y marca personal de los mapaches y la poca "seriedad" a la hora de trabajar.
---

Design Inspirations and Creative Process

Design Inspirations:
* Minimalist Developer Profiles: I looked at standard GitHub profiles and minimalist portfolio websites. The goal is to present information quickly without unnecessary visual clutter.
* Dark Mode UI: Inspired by modern code editors (like VS Code), I chose a dark theme. It reduces eye strain for students and developers who spend hours looking at screens.
* Humor and Personality: I chose to use a raccoon profile more than anything because it is the brand that I usually use in all my projects, for me it reflects a less serious vision to avoid so much rigidity and it is more striking in itself, plus I like them a lot.

Creative Process Documentation:
* Initial Concept: The primary goal was to build a basic, accessible frontend profile using HTML and CSS.
* Color Palette: I cchose a dark gray background (`#5d5d5d`) to resemble my page to the colors of a raccoon and thus contrast with the photo. During the iterative design process (following UCD principles), I focused on ensuring the text had enough contrast to the dark background to meet WCAG accessibility standards.
* Layout: I used CSS Flexbox to center all the content perfectly on the screen. It is the most efficient way to ensure the design adapts well to different screen sizes.
* Images: I added a circular crop to the profile picture with a solid white border to match the standard UI conventions of platforms like GitHub and LinkedIn, making it instantly recognizable for the user yeii.

Portfolio Contact Automation - n8n Workflow

1. Overview
This workflow automates the reception and management of messages sent through the contact form on my personal web portfolio. It acts as an Intelligent Process Automation (IPA) tool, classifying incoming messages and storing data efficiently.

2. Trigger and Workflow Logic
* Trigger: The flow starts with a Webhook node. When a user submits the HTML contact form on my website, a POST request is sent to this webhook containing their name, email, and message.
* Logic (Processing): I implemented an IF node to analyze the content of the message. It checks if the string contains the word "proyecto" (project). This basic conditional logic helps prioritize potential freelance job offers.
* Integrations (Services):
  1. Telegram API: If the message contains the keyword "proyecto", the True branch triggers a Telegram bot to send an immediate push notification to my phone, alerting me of a high-priority contact.
  2. Google Sheets: Regardless of the IF node outcome, both branches eventually connect to a Google Sheets node. This appends a new row to a spreadsheet, creating a historical database of all my contacts and inquiries without any manual data entry.

3. Why it is useful
As a Junior Developer, managing potential client interactions professionally is crucial. This automation saves time, ensures I never lose a contact's email (safely stored in the Cloud via Google Sheets), and provides real-time alerts for important opportunities.

4. Implementation Challenges
The main challenge was understanding how to properly map the JSON payload coming from the Webhook into the specific fields required by the Google Sheets node. Learning to use n8n's expression syntax (`{{$json.body.name}}`) was so hard.

![kinger-the-amazing-digital-circus](https://github.com/user-attachments/assets/9a97ff9b-de6f-4e11-8df6-0a6bd9f5fefa)

profe mirese Digital Circus
