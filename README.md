# PROYECTO PM1

## En este proyecto se van a mostrar los comandos utilizados para la realización del exámen 1ra parte de la unidad.

### - Primeramente se creó un repositorio en Github llamado PM1.

   

![](https://github.com/ItzaBesanilla/PM1/blob/a8bb59c9c6dc80dec52821b99f3e8c5023f64362/Imagenes/Crear%20nuevo%20repositorio.png)

### - Después se clonó y se conectó en el repositorio local dentro de la terminal de Git Bash.

    git clone <URL del repositorio a clonar>
    git remote add origin <URL>
    
![](https://github.com/ItzaBesanilla/PM1/blob/a8bb59c9c6dc80dec52821b99f3e8c5023f64362/Imagenes/Clonar%20remoto%20a%20local.png)

![](https://github.com/ItzaBesanilla/PM1/blob/a8bb59c9c6dc80dec52821b99f3e8c5023f64362/Imagenes/Conexion%20entre%20remoto%20y%20local.png)

-----------
## README

### - Se crea el readme y se agrega un commit inicial.

![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Readme.png)

----------
## IGNORAR ARCHIVOS

### - Crear en el repositorio local un archivo llamado "privado.txt"
### - Crear en el repositorio local una carpeta llamada "privada"

    mkdir  privado.txt
    cat>privado.txt/privada
    
![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Se%20crea%20fichero%20privado.txt%20y%20carpeta%20privada.png)

### - Realizar cambios necesarios para agregar las carpetas a .gitignore

    cat>.gitignore
    privado.txt
    
    
![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/se%20crea%20gitignore.png)

----------
### - Añadir archivo 1.txt al repositorio local.
### - Crear el tag v0.1
### - Subir el tag v0.1 al repositorio remoto

    cat > 1.txt
    git tag v0.1
    git add . 
    git commit -m "Se añadió..."

![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Se%20crea%201txt%20y%20el%20tag%20v01.png)

![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Se%20agrega%20el%20tag%20a%20rep%20remoto.png)

----------
## CREAR UNA RAMA v0.2

### - Se creará una rama y se posicionará el working diectory en esta rama.

    git branch v0.2
    git checkout v0.2

![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Se%20crea%20rama%20v02.png)

-----------
## AÑADIR ARCHIVO 2.txt EN LA RAMA v0.2

    cat > 2.txt
    
![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Se%20crea%20archivo%202txt.png)

-----------
## RAMA REMOTA v0.2
### Se crea en Github

![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Se%20crea%20rama%20remota.png)

### Se agregan cambios en el repositorio remoto

    git add .
    git status
    git commit -m "......"
    
![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Se%20agregan%20cambios%20al%20repositorio%20remoto.png)

-------------
## MERGE DIRECTO

### - Posicionarse en la rama master y hacer merge de la rama v0.2 en la rama master.

    git checkout master
    git merge v0.2
    
![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Merge%20directo.png)

-------------
## MERGE CONFLICTIVO

### - En la rama master poner Hola en el fichero 1.txt y hacer commit.

    git checkout master
    nano 1.txt
    git add .
    git commit -m "....."
    
![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Merge%20-%20master.png)

### - Posicionarse en la rama v0.2 y poner Adios en el fichero 1.txt y hacer commit.

    git checkout v0.2
    nano 1.txt
    git add .
    git commit -m "...."
    
![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Merge%20-%20v02.png)

### - Posicionarse en la rama master y hacer merge con la rama v0.2

    git checkout master
    git merge v0.2

![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Fusion%20de%20master%20con%20v02.png)

----------
## LISTADO DE RAMAS

### - Listar las ramas con merge y las ramas sin merge.

    git branch --merged
    git branch --no-merged
    
![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Listar%20ramas%20con%20merge%20y%20sin%20merge.png)

-----------------
## ARREGLAR CONFLICTO

### - Arreglar el conflicto anterior y hacer un commit.

####      Primeramente entramos a nano para seleccionar el commit final. Solamente se borrará aquella línea de cambio que no queremos mantener.

    nano 1.txt
    
![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Arreglar%20conflicto.png)

![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Arreglar%20conflicto%202.png)

####    Y finalmente realizamos un commit para confirmar cambios y que el conflicto quede resuelto.

![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Commit%20a%20la%20solucion%20del%20conflicto.png)


----------------
## BORRAR RAMA

### - Crear un tag v0.2
### - Borrar la rama v0.2

    git tag v0.2
    git branch -D v0.2

![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Crear%20tag%20v02%20y%20borrar%20rama%20v02.png)

---------------

## LISTADO DE CAMBIOS

### Listar los distintos commits con sus ramas y sus tags

    git branch -l
    git branch -v
    git log
    
![](https://github.com/ItzaBesanilla/PM1/blob/f4fe6d24d3807cb1da1138f948fec555564c2598/Imagenes/Listar%20commits.png)

--------------
    


