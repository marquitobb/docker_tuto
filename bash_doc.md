1. Crear el script
Crea un archivo llamado menu.sh y agrega el siguiente contenido:
```sh
#!/bin/bash
# --------------------------------------------------
# Script: menu.sh
# Descripción: Un ejemplo de menú interactivo en Bash.
# Uso: ./menu.sh
# --------------------------------------------------

while true; do
    clear
    echo "Menú Principal"
    echo "1. Opción 1: Mostrar mensaje"
    echo "2. Opción 2: Otra acción"
    echo "3. Salir"
    echo
    read -p "Elige una opción [1-3]: " opcion

    case $opcion in
        1)
            echo "Has seleccionado la Opción 1."
            read -p "Presiona Enter para volver al menú..."
            ;;
        2)
            echo "Has seleccionado la Opción 2."
            read -p "Presiona Enter para volver al menú..."
            ;;
        3)
            echo "Saliendo..."
            exit 0
            ;;
        *)
            echo "Opción inválida, intenta de nuevo."
            read -p "Presiona Enter para continuar..."
            ;;
    esac
done
```
Este script crea un menú interactivo en Bash con tres opciones: mostrar un mensaje, realizar otra acción y salir del menú. Puedes personalizar las opciones y acciones según tus necesidades.

2. Dar permisos de ejecución
Para poder ejecutar el script, debes darle permisos de ejecución. Ejecuta el siguiente comando en la terminal:
```sh
chmod +x menu.sh
```
Esto permitirá que el script sea ejecutable.

3. Ejecutar el script
Para ejecutar el script, simplemente escribe el siguiente comando en la terminal:
```sh
./menu.sh
```
Esto mostrará el menú interactivo en la terminal y te permitirá seleccionar las opciones disponibles.