# Viva Global Admin Panel

## Descripción

El objetivo de este proyecto es crear una herramienta la cuál permita al usuario la manipulación de distintos módulos, proporcionando de manera sencilla la interacción con APIs sin tener que tener conocimientos de código. También se utilizan las tecnologías más recientes a la fecha en este proyecto, permitiendo que este tenga una vida útil superior, además de esta manera permitir su mantenibilidad.

También tiene el beneficio que al ser modular la escalabilidad de este es bastante fácil, al solamente tener que añadir componentes para la funcionalidad, es por ello que también se implementó con principios de arquitectura limpia y diseño atómico.

## Tabla de contenido

- [Arquitectura](#arquitectura)
- [Instalación](#instalacion)
- [Uso](#uso)
- [Creditos](#creditos)
- [Licencia](#licencia)

## Arquitectura

![Logo](https://programmingideaswithjake.files.wordpress.com/2022/12/untitled.png)

La arquitectura que emplea este proyecto es una basada de la [Clean Architecture](https://medium.com/profusion-engineering/clean-architecture-a-practical-approach-cfc86ceac994) ([repositorio de ejemplo](https://gitlab.com/taager-com/examples/-/tree/main/clean-architecture-angular)).

![Logo](https://www.ngserve.io/content/images/size/w2000/2024/05/xatomic-design-product-1024x604.jpg.pagespeed.ic.imHmsDQ4HL.webp)

Además se al momento de crear componentes se realizaron basados al [Atomic Design](https://www.auberginesolutions.com/blog/how-to-use-angular-and-atomic-design-to-create-web-applications-a-guide-for-new-developers/).

### Estructura de Carpetas

```sh
.
  | - src
  |  | - app
  |  | - assets
  |  |  | - fonts
  |  |  | - icons
  |  |  | - img
  |  |  | - lotties
  |  | - common
  |  |  | - models
  |  |  | - utils
  |  | - core
  |  |  | - base
  |  |  | - domain
  |  |  |  | - auth
  |  |  |  | - persistence
  |  |  |  | - users
  |  |  |  | - ...
  |  |  |  |  | - models
  |  |  |  |  | - repositories
  |  |  |  |  | - services
  |  |  |  |  | - usecases
  |  | - data
  |  |  | - auth
  |  |  | - persistence
  |  |  | - users
  |  |  | - ...
  |  |  |  | - providers
  |  |  |  | - repositories
  |  |  |  | - services
  |  | - environments
  |  | - styles
  |  |  | - layout
  |  |  | - navigation
  |  |  | - variables
  |  | - ui
  |  |  | - pages
  |  |  | - shared
  |  |  |  | - components
  |  |  |  | - icons
```

#### APP

Esta carpeta contiene los módulos y componentes principales de la aplicación. Aquí se encuentra la estructura fundamental del proyecto y el `AppComponent`, que es el punto de entrada del módulo raíz de la aplicación Angular.

#### ASSETS

Esta carpeta almacena archivos estáticos como imágenes, fuentes, iconos, archivos JSON, entre otros. El contenido de esta carpeta es accesible públicamente y se puede cargar directamente desde el navegador.

#### COMMON

Aquí se encuentran los componentes y utilidades reutilizables en varias partes de la aplicación. Esta carpeta puede incluir directivas, pipes personalizados, y servicios que son comunes a todo el proyecto.

#### CORE

Esta carpeta contiene servicios de nivel superior y clases centrales que se inicializan una sola vez en toda la aplicación, como `AuthService`, `ApiService`, o interceptores.

#### DATA

Esta carpeta se encarga de gestionar la lógica relacionada con la obtención y manipulación de datos, como modelos, interfaces, repositorios, y casos de uso que interactúan con APIs o fuentes de datos. Se gestionan mediante servicios que se inyectan directamente en los componentes standalone.

#### ENVIRONMENTS

Contiene archivos de configuración para distintos entornos (production, development). Los archivos de entorno, como environment.ts y environment.dev.ts, definen variables específicas para cada entorno de despliegue.

#### STYLES

En esta carpeta se encuentran los archivos de estilos globales como `styles.scss`. Aquí puedes definir estilos compartidos, variables de diseño, mixins, y clases CSS reutilizables en toda la aplicación. Los estilos globales son aplicados en la configuración principal del proyecto.

#### UI

Esta carpeta alberga los componentes standalone relacionados con la interfaz gráfica. Aquí se encuentran los componentes de la interfaz de usuario (UI) construidos con Angular. Estos componentes standalone son responsables de la presentación visual y la interacción con el usuario.

## Instalacion

La instalación de este proyecto es bastante sencilla, pero son necesarias tener instaladas ciertas versiones para su ambientación

### Requisitos

- Node [20.18.0]
- Angular CLI [18.2.7]
- Dependencias del proyecto

#### Pasos para la instalación

##### Node

1. Utilizar NVM (no es obligatorio, pero altamente recomendable)

    ```sh
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash
    ```

2. Instalar la versión necesaria

    ```sh
    nvm install 20.18.0
    ```

3. Utilizar la versión descargada

    ```sh
    nvm use 20.18.0
    ```

##### Angular CLI

- Correr el siguiente comando (necesaria la versión de node especificada):

    ```sh
    npm install -g @angular/cli@18.2.7
    ```

##### Dependencias del proyecto

- Correr el siguiente comando ubicandose dentro de la raíz del proyecto (necesaria la versión de node especificada):

    ```sh
    npm install
    ```

## Uso

Para correr el proyecto después de la instalación se ejecuta el siguiente comando dentro de la raíz del proyecto:

```sh
npm start
```

O en su lugar utilizar el comando del Angular CLI

```sh
ng serve
```

## Creditos

## Licencia
