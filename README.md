   
 # Historia técnica ED-002  

## datebase

* la base de datos y utilizemos es **mySQL** crea una base de datos con el nombre tienda online, después crea una tabla con los campos únicos a rellenar con los siguientes campos: ID (llave primaria), Nombre, descripción, imagen y existencia. 
* Creando la tabla con los siguientes campos:   

|code|name|description|image|stock|price|
|-|:-:|-:|-:|-|-|
| | ||
| | | |
| | | |

**Installation**
```bash
$ npm install
```

**Running the app** 

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```
### Metodos: 
 Metodos para utilizar 
* POST: [Crear un nuevo producto]

* GET: [Mostrar los productos] 
* DELETE: [Eliminar un producto] 
* PATCH: [Actualizar un producto] 

> **NOTA:** Estos metodos solamente se deben utilizar con Postman, para manejar las peticiones post, delete y patch.

### URLs de ENDpoints. 

* [Crear productos:](http://localhost:3000/products)
* [Mostrar productos:](http://localhost:3000/products)
* [Mostrar un producto:](http://localhost:3000/products/id)
* [Eliminar productos:](http://localhost:3000/products/id)
* [Actualizar productos:](http://localhost:3000/products/id)

### Body de la solicitud 
El body que se va enviar en la peticion https por el metodo post es: 
```jsn
{
  "code": "Codigo del producto", 
  "name": "Nombre del producto",
  "description": "Descripcion del producto",
  "image": "Imagen del producto",
  "stock": "Existencia de tu producto en numerico ",
  "price": "Precio del producto"
}
```

El body que se va utilizarse para actualizar un producto es el siguiente: 

```jsn
{
  "code": "El valor que va actualizar", 
  "name": "El valor que va actualizar",
  "description": "El valor que va actualizar",
  "image": "El valor que va actualizar",
  "stock": "El valor que va actualizar",
  "price": "El valor que va actualizar"
}
```
 > Para actualizar un producto debe agregarse un ID al final de una URl.
 > En el ejemplo anterior puede elegir cualquier valor que va actualizar en el Jsn.
 
 ### Respuestas 
 * **POST**: Se ha registrado un producto nuevo satisfactoriamente.
 * **GET**:  Respuesta para mostrar un producto 
 ```jsn 
{
  "code": "Codigo del producto", 
  "name": "Nombre del producto",
  "description": "Descripcion del producto",
  "image": "Imagen del producto",
  "stock": "Existencia de tu producto en numerico ",
  "price": "Precio del producto"
}
```
Mostrar varios productos 
> Esto se va mostrar solamente como parámetro de la URL, si coloca la ID. 
```jsn 
[
   {
  "code": "Codigo del producto", 
  "name": "Nombre del producto",
  "description": "Descripcion del producto",
  "image": "Imagen del producto",
  "stock": "Existencia de tu producto en numerico ",
  "price": "Precio del producto"
},
{
  "code": "Codigo del producto", 
  "name": "Nombre del producto",
  "description": "Descripcion del producto",
  "image": "Imagen del producto",
  "stock": "Existencia de tu producto en numerico ",
  "price": "Precio del producto"
}
]
``` 
* Delete:  
Se ha eliminado correctamente.  

* Patch: 
Se ha actualizado correctamente.

### Codigo **HTTP** De las respuestas

* POST: 201 Ok, 409 Error

* GET:  200 Ok, 404 Not Fount

* DELETE: 200 Ok, 404 Not Fount

* PATCH: 200 Ok, 404 Not Fount 

### Mensaje de error 

* POST: Este Producto ya Existe

* GET/:id, DELETE, PATCH: Este Producto No Existe
