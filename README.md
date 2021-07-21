## Sistema de Recomendación con python  

En la práctica, los sistemas de recomendación abarcan una clase de técnicas y algoritmos que pueden sugerir elementos "relevantes" a los usuarios. Idealmente, los elementos sugeridos son tan relevantes para el usuario como sea posible, de modo que el usuario pueda interactuar con esos elementos: videos de YouTube, artículos de noticias, productos en línea, etc.  

Los elementos se clasifican según su relevancia y se muestran al usuario los más relevantes. La relevancia es algo que debe determinar el sistema de recomendación y se basa principalmente en datos históricos. Si recientemente miraste videos de YouTube sobre elefantes, entonces YouTube comenzará a mostrarte muchos videos de elefantes con títulos y temas similares.  

Los sistemas de recomendación generalmente se dividen en dos categorías principales: filtrado colaborativo y sistemas basados en contenido.  

### Sistemas de filtrado colaborativo   
Los métodos de filtrado colaborativo para los sistemas de recomendación son métodos que se basan únicamente en las interacciones pasadas entre los usuarios y los elementos de destino. Por lo tanto, la entrada a un sistema de filtrado colaborativo serán todos los datos históricos de las interacciones del usuario con los elementos de destino. Estos datos generalmente se almacenan en una matriz donde las filas son los usuarios y las columnas son los elementos.  

La idea central detrás de estos sistemas es que los datos históricos de los usuarios deberían ser suficientes para hacer una predicción. Es decir, no necesitamos nada más que esos datos históricos, ningún impulso adicional del usuario, ninguna información de tendencia actual, etc.  

Más allá de esto, los métodos de filtrado colaborativo se dividen en dos subgrupos: ***métodos basados en memoria y métodos basados en modelos***. 


<img src="https://github.com/luishernand/recomendations-system/blob/main/63115930-5f6c1900-bf66-11e9-894f-ecde5ec531b0.png" alt="JuveR" width="500px">  

**Los métodos basados en memoria** son los más simplistas, ya que no utilizan ningún modelo. Asumen que las predicciones se pueden hacer en la “memoria” pura de datos pasados y, por lo general, solo emplean un enfoque simple de medición de distancia, como el vecino más cercano.

**Los enfoques basados en modelos**, por otro lado, siempre asumen algún tipo de modelo subyacente y básicamente tratan de asegurarse de que las predicciones que surjan se ajusten bien al modelo.

A modo de ejemplo, digamos que tenemos una matriz de los usuarios a los artículos de almuerzo preferidos donde todos los usuarios son estadounidenses que aman las hamburguesas con queso (son fenomenales). Un método basado en la memoria solo observará lo que el usuario ha comido durante el último mes, sin considerar el pequeño hecho de que son estadounidenses amantes de las hamburguesas con queso. Un método basado en modelos, por otro lado, asegurará que las predicciones siempre se inclinen un poco más hacia ser una hamburguesa con queso, ya que la suposición del modelo subyacente es que la mayoría de las personas en el conjunto de datos deberían amar las hamburguesas con queso.  

### Sistemas basados en contenido  
A diferencia del filtrado colaborativo, los enfoques basados en contenido utilizarán información adicional sobre el usuario y / o elementos para hacer predicciones.  

Por ejemplo, un sistema basado en contenido podría considerar la edad, el sexo, la ocupación y otros factores personales del usuario al hacer las predicciones. Es mucho más fácil predecir que a la persona no le gustaría el video si supiéramos que se trataba de patinetas, ¡pero la edad del usuario es 87!  

Por eso, cuando te registras en muchos sitios web y servicios en línea, te piden (opcionalmente) que proporciones tu fecha de nacimiento, sexo y origen étnico. Son solo más datos para que su sistema haga mejores predicciones.  

Por lo tanto, los métodos basados en contenido son más similares al aprendizaje automático clásico, en el sentido de que crearemos funciones basadas en datos de usuarios y elementos y las usaremos para ayudarnos a hacer predicciones. La entrada de nuestro sistema son las características del usuario y las características del artículo. La salida de nuestro sistema es la predicción de si al usuario le gustaría o no el artículo.  


