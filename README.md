Proyecto AR: Explorando el Interior de una PC

Este proyecto es una experiencia de Realidad Aumentada (RA) desarrollada para la consigna del ciclo básico de la carrera Técnico en Computación.

Experiencia en vivo: [ENLACE A TU GITHUB PAGES] (Ej: https://www.google.com/search?q=https://tu-usuario.github.io/tu-repo/index.html)

Integrantes:



1. Investigación Inicial

Justificación del Tema

Tema elegido: Arquitectura de Computadoras – “Explorando el interior de una PC en Realidad Aumentada”.

La arquitectura de computadoras es una base esencial de la carrera. Entender la interconexión física de los componentes (CPU, memoria, GPU) es crucial para comprender el funcionamiento y rendimiento de los sistemas. La RA ofrece una visualización inmersiva y dinámica que supera las limitaciones de diagramas planos, facilitando la comprensión de conceptos abstractos.

 Referencias Técnicas y Conceptuales

Frameworks de RA Web:

MindAR: [https://github.com/hiukim/mind-ar-js] - Framework liviano y de código abierto para WebAR, ideal para Image Tracking.

A-Frame: [https://aframe.io/] - Framework para construir escenas 3D/VR/AR usando una estructura declarativa basada en HTML.

Recursos 3D/Conceptuales:


2. Diseño de la Experiencia
 Objetivo Pedagógico

Identificación: El estudiante identificará y localizará los componentes principales de una PC.

Función: El estudiante comprenderá la función básica de la Placa Madre, CPU, RAM y GPU mediante interacción directa.

Conexión: El estudiante visualizará la interconexión y la disposición espacial de los elementos.

 Tipo de RA

RA basada en imagen (Image Tracking): Se utiliza un marcador visual de alto contraste.

Flujo de Usuario:

El usuario abre la aplicación (index.html) en su celular.

Escanea el marcador (marcador.html abierto en otra pantalla).

Aparece el modelo 3D esquemático de los componentes de la PC.

El usuario toca un componente (ej. CPU) para activar un texto emergente con su descripción.

 Elementos Visuales

Marcador: Se utiliza un marcador de prueba estable (que debe ser reemplazado por uno propio).

Modelos 3D: Cajas (<a-box>) con colores diferenciados para representar esquemáticamente la Placa Madre (verde), CPU (gris), RAM (azul) y GPU (negro).

3. Desarrollo Técnico

 Tecnología Seleccionada

La elección de MindAR + A-Frame fue por su enfoque en la WebAR y su ligereza, permitiendo que la experiencia se ejecute directamente en el navegador de cualquier dispositivo móvil sin necesidad de instalaciones adicionales.

 Implementación

La experiencia está contenida en index.html.

3D: Se definen los componentes como entidades de A-Frame con coordenadas relativas al centro del marcador.

Interacción: Se usa un componente JavaScript que escucha el evento click sobre cualquier objeto con la clase .clickable, actualizando un elemento <a-text> flotante con la información correspondiente.

 Dificultades y Soluciones

Dificultad #1: Errores de seguridad de la cámara y carga de assets al ejecutar el archivo HTML localmente (usando file://...).

Solución: Se forzó la ejecución a través de un servidor web (GitHub Pages) y se utilizaron URL de CDN estables para la carga de recursos de MindAR.

Dificultad #2: Falta de modelos 3D detallados (.glb).

Solución: Se implementó la solución con primitivas geométricas (<a-box>) para asegurar la funcionalidad y el concepto inicial.

4. Próximos Pasos y Mejoras (Plan de Ejecución)

[ ] Personalización del Marcador: Compilar una imagen propia del grupo para usar como marcador (reemplazar el archivo .mind y la URL de la imagen en ambos HTML).

[ ] Modelos Detallados: Reemplazar las cajas esquemáticas por modelos 3D reales de CPU, RAM y GPU.

[ ] Usabilidad: Mejorar el contraste y la tipografía de los textos emergentes.

[ ] Contenido Adicional: Añadir audio descriptivo o animaciones simples (Ej. la CPU "procesando").
