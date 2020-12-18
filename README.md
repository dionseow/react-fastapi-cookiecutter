# React/Fastapi cookiecutter
This cookiecutter uses react as a frontend and fastapi as a backend.  
It was created to easily prototype data science POCs  

## Prerequisites
docker

## Modes
There are 2 different modes available, production mode and development mode  

Production mode builds the frontend as static html and then serves these files via nginx.  
To connect to the backend, nginx is configured to proxy all /api endpoints to the backend container (http://backend/api)  

Development mode runs both a frontend node server and backend fastapi server that are automatically reloaded  
To connect to the backend, the node server has been configured to proxy all unknown endpoints to the backend container (http://backend).   
This is done via the proxy settings in package.json  


### Production mode

```docker-compose -f docker-compose-prod.yml up --build```

### Development mode

```docker-compose up --build```

