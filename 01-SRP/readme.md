# Principio de responsabilidad única (SRP)

## ¿Qué es el SRP?

El principio de responsabilidad única (SRP) establece que una clase debe tener una única responsabilidad. Esto significa que una clase debe tener solo una razón para cambiar, y esa razón debe ser su responsabilidad única.


## ¿Cómo se aplica el SRP en Javascript?

En JavaScript, podemos aplicar el principio de responsabilidad única de varias maneras. Una de ellas es mediante la creación de funciones y objetos que tengan una única responsabilidad clara.


Por ejemplo, si tenemos una clase que se encarga de manejar la validación de formularios y, al mismo tiempo, se encarga de realizar la llamada a una API para enviar los datos del formulario, esto viola el principio de responsabilidad única. En su lugar, deberíamos tener dos clases diferentes: una para la validación del formulario y otra para la llamada a la API.

Veamos un ejemplo concreto en JavaScript:

``` javascript
class ValidadorFormulario {
  constructor(formulario) {
    this.formulario = formulario;
  }
  
  validar() {
    // Lógica de validación del formulario
  }
}

class EnviarDatosFormulario {
  constructor(formulario) {
    this.formulario = formulario;
  }
  
  enviar() {
    // Lógica para enviar los datos del formulario a través de una API
  }
}
```

En este ejemplo, hemos creado dos clases diferentes: ValidadorFormulario y EnviarDatosFormulario. La primera se encarga de la validación del formulario, mientras que la segunda se encarga de enviar los datos a través de una API.

De esta manera, hemos aplicado el principio de responsabilidad única, ya que cada clase tiene una única responsabilidad y una única razón para cambiar. Si en el futuro necesitamos cambiar la lógica de validación del formulario, solo tendremos que hacer cambios en la clase ValidadorFormulario, sin afectar a la clase EnviarDatosFormulario.

En resumen, al aplicar el principio de responsabilidad única en JavaScript, podemos mejorar la calidad y mantenibilidad de nuestro código, creando clases y objetos que tengan una única responsabilidad clara y evitando clases con múltiples responsabilidades que puedan causar problemas de mantenibilidad en el futuro.

[ 🏠 Regresar al Menu](https://github.com/holasoymalva/curso-principios-solid)
