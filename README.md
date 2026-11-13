# MISTO · tu mes, listo

Prototipo móvil de una experiencia de cierre de ciclo mensual para una app bancaria. Ayuda a una persona joven a **decidir qué hacer con su saldo positivo** y a **aportar a su meta de primera vivienda**.

Proyecto del taller de Diseño de Interacción Digital (UDD), desarrollado a partir del desafío **Bci Labs: acceso a la primera vivienda**.

> **Prototipo de investigación.** Los datos son de ejemplo y no hay conexión con ningún banco. Es un trabajo académico, no un producto de Bci.

---

## Qué demuestra

El flujo recorre el cierre de un mes en tres pasos:

1. **Revisa tu ciclo:** resumen del mes que terminó y simulación del mes siguiente ("Simula tu mayo").
2. **Decide sobre tu saldo:** aportar a la vivienda, dejarlo en la cuenta o pagar la tarjeta de crédito.
3. **Confirma tu aporte:** el usuario ve cómo avanza su meta y cuántos meses se acorta el plazo.

El tono busca ser cercano y levemente emocional, sin exagerar, y educar en finanzas: se felicita el cierre con saldo positivo y se explica por qué cada decisión importa.

## Cómo probarlo

El prototipo es un único archivo, `index.html`, sin dependencias ni instalación.

- **En el computador:** abre `index.html` en el navegador. Se muestra dentro de un marco de teléfono.
- **En el celular:** abre la página publicada con GitHub Pages (ver más abajo). Se ve a pantalla completa.

Guion sugerido para una sesión de prueba:

1. En **Inicio**, define tus tres motivos.
2. Entra a **Mi mes** y revisa el ciclo; prueba "Simula tu mayo" en la pestaña "Por semana".
3. Elige qué hacer con tu saldo positivo y confirma el aporte.
4. Si te equivocas, usa **Cambiar mi decisión**. En **Perfil** puedes reiniciar el prototipo.

## Publicarlo con GitHub Pages

1. Sube `index.html` a la raíz del repositorio.
2. En **Settings → Pages**, elige la rama `main` y la carpeta `/ (root)`.
3. Espera 1 o 2 minutos y abre la dirección que GitHub muestra.

Si actualizas el archivo y no ves los cambios, recarga con fuerza o usa una pestaña privada: el navegador guarda copias en caché.

## Decisiones de diseño

- **Look and feel Bci:** paleta y botones según la guía de color (verde para acción principal y meta, azul para información, gris para texto y pasado, amarillo solo como detalle).
- **Menos color y menos ruido:** tarjetas blancas sin borde y con sombra suave; solo las barras de progreso conservan contorno. La barra se rellena de verde y su contenedor es transparente con borde.
- **Menos cifras en pantalla:** los gráficos resumen la información y muestran solo el valor esperado; el detalle está en "Ver detalle".
- **Lenguaje:** se usa "saldo positivo" en lugar de "sobra" y "esperado" en lugar de "previsto".
- **Accesibilidad:** textos con contraste mínimo de 4,5:1, botones de al menos 44 px en las acciones principales, avisos para lectores de pantalla y soporte de teclado en el menú modal.

## Cómo se guardan los datos

El prototipo guarda su estado solo en el navegador (`localStorage`, clave `misto-proto-v1`): motivos, decisión, aporte y un registro de uso con las pantallas vistas y los toques. Nada se envía a ningún servidor. En **Perfil → Copiar registro de uso** se puede copiar ese registro para revisar el recorrido de cada persona.

## Evaluación de usabilidad

El prototipo se evalúa con:

- **Prueba con usuarios:** 1 ronda, 5 personas, 3 o 4 tareas. Se miden efectividad, eficiencia y satisfacción, con SEQ por tarea y SUS al final.
- **Revisión heurística interna:** las 10 heurísticas de Nielsen (principios de la ISO 9241-110).
- **Revisión rápida de accesibilidad:** WCAG 2.2 nivel AA (contraste, tamaño de texto y botones, navegación).

## Estructura

```
index.html   Prototipo completo (HTML, CSS y JavaScript en un solo archivo)
README.md    Este documento
```

## Tecnología

HTML, CSS y JavaScript sin librerías. Navegación por rutas con hash (`#/inicio`, `#/mimes`, `#/ciclo`, `#/decide`, `#/aporte`, `#/confirmado`, `#/productos`, `#/perfil`).

## Autoría

Margarita, estudiante de Diseño de Interacción Digital, Universidad del Desarrollo.

## Aviso

Marca, colores y referencias visuales de Bci se usan solo con fines académicos. Este proyecto no está afiliado ni respaldado por Bci.
