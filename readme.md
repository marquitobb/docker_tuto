# Configuración de una máquina virtual Ubuntu con Docker

1. **Instalar Docker:**  
   Asegúrate de tener Docker instalado en tu sistema. Puedes seguir la [documentación oficial de Docker](https://docs.docker.com/get-docker/) para instalarlo según tu sistema operativo.

2. **Descargar la imagen de Ubuntu:**  
   Ejecuta el siguiente comando para descargar la imagen oficial de Ubuntu:

   ```sh
    docker pull ubuntu
    ```

3. **Crear un contenedor de Ubuntu:**
   Ejecuta el siguiente comando para crear un contenedor de Ubuntu:

   ```sh
    docker run -it --name ubuntu-container ubuntu
    ```

   - `-it`: Permite interactuar con el contenedor.
   - `--name`: Asigna un nombre al contenedor.

4. **Configurar el contenedor de Ubuntu:**
   Una vez dentro del contenedor, actualiza el sistema y configura las herramientas necesarias:

   ```sh
    apt update
    apt upgrade
    apt install nano
    apt install curl
    apt install wget
    apt install git
    ```
5. **Salir del contenedor de Ubuntu:**
    Para salir del contenedor de Ubuntu, ejecuta el siguiente comando:
    
    ```sh
     exit
     ```
6. **Guardar los cambios en una nueva imagen:**
    Una vez que hayas realizado las configuraciones necesarias, puedes guardar los cambios en una nueva imagen de Docker. Para ello, primero detén el contenedor:

    ```sh
     docker stop ubuntu-container
     ```

    Luego, guarda los cambios en una nueva imagen:

    ```sh
     docker commit ubuntu-container ubuntu-custom
     ```

    - `ubuntu-container`: Nombre del contenedor actual.
    - `ubuntu-custom`: Nombre de la nueva imagen.