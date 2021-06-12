

<details open="open">
  <summary>Glosario de contenido</summary>
    <li><a href="#arquitecturaWeb">Asignatura</a></li>
    <li><a href="#Integrantes">Integrantes </a></li>
    <li><a href="#uso">Como usar</a></li>
    <li><a href="#licencia">Licencia</a></li>
    <li><a href="#Contacto">Contacto</a></li>
  </ol>
</details>

## Asignatura : Desarrollo Web de la Universidad de Palermo

## Integrantes: Guido D'Amore (0082636)

El proyecto de este trabajo practico propone tener acceso CRUD a una base de datos de peliculas en MONGODB creada por este fanatico de Sci-fi 

## uso : 

#ENDPOINT:  http://localhost:3000/api/pelicula/    

# GET (general)

get http://localhost:3000/api/pelicula/

Se utiliza para ver todas las peliculas cargadas en la base de datos.

# GET (id)
get http://localhost:3000/api/pelicula/ID

Se utiliza para ver una pelicula especifica (id) de la base de datos. 

ejemplo : get http://localhost:3000/api/pelicula/60c3eb2e07ee5d449cc11a61

# POST 
En esta base de datos tenemos 5 datos que son vitales: name, picture, price, category y description
Al hacer post deberemos enviar esos valores en ese orden para poder guardarlos en la base de datos

Ej : POST http://localhost:3000/api/pelicula/ 

POST /api/pelicula
{
  name: 'INGRESE PELICULA',
  picture: 'INGRESE FOTO . FORMATO',
  price: 'INGRESE PRECIO',
  category: 'INGRESE CATEGORIA',   
  description: 'INGRESE DESCRIPCION' 
}

EL POST SOLO ACEPTARA FORMATO STRING PARA : name, picture y description
EL POST SOLO ACEPTARA LAS SIGUIENTES category: ['Drama','Sci-fi', 'Accion','Aventura', 'Comedia', 'Thriller'] En caso de no respetarlos, se devolverá un mensaje de error. 
EL POST SOLO ACEPATAR FORMATO INTEGER PARA : price 

# DELETE
Se podrá borrar peliculas ùnicamente por su ID 
podrá obtener el id de las peliculas cargadas en la base de datos usando post 

DELETE /api/pelicula/60c3f01a087e1f44b07078ce
(DELETE http://localhost:3000/api/pelicula/60c3f01a087e1f44b07078ce) 

#PUT
Se puede modificar la cantidad de valores que se desee. Desde uno, hasta todos.
Se deberà efectuar un put con el ID de la pelicula y luego, respestando los formatos nombrados en el segmento de "post" modificar los campos que se desee

por ej: 
Put http://localhost:3000/api/pelicula/60c3eb2e07ee5d449cc11a61
{
    "pelicula": {
        "price": 1500,
        "name": "y donde estan las morochas?",
        "picture": "xxx.JPG",
        "category": "Sci-fi",
        "description": "alta peli de sci-fi",
        "__v": 0
    }

Estaremos modificando todos los campos del id 60c3eb2e07ee5d449cc11a61

## Licencia :  
Solo puede utilizarse si el alumno aprueba la cursada de Desarrollo web


## Contacto :
  guido.damore@hotmail.com // gdamor@palermo.edu 

