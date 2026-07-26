# Contenido

## 1. Introducción
    - Definición y características principales.
    - Historia y evolución (`SGML` -> `XML 1.0`).
    - Ventajas y casos de uso comunes (intercambio de datos, configuración, web services).

## 2. Estructura y sintaxis básica
    - Prolog (declaración `<?xml version="1.0" encoding="UTF-8"?>`).
    - Elementos y etiquetas: apertura, cierre y anidamiento correcto.
    - Atributos: sintaxis y uso adecuado.
    - Comentarios (`<!-- Comentario -->`).
    - Entidades predefinidas y escape de caracteres (por ejemplo: `&amp;`, `&lt;`, `&gt;`).

## 3. Validación y definiciones de tipo
    - DTD (Document Type Definition):
        - Declaración interna v/s externa.
        - Elementos, atributos y entidades en DTD.
    - XSD (XML Schema Definition):
        - Estructura básica de un esquema (elementos `xs:element`, tipos simples y complejos).
        - Restricciones de datos (tipos de datos primitivos, patrones y rangos).
        - Referencias e importación de esquemas.
    - Diferencias clave entre DTD y XSD.

## 4. Espacios de nombres (Namespaces)
    - Concepto y motivación (evitar colisiones de nombres).
    - Declaración de espacios de nombres (atributos `xmlns` y prefijos).
    - Uso de múltiples espacios de nombres en un solo documento.
    - Ejemplos prácticos de combinación de elementos de distintos esquemas.

## 5. Consulta y transformación de XML
    - XPath:
        - Sintaxis básica (ejes, nodos y predicados).
        - Selección de nodos (por etiqueta, atributo, posición).
        - Funciones comunes (`string()`, `number()`, `boolean()`).
    - XSLT (eXtensible Stylesheet Language Transformations):
        - Estructura de una hoja de estilo XSLT (`<xsl:template>`, `<xsl:value-of>`, `<xsl:for-each>`).
        - Plantillas, coincidencia de patrones y prioridad.
        - Ejemplo práctico: convertir XML a HTML.

## 6. Procesamiento y herramientas
    - Análisis de XML en diferentes lenguajes (p. ej., Java con `JAXP`, Python con `ElementTree`).
    - Validación automática usando herramientas (o línea de comandos: `xmllint`, editores con soporte integrado).
    - Editores recomendados (VS Code, Oxygen XML Editor, Notepad++).
    - Buenas prácticas de indentación y estilos de documento.
    - Integración en flujos de automatización (por ejemplo, validación previa a despliegues).