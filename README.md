¿Por qué son preferibles las variables de entorno a las credenciales hardcodeadas? Las variables de entorno son preferibles porque permiten separar la configuración sensitiva (secretos) del archivo fuente. Esto es muy importante por las siguientes razones:


Seguridad: Se evitarán poner en riesgo las contraseñas o las API keys. Te aseguras que no acaben en el repositorio de código (por ejemplo, Git).


Flexibilidad: Dota a tu aplicación de la característica de usar diferentes credenciales para distintos entornos (dev, test y prod) sin la necesidad de tener que modificar el código.


¿Qué ventaja te ofrece Docker Compose frente a lanzar contenedores por se separada? Docker Compose es la herramienta que te permite definir y orquestar una aplicación que conlleve varios contenedores (por ejemplo, una app web y una base de datos) de manera sencilla, como un único servicio. Su principal ventaja está en su sencillez de la orquestación, ya que puedes levantar todos los contenedores usando un solo fichero (docker-compose.yml) y un solo comando (por ejemplo, docker-compose up). Te configura sus redes de forma automática para que las distintas partes puedan comunicarse y te monta sus volúmenes.


¿Qué pasa si eliminas el volumen de datos docker volume rm db_data? Se eliminan de forma permanente todos los datos que se guardan en la base de datos (tablas, registros, etc.). El uso de volúmenes es para que los datos persistan pase lo que pase aunque se elimine el propio contenedor. Si borras el volumen db_data, estás borrando esos datos.
