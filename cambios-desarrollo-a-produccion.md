# Cambios que se realizan para hacer el deploy en Heroku
### package.jsonpackage.json
```
"name": "express-locallibrary-tutorial",  
"version": "0.0.0",  
```
**"engines": {  
"node": "8.9.1"  
},**  
```
"private": true,  
```
### app.js

Añadir una variable de entorno para la url de conexión a mongoDB

Cambiar:

```var mongoDB = 'mongodb://your_user_id:your_password@ds119748.mlab.com:19748/local_library';```

por 

```var mongoDB = process.env.MONGODB_URI || 'mongodb://your_user_id:your_password@ds119748.mlab.com:19748/local_library';```
  
  
