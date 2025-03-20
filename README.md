Este es un proyecto básico de Django que puede ser ejeuctada en diferentes entornos debido a la funcionalidad de los contenedores de Docker.
Tiene la función de demostrar como funciona un archivo Dockerfile para un entorno de desarrollo con el Framework Django, a su vez integrando un servidor proxy reverso con NGINX que permite recibir las peticiones HTTTP que hacen los usuarios y reditigirlos al servidor de Django.
En este proyecto se usa dos contenedores:
  . Contenedor1 => Para el servidor Django
                => El servidor Django ejecuta automaticamente el script "python manage.py runserver 0.0.0.0:8000" que pemrite levantar la aplicación en el puerto 8000.
  . Contenedir2 => Para el servidor proxy NGINX
Con un archivo docker-compose que construye los contenedores y los interconecta, haciendo que el servidor Proxy pueda funcionar solo si el servidor Django esta activo
=> Si el proyecto necesita de mas dependencias para Django solo sera necesario especificar cuales son las que necesitamos en el requirements.txt
=> Si necesitamos la integración de otros contenedores como Bases de Datos, será necesario especificarlo en el docker composer a través de una imagen de Docker para cada tipo de requerimiento.  
