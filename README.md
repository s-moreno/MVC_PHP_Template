## Patrón MVC en PHP

Estructura típica de un proyecto PHP organizado en el patrón de arquitectura MVC (Modelo-Vista-Controlador). Vamos a ver la función de cada carpeta:

- `app/`:
  - **Propósito**: Contiene el núcleo de la aplicación.
  - Subcarpetas:
    - `controllers/:` Aquí se almacenan los controladores. Los controladores son clases que manejan la lógica de la aplicación y actúan como intermediarios entre los modelos y las vistas. Reciben las solicitudes del usuario, interactúan con los modelos y determinan qué vista devolver.
    - `core/`: Suele contener el núcleo de la aplicación, como las clases base para los controladores y los modelos, y el archivo de enrutamiento. Aquí también podríamos encontrar clases utilitarias, ayudantes y componentes de inicialización.
    - `models/`: Aquí se ubican los modelos, que representan los datos y la lógica de negocio de la aplicación. Los modelos se encargan de acceder a la base de datos, realizar operaciones CRUD (crear, leer, actualizar, eliminar) y manipular los datos.
    - `views/`: Almacena las vistas de la aplicación, que son archivos PHP responsables de la interfaz de usuario. Cada vista muestra los datos proporcionados por el controlador en una plantilla HTML para ser mostrada al usuario.
- `public/`:
  - **Propósito**: Esta carpeta contiene los archivos públicos de la aplicación, es decir, los que son accesibles directamente desde el navegador.
  - **Contenido**: Normalmente contiene el archivo index.php (punto de entrada de la aplicación), archivos CSS, JavaScript y otros activos (imágenes, fuentes, etc.). index.php suele ser el primer archivo que se ejecuta, iniciando el proceso de enrutamiento y carga de controladores.
- `config/`:
  - **Propósito**: Contiene archivos de configuración de la aplicación. Aquí podrías encontrar archivos para gestionar la configuración de la base de datos, la carga de clases, la configuración del entorno, y otros ajustes generales.
- `vendor/`:
  - **Propósito**: Almacena las dependencias y paquetes externos instalados mediante Composer (el gestor de dependencias en PHP).
  - **Contenido**: Esta carpeta se crea cuando ejecutas composer install y contiene bibliotecas de terceros que ayudan a extender la funcionalidad de la aplicación, como el autoload de Composer.
- `logs/`:
  - **Propósito**: Esta carpeta suele utilizarse para almacenar archivos de log o registro. Los logs ayudan a rastrear errores, advertencias y la actividad general de la aplicación. Puede ser útil para monitorear el comportamiento del sistema y diagnosticar problemas.
