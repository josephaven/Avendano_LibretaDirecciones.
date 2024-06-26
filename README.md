# Proyecto Libreta de Direcciones

## Sección A: Descripción
El sistema de libreta de direcciones es una aplicación basada en consola diseñada para gestionar información de contacto. Proporciona funcionalidades para cargar entradas desde un archivo, agregar nuevas entradas, eliminar entradas existentes, buscar entradas por apellido y listar todas las entradas. 


### A.1) Estado del sistema
**Carga de Entradas desde un Archivo:**
- **Estado:** Funciona correctamente.
- **Descripción:** El sistema permite al usuario cargar entradas de contacto desde un archivo de texto. Para que la carga sea exitosa, el usuario debe proporcionar la ruta completa del archivo (por ejemplo, C:\ruta\completa\a\Datos.txt). El archivo debe estar en formato CSV, donde cada línea representa una entrada de dirección con los siguientes campos separados por comas: nombre, apellido, calle, ciudad, estado, código postal, correo electrónico y teléfono. Una vez cargado el archivo, las entradas se almacenan en la libreta de direcciones y están disponibles para ser listadas o buscadas.

**Agregar una Nueva Entrada:**
- **Estado:** Funciona correctamente.
- **Descripción:** Los usuarios pueden agregar nuevas entradas de contacto proporcionando la información requerida directamente a través de la consola. La información incluye nombre, apellido, calle, ciudad, estado, código postal, correo electrónico y teléfono. La nueva entrada se agrega a la libreta de direcciones y se puede verificar su adición listando todas las entradas.

**Eliminar una Entrada:**
- **Estado:** Funciona correctamente.
- **Descripción:** Los usuarios pueden eliminar entradas de contacto existentes buscando por apellido. El sistema muestra todas las entradas que coinciden con el apellido proporcionado y permite al usuario seleccionar cuál de ellas eliminar. Si no se encuentran entradas con el apellido dado, el sistema informa al usuario.

**Buscar Entradas:**
- **Estado:** Funciona correctamente.
- **Descripción:** Los usuarios pueden buscar entradas en la libreta de direcciones proporcionando un apellido o el inicio de un apellido. El sistema devuelve todas las entradas que coinciden con el criterio de búsqueda y las muestra en la consola. Esta funcionalidad es útil para encontrar rápidamente información de contacto específica.

**Mostrar Todas las Entradas:**
- **Estado:** Funciona correctamente.
- **Descripción:** El sistema puede listar todas las entradas almacenadas en la libreta de direcciones. Esta funcionalidad permite al usuario revisar rápidamente toda la información de contacto disponible. Si no hay entradas en la libreta de direcciones, el sistema informa al usuario.

### A.2) Lista de clases
##### AddressBook
- **Propósito:** Gestiona una colección de entradas de direcciones. Permite agregar, eliminar, buscar, listar y cargar entradas desde un archivo.
- **Estructura de datos:** Utiliza un TreeMap<String, List<AddressEntry>> donde la clave es el apellido y el valor es una lista de entradas de direcciones con ese apellido.
- **Eficiencia:** Las operaciones de agregar y eliminar son eficientes, aunque la búsqueda tiene una complejidad lineal debido a la necesidad de recorrer la lista.

##### AddressEntry
- **Propósito:** Representa una entrada de dirección con información de contacto como nombre, apellido, calle, ciudad, estado, código postal, correo electrónico y teléfono.
- **Estructura de datos:** Contiene variables de clase para almacenar información como nombre, apellido, calle, ciudad, estado, código postal, correo electrónico, y teléfono. 
- **Eficiencia:** Los métodos set y get tienen una complejidad constante.

##### AddressBookApplication
- **Propósito:** Clase principal que inicia la aplicación de la libreta de direcciones y muestra el menú.
- **Estructura de Datos:** Contiene el método main que crea una instancia de AddressBook y Menu, y llama al método displayMenu.
- **Eficiencia:** Maneja las operaciones de entrada/salida y coordina las acciones del usuario con las funciones de la libreta de direcciones.

##### Menu
- **Propósito:** Proporciona una interfaz de usuario para interactuar con la libreta de direcciones. Ofrece opciones para cargar entradas desde un archivo, agregar, eliminar, buscar y listar entradas.
- **Estructura de Datos:** Utiliza un Scanner para la entrada del usuario y métodos que interactúan con una instancia de AddressBook.
- **Eficiencia:** La eficiencia depende de las operaciones subyacentes que invoca en AddressBook.

## Sección B: URL de JavaDoc
La documentación JavaDoc del proyecto está disponible en el siguiente enlace:
https://steady-capybara-4431d8.netlify.app/

## Sección C: UML/Diseño
### C.1) Diagrama de jerarquía de clases UML
![Diagrama en blanco (1)](https://github.com/josephaven/Avenda-o_LibretaDirecciones./assets/153795069/28de47ab-ed6b-4190-b7a4-01c2fddea02b)


## Sección D: Capturas de pantalla del sistema
### D.1) Evidencia 1
Leer entradas del archivo de datos seguidas de Mostrar listado. El archivo de datos debe contener un mínimo de 2 direcciones. Incluir captura de pantalla de salida y también mostrar el contenido correspondiente del archivo de datos.

**Archivo:**
![image](https://github.com/josephaven/Avenda-o_LibretaDirecciones./assets/153795069/e71d7d9b-8ac3-453d-8afb-9af66d7ec402)

**Salida:**
![image](https://github.com/josephaven/Avenda-o_LibretaDirecciones./assets/153795069/e7aba8c1-066e-4751-9878-69a377677fcf)

### D.2) Evidencia 2
Inmediatamente después de D.1, agregue un nuevo objeto AddressEntry seguido de un mostrar el resultado de un nuevo listado en consola.

![image](https://github.com/josephaven/Avenda-o_LibretaDirecciones./assets/153795069/11b6dcf8-5484-46bc-95bd-667b304dfed8)
![image](https://github.com/josephaven/Avenda-o_LibretaDirecciones./assets/153795069/49b69ce7-6265-4318-9778-b9cd42474c05)



### D.3) Evidencia 3
Inmediatamente después de D.2 hacer una eliminación de una entrada seguida de un mostrar listado.
![image](https://github.com/josephaven/Avenda-o_LibretaDirecciones./assets/153795069/ef47017e-5635-4060-a176-5db33ae96393)
![image](https://github.com/josephaven/Avenda-o_LibretaDirecciones./assets/153795069/baecfb4c-8eb1-4fa3-947f-c97965a6ff29)


### D.4) Evidencia 4
Inmediatamente siguiendo D.3 hago una búsqueda usando una entrada que debería recuperar al menos una entrada. Ahora haga una búsqueda usando una entrada que no debería recuperar ninguna entrada.

**Entrada que deberia ser recuperada:**

![image](https://github.com/josephaven/Avenda-o_LibretaDirecciones./assets/153795069/bd178503-943e-4571-918e-bb70f65f5640)



**Entrada que deberia no ser recuperada:**

![image](https://github.com/josephaven/Avenda-o_LibretaDirecciones./assets/153795069/2c63feaf-0f43-46a3-b914-745a5f924249)


### D.5) PSP
Adjunto el link de mi PSP: 
https://docs.google.com/spreadsheets/d/1Ojdku2QltyRpMDz17iu3HNfK1VGl0YTK/edit?usp=sharing&ouid=102900964963172073823&rtpof=true&sd=true

