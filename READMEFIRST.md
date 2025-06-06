# Base de datos no relacionales usando MongoDB con comandos en consola (mongosh)

Primero que todo vamos a definir el nombre de la base de datos

```javascript 

use Mis_recursos_app

```

luego insertaremos todo los registros usando insertMany de [Resgistros](InsercionDeRegistros.md)

```javascript

db.recursos.insertMany([
    {
        "nombre": "Score pattern question",
        "genero": "Terror",
        "plataforma": "HBO Max",
        "estado": "En progreso",
        "formato": "Serie",
        "fecha_terminacion": "2025-05-02",
        "valoracion": 1,
        "resena": "Race question like test.",
        "usuario_id": 1
    },
    {
        "nombre": "Group forget",
        "genero": "Ciencia Ficción",
        "plataforma": "Crunchyroll",
        "estado": "Terminado",
        "formato": "Libro",
        "fecha_terminacion": "2025-04-11",
        "valoracion": 2,
        "resena": "Sense them language position herself above popular.",
        "usuario_id": 2
    },
    {
        "nombre": "Career",
        "genero": "Acción",
        "plataforma": "Netflix",
        "estado": "Terminado",
        "formato": "Serie",
        "fecha_terminacion": "2025-04-12",
        "valoracion": 3,
        "resena": "And they difficult scientist Republican hot.",
        "usuario_id": 3
    }... ])

```

## Filtros usando find()

para filtar todos los recursos cuyo estado esten en "Terminado"


```javascript
db.recursos.find({estado:"Terminado"})
```

para filtar todos los recursos cuyo estado esten en "En progreso"


```javascript
db.recursos.find({estado:"En progreso"})
```

para filtar todos los recursos cuyo estado esten en "Pendiente"

```javascript
db.recursos.find({estado:"En progreso"})
```

para filtar todos los recursos cuyo Formato esten en "Serie"  

```javascript
db.recursos.find({formato:"Serie"})
```

para filtar todos los recursos cuyo Formato esten en "Película"  

```javascript
db.recursos.find({formato:"Película"})
```


para filtar todos los recursos cuyo Formato esten en "Libro"  

```javascript
db.recursos.find({formato:"Libro"})
```

para consultar todos los recursos que correspondan a cada plataforma específica dentro de la coleccion

```javascript
db.recursos.find({ plataforma: "Amazon Prime" });
db.recursos.find({ plataforma: "Apple TV+" });
db.recursos.find({ plataforma: "Crunchyroll" });
db.recursos.find({ plataforma: "Disney+" });
db.recursos.find({ plataforma: "HBO Max" });
db.recursos.find({ plataforma: "Kindle" });
db.recursos.find({ plataforma: "Netflix" });
db.recursos.find({ plataforma: "YouTube" });
```



