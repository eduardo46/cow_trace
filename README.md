cow_trace
==================

Descripcion
==================

Cow trace trata de solucionar el problema de la trazabilidad en la cadena carnica donde los clientes cada dia exigen mas informacion. 
Es este caso se quiere registrar todos los eventos por los que pasa un animal desde su nacimiento hasta su entrada al matadero.
Esto ademas de permitirnos saber la trazabilidad del animal nos ayudaria en posibles enfermedades que haya tenido el animal o alguno que se haya 
criado con este.
Para solucionar este problema utilizaremos la blockchain de near la cual es ideal para este problema ya que es barata y escalable.
Las funciones que permitira hacer el smart contract son las siguientes


1. registrarGanado
2. registrarUsuario
3. actualizarEstado
4. consultarEstados
5. consultarGanado
6. buscarGanado
7. comprarGanado


Instalacion
===========

Para ejecutar el proyecto local, se deben seguir los siguientes pasos:

Paso 1. Prerequisitos

1. [Node,js] >= 12
2. instalar dependencias: npm install o yarn install
3. Tener una cuenta de prueba near
4. Tener instalado el near cli global
   yarn install --global near-cli

## Uso

### Compilando y desplegando

Lo primero que debemos hacer es instalar las dependencias necesarias para que el proyecto funcione.

```sh
npm install
```

ó

```sh
yarn install
```

Una vez hecho esto, podemos compilar el código.

```sh
npm run build
```

ó

```sh
yarn build
```

El contrato compilado en WebAssembly se guarda en la carpeta `AssemblyScript/build/release/`. Ahora solo es necesario desplegarlo en una cuenta de desarrollo.

```sh
near dev-deploy build/release/contrato.wasm
```

### Usando variables de entorno

Una vez compilado y desplegado tu proyecto, vamos a requerir identificar la cuenta neardev. Esta la puedes encontrar en el archivo `AssemblyScript/neardev/neardev`. Podemos almacenar este contrato en una variable de entorno ejecutando lo siguiente en la consola, y sustituyendo por tu cuenta de desarrollo:

```sh
export CONTRATO=dev-0000000000000-000000000
```

Haciendo esto, podemos comprobar que la variable `CONTRATO` tiene almacenada nuestra cuenta dev.

```sh
echo $CONTRATO
```


Paso 3: Metodos
---------------

Los siguientes comandos le permiten interactuar con el contrato inteligente.

1. Registrar un ganado en la blockchain

```near call $CONTRATO registrarGanado '{"ubicacion":"ubicacion", "genero":"genero", "raza":"raza","tamano":"tamano", "precio":"1"}' --accountId <su cuenta test>```

2. Consultar el ganado que registro

```near view $CONTRATO consultarGanadoRegistrado '{"idCuenta": "su_cuenta_test"}' --accountId <su cuenta test>```




Mockup interfaz grafica
===============

Poner aca el mockup de la interfaz grafica
