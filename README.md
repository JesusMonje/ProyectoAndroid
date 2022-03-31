# ProyectoAndroid

Cualquier duda podeis decirme. Diré por aquí lo que pone en el .kt

-Main Acitivty 1-

Declaro dos Val llamadas imagen 1 e imagen 2. Ambas se corresponden con un ImageView puesto en el XML. Debajo de imagen 1 inicio Glide con la iamgen de la nube, y debajo de la imagen2 inicio Glide pero con una imagen en mi carpeta drawable. Lo siguiente que hay es un botón para pasar a la siguiente página. 

-Main Activity 2-

Este ejercicio se divide en 4 con SoundPool y 2 con MediaPlayer, primero iremos con los 4 y luego con los otros dos.
Declaro el "audioAttributes" para inicializar como indica Fran. Luego también inicio otra val del primer soundPool, que lo que hace es aplicar los audioAttributes seteados anteriormente. Luego se incia el objeto AudioManager para setear el SystemService, el context es AUDIO_SERVICE  //(Audio del dispositivo)// .

Cerramos dicho objeto seteando de nuevo que es un AudioManager. Por último antes de empezar donde entendemos, hay que declarar la val volume, ayudada por la val anterior AudioManager.//(Todo esto sale en el pdf de Fran, las características técnicas las desconozco, pero deben ir en ese orden para el correcto funcionamiento.

Ahora si empezamos a declar las VAL que entenderiamos //(Recuerdo que VAL es para que no cambie una vez establecido)//. Bien, definimos las 4 primeras de SoundPool de la forma escrita en el .kt, lo importante aquí es saber que al final de la declaración en " R.raw.mario," la R es normal que esté, el "raw" es la carpeta en cuestión y el "mario" es el sonido en cuestión, su nombre. !!Siempre en miniscula y lo más conciso posible. 

Bien continuamos con los otros 3 que faltan y hacemos 6 botones para así poder poner los 6 sonidos. Aunque actualmente solo tengamos 4, recuerdo que en total son 6. 

Iniciamos la primera acción del primer botón con el setOnClickListener y dentro metemos lo siguiente:

" soundPool1.play(sound1,volume.toFloat(),volume.toFloat(),1,0,1f) "

Bien, como recordais al principio habiamos seteado el SoundPool1 con los audioAttributes, bien pues para esto era. Luego, simplemente lo único a tener en cuenta es que donde va "sound1" debe ir el nombre de la val que le habeis dado al sonido //(donde poneis la carpeta y nombre del archivo, esa val)//. 

Los siguiente dos "volume.toFloat" es para setear el volumen del lado izquierdo o derecho, lo dejamos vacíos porque no lo necesitamos. Por último están los 3 campos que resta, el primero es la prioridad, el segundo es el Loop  y el tercero la velocidad, que lleva la f detrás.

Pasando ya al mediaplayer, es bastante más sencillo:

"var mediaPlayer: MediaPlayer? = null
        mediaPlayer = MediaPlayer.create(this,R.raw.mariomoneda)
"

Esto es lo importante, y es que declaramos una var de cualquier nombre, los dos puntitos para decirle que se refiere a un objeto MediaPlayer, la interrogación para como dijo Fran que el programa si eso falla, no se parase, y lo igualamos a null //(En minuscula). Tras ello simplemente con el nombre de nuestra variable pues la igualamos a "MediaPlayer.create" y el nombre de la carpeta y el archivo. 

Basicamente hacemos lo mismo otra vez, asignamos los dos botones que nos falta y dentro de estos ponemos " mediaPlayer?.start()" que sería el nombre de nuestra variable, la interrogación y el ".start" para que funcione.  Y ahí finalizamos el apartado 2

-Main Activity 3-

Pendiente de documentar.
