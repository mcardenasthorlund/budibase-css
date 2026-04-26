# <img src="https://res.cloudinary.com/daog6scxm/image/upload/v1695395225/Branding/Assets/Symbol/RGB/Keyline/Budibase_Symbol_RGB_Keyline_Positive_giy7pq.svg" width="30" height="30" alt="Budibase Logo"> budibase-css

Este repositorio contiene hojas de estilo (CSS) personalizadas para extender y modificar la apariencia visual de las aplicaciones desarrolladas en [Budibase](https://budibase.com).

## 🎯 Objetivo
El objetivo principal es permitir una personalización estética avanzada de los componentes de Budibase mediante la inyección de código CSS en el control "Embed".

## ⚠️ Aviso Importante
Este proyecto tiene un **carácter puramente lúdico** y está destinado exclusivamente a **proyectos personales**.

*   **Uso No Profesional:** No se recomienda su uso en entornos de producción o aplicaciones profesionales.
*   **Sin Testear:** El código no ha sido sometido a pruebas exhaustivas de compatibilidad o rendimiento. Su funcionamiento puede variar entre diferentes versiones de Budibase o navegadores.




---

# Guía de Uso: Budibase Custom CSS

Este documento detalla cómo utilizar las hojas de estilo personalizadas de este repositorio para transformar la apariencia de tus aplicaciones en Budibase.

## 🚀 Cómo aplicar los estilos

Para utilizar cualquiera de los archivos CSS de este repositorio en tu App de Budibase:

1.  Copia el contenido del archivo CSS deseado (ej. `estilo-jira.css`).
2.  En el **Builder** de Budibase, añade un componente **Embed** a tu pantalla (preferiblemente al final del árbol de componentes).
3.  Pega el código CSS dentro de etiquetas `<style></style>` en el editor del componente Embed:
    ```html
    <style>
      /* Pega aquí el contenido del archivo .css */
    </style>
    ```

## 🏷️ Convención de Nombres (`data-name`)

La mayoría de los estilos se aplican basándose en el nombre que asignes a los componentes en el panel derecho de Budibase. El CSS utiliza selectores de atributos como `div[data-name*="nombre"]`.

### Selectores de Estructura
| Nombre del Componente | Descripción |
| :--- | :--- |
| `ctCuerpo` | Contenedor principal de la página. Suele centrar el contenido y limitar el ancho máximo (ej. 1100px - 1200px). |
| `ctMenu` | Contenedor para el menú lateral o barra de navegación secundaria. |
| `ctContenido` | Contenedor principal de datos o formularios, situado normalmente junto al menú. |
| `ctPieGeneral` | Contenedor para crear un pie de página fijo (*sticky footer*). |

### Selectores de Utilidad
| Sufijo/Nombre | Efecto |
| :--- | :--- |
| `titulo` | Aplica el color corporativo del tema y estilo de encabezado. |
| `negrita` | Aplica `font-weight: bold` o semi-bold según el tema. |
| `xs` | Reduce el tamaño de la fuente (útil para subtítulos o notas). |
| `center` | Centra el texto y el contenido del componente. |
| `xl` | Aplicado a botones para que ocupen el 100% del ancho de su contenedor. |
| `menu` | Estiliza elementos de lista como opciones de navegación. |
| `selec` | Indica el estado activo o seleccionado de un elemento. |

## 📱 Soporte Móvil y Responsividad

Se han incluido clases específicas para gestionar el comportamiento en dispositivos móviles (pantallas < 768px):

*   **`icono-menu`**: Diseñado para iconos que solo deben destacar en móvil para abrir menús colapsables.
*   **`hidden`**: Oculta el componente en dispositivos móviles.
*   **`show`**: Muestra el componente únicamente en dispositivos móviles (útil para menús hamburguesa).
*   **`collapse`**: Cambia la dirección de contenedores flex de fila a columna en pantallas pequeñas.

## 🎨 Componentes de Spectrum UI

Las hojas de estilo modifican directamente los componentes nativos de Budibase (basados en Adobe Spectrum). Al aplicar el CSS, se verán afectados automáticamente:

*   **Botones (`.spectrum-Button`)**: Cambian radios de borde, sombras y efectos hover.
*   **Tarjetas (`.spectrum-Card`)**: Adaptan su elevación y bordes al estilo del tema (ej. estilo "Ticket" en Jira).
*   **Inputs (`.spectrum-Textfield-input`)**: Modifican el color de foco y grosor de borde.
*   **Navegación (`.nav-wrapper`)**: Personaliza la barra de navegación superior de la App.

## 🛠️ Personalización Avanzada

Cada archivo CSS define variables en el bloque `:root` para que puedas cambiar colores globales fácilmente:

```css
:root {
    --primary-color: #XXXXXX; /* Cambia este valor para ajustar el color principal */
}
```

---
*Nota: Asegúrate de que el nombre del componente en Budibase coincida exactamente o contenga la palabra clave definida en el CSS.*

