# Cardinal

## 1. ¿Qué es Cardinal?

Cardinal es un proyecto que busca aumentar las herramientas que pueden usar los estudiantes, ya sean universitarios o de colegios, y permitirle a los docentes manejar dichas herramientas mediante permisos y conteo de estudiantes usando el programa durante sus clases.

## 2. ¿Qué problema pretende resolver?

La educación actual se ha quedado atrás en comparación con las herramientas que tienen los estudiantes para usar actualmente y, por el miedo a recurrir a la trampa o a la pereza, estas herramientas se restringen o directamente se omiten.

Con Cardinal buscamos que tanto profesor como estudiante puedan utilizar estas herramientas sin que se les salga de las manos. El estudiante podrá usar herramientas de manera restringida por el profesor, quien escoge qué herramientas, páginas o programas podría llegar a utilizar, bloqueando las demás y así haciendo que el estudiante se desenvuelva con lo dado.

Al darle limitaciones con las herramientas actuales no queremos que el estudiante se vea sin opciones o "amarrado", sino que busque sacarle el máximo provecho a las herramientas dadas, así logrando que el estudiante logre desenvolverse en un entorno controlado.

## 3. Objetivo general

Mejorar el modelo de enseñanza y el aprendizaje de los estudiantes, permitiendo así que tanto maestro como alumno aprendan el uso de las herramientas actuales, aplicándolo a la vida real.

## 4. Objetivos específicos

* Mejorar el modelo académico y evaluativo.
* Retirar el miedo a las herramientas que salen día con día.
* Permitir el desarrollo de un entorno para el desarrollo de habilidades.
* Mejorar el entendimiento maestro-alumno con la familiaridad de las herramientas propuestas.
* Permitir a los estudiantes el aprendizaje mayoritario del uso de las herramientas en un entorno controlado.

## 5. Alcance inicial

Esto será un proyecto que se probará en una clase universitaria real cuando esté finalizado para probar su efectividad.

Inicialmente, Cardinal estará orientado a equipos que utilicen GNU/Linux dentro de un entorno académico y que puedan ser administrados por la institución educativa.

La primera versión se enfocará en permitir al docente controlar temporalmente las aplicaciones y páginas web que pueden utilizar los estudiantes durante una actividad o clase.

## 6. Actores

### 6.1. Docente

Es el encargado de administrar Cardinal durante una clase o actividad académica.

El docente podrá:

* Iniciar una sesión académica.
* Seleccionar los estudiantes o equipos que participarán.
* Seleccionar las páginas web permitidas.
* Seleccionar los programas permitidos.
* Establecer las restricciones de la sesión.
* Iniciar y finalizar el modo controlado.
* Consultar qué estudiantes están conectados.
* Consultar el estado de los equipos.

### 6.2. Estudiante

Es quien utiliza el computador durante la sesión académica.

El estudiante podrá:

* Utilizar las herramientas autorizadas por el docente.
* Acceder a las páginas permitidas.
* Ejecutar los programas permitidos.
* Conocer las restricciones que se encuentran activas, cuando Cardinal lo permita.
* Utilizar las herramientas proporcionadas dentro del entorno controlado.

El estudiante no podrá modificar las restricciones establecidas por el docente durante la sesión.

### 6.3. Administrador

Es el encargado de la configuración general del sistema.

El administrador podrá:

* Registrar equipos.
* Configurar Cardinal.
* Administrar docentes.
* Administrar estudiantes o grupos.
* Configurar parámetros generales.
* Realizar mantenimiento del sistema.

Algunas de estas funciones podrán quedar para versiones posteriores del proyecto.

## 7. Funcionamiento general

El funcionamiento inicial de Cardinal será el siguiente:

```text
Docente
   │
   ▼
Inicia sesión en Cardinal
   │
   ▼
Crea una sesión académica
   │
   ▼
Selecciona herramientas permitidas
   │
   ├── Páginas web
   └── Programas
   │
   ▼
Selecciona los equipos/estudiantes
   │
   ▼
Inicia la sesión
   │
   ▼
Cardinal envía las restricciones
   │
   ▼
Computadores de estudiantes
   │
   ├── Herramienta permitida → Acceso
   │
   └── Herramienta no permitida → Bloqueada
   │
   ▼
Docente finaliza la sesión
   │
   ▼
Cardinal restaura el acceso normal
```

## 8. Requisitos funcionales

### RF-01 — Gestión de sesiones

Cardinal deberá permitir al docente crear, iniciar y finalizar sesiones académicas.

### RF-02 — Gestión de estudiantes y equipos

Cardinal deberá permitir al docente identificar los estudiantes o equipos que participarán en una sesión.

### RF-03 — Gestión de aplicaciones

Cardinal deberá permitir al docente seleccionar las aplicaciones que podrán utilizar los estudiantes durante una sesión.

### RF-04 — Gestión de sitios web

Cardinal deberá permitir al docente seleccionar los sitios web que podrán ser utilizados durante una sesión.

### RF-05 — Aplicación de restricciones

Cardinal deberá aplicar las restricciones configuradas por el docente durante la sesión.

### RF-06 — Bloqueo de recursos no autorizados

Cardinal deberá impedir temporalmente el acceso a aplicaciones y sitios web que no hayan sido autorizados.

### RF-07 — Restauración del acceso

Cardinal deberá restaurar el acceso normal de los equipos al finalizar una sesión.

### RF-08 — Estado de los equipos

Cardinal deberá permitir al docente consultar el estado de conexión de los equipos participantes.

### RF-09 — Comunicación

Cardinal deberá permitir la comunicación entre el equipo del docente y los equipos de los estudiantes.

### RF-10 — Identificación de equipos

Cardinal deberá identificar cada equipo conectado mediante un identificador único.

## 9. Requisitos no funcionales

### RNF-01 — Sistema operativo

El cliente de Cardinal deberá funcionar en sistemas GNU/Linux compatibles.

### RNF-02 — Seguridad

Las restricciones aplicadas al equipo del estudiante no deberán poder modificarse desde la interfaz normal del estudiante.

### RNF-03 — Rendimiento

Cardinal deberá consumir una cantidad razonable de recursos del sistema para no interferir significativamente con las actividades académicas.

### RNF-04 — Disponibilidad

El sistema deberá poder mantener una sesión activa mientras exista comunicación entre el servidor y los clientes.

### RNF-05 — Usabilidad

La interfaz del docente deberá permitir configurar una sesión sin requerir conocimientos avanzados de administración de sistemas Linux.

### RNF-06 — Recuperación

Al finalizar una sesión, Cardinal deberá restaurar las configuraciones modificadas durante la sesión.

## 10. Restricciones del proyecto

La primera versión de Cardinal estará diseñada principalmente para:

* Sistemas GNU/Linux.
* Entornos educativos.
* Computadores administrados por la institución.
* Control temporal de recursos.
* Aplicaciones y sitios web seleccionados por el docente.

Inicialmente no se contempla:

* Compatibilidad inmediata con Windows o macOS.
* Administración de computadores personales que no estén administrados por la institución.
* Administración remota fuera de la red académica.
* Captura de pantalla permanente de los estudiantes.
* Vigilancia innecesaria del estudiante.
* Registro innecesario de información personal.

Estas funciones podrán ser evaluadas posteriormente si son necesarias para el proyecto.

## 11. Tecnologías previstas

Las tecnologías planteadas inicialmente para el desarrollo de Cardinal son:

* **Python:** lenguaje principal.
* **FastAPI:** desarrollo del servidor y API.
* **HTML, CSS y JavaScript:** interfaz del sistema.
* **SQLite:** base de datos inicial.
* **HTTP y WebSocket:** comunicación entre los componentes.
* **systemd:** administración del cliente como servicio en Linux.
* **nftables:** control del tráfico de red.
* **Git:** control de versiones.
* **GitHub:** almacenamiento y colaboración del código.

Estas tecnologías son una propuesta inicial y podrán cambiar durante el desarrollo si se encuentra una alternativa más adecuada.

## 12. Arquitectura inicial

Cardinal estará compuesto inicialmente por un servidor, un panel de control para el docente y clientes instalados en los computadores de los estudiantes.

```text
                    CARDINAL
                       │
             ┌─────────┴─────────┐
             │                   │
          SERVIDOR             CLIENTE
             │                   │
             │              Computador
             │                estudiante
             │                   │
             ▼                   ▼
          FastAPI             Python
             │                   │
             │   WebSocket       │
             └───────────────────┘
                       │
                       ▼
                Política activa
                       │
                ┌──────┴──────┐
                ▼             ▼
            Aplicaciones    Internet
```

El servidor será el encargado de gestionar las sesiones y las políticas establecidas por el docente.

El cliente será el encargado de recibir dichas políticas y aplicarlas en el computador del estudiante.

## 13. Filosofía del proyecto

Cardinal no busca que el estudiante se vea sin opciones o "amarrado" por las restricciones.

El objetivo es permitir que el estudiante utilice las herramientas actuales dentro de un entorno controlado, buscando que aprenda a sacarles el máximo provecho a las herramientas proporcionadas por el docente.

La restricción de herramientas busca convertirse en una oportunidad para que el estudiante se desenvuelva con los recursos disponibles, en lugar de simplemente impedir su utilización.

## 14. Estado del proyecto

**Estado actual:** planificación inicial.

En esta etapa se están definiendo:

* El propósito del proyecto.
* El problema que busca resolver.
* Los objetivos.
* El alcance.
* Los actores.
* Los requisitos.
* La arquitectura inicial.
* Las tecnologías que serán utilizadas.

El desarrollo del software comenzará una vez finalizada la planificación inicial.
