README del Coder & Especificaciones
 Coder: Camilo Phillips Jaramillo
 Clan: Tesla
Q1: ¿Por qué el enfoque mobile-first produce menos código que diseñar primero para escritorio?

El enfoque mobile-first parte de la pantalla más pequeña donde los elementos se organizan de forma natural en columnas únicas (por defecto, apilados en flujo vertical). Esto elimina la necesidad de escribir y mantener reglas complejas de reseteo o anulación de anchos. En escritorio (con prefijos como sm:, md:, lg:), solo agregamos las excepciones espaciales progresivas que la pantalla grande requiere, resultando en hojas de estilo y clases notablemente más limpias, directas y con menor redundancia.
Q2: ¿Qué decisión tomaste para que un producto con un nombre de 3 líneas no descuadre la grilla?

Para garantizar una alineación perfecta en la grilla sin importar variaciones en la longitud del texto, implementamos tres decisiones técnicas combinadas:

    Flexbox Vertical en la Tarjeta: Se aplicó flex flex-col al contenedor article junto con un flex-grow en el bloque de contenido interno.
    Anclaje del Botón al Fondo (`mt-auto`): El bloque de precio y botón de compra cuenta con la clase mt-auto, lo que empuja obligatoriamente dicho bloque hacia el borde inferior de cada tarjeta, alineándolos visualmente en toda la fila de la grilla.
    Control de Líneas (`line-clamp-2`): Se limitaron los títulos a un máximo de 2 líneas con puntos suspensivos automáticos, manteniendo la altura de la cabecera del producto uniforme.

