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

Como usuario verificado, quiero poder hacer una busqueda, para encontrar recetas.

**Estado:** descompuesta en US-01, US-02 y US-03. Conserva la necesidad conjunta.

## Justificación de la división

La búsqueda se puede hacer mediante diferentes filtros y opciones. Por ello, la división se basa en los diferentes criterios posibles para la búsqueda

## US-01

**Título:** Buscar por una palabra o frase

Como usuario verificado, quiero buscar usando palabras o frases, para encontrar una receta en concreto.

**Fuentes:** UR-08; UC-21; FR-085; acta, 2. Acuerdos.

### Criterios de aceptación

- **CA-01.** Dada una receta que tenga texto coincidente con el criterio en su nombre o descripción, cuando busque usando palabras o frases como criterio, entonces el sistema mostrará esa receta en los resultados.
- **CA-02.** Dados otros criterios de búsqueda simultáneos, cuando se busca por frases o palabras, entonces el sistema mostrará recetas que cumplan todos los criterios a la vez.
- **CA-03.** Dado un error detectado como fallo ortográfico en un texto que lo admita, cuando se busca por palabras o frases, entonces el sistema muestra sugerencias para corregir el error.

## US-02

**Título:** Buscar por ingredientes incluidos

Como usuario verificado, quiero usar los ingredientes incluidos como criterio de búsqueda, para encontrar recetas concretas.

**Fuentes:** UR-08; UC-21; FR-086; acta, 2. Acuerdos.

### Criterios de aceptación

- **CA-01.** Dada una receta con un ingrediente en concreto, cuando se use ese ingrediente como criterio de inclusion, entonces esa receta aparecerá en los resultados.
- **CA-02.** Dados varios ingredientes usados como criterio de inclusión, cuando se use la búsqueda, entonces los resultados contendrán todos los ingredientes usados como criterio.
- **CA-03.** Dado un ingrediente usado a la vez como criterio de inclusión y de exclusión, cuando se utilice la búsqueda, entonces se informa al usuario de que debe corregir, denegando la búsqueda.

## US-03

**Título:** Buscar por ingredientes excluidos

Como usuario verificado, quiero usar ingredientes como criterio de exclusion, para evitar recetas que tengan ese ingrediente.

**Fuentes:** UR-08; UC-21; FR-087; acta, 2. Acuerdos.

### Criterios de aceptación

- **CA-01.** Dada una receta que contenga un ingrediente concreto, cuando se use, entonces esa receta no estará en los resultados.
- **CA-02.** Dados varios ingredientes excluidos, cuando se busquen recetas, entonces las recetas resultantes no tendrán ninguno de ellos.
- **CA-03.** Dado que el usuario acepte sugerencias, cuando su búsqueda no se ha encontrado, entonces los resultados seguirán conservando las exclusiones.

## Revisión INVEST

La revisión abarca US-01, US-02 y US-03. «Aplicado» indica si se ha realizado la comprobación. «Cumple» indica si todas las historias cumplen el criterio. Si alguna no lo cumple, indicar «No» e identificar la historia y el motivo en la justificación. Si no se ha realizado la comprobación o faltan datos, indicar «Pendiente» en «Cumple».

| Criterio | Pregunta de revisión | Aplicado | Cumple | Justificación |
| --- | --- | --- | --- | --- |
| Independiente | ¿Puede implementarse cada historia y ofrecer un resultado útil sin implementar antes las otras historias del conjunto? Puede compartir infraestructura con ellas. | Si | Si |  |
| Negociable | ¿Cada historia explica qué necesita la persona y deja margen para discutir los detalles de la solución, respetando los acuerdos confirmados? | Si  | Si  |  |
| Valiosa | ¿La parte «para…» de cada historia explica el beneficio que obtiene la persona al usar esa capacidad? | Si  | Si  | |
| Estimable | ¿Están claros el alcance y los datos necesarios para estimar el trabajo de cada historia? | Si  | Si  |  |
| Pequeña | ¿Se centra cada historia en una única capacidad de alcance manejable? | Si  | Si  | |
| Comprobable | ¿Los criterios de aceptación de cada historia describen acciones y resultados observables que permiten distinguir un comportamiento correcto de uno incorrecto? | Si  | Si  |  |

## Dudas pendientes

Ninguna
