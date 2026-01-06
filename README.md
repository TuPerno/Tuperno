# Tuperno

## Descripción del Proyecto
Este repositorio contiene el desarrollo y documentación asociada a la creación de una landing page para la ferretería Tuperno.
El proyecto busca establecer presencia digital, aumentando la visibilidad del negocio y el contacto con potenciales clientes.

## Flujo de Trabajo en Git
El repositorio se organiza en tres capas principales:

- `main`: Rama estable del proyecto. Contiene la versión validada.
- `integration`: Rama de integración, utilizada como paso previo a la liberación hacia main.
- `develop`: Rama de desarrollo continuo, integrando los avances del equipo.

El desarrollo se realiza mediante ramas de tipo `feature/`, las cuales deben crearse siempre a partir de la rama `develop`. Cada rama `feature` representa una tarea o funcionalidad específica del proyecto.
Por ejemplo: `feature/levantamiento-doc`, `feature/landing-wireframe`

### Flujo de integración hacia main

1. El equipo desarrolla los cambios en una rama `feature/`
2. Los cambios se integran mediante Pull Request desde la rama `feature/` hacia la rama `develop`
3. Al completar un hito relevante del proyecto, se deberá realizar una Pull Request desde `develop` hacia `integration`
4. Luego de validar los cambios en la rama `integration` se hará la Pull Request hacia `main`

Este flujo de trabajo permite revisar los cambios y detectar errores, manteniendo la rama main siempre estable.
