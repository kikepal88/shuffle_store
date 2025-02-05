# Sluffle Store

Welcome to **Sluffle Store**, the best online  clothing store. This is a landing page developed in a lightweight environment designed to help developers explore Shopify's Liquid templating language and dynamic section-based architecture.

---

## **Project Structure**

```
/simulator
├── /config
│   ├── settings_schema.json      # Defines configurable settings for sections
│   ├── settings_data.json        # Stores dynamic data for rendering sections
├── /data
│   ├── products.json             # Sample product data
│   ├── collections.json          # Sample collection data
├── /public
│   ├── styles.css                # Compiled CSS file
│   ├── main.js                   # Compiled JavaScript file
├── /sections
│   ├── collection                # Folder with a main section rendering collection section
│   ├── featured-products         # Folder with a main section rendering product lists
│   ├── footer                    # Folder with a main section rendering footer section
│   ├── header                    # Folder with a main section rendering header section
│   ├── hero                      # Folder with a main section rendering hero section
│   ├── top-bar                   # Folder with a main section rendering top-bar section
├── /snippets
│   ├── button                    # Folder with a reusable snippet to rendering a individual button
│   ├── marquee-item              # Folder with a reusable snippet to rendering a individual marquee-item
│   ├── pay-icons                 # Folder with a reusable snippet to rendering a individual pay-icons
│   ├── product-card.liquid       # Reusable snippet for individual product cards
├── /templates
│   ├── index.liquid              # Main template file
├── /src
│   ├── styles                    # Folder with general SASS files
│   ├──     ├──mixins.scss        # File with SASS mixins
│   ├──     ├──reset.scss         # File with general styles
│   ├──     ├──variables.scss     # File with SASS variables
│   ├── styles.scss               # Base SASS file where imported all SASS files
│   ├── app.js                    # Base JavaScript logic
├── /assets                       # Images for products, banners, and collections
├── package.json
├── webpack.config.js
├── server.js
```

---

## **Setup Instructions**

This repository runs with the node version **V20.13.1**

### **Install Dependencies**

```bash
npm install
```

### **Run the Server**

```bash
npm start
```

### **Build Styles and Scripts**

```bash
npm run build
```

---

## **Additional Notes**

### **Testing the Application**

Visit `http://localhost:3000` in your browser to view the simulator in action.

---
---

## Acerca de la Prueba

En relación con la prueba, hay algunos aspectos que me gustaría mencionar. Logré completar los objetivos principales, desarrollando las secciones top-bar, header, hero-banner, collections y footer. Sin embargo, me hubiera gustado también completar la sección de productos, probablemente la más compleja de construir.

No pude finalizarla debido a varios obstáculos que encontré durante el desarrollo, los cuales explicaré más adelante. Estos me hicieron perder tiempo valioso, y al final, opté por priorizar las secciones hero-banner y collections, que requerían menos complejidad técnica.

### Obstaculos

Considero importante mencionar los obstáculos y errores que enfrenté, ya que de ellos se aprende y me ayudan a recordar que siempre hay margen de mejora.

- Entorno de desarrollo: Mi mayor desafío fue configurar correctamente el entorno de trabajo. No tenía experiencia previa con Liquid, ni con su integración en un entorno basado en Node, Express y Webpack. Logré modificar los archivos de configuración (webpack.config.js y server.js) para que el proyecto funcionara, aunque no de la mejor manera. Al principio, la compilación del proyecto, especialmente los estilos, no se realizaba correctamente. Al final, conseguí que el entorno funcionara, pero para ver los cambios en el código, siempre tenía que ejecutar npm run build en una terminal aparte para reflejar las actualizaciones en el navegador.
- Búsqueda y creación de imágenes: La recopilación y edición de imágenes consumió más tiempo del esperado, ya que varios recursos gráficos del diseño no estaban disponibles en el repositorio.
- Relación entre settings_data.json y settings_schema.json: Al principio, no comprendía bien cómo interactuaban estos archivos. Pensé que no sería necesario modificar settings_schema.json, pero luego tuve problemas para renderizar varios datos desde settings_data.json. Tras investigar, entendí la relación entre ambos y la razón por la cual algunos datos no se mostraban correctamente.

### Mejoras
Durante el desarrollo, realicé algunas mejoras y añadí detalles adicionales para mejorar la experiencia visual y de usuario:

- Recursos gráficos: Dado que algunas imágenes e íconos del diseño no estaban en los archivos del repositorio, creé algunas imágenes y busqué y descargué otras para completar la interfaz.
- Animaciones y efectos adicionales: Implementé algunos detalles visuales que no estaban especificados en el diseño inicial, como:
  - Navegación del header en versión mobile.
  - Text shadow en las tarjetas de colecciones.
  - Efectos hover en enlaces, botones y tarjetas de colección.

### Comentarios
- Hubo algunas instrucciones que me generaron confusión, especialmente en la información del diseño y los archivos JSON, ya que en algunos casos no coincidían. En ciertos momentos, modifiqué los JSON para alinearlos con el diseño, mientras que en otros decidí seguir la información original de los JSON. Opté por esta última opción en la sección de colecciones.

Por último, quiero destacar que me esforcé bastante en la realización de esta prueba y la trabajé con dedicación. Si bien me apoyé en herramientas de IA para investigar algunos aspectos técnicos y solucionar obstáculos, también consulté documentación oficial y tutoriales para comprender mejor el proyecto.