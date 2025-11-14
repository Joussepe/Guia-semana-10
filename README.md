# 🧠 Implementación  
### *Dev Kata — El Desafío del Estudio*

Proyecto desarrollado para la **Guía Práctica #12** del curso *Desarrollo de Videojuegos*.  
Aquí implementamos una IA basada en el **Patrón State**, un sistema de aturdimiento (*StunState*) y un arma láser interactiva.

---

## 🎮 Nombre del Estudio:  
**FraJou**

---

## 👥 Miembros y Roles  

| Miembro | Rol | Descripción |
|--------|------|-------------|
| **Camargo Ambicho Joussepe Josue** | Arquitecto de IA | Implementación del Patrón State, creación del *StunState*, lógica del AIController. |
| **Rojas Ortis Franklin** | Diseñador de Comportamiento | Configuración del enemigo, Waypoints, valores de búsqueda, velocidad y ajustes de *stunDuration*. |

---

## 🧩 Descripción del Hito  
Este hito consistió en implementar una IA completa utilizando el **Patrón State**, integrarla al entorno del jugador y añadir un sistema de aturdimiento mediante un arma láser. En esta práctica implementamos un sistema de Inteligencia Artificial completo basado en el Patrón de Diseño *State*. La IA del enemigo ahora cuenta con tres comportamientos principales: patrullar una ruta establecida, detectar y perseguir al jugador, y un nuevo estado de aturdimiento (*StunState*) que detiene temporalmente al agente mediante un arma láser creada por el equipo. Este hito integró programación y configuración en Unity para lograr una IA funcional.

Se desarrolló lo siguiente:

- ✔️ **Patrulla automática** usando `NavMeshAgent`.  
- ✔️ **Estados IA:** `PatrolState`, `ChaseState`, `StunState`.  
- ✔️ **Sistema de aturdimiento:** La IA se detiene durante un tiempo configurable.  
- ✔️ **Láser interactivo:** Implementado con **Raycast + LineRenderer**.  
- ✔️ **Configuración del diseñador:** Ajuste de radios, velocidades, rutas y temporizadores.  
- ✔️ **Integración y pruebas:** Colocación de prefabs, control de escenas y revisión en equipo.

---

## 💭 Reflexión del Estudio

### **1. Sinergia y Fricción: ¿Cuál fue el mayor beneficio de trabajar en equipo para esta tarea? ¿Y cuál fue el mayor desafío de comunicación o coordinación que enfrentaron y cómo lo resolvieron?**  
El mayor beneficio de trabajar en equipo fue la combinación de perspectivas. Cada integrante aportó una forma distinta de analizar los problemas, lo que permitió encontrar soluciones más rápidas y creativas. Mientras uno podía enfocarse en la lógica, otro se centraba en la organización visual o en el comportamiento del jugador, logrando un resultado más completo de lo que habríamos producido individualmente.
Sin embargo, el principal desafío estuvo en la coordinación del trabajo, especialmente al dividir tareas y asegurarnos de que todos entendieran la misma visión del proyecto. En algunos momentos, las explicaciones se interpretaban de manera distinta o se avanzaba en direcciones paralelas. Lo resolvimos implementando pequeñas pausas de revisión y comunicación: antes de continuar o integrar algo nuevo, nos asegurábamos de alinear objetivos, aclarar dudas y confirmar que todos estábamos trabajando bajo la misma idea. Esto nos ayudó a mantener fluidez sin perder coherencia en el desarrollo.

### **2. El Alma de la Máquina: Más allá del código, ¿qué parámetro ([SerializeField]) descubrieron que tenía el mayor impacto en hacer que la IA se sintiera más "viva" o "inteligente"? 
**(Ejemplo: detectionRadius, chaseSpeed, la diferencia entre detectionRadius y loseSightRadius, etc.)** 

El parámetro que más impacto tuvo en hacer que la IA se sintiera realmente “viva” fue la diferencia entre detectionRadius y loseSightRadius. Jugar con estos dos valores permitió que el comportamiento del enemigo tuviera un toque más orgánico: ya no reaccionaba de manera inmediata y robótica, sino que “notaba” la presencia del jugador, tomaba decisiones y podía perder interés si lo perdía de vista. Esta pequeña variación entre cuándo la IA detecta al jugador y cuándo deja de perseguirlo añade un nivel de naturalidad y credibilidad, haciendo que su comportamiento parezca más parecido al de un ser consciente que evalúa su entorno, en lugar de un simple interruptor encendido/apagado.

En general el balance estuvo entre estos elementos:

- `detectionRadius`  
- `chaseSpeed`  
- `loseSightRadius`  
- `stunDuration`  

Estos valores hicieron que la IA se comportara de manera más natural.

---
