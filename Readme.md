### Práctica de Comandos básicos de Docker
## 1- Descarga la imagen 'ubuntu y comprueba que está en tu equipo
 Para hacer eso, tenemos varios comandos tales cómo docker pull o hacer docker run y dejar que ese comando te dé la ultima versión.
 Si quieres saber que está en tu equipo, puedes usar  o bien docker ps para ver cuales tienes activos o usar docker container ls -a para verlos todos.
## 2- Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre
 Está en marcha, si pones un docker ps, verás que le pusieron un nombre aleatorio.
## 3- Crea un contenedor con el nombre 'dam_ubu1'. ¿Como puedes acceder a él?
 O bien haciendo un docker build o haciendo un docker run del contenedor que quieres hacer. Para que se llame dam_ubu1, debe tener el parametro --name dam_ubu1 en él.
 Para acceder a él puedes ponerle (o bien al hacer el contenedor o al pararlo y correrlo otra vez) los parámetros -i y/o -t en ellos, o bien puedes asignarles un puerto en tu local host para poder verlo en tu browser de preferencia.
## 4- Comprueba que ip tiene y si puedes hacer un ping a google.com
 Los contenedores no suelen empezar con utensilios tan básicos como ifconfig o ping. Debes de actualizar el contenedor e instalar net-tools e iputils-ping para poder hacerlo.
## 5- Crea un contenedor con el nombre 'dam_ubu2'. ¿Puedes hacer ping entre los contenedores?
Tras haber hecho un segundo contenedor actualizado,y con los packs instalados. He sido capaz de hacer ping con los 2 contenedores que estaban en la misma red, desde la dirección 172.17.0.2 a la 172.17.0.3 y vice versa.
## 6- Sal del terminal, ¿que ocurrió con el contenedor?
Aunque haya salido del terminal, el contenedor seguirá activo.
## 7-¿Cuanta memoria en el disco duro ocupaste?
## 8-¿Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.
Mientras usaba docker stats cuando los contenedores estaban haciéndose ping entre ellos. Llegué a la conclusión de que entre los dos gastaron, 2 MB de los 15 GB que tienen como límite y un 0,02% de la memoria RAM que hay en la PC.