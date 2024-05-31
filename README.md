
## Parcial Sobredosis de TV

- [Enunciado](https://docs.google.com/document/d/1PWOUE7_j_b085-esgH2-QkANAPVNzTBfvWccARGIzrE/edit?pli=1)


## Decisiones de diseño - Sobredosis de TV

## Dónde están los programas?

Opciones:
1. objeto Canal,
2. objeto Grilla (o clase Grilla)
3. Repositorio de Programas -> ojo porque no queremos que el repositorio tome otras responsabilidades que no sean alta, baja, modificación, consulta


## Cómo asocio restricciones a cumplir vs. acciones que deben ocurrir

Opciones
- Un programa tiene n restricciones y cada restricción m acciones
- Tener un objeto regla que sea conocido por el canal/grilla, que conozca n restricciones y m acciones pero también UN programa (tiene una indirección extra y además tengo que poder determinar si el programa está en revisión, es una solución más compleja)
- Un modelo que tenga reglas pero no se asocie a un programa le falta algo => hay que tomarlo en cuenta. Las restricciones NO son globales.
- Necesitamos separar por un lado las restricciones y por otro las acciones. Mezclarlas nos llevaría a no poder combinarlas.

## Cómo defino que un programa queda en revisión

Acá las opciones son parecidas:
- el canal o la grilla pone una lista de programas "En revisión"
- el programa tiene un estado "Normal" y otro "En revisión"

De esa manera podemos filtrar los programas para el proceso de revisión.

## Proceso principal

- Debo poder agregar n restricciones con m acciones asociadas, eso tiene agregarse ... al programa (o tengo que cambiar la información que almaceno)
