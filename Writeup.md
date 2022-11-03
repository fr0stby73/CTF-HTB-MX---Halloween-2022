Después llenar la información inicial del google forms que nos mandaron para poner las respuestas del CTF nos dan un link con instrucciones para empezar la investigación :sunglasses:

![image](https://user-images.githubusercontent.com/70277640/199788187-e5908202-0475-4dce-8133-324e54ece0e2.png)

Sin más tiempo que perder nos ponemos manos a la obra

![image](https://user-images.githubusercontent.com/70277640/199788224-98066740-ddcc-48dc-a264-e479dde401b8.png)

# ¿Cuál es el username del dueño del celular?

Al abrir el link con las instrucciones encontramos un drive de Google con 2 archivos, un txt explicando el caso y una foto (hmmmm sospechoso, muy sospechoso). Al abrir el txt encontramos un expediente que nos habla de una desaparición, que está ligada a otras desapariciones, en donde menciona que el único indicio que tenemos del desaparecido es una fotografía enviada por el sujeto en cuestión (parece que nuestras sospechas sobre la foto van haciendo más sentido)

![image](https://user-images.githubusercontent.com/70277640/199788249-3175883d-2d8e-498d-9625-b6927d33c47e.png)

Siguiendo lo que nos indica el expediente, y nuestra sospecha, analizamos los metadatos de la fotografía usando metadata2go para encontrar el nombre del autor de la foto (sospecha confirmada), el cual también es la primera respuesta al CTF

![image](https://user-images.githubusercontent.com/70277640/199788286-be4e37f1-8691-4b79-a2e0-9f4c3a8909e2.png)

**Primera respuesta: turnipenvivo**

# ¿Cuál es el trabajo de día de la persona?

El nombre del autor nos da una idea de cómo seguir con nuestra investigación. Siguiendo nuestros instintos de Sherlock Holmes vamos a Twitch y buscamos turnipenvivo para ver si encontramos algo. Al hacer esto vemos que nuestro instinto estaba en lo cierto, turnipenvivo es una cuenta existente de Twitch

![image](https://user-images.githubusercontent.com/70277640/199788327-30d6811d-6ef3-4fdb-b2d1-f1e5dc9509b6.png)

Como podemos ver en la información de este canal de Twitch, descubrimos que el trabajo de día de la persona es Diseñador grafico, obteniendo así nuestra segunda respuesta

![image](https://user-images.githubusercontent.com/70277640/199788369-517229f6-baea-4378-a086-f82d6c6c1e5b.png)

**Segunda respuesta: Diseñador grafico**

# ¿Cuál es la criatura que investiga en el caso #12?

¿Qué dijeron, que nos quedamos sin pistas? Pues nel, un buen detective nunca se queda sin pistas xd. En el canal de Twitch vemos que hay un link para la cuenta de Twitter de turnip y como la gente chismosa que somos, le damos click pa ver que tan buenos tweets se carga el turnip xd

![image](https://user-images.githubusercontent.com/70277640/199788452-2df3deb1-c4f2-42b8-98b3-9129fd015ce9.png)

En su feed de Twitter podemos ver que turnip probablemente hizo un tweet que después borró

![image](https://user-images.githubusercontent.com/70277640/199788494-69a6fb7d-4634-4be0-9d55-15b035899de4.png)

Oh no, no tenemos una máquina del tiempo ahora, ¿Quién podrá salvarnos?. Pues no, no es el chapulín colorado quien nos salvará, sino nuestro buen amigo que nos recuerda todas las estupideces que tweeteamos en momentos donde queremos atención desesperadamente: Wayback Machine

![image](https://user-images.githubusercontent.com/70277640/199788529-82dad20f-10df-4e6e-aa3e-42747af40d74.png)

Tqm Wayback Machine. Encontramos un snapshot de la página de Twitter de turnip. En el snapshot podemos ver que el tweet que turnip borró era un link a un documento de Google con sus investigaciones para sus teorías conspirativas

![image](https://user-images.githubusercontent.com/70277640/199788568-b3805d56-f422-4108-b131-dd80247ab6c2.png)

En el documento de las investigaciones de turnip encontramos nuestra tercera respuesta, además de fotos de un bonito jackalope 

![image](https://user-images.githubusercontent.com/70277640/199788602-a1437b74-d0db-4cb3-b7f7-e6bd3306570a.png)

**Tercera respuesta: jackalope**

# ¿Cuál es la contraseña del Mega?

En el mismo documento, si bajamos un poco más podemos ver el caso #14, en donde turnip describe que un usuario de reddit le había contado sobre una detective había desaparecido y que esta detective a su vez estaba investigando a personas desaparecidas y también le compartió el tablero de investigación de la detective (pro tip: si no quieren terminar teniendo un buen de faltas de ortografía cuando escriben, como este sujeto, échenle ganas a COE banda xd)

![image](https://user-images.githubusercontent.com/70277640/199788638-7086e3f2-cf6c-4414-ad7b-2fe9c4bdc479.png)

En el tablero de la detective vemos el avance que llevaba en su investigación sobre las personas desaparecidas y vemos algo que suena interesante: #4 Comunicación por decifrar

![image](https://user-images.githubusercontent.com/70277640/199788671-cd951bd2-41b6-44a8-9940-b10cb1d16954.png)

Dentro de este punto de su investigación encontramos una cadena que parece estar encriptada en base64 al igual que un link para una carpeta de Mega (nuestra investigación va bien)

![image](https://user-images.githubusercontent.com/70277640/199788740-b8240358-dc94-4357-85a0-2cfd27eb9698.png)

Al ingresar al link de Mega vemos que necesitamos una llave para desencriptar el contenido y poder acceder a él

![image](https://user-images.githubusercontent.com/70277640/199788793-61a66400-eae1-4432-b367-d67b29175880.png)

Tomamos la cadena codificada en base64 y vamos con nuestro buen amigo CyberChef para desencriptarla

![image](https://user-images.githubusercontent.com/70277640/199788826-9d6bcce9-4651-44e4-9e85-ae93df4bc51c.png)

Aunque logramos obtener algo un poco más leíble, esto sigue sin ser algo que tenga completo sentido. Hmmmm ¿uggc://? los :// suenan como a algo que he visto antes, ¿quizás una página web? Algo como ¿http://?. Creo que vamos por buen camino. Como todo buen detective frente a un texto codifcado el cual no está seguro con qué haya sido codificado le calamos con ROT13 a ver que sale

![image](https://user-images.githubusercontent.com/70277640/199788859-5a78ae62-4ed8-449d-b8d5-41c85d6e6e7b.png)

Como diría número uno de los KND, nombre a veces soy una cosa pero bárbara. Ahora si obtenemos algo que tenga sentido; podemos ver que es un link de TOR, por lo que inciamos nuestro buscador de TOR en corto, pegamos el link en la barra buscadora y presionamos enter sin tener miedo a que nos roben nuestra información bancaria xd

![image](https://user-images.githubusercontent.com/70277640/199788884-59b1a5df-b901-4452-914e-b80f3cdc7621.png)

Dentro de la página de TOR no solo encontramos la llave para desencriptar la carpeta de MEGA (y nuestra cuarta respuesta), sino que también revisamos nuestra cuenta de banco y vemos que seguimos teniendo los 5 peso que siempre hemos tenido, todo bien

**Cuarta respuesta: JynWGbh6o-UEKarEz7pfKA**

# ¿Qué se está llevando a las personas?

Dentro de la carpeta de MEGA a la que acabamos de acceder encontramos 3 audios

![image](https://user-images.githubusercontent.com/70277640/199788938-8bbc9f44-4ab8-46a7-86eb-1adbc3005513.png)

Después de 10 minutos de tratar de entender ruso y fallar miserablemente nos damos cuenta de que los primeros 2 audios no nos llevan a nada (gracias por los rabbit holes Chava). Al escuchar el 3er audio nos podemos dar cuenta de que es código morse lo que estamos escuchando. Buscamos una herramienta en línea que tome audios de código morse y los pase a texto (ya que nuestras skills de código morse no están muy finas xd). Para nuestra suerte encontramos una herramienta perfecta para esto. Al meter el audio al decodificador de código morse  y dejar que la herramienta haga lo suyo obtenemos el mensaje encriptado

![image](https://user-images.githubusercontent.com/70277640/199789009-e5578a9e-5301-4112-9a62-25a0ce74fa8f.png)

Dentro de este texto encontramos un indicio: "NOESUNCULTOESUNAFAM". Metemos esto tal cual en Google y le damos click a 'Voy a tener suerte' porque nos sentimos suertudos y tadaaaaa, encontramos una página de reddit de un vato conspiracionista (porque ¿Qué es reddit sino una serie de cuentas conspiracionistas? Xd)

![image](https://user-images.githubusercontent.com/70277640/199789049-78bb2a96-0fe4-4222-a823-27ae874447eb.png)

![image](https://user-images.githubusercontent.com/70277640/199789076-c3ab448d-b863-4d48-a172-9edcabae83e3.png)

Dentro de su página de reddit vemos un link que dice 'conoce la verdad', como no nos gusta que nos hagan sentir como personas ingnorantes le damos click en corto xd

![image](https://user-images.githubusercontent.com/70277640/199789097-005364d4-ce3b-4ece-82f1-aed9c6df4418.png)

En la página encontramos lo que esperabamos de cualquier persona conspiracionista: Aliens. El creador de esta página relata el ritual en el que participaba de ofrecer parejas de hombre y mujer a aliens, en el cual después es traicionado y ofrecido junto con la investigadora desaparecida (los puntos comienzan a conectarse), pero antes de que los Aliens se los lleven, la investigadora logra desatar al hombre para que él huya y le cuente la verdad al mundo. Así es como nuestro usuario de reddit se encuentra con turnip y le cuenta todo lo que sabe sobre las abducciones alienígenas 

![image](https://user-images.githubusercontent.com/70277640/199789118-f60064d8-0574-4bc2-87e6-93f25c671751.png)

**Quinta respuesta:**

![image](https://user-images.githubusercontent.com/70277640/199789149-f11b856e-333c-4e8f-b139-400609d47680.png)

# ¿Cuál es la mejor defensa de la humanidad?

Después de descargar todas las imágenes que hay en esa página para meterlas a metadata2go, darnos cuenta de que la respuesta a la siguiente pregunta no se encuentra en los metadatos de las imágenes y perder como 20 minutos tratando de avergiuar cuál es el siguiente paso, nos llega la iluminación: robots.txt. Por su puesto, ¿cómo pudimos olvidar lo más básico de enumeración de páginas web? Tanta teoría conspiracional nos dejó mal xd. Pero bueno, al ir al robots.txt de la página encontramos 2 rutas con nombres muy interesantes

![image](https://user-images.githubusercontent.com/70277640/199789180-f2ef9c98-bcbe-4d4e-99e4-07673c0c83b4.png)

Al navegar a /solucion.html encontramos la sexta respuesta y aprendemos que los tlacuaches son la mejor solución para sobrevivir a la inminente invasión alienígena (¿cómo no se nos había ocurrido antes?)

![image](https://user-images.githubusercontent.com/70277640/199789202-f110da22-17e5-4297-9d0e-105693e4fb51.png)

**Sexta respuesta: tlacuaches**

![image](https://user-images.githubusercontent.com/70277640/199789268-4a19b556-1075-47b8-be29-4abceb440e19.png)

# ¿Será este el final del hombre araña?

Al navegar a /diario.html encontramos el diario (¿Quién lo diría? Xd) del hombre que logró escapar y encontramos algo muy interesante: una MAC Address

![image](https://user-images.githubusercontent.com/70277640/199789300-89129181-05ea-4e81-a297-9a73afb27d1f.png)

Tristemente, al detective (yo xd) le faltaron 5 peso y tiempo pa terminar la investigación. Hasta aquí fue hasta donde logré llegar y aunque tuve algunas ideas ninguna de ellas funcionó para obtener la respuesta a la última pregunta ¿En qué ciudad ocurren las abducciones? (Ya que en su tiempo no sabía de la existencia de la herramienta https://wigle.net/ xd)

![image](https://user-images.githubusercontent.com/70277640/199789316-12e85446-5bf9-4c26-8b80-f790ed52b6f9.png)

**FIN**
