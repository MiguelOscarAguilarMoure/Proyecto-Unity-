# Tactical Breach: Operación Sombras - Documento de Diseño (GDD)

## 1. Ficha del juego

| Campo | Detalle |
|---|---|
| **Título** | Tactical Breach: Undercover-ops |
| **Autor/a** | Miguel Aguilar Moure |
| **Género** | Tactical Top-Down Shooter  |
| **2D / 3D** | 2D (Vista Cenital / Top-Down) |
| **Plataformas** | Windows |
| **Versión de Unity y pipeline** | Unity 6 - URP (Universal Render Pipeline 2D) |
| **Público objetivo y PEGI** | PEGI 16 (Acción y estrategia táctica en vista superior) |
| **Duración de una partida** | 2 - 4 minutos por nivel |
| **Repositorio** | [Enlace a tu GitHub / GitLab] |
| **Página de itch.io** | [Pendiente de creación] |

---

## 2. Concepto

### Resumen
*Tactical Breach* es un juego de disparos táctico en perspectiva cenital 2D en el que el jugador asume el rol de un operador spec-ops que debe infiltrarse y despejar recintos cerrados . Combinando control directo en tiempo real con una mecánica de **Pausa Táctica** y un **sistema dinámico de visión (Niebla de Guerra)**, el jugador analiza las salas, ejecuta brecheos de puertas y neutraliza amenazas en escenarios de espacio reducido (CQB).

### Pilares de diseño
* **Pausa Táctica y Planificación Rápida:** La información y la paciencia prevalecen sobre los reflejos. Congelar el tiempo permite evaluar el entorno antes de irrumpir en una habitación.
* **Interacción y Brecheo de Puertas:** Las puertas actúan como puntos de decisión crítica (abrir en silencio, disparar a través de ellas o patearlas para aturdir).
* **Visión Dinámica y Penumbra:** Iluminación 2D que oculta lo que hay detrás de muros y puertas cerradas, generando tensión y necesidad de cubrir cada ángulo.

### Referencias
* **Door Kickers:** Estética top-down, temática táctica SWAT y planificación en la irrupción de habitaciones.
* **Hotline Miami:** Agilidad en los controles y reinicio instantáneo tras morir.
* **Ready or Not:** Atmósfera de tensión en recintos cerrados y uso de linternas/iluminación en penumbra.

### Qué lo hace diferente
Simplifica la complejidad del control de escuadrones de los *tactical shooters* tradicionales enfocándose en un único operador (*Lone Wolf*). Combina el ritmo directo de un shooter cenital con pausa táctica e iluminación realista 2D mediante las luces nativas de Unity.

---

## 3. Historia y ambientación
Una célula hostil ha tomado un complejo de oficinas y almacenes. Como miembro del equipo de respuesta táctica rápida, tu misión es infiltrarte en solitario en las instalaciones y despejar de forma metódica cada estancia piso por piso.

---

## 4. Mecánicas

| Mecánica | Descripción | Control | Nivel en el que aparece |
|----------|-------------|---------|-------------------------|
| **Movimiento 8-Dir** | Desplazamiento libre del operador por el escenario con físicas 2D | W, A, S, D | Nivel 1 |
| **Apuntado Cenital** | Rotación constante del personaje hacia la posición del cursor del ratón | Mover Ratón | Nivel 1 |
| **Disparo (Raycast)** | Disparo inmediato mediante *Raycast2D* que calcula colisiones con enemigos y paredes | Clic Izquierdo | Nivel 1 |
| **Abrir / Cerrar Puerta** | Interacción silenciosa para abrir o cerrar puertas en la zona de paso | Tecla E | Nivel 1 |
| **Patear Puerta (Breach)** | Derriba la puerta de un golpe e impacta/aturde a los enemigos cercanos durante 2s | Tecla F / Espacio + E | Nivel 1 |
| **Pausa Táctica** | Congela el tiempo (`Time.timeScale = 0`) para inspeccionar la sala y planificar la entrada | Barra Espaciadora | Nivel 1 |
| **Recarga** | Recarga la munición del arma equipada desde la reserva | Tecla R | Nivel 1 |
