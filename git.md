# Instalar git

Orden para instalar Git en nuestra distribución basada en Debian

Sintaxis:

```
apt-get install git
```

# Configurar identidad

Ordenes para configurar la identidad del usuario para el uso de GIT.

## Configurar nombre Usuario
Sintaxis:

```
$ git config --global user.name "J M"
```

## Configurar email Usuario
Sintaxis:

```
$ git config --global user.email "Correo@gmail.com"
```

## Configurar editor de texto del Usuario
Sintaxis:

```
$ git config --global core.editor nano
```

## Comprobar la configuración
Sintaxis:

```
git config --list
```

## Obtener ayuda sobre un comando
Sintaxis:

```
$ git help (nombre de la orden)
```

Ejemplo:

```
$ git help config
```

## Iniciar repositorio Git
Sintaxis:

```
$ git init
```
## Añadir elemento/s a la cola de subida

Con la siguiente orden permitirá preparar archivos para su subida al repositorio que tenemos configurado. Puede subirse toda la carpeta, un solo archivo en específico o carpetas.

Sintaxis:

```
$ git add *.c
$ git add LICENSE
```
## Subir los cambios al repositorio

Con la siguiente orden subiremos los archivos añadidos con la orden anterior, cada commit creará una versión con todos los cambios realizados.
Con el parámetro "-m" nos permitirá darle un nombre al commit

Sintaxis:

```
$ git commit -m 'initial project version'
```

## Clonar un repositorio

Con esta orden podremos clonar un repositorio que este en el mismo equipo, en otro o inclusive en Internet.

Sintaxis:

```
$ git clone https://github.com/libgit2/libgit2
```

Si se quiere indicar un directorio destino se debería de escribir de la siguiente manera:

```
$ git clone https://github.com/libgit2/libgit2 mylibgit
```

## Comprobar estado de Git

Con esta orden podremos saber en que estado está el git, permitiendo saber si se ha añadido algo para subir o no.
Sintaxis:

```
$ git status
```

Para obtener un estado abreviado de GIT deberemos de escribirlo de la siguiente manera:

```
$ git status -s
```

## Ignorar archivos

Si escribimos un archivo oculto llamado ".gitignore", si dentro del mismo escribimos las extensiones de archivos o carpetas, podemos hacer que, al realizar un commit, no se añada cuando se suba los archivos indicados.

Ejemplo de sintaxis:

```
$ cat .gitignore
# ignora los archivos terminados en .a
*.a

# pero no lib.a, aun cuando había ignorado los archivos terminados en .a en la línea anterior
!lib.a

# ignora unicamente el archivo TODO de la raiz, no subdir/TODO
/TODO

# ignora todos los archivos del directorio build/
build/

# ignora doc/notes.txt, pero no este: doc/server/arch.txt
doc/*.txt

# ignora todos los archivos .txt del directorio doc/
doc/**/*.txt
```