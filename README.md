
# # ml-interview-sample

 Proyecto de ejemplo para MercadoLibre ambientado en un buscador de productos con módulo de resultados y detalles.


## Requerimientos

Para correr este conjunto integrado se requiere las siguientes herramientas:

### Alternativa con Docker (recomendado)

 - [Docker](https://www.docker.com/)

### Alternativa local

 - [Nodejs.](https://nodejs.org/es/)
 - [npm.](https://www.npmjs.com/get-npm) (Se instala a la par de Nodejs)

  

## Instalacion

### Alternativa Docker:
Descargar el ecosistema:

```bash
git clone --recursive git@github.com:Maracartman/ml-interview-sample.git
```

o con:

```bash
git clone --recursive https://github.com/Maracartman/ml-interview-sample.git
```
Luego de descargar y con Docker instalado; posicionarse en la carpeta descargada y ejecutar:
```bash

docker-compose up --build

```
Con esto; Docker generará un ecosistema con los contenedores de Nginx, proyecto frontend y backend necesarios para correr el aplicativo.

Al culminar de montar el compuesto puede acceder al sample en la ruta:

***[http://localhost:3050/](http://localhost:3050/)***


### Alternativa local

Con **[fe-products-searcher-ml (front-end)](https://github.com/Maracartman/fe-products-searcher-ml)** y **[be-products-searcher-ml (back-end)](https://github.com/Maracartman/be-products-searcher-ml)** descargados, posicionarte en la carpeta descargada y ejecutar:
```bash

npm install

```
Hacer lo mismo con la carpeta respectiva faltante.

#### Ojo: 
debe cambiar el archivo [api](https://github.com/Maracartman/fe-products-searcher-ml/blob/902bd631647cbba046aae42d36e235a6a540b9a6/src/services/api.js) del proyecto: **fe-products-searcher-ml** para que la instancia axios apunte al host local de api (http://localhost:6512/api)

    const instance = Axios.create({
	   baseURL: 'http://localhost:6512/api',
	   timeout: 20000,
	   headers: {
	   Accept: 'application/json'
	    }
    });

## Pruebas

  En ambos proyectos ejecutar:

```bash

npm run test

```

  

```bash

npm run test:watch

```

  

## Contribuyendo

  El proyecto es de elaboración personal por lo que no esta abierto a contribución.

  

## Autor

- Luis Maracara

  

## Repositorio oficial

El proyecto contiene dos artefactos:
### **[fe-products-searcher-ml (front-end)](https://github.com/Maracartman/fe-products-searcher-ml)**

### **[be-products-searcher-ml (back-end)](https://github.com/Maracartman/be-products-searcher-ml)**

## License

MIT