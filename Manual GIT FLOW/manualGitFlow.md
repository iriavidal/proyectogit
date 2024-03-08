# MANUAL DE GIT FLOW

## ÍNDICE DE CONTENIDOS


1. INTRODUCCIÓN 

2. VENTAJAS, NECESIDADES Y MOTIVOS

3. WORKFLOWS: ALTERNATIVAS A GIT FLOW

4. ## FUNCIONAMIENTO DE GIT FLOW

Gitflow se basa en la existencia y utilización de distintas ramas, cada una con un rol determinado, durante el desarrollo de un proyecto. De esta forma, no se trabaja únicamente sobre la rama master permitiendo un flujo de trabajo más flexible y con menos errores al hacer merge, donde cada equipo se puede centrar en el desarrollo de una parte sin afectar al trabajo de los demás. 

Las ramas que usa Gitflow son las siguientes:

1. **Master o main**
Rama principal que se crea cuando se inicia un nuevo repositorio en Git. En ella se guardará el historial de todas las versiones del software que han sido publicadas. Por lo tanto, esta rama solamente contendrá una parte de la totalidad del proyecto.

2. **Develop o dev** 
Esta rama es la rama de desarrollo donde se irán añadiendo las diferentes partes del proyecto. Por lo tanto, esta rama contiene la totalidad del proyecto, incluido el que todavía está en desarrollo, donde se irán fusionando todas ramas feature cada vez que se añada una nueva funcionalidad. Todos los equipos de desarrollo trabajarán a partir de esta rama, creando las diferentes features a partir de ella para luego fusionarlas a develop una vez que estén finalizadas.

3. **Feature**
Las ramas features son las que se utilizan para añadir nuevas funcionalidades al proyecto. Como se indica en el apartado anterior, las ramas feature utilizan la rama develop como rama primaria, partiendo de ella y fusionándose de nuevo cuando la feature está terminada. 

4. **Release**
Las ramas de release sirven para guardar la parte del software que será publicado. Esta rama parte de la rama develop y, una vez incorporado el código, no se podrán añadir nuevas funcionalidades a esta rama. Estas nuevas funciones se quedarán en la rama develop a la espera de ser añadidas a la siguiente release. Los únicos cambios que se podrán realizar sobre esta rama son para la corrección de errores que no hayan sido detectados en la rama dev o en las features. 
En cuanto la pulicación esté preparada, se fusionará la rama release con la rama master, indicando en un TAG la versión correspondiente, y con la rama develop para que esta última contenga los últimas correcciones que se hayan podido realizar sobre la rama release y tenga siempre una copia completa de todo el código. Al igual que las features, una vez se haya fusionado con master y con develop, se eliminará la rama release.

5. **Hotfix**
Estas ramas sirven para arreglar aquellos errores que deban ser correjidos rápidamente. Esta rama parte de la rama master, por lo que una vez correjido el problema, debe fusionarse de nuevo con esta añadiendo un nuevo TAG con la versión actualizada. También debe ser fusionada a la rama develop. La existencia de esta rama permite corregir los errores del código principal sin interrumpir el desarrollo de nuevas partes y sin tener que esperar a la próxima publicación para incluir las correcciones.

![Esquema ramas gitflow](./img/esquema.png)


5. COMANDOS DEL WRAPPER DE GITFLOW


