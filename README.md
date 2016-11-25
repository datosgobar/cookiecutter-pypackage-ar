
# Cookiecutter PyPackage - Datos Argentina

Cookiecutter template para paquetes de Python del equipo de Datos Argentina.

*Nota: Este proyecto recién está comenzando a ser una **idea**, usar con precaución. Todavía deben adaptarse/traducirse varias partes y eliminar algunas cosas que no usamos.*

Esto es un fork del [audrey/cookiecutter-pypackage](https://github.com/audreyr/cookiecutter-pypackage/) que estamos adaptando y traduciendo para uso de los nuevos repositorios pythonicos del equipo de Datos.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Features](#features)
- [Instalación](#instalaci%C3%B3n)
- [Uso](#uso)
- [Release checklist](#release-checklist)
- [Otros cookiecutter templates](#otros-cookiecutter-templates)
- [Créditos](#cr%C3%A9ditos)
- [Contacto](#contacto)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Features

* Travis-CI: Preparado para integración continua con Travis CI.
* Sphinx docs: Documentación preparada para generar con ReadTheDocs.
* Auto-release a PyPI: Cada vez que se hace un *tag* con una nueva versión, se publica en PyPi automáticamente.

## Instalación

Instalar la última versión de Cookiecutter (este template requiere
Cookiecutter 1.4.0 o mayor)::

    pip install -U cookiecutter

## Uso

1. Crear un repositorio en Github y clonarlo localmente
2. `cookiecutter https://github.com/datosgobar/cookiecutter-pypackage-ar.git` para crear estructura del repo. Mover todo el contenido a la carpeta del repo clonado.
2. `pip install -r requirements_dev.txt` para instalar las dependencias de desarrollo (se recomienda crear un entorno virtual para el proyecto primero)
3. Ir a tu cuenta de Travis CI y agregar este repo (*switch on*)
4. `make pypi` para registrar el repo en Pip y activar el auto-deploy con tags en Travis CI (requiere una cuenta en PyPi).
5. Agregar el repo a tu cuenta de ReadTheDocs y *switch on* para activar el servicio.
  - `make docs` para crear la documentación localmente, luego pushear para que vaya a Read The Docs.

Para más detalles ver [cookiecutter-pypackage tutorial](https://cookiecutter-pypackage.readthedocs.io/en/latest/tutorial.html).

## Release checklist

Antes de cada nuevo release a PyPi, deben seguirse estos pasos:

0. Que corran OK todos los tests
1. Cambiar la versión en el `setup.py`
2. Cambiar la versión en el `__init__.py` del package `pydatajson`
3. Agregar una nueva entrada al `HISTORY.md` bulleteando brevemente las diferencias que tiene el nuevo release respecto del anterior
4. Correr `make docs` en el root del repo antes de pushear
5. Commitear y pushear
6. Taggear el commit con la versión del nuevo release

## Otros cookiecutter templates

Ver repositorio de [audrey/cookiecutter-pypackage](https://github.com/audreyr/cookiecutter-pypackage/) para otros templates de repos en python o directamente el de [audreyr/cookiecutter](https://github.com/audreyr/cookiecutter) para una lista de templates de todo tipo.

## Créditos

* [@audrey](https://github.com/audrey) por su fantástico *ultimate template* para un repositorio modelo en Python [audrey/cookiecutter-pypackage](https://github.com/audreyr/cookiecutter-pypackage/).

## Contacto

Te invitamos a [crearnos un issue](https://github.com/datosgobar/{{ cookiecutter.project_repo_name }}/issues/new?title=Encontre un bug en {{ cookiecutter.project_repo_name }}) en caso de que encuentres algún bug o tengas feedback de alguna parte de `{{ cookiecutter.project_repo_name }}`.

Para todo lo demás, podés mandarnos tu comentario o consulta a [datos@modernizacion.gob.ar](mailto:datos@modernizacion.gob.ar).
