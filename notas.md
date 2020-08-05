# NPM

## Iniciar proyecto

```
npm init
```

## Iniciar proyecto y autocompletar información

```
npm init -y

npm init -yes
```

## Configurar author email, author name and licence default

```
npm set init.author.email "fflores.ic.ipn@gmail.com"

npm set init.author.name "Francisco Flores"

npm set init.license "MIT"
```

## Instalación de dependencias

### Dependencia parte del proyecto

```
npm install moment --save
npm i moment -S
npm i moment # en version npm superior 5 --save no es necesario
```

### Dependencia desarrollo

```
npm install date-fns --save-dev
npm i date-fns -D
```

### Dependencia global

```
(sudo) npm install -g nodemon
```

### Dependencia opcional

```
npm i eslint -O
```

### Simular instalación

```
npm i react --dry-run
```

### Instalación forzada del ultimo recurso desde el servidor de NPM

```
npm i webpack -force
npm i webpack -f
```

### Instalación completa de todas las dependencias en package.json

```
npm install
npm i
```

### Instalación versión especifica

```
npm install json-server@0.15.0 #version especifica o superior
npm i <package>@<version> #version especifica o version menor superior
npm i <package>@<version> --save-exact #version exacta
npm install <package>@latest #ultima version
```

## Listar, Actualizar y Eliminar paquetes

### Lista de paquetes instalados de forma global

* --depth : profundidad en jerarquia (dependencias incluidas)

```
npm list -g --depth 0
```

### Listar paquetes del proyecto

* --depth : profundidad en jerarquia (dependencias incluidas)

```
npm list --depth 1
```

### Paquetes desactualizados

```
npm outdate
npm outdate --dd # Con output para ver lo que va sucediendo
```

### Actualizar dependencia

```
npm update #Actualiza todos los paquetes
npm update <paquete>
npm update <paquete> --depth 2 #Profundidad para actualizar también dependencias 
```

### Desinstalar dependencia

```
npm uninstall <paquete>
npm uninstall <paquete> --no-save #no lo quita de package.json
```

## Versiones

```
<mayor>.<menor>.<parche>
3.9.2

Major = Mayor = Breaking change
Minor = Menor = Backwards compatible new functionality, old functionality deprecated, but operational, large internal refactor
Patch = Parche = bug fixes

^ indica que se instale la versión especificada o una versión superior menor o parche

~ indica que se instale la versión especificada o una superior parche
```

### Eliminar cache

```
npm cache clean --force
```

### Validar cache

```
npm cache verify
```

### Eliminar carpeta node_modules

```
rm -rf node_modules
```

### Modulo para eliminar carpeta node_modules

```
npm i -g rimraf
rimraf node_modules
```

### Auditar proyecto

```
npm audit
npm audit --json #genera json detallado
npm audit fix #Corrige vulnerabilidades

snyk proyecto para mantener seguridad
```

## Creación de un paquete para NPM

