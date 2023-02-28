# Frontend
A frontend application using reactjs.

## Get Started

``` bash
# Setting env vars
export REACT_APP_BACKEND_BASE_URL=http://localhost:3800

npm install
npm start
```

## Get Started with Docker

``` bash
docker run -d -p 3000:80 mifrontend:0.1.0-nginx-alpine
```

# Solucion Actividad 3 
Para la solucion de la aplicacion de la actividad 3, se agrego un archivo nginx.conf y en el nginx.Dockerfile se agrego la linea COPY default.conf /etc/nginx/conf.d/default.conf