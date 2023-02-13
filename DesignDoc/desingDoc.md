# Clon de Nintendo Frontend 

Author(s): Camila Silva

Status: [Draft]

Ultima actualización: 2023-02-13

## Contenido
- Goals
- Non-Goals
- Background
- Overview
- Detailed Design
  - Solucion 1
    - Frontend
    - Backend
  - Solucion 2
    - Frontend
    - Backend
- Consideraciones
- Métricas

## Links
- [Un link](#)
- [Otro link](#)

## Objetivo
Construir un clon del Home de Nintendo con HTML, CSS y JavaScript vanilla

## Goals
- Practicar mis skills de HTML, CSS  
- Manipulación del DOM 
- Integración con la API de Google traductor para la traducción de la pagina en multiples idiomas. 

## Non-Goals
- Interacciones mas alla de la pagina principal

## Background
Practicar mis skills de HTML, CSS y JavaScript desafiandome con la integracion de la API de traducción. 

## Overview
Necesitamos una API que traduzca los textos de la pagina web al idioma que seleccionemos en el "menu de idioma"  

Google ofrece una [API](https://cloud.google.com/translate/docs/basic/translating-text?hl=es-419) que podemos usar para traducir los textos de la pagina web 

## Solución 1

## Google

Para usar la API necesito crear un proyecto en Google Cloud y habilitar Cloud Translation y las credenciales para realizar llamadas autenticadas. 

### Obtener 
Debemos instalar la libreria 

{
  npm install @google-cloud/translate
}

### Traducir textos 
Una vez instalada la libreria, 

ejemplo de para iniciar la tracucción 
```translate.js
{
  const projectId = 'YOUR_PROJECT_ID';

// Imports the Google Cloud client library
  const {Translate} = require('@google-cloud/translate').v2;

// Instantiates a client
  const translate = new Translate({projectId});

  async function quickStart() {
  // The text to translate
    const text = 'Hello, world!';

  // The target language
    const target = 'ru';

  // Translates some text into Russian
  const [translation] = await translate.translate(text, target);
    console.log(`Text: ${text}`);
    console.log(`Translation: ${translation}`);
  }

  quickStart();
}
```

## Consideraciones
- La API es gratis hasta cierto punto.
- Se debe crear un proyecto en Google cloud para poder usar la API 

