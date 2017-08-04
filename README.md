# Reto Damappa

![Image of Heartpoo](http://heartpoo.com/Fondo_ico2.png)

Repositorio de datasets de imágenes y texto para el reto Damappa para la hackathon: Hacksociety de Ai-Society

Hola! Gracias por participar en el `Reto Damappa` para la Hackathon de Ai-Society!

El objetivo de este repositorio es dar ejemplos, recordar los objetivos del reto, dar recomendaciones para abarcar el reto y adicionalmente dar unos datasets que pueden ser útiles para poder atacar el reto.

## Introducción Reto

Queremos hacer del mundo un lugar muy seguro; con el auge de las redes sociales y las discusiones online, el mundo ha acortado los medios para comunicarnos entre nos
os. Sin embargo, algunos han logrado utilizar estas plataformas para acosar, atacar y odiar. Por eso, queremos crear plataformas mas seguras para todo público, identificando acoso y maltrato online.

## Objetivo

Identificar *publicaciones* que sean de acoso, o bully electrónico. Por publicación se entiende una imagen acompañada de un texto.

## Datos para el Reto

Hemos recopilado una serie de datasets que pueden ser utilizados para ayudar a completar el Reto, a continuación describimos qué contienen los archivos y su uso.

Recordando que una publicación es un **texto + imagen**, el repositorio tiene dos carpetas, una con datasets de imagenes y otra con un dataset de textos.

  - Image Datasets: La carpeta que contiene los archivos de imagenes
    - FlickerImages.csv: Un csv con urls de imágenes con metadatos adicionales de situaciones regulares. Algunas de estas imágenes pueden contener humanos.
    - instagram-images.json: Un arreglo de urls de imágenes de la sección de selfies de Instagram. Estas imágenes tienen la particularidad de que son cercanas a la cámara, el enfoque es en una solo persona y hay poco contexto. 
    
  - Text Datasets: La carpeta que contiene los archivos de textos  
    - reviews_Patio_Lawn.json: Un archivo json con reseñas de Amazon correspondientes a la categora de Outdoor. En este los textos son comentarios (en su mayoría sin contenido ofensivo) y puede ser usado como textos control.
    - twitter_hate_speech.csv: Un excelente dataset donde se clasifican tweets (pedazos cortos de texto) con las siguientes características:
      - Contiene hate speech
      - Es ofensivo
      - Tiene lenguaje ofensivo
      - Es seguro (no contiene lenguaje ofensivo ni es ofensivo)

## Ejemplos

- Un selfie de una persona con lenguaje ofensivo clasifica la publicación como bully o acoso.
- Un selfie de una persona con un texto acompañante normal no clasifica como bully o acoso.
- Probablemente una imagen regular (por ejemplo de un carro sin humanos dentro de la imagen) con texto acompañante ofensivo puede ser clasificada como no ofensivo.
- Una imagen regular con un texto regular acompañante no es ofensiva.

## Sugerencia de Pasos para Atacar el Problema 
- Empezar reconociendo publicaciones que no muestran personas, ya hay algoritmos que por ejemplo logran identificar caras. 
- Posteriormente analizar elementos de la imagen, si es posible tratar de detectar, en el caso de que haya una cara es de alguien de interés público. 
- Si se descarta que no es de alguien conocido, intentar detectar qué elementos hay en la imagen para analizar si es posible que sea caso de bully electrónico.

## Retos adicionales

Nota: No es necesario completar los siguientes items para considerar el reto como completo pero lograr alguno o varios de los items puede afectar de manera positiva la puntuación final para escoger un ganador, ánimo! Es importante recalcar que primero se debe cumplir con los objetivos del reto antes de intentar alguno de los puntos de abajo.

- [ ] Identificar si el texto y la imagen no tienen ninguna correspondencia. 
- [ ] Identificar imágenes con contenido explícito.
- [ ] Identificar imágenes que no tienen contenido
- [ ] Identificar si el texto acompañante de una imagen que contiene un humano no hace referencia a la persona. O si hace referencia a algún humano dentro de la imagen.
