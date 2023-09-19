# 1.

Para descargar la imagen se usa empleo de: **"docker run"**. Además se puede utilizar el parámetro **"-it"** para interactuar con la terminal y **"--name"** para asignar un nombre al contenedor y **“bash”** para utilizar comandos

**Ejemplo:** docker run -it --name asir2 ubuntu:mantic-20230819 bash

Y para comprobar que se ha descargado la imagen se utiliza **"images"**

**Ejemplo:** docker images

# 2.

Se emplea el comando **“run”** sin utilizar el parámetro **“--name”** 

**Ejemplo:** docker run -it ubuntu bash

# 3. 

Con el parámetro **“--name”** se le asigna el nombre **"ubu1"**

**Ejemplo:**  docker run -it --name ubu1 ubuntu bash

Para acceder al contenedor se utiliza el comando **“exec”**

**Ejemplo:** docker exec -it ubu1 bash

# 4.

Por defecto no se puede. Hay que instalar el paquete **“net-tools”**. Se puede hacer utilizado los siguientes comandos:

    apt update
	apt install net-tools

Una vez instalado podemos revisar la ip utilizando el comando **“ifconfig”**

Al igual que con la ip, por defecto no se puede hacer ping. Hay que instalar el paquete **“iputils-ping”** 

Una vez hecho eso, pues se realiza ping a la IP 8.8.8.8 que es la de Google 

# 5.

Se crea contenedor mediante el parámetro **“–name”**. Se le asigna el nombre de **“ubu2”**

# 6. 
El contenedor se detiene, esto se puede comprobar realizando un ping entre **“ubu1”** y **“ubu2”** y ver que sale destino inalcanzable

# 7.

Si, hay una herramienta la cual es **“system”**. Esta herramienta permite ver de forma global la cantidad de espacio en el disco que ocupan los contenedores

**Ejemplo:** docker system

Si se quiere ver el peso de cada contenedor se usa utiliza el parámetro -v

**Ejemplo:** docker system -v 

# 8. 
Para ver la memoria del sistema utilizada por los contenedores se utilizará el comando **“stats”** 

**Ejemplo:** docker stats