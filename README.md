# 🖥️ Configuración de Hyprland + Quickshell

Este repositorio contiene mi configuración personal para el gestor de ventanas **Hyprland**, diseñada para ser rápida, visualmente atractiva y fácil de usar. Toda la interfaz gráfica y los widgets están impulsados por **Quickshell**.

## ⚙️ Características Generales

* **Apariencia:** Bordes de tamaño 2, esquinas redondeadas (radio 4) y un efecto de desenfoque visual (blur) para las ventanas.
* **Fuente:** JetBrains Mono.
* **Animaciones:** Transiciones suaves y personalizadas usando curvas `myBezier` para ventanas y espacios de trabajo.
* **Teclado y Ratón:** Distribución de teclado en inglés (US) y desplazamiento natural activado para el panel táctil.

---

## 🖥️ Monitores y Gráficos

La configuración está preparada para múltiples pantallas y tarjetas gráficas NVIDIA:
* **Pantalla Principal (Laptop):** Resolución de 1920x1080 a 144Hz.
* **Pantalla Secundaria (HDMI):** Resolución de 1920x1080 a 75Hz.
* **Entorno NVIDIA:** Se incluyen variables de entorno (`__NV_PRIME_RENDER_OFFLOAD`, `LIBVA_DRIVER_NAME`, `__GLX_VENDOR_LIBRARY_NAME`) para asegurar el correcto funcionamiento del rendimiento por hardware y los gráficos.

---

## 🚀 Servicios de Inicio (Autostart)

Al iniciar el sistema, se ejecutan automáticamente los siguientes servicios:
* **Quickshell:** Carga la barra superior, el menú flotante, la interfaz principal y el modo de concentración (Focus Time).
* **SwayOSD:** Servidor para mostrar los indicadores visuales en pantalla para el volumen y el brillo.
* **Cliphist:** Gestor del historial del portapapeles, guardando tanto texto como imágenes copiadas.
* **Componentes base:** Gestor de energía (`hypridle`), controles multimedia (`playerctld`) y agentes de autenticación (`hyprpolkitagent`).

---

## ⌨️ Atajos de Teclado Principales

La tecla principal del sistema (Modificador) es **SUPER** (la tecla de Windows).

### 🛠️ Sistema y Aplicaciones
| Atajo | Acción |
| :--- | :--- |
| `SUPER + T` | Abrir Terminal (Kitty) |
| `SUPER + C` | Cerrar la aplicación actual |
| `SUPER + E` | Abrir el administrador de archivos (Nautilus) |
| `SUPER + F` | Abrir el navegador web (Google Chrome) |
| `ALT + P` | Abrir terminal visual (Edex-ui) |
| `SUPER + L` | Bloquear la pantalla |
| `SUPER + Esc` | Tomar una captura de pantalla |
| `SUPER + Espacio` | Poner la ventana en modo flotante |

### 🎨 Widgets de Quickshell
| Atajo | Widget |
| :--- | :--- |
| `SUPER + D` | Lanzador de aplicaciones |
| `SUPER + V` | Menú de volumen |
| `SUPER + N` | Menú de red e internet |
| `SUPER + B` | Estado de la batería |
| `SUPER + O` | Cambiar el fondo de pantalla |
| `SUPER + S` | Calendario |

### 🔊 Volumen y Brillo
| Atajo | Acción |
| :--- | :--- |
| `Teclas de Volumen` | Subir/Bajar/Silenciar audio (con indicador visual SwayOSD) |
| `SUPER + Teclas de Volumen` | Ajustar el brillo de la pantalla en bloques de 10% |

### 🖱️ Atajos del Ratón
| Acción | Resultado |
| :--- | :--- |
| `SUPER + Clic Izquierdo` | Mover la ventana de lugar |
| `SUPER + Clic Derecho` | Cambiar el tamaño de la ventana |
| `Botón lateral (276)` | Abrir Visual Studio Code |
| `Botón lateral (275)` | Abrir Spotify |

---

## 🪟 Reglas de Ventanas y Capas

Para mantener el orden visual, el entorno tiene reglas específicas para ciertas herramientas:
* **Lanzador de aplicaciones:** Se abre siempre flotando en el centro de la pantalla, con un tamaño exacto de 1200x600.
* **Quickshell:** Los contenedores principales no tienen sombras ni toman el foco inicial, para integrarse de forma natural con el fondo.
* **Indicadores rápidos:** Las barras de volumen, brillo y el selector de color se muestran de inmediato sin animaciones para no causar retrasos visuales.
* **Bloqueo de sesión:** La pantalla de bloqueo tiene un efecto de desenfoque aplicado al fondo.
