#MANUAL DE GIT

##ÍNDICE DE CONTENIDOS

1. Conceptos
2. Funcionamiento
3. Ventajas

4. Comandos básicos

### GIT CONFIG

- git config --global user.name "tunombre": establece el nombre de usuario
- git config --global user.email "tuemail": establece el correo electrónico
- git config --global color.ui auto: activa el coloreado de la salida
- git config --global merge.conflictstyle diff3: muestra el estado original en los conflictos
- git config --list: muestra la configuración

### CREACIÓN DE UN REPOSITORIO NUEVO

- git init <nombre-repositorio>: crea una nueva carpeta con el nombre del repositorio que a su vez contiene otra carpeta oculta llamada **.git** que contiene la base de datos donde se registran los cambios en el repositorio.

### COPIA DE REPOSITORIOS

- git clone <url-repositorio>: crea una copia local del repositorio que se le indica. Una vez creada la copia los dos repositorios (original y copia) son independientes el uno del otro.

### GIT ADD

- git add <fichero>: añade los cambios en el fichero del directorio de trabajo a la zona de intercambio temporal.
- git add <carpeta>: añade los cambios en todos los ficheros de la carpeta del directorio de trabajo a la zona de intercambio temporal.
- git add .: añade todos los cambios de todos los ficheros no guardados aún en la zona de intercambio temporal.

### GIT COMMIT

- git commit -m "mensaje": confirma todos los cambios de la zona de intercambio temporal añadiéndolos al repositorio y creando una nueva versión del proyecto. ()

5. Distintos tipos de clientes
6. Integración con otras herramientas??
