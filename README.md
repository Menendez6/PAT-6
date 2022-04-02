# Practica 6: Testing de una aplicacion de Spring Boot

## Ver la práctica
[![](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/Menendez6/PAT-6)

## Objetivo de la práctica

Dado un desarrollo de Spring Boot, es necesario anhadir tests a las siguientes clases:

- DNI & Telefono (Unit Tests) (Cada clase tiene un metodo y varias casuisticas para probar)
- ProcessController (E2E Tests) (2 endpoints)


## Pruebas

### DNI
En el caso de DNI, se prueban 4 casos diferentes:
- El primero es si el DNI ha sido escrito de forma correcta, y se comprueba que no hay fallo
- El segundo es cuando el DNI se encuentra entre los de la lista de no válidos, debe devolver false
- El tercero es cuando el DNI no sigue el formato DNI, es decir, que tenga una letra donde debería haber un número, por ejemplo.
- El último caso, es aquel en el que los números del DNI no concuerdan con la letra, siguiendo la relación de la división entre 23.

### Teléfono
En el caso del teléfono, hemos realizado 2 pruebas:
- La primera, con varios números tanto nacionales como internacionales válidos para ver si había algún fallo.
- La segunda, con números de teléfono falsos que no cumplen el registro de ningún número de teléfono en el mundo.

### End to end
Hemos comprobado también que al enviar los datos, la respuesta obtenida era la adecuada en dos casos:
- En primer lugar, comprobamos que al enviar los datos obtenemos una respuesta de OK tanto de status como en el cuerpo si los datos son correctos.
- En segundo lugar, comprobamos que al enviar los datos, el HTML que vamos a insertar en el documento también es el adecuado en función de si se han enviado los datos o ha habido algún error.