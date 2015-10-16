# prueba-inicial
-----------------

Este es un ejemplo de Github para probar cómo funciona

Primero, instalamos GIT:
	
	apt-get install git-core

Una vez instalas GIT, hay que configurarlo:
	git config --global user.name "Pablo Insua"
	git config --global user.email "xxxxxx@xxxxxx.com"

Arrancar el proyecto:
	
	git init
	touch README
	git add README
	git commit -m "Mi primer commit"
	git push
	git status 		#comprueba si hay alguna modificación

Para conectar Git con GitHub necesitamos antes generar una Public Key:

	ssh-keygen

Seguimos las instrucciones que se indican. Una vez finalizado, leemos la key para copiar a GitHub:
	
	cat /.ssh/id_rsa.pub  
	#esta es la clave pública, en el archivo id_rsa está la privada nuestra

Una vez metida la clave pública, ligamos los dos proyectos:

	#La URL se pilla en un espacio señalado en nuestro proyecto en GitHub
	git remote add origin https://github.com/KnucklesEQ/prueba-inicial.git
	#Se producirá un merge entre el proyecto de GitHub y lo que hay en 
	#nuestro PC

Copiamos lo que haya en GitHub y lo traemos a nuestro PC:

	git pull origin master  #Copia la rama 'master', es decir, todo

Cargamos en GitHub lo que hay en nuestro PC:

	git push origin master  #Copia a la rama 'master'

--------------
Cambiamos de tercio, y entramos en el concepto de 'branch' o ramas. Para crear una rama:
	
	git branch dev     #creamos la rama 'dev'
	git branch vagalume  #creamos la rama 'vagalume'

Se pueden crear tantas ramas como deseemos. Hay una rama inicial y principal que es 'master', de la cual parte el resto que vayamos creando.
Para cambiar de rama o branch, tecleamos:

	git checkout dev	#cambiamos a la rama dev
	git branch		 #me informa de las ramas existentes y en la que estoy

