# Uso de Github

## ¿Qué es un repositorio de código?

[Introducción a Github y Git](https://www.youtube.com/watch?v=FyfwLX4HAxM)

## Cómo crearse una cuenta en github

Easy Peasy! Eso es fácil de hacer no?

## Cómo instalar Git en tu máquina

### Windows

> [Instalación de **Cmder**](c%C3%B3mo-instalar-git-en-tu-m%C3%A1quina) (hasta el minuto 1:17).

[Usando git en Cmder](https://youtu.be/BFhQfTPEDHw?t=1m18s)

### Linux / Mac

* Linux
```bash
apt-get install git
```

* Mac

Necesitarás [**homebrew**](https://brew.sh/index_es.html). Una vez instalado, ejecuta lo siguiente desde el terminal

```bash
brew install git
```

## Configuración de git (Instrucciones para windows)



Para la clonación, necesitamos:

1. Crear claves ssh (localmente)
2. Agregue una clave pública a github (en un servidor remoto)
3. Conexión de prueba (localmente)
4. Clona el repositorio (localmente :))

### Creando claves ssh

> Sustituye **%YOUR_USER_NAME%** por tu nombre de usuario en tu máquina

Compruebe la existencia del directorio con las claves (generalmente ubicado en el directorio de inicio del usuario)
```bash
ls "C:\Users\%YOUR_USER_NAME%\.ssh"
```
Si no hay un directorio **.ssh** , crearlo

```bash
cd "C:\Users\%YOUR_USER_NAME%"
mkdir .ssh
cd .ssh
```

### Crear nuevas claves

> Sustituye **your_email@example.com** por el email con el que te creaste la cuenta de github

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

### Ejecute ssh-agent (en una tarea en segundo plano)

```bash
ssh-agent -s
```

### Copie el clip de clave pública en el clip del portapapeles

```bash
<id_rsa.pub
```


### Agregue una clave pública a github (haga esto en el servidor remoto, donde se encuentra el repositorio)

Abre un navegador y haz login en tu cuenta de github.com

Entramos en: **Configuraciones> Teclas SSH> Agregar clave SSH> Agregar clave**

Añade una nueva clave, dándole un nombre y pegando la clave que tienes en el portapapeles.

### Conexión de prueba (localmente)

Desde el terminal de **cmder** , ejecuta:

```bash
ssh -T git@github.com
```

La respuesta debería ser: "Hola, nombre de usuario! Has autenticado con éxito, pero GitHub no proporciona acceso de shell".

### Clonar un repositorio localmente

>Vamos a usar el este mismo repositorio como ejemplo

Copia la siguiente url en tu portapapeles.

```bash
https://github.com/esri-es/referencias_desarrollo_html5.git
```

Nos movemos al directorio con el proyecto, donde clonaremos el repositorio.

Crea una carpeta **proyectos** en tu escritorio y desde el terminal mueveté a esa carpeta.

Ahora teclea en el terminal

```bash
git clone https://github.com/esri-es/referencias_desarrollo_html5.git
cd referencias_desarrollo_html5
```


5. Creando cambios

Debe agregar un archivo o cambiar el contenido de un archivo existente.

Abre la carpeta **referencias_desarrollo_html5** que acabamos de crear en **Atom** y modifica alguno de los ficheros, salvando los cambios.

Ahora desde el terminal , ejecuta

```bash
git status
```




## Referencias para tener a mano

[Chuleta commandos git](https://www.git-tower.com/blog/git-cheat-sheet/)
