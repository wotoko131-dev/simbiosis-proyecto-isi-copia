# Historias de usuario de búsqueda

| Campo | Valor |
| --- | --- |
| Proyecto | Proyecto Simbiosis |
| Fecha | 27/10/2026 |
| Versión | 0.1 |
| Estado | Borrador |

## Fuentes comunes

- [Acta de UC-21 Buscar recetas](../captura/acta-acuerdos-uc-21-buscar-recetas.md), v1.1, Vigente.
- [Catálogo de requisitos](catalogo-requisitos.md), UR-08 y FR pertinentes.
- [Modelo de casos de uso](../modelos/modelo-casos-de-uso.md), UC-21.

## Épica de búsqueda

Como usuario, quiero poder hacer una busqueda, para encontrar recetas.

**Estado:** descompuesta en US-01, US-02 y US-03. Conserva la necesidad conjunta.

## Justificación de la división

La búsqueda se puede hacer mediante diferentes filtros y opciones. Por ello, la división se basa en los diferentes criterios posibles para la búsqueda

## US-01

**Título:** Buscar por una palabra o frase

Como usuario, quiero buscar usando palabras o frases, para encontrar una receta en concreto.

**Fuentes:** UR-08; UC-21; FR-085; acta, 2. Acuerdos.

### Criterios de aceptación

- **CA-01.** Dado que una receta tenga la clave en su nombre o descripción, cuando busque usando una clave, entonces el sistema mostrará esa receta en los resultados.
- **CA-02.** Dado que se usen otros filtros, cuando buscamos por frases o palabras, entonces los resultados cumplirán ambos tipos de busqueda.
- **CA-03.** Dado que el sistema detecte un error como una falta ortográfica, cuando buscamos por texto, entonces el sistema muestra sugerencias de corrección, de haberlas.

## US-02

**Título:** Buscar por ingredientes incluidos

Como usuario, quiero usar los ingredientes incluidos como criterio de búsqueda, para encontrar recetas concretas.

**Fuentes:** UR-08; UC-21; FR-086; acta, 2. Acuerdos.

### Criterios de aceptación

- **CA-01.** Dada una receta que incluya un ingrediente en concreto, cuando use la búsqueda, entonces esa receta aparecerá en los resultados.
- **CA-02.** Dados varios ingredientes usados como criterio de inclusion, cuando se use la busqueda, los resultados contendrán todos los ingredientes usados como criterio.
- **CA-03.** Dado que un ingrediente aparece a la vez como criterio de inclusión y de exclusión, cuando el usuario busque, entonces se informa al usuario de que debe cambiarlo antes de hacer una búsqueda.

## US-03

**Título:** Buscar por ingredientes excluidos

Como usuario, quiero usar ingredientes como criterio de exclusion, para evitar recetas que tengan ese ingrediente.

**Fuentes:** UR-08; UC-21; FR-087; acta, 2. Acuerdos.

### Criterios de aceptación

- **CA-01.** Dada una receta que contenga un ingrediente concreto, cuando se use, entonces esa receta no estará en los resultados.
- **CA-02.** Dados varios ingredientes excluidos, cuando se busquen recetas, entonces las recetas resultantes no tendrán ninguno de ellos.
- **CA-03.** Dado que el usuario acepte sugerencias, cuando su búsqueda no se ha encontrado, entonces los resultados seguirán conservando las exclusiones.

## Revisión INVEST

La revisión abarca US-01, US-02 y US-03. «Aplicado» indica si se ha realizado la comprobación. «Cumple» indica si todas las historias cumplen el criterio. Si alguna no lo cumple, indicar «No» e identificar la historia y el motivo en la justificación. Si no se ha realizado la comprobación o faltan datos, indicar «Pendiente» en «Cumple».

| Criterio | Pregunta de revisión | Aplicado | Cumple | Justificación |
| --- | --- | --- | --- | --- |
| Independiente | ¿Puede implementarse cada historia y ofrecer un resultado útil sin implementar antes las otras historias del conjunto? Puede compartir infraestructura con ellas. | Si | Si | [Historias y motivo] |
| Negociable | ¿Cada historia explica qué necesita la persona y deja margen para discutir los detalles de la solución, respetando los acuerdos confirmados? | Si  | Si  | [Historias y motivo] |
| Valiosa | ¿La parte «para…» de cada historia explica el beneficio que obtiene la persona al usar esa capacidad? | Si  | Si  | [Historias y motivo] |
| Estimable | ¿Están claros el alcance y los datos necesarios para estimar el trabajo de cada historia? | Si  | Si  | [Historias y motivo] |
| Pequeña | ¿Se centra cada historia en una única capacidad de alcance manejable? | Si  | Si  | [Historias y motivo] |
| Comprobable | ¿Los criterios de aceptación de cada historia describen acciones y resultados observables que permiten distinguir un comportamiento correcto de uno incorrecto? | Si  | Si  | [Historias y motivo] |

## Dudas pendientes

[Cuestiones pendientes de aclaración. Si no quedan cuestiones, indicar «Ninguna».]
