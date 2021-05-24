# Angular: Pruebas Unitarias con Jasmine y Karma.

## Conceptos generales
- ¿Qué es un test unitario?

Test Unitario es el encargado de **comprobar que un fragmeto de codigo funciona** correctamente (Ej: metodos). El conjunto de estas pruebas nos ayudan a garantizar el funcionamiento de una aplicacion.

- Unit test - Integration test - E2E



Unit Test: Solo testean metodo dentro de las clases, si necesitan acceso a otras clases estan se van a simular.
 
Test de integracion: Los acceso a otras clases no seran simuladors

E2E: Simular un usuario real utilizando la aplicacion.

![Unit test - Integration test - E2E](./readme/typetest.png)

Mas arriba de la piramide ams lienas de codigo podremos probar con menos cantidad de casos de prueba.
 
Por lo que al realizar test unitarios del metodo getProducts del componente deberiamos llamar a otra clase (servicio), pero como ya digimos esto no se debe hacer en los test unitarios debemos SIMULAR esta ultima. El porque de esto es ya que imaginemos que el metodo getProducts() tiene alguna error si intanciamos el servicio real en los test unitarios del componente estos van a fallar pero el fallo no esta en el componente sino que en el servicio. Si conseguimos esto que los test unitarios esten totalmente aislados entre clases el debug/ busqueda de errores sera sumamente simple. 
- ¿Cómo funciona un test unitario?
  
 ![Como funciona](./readme/howworks.png)

 En este ejemplo el componente tiene 3 metodos que lo que hacen es llaman a otros metodo en el servicio. 
  

- Cobertura/Coverage

Cobertura es una medida en porcentake que mide el grado en que el codigo fuente de un programa ha sido comprobado. Esto se calcula en base a la totalidad de las lineas de codigo vs la totalidad de lines probadas. 60 - 80 estimado,

- Jasmine y Karma

**Jasmine** es un marco de pruebas javascript y es el utilizado por Angular
**Karma** es una herramienta web que nos permite ejerutar en un navegador pruebas de jasmine.  

## Jasmine y Karma


- Configuración de Karma

**angular.js**:

Opcion para por default siempre calcular coverage.
![angularjsoncodecoverage](./readme/angularjsoncodecoverage.png)

**karma.conf.js**

![karma](./readme/karma.png)

Configuracion de karma.


- Carpeta coverage

- Lanzar tests

- Nueva dependencia en Karma (Angular 11 o superior)
