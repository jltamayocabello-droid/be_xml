# XML - Backend Developer

![Estado del Proyecto](https://img.shields.io/badge/Estado-Completado-green)
![XML Version](https://img.shields.io/badge/XML-1.0-FF6600?logo=xml&logoColor=white)
![DTD](https://img.shields.io/badge/DTD-Validaci%C3%B3n-blue)
![XSD](https://img.shields.io/badge/XSD-Esquemas-blue)
![Udemy Course](https://img.shields.io/badge/Curso-Backend%20Developer%20(Udemy)-ec1c24?logo=udemy&logoColor=white)

---

## 📖 Descripción del Proyecto
Este repositorio reúne el conjunto de prácticas y ejercicios desarrollados a lo largo de mi aprendizaje sobre el lenguaje de marcado XML (eXtensible Markup Language), su estructura jerárquica, validación sintáctica mediante DTD (Document Type Definition) y XSD (XML Schema Definition), el uso de espacios de nombres (Namespaces) para evitar colisiones de etiquetas, y la consulta y transformación de datos usando XPath y XSLT. Todo el contenido forma parte de mi especialización académica orientada al desarrollo backend:

1. **Curso de Backend Developer (Udemy):** Un recorrido integral por el diseño, estructuración y procesamiento de información en formato XML. Abarca desde la comprensión de las reglas del documento bien formado, la creación de reglas gramaticales con DTD y esquemas tipados rígidos con XSD, hasta el uso de selectores jerárquicos (XPath) y la generación de documentos HTML a partir de fuentes XML (XSLT).
2. **Prácticas en Formato XML (`be_xml`):** Conjunto de archivos XML de ejemplo, esquemas de validación (DTD, XSD) y plantillas XSLT listas para ser interpretadas y validadas.

---

## 🎯 Objetivo
Consolidar el dominio técnico en la estructuración, validación, transformación y consulta de documentos XML bajo estándares profesionales de desarrollo backend, logrando:

- Diseñar y estructurar archivos XML válidos y bien formados respetando la sintaxis de elementos, atributos, comentarios y entidades de escape.
- Implementar validaciones estructurales estrictas utilizando tanto declaraciones DTD internas y externas como esquemas tipados complejos en XSD.
- Resolver colisiones de etiquetas en documentos compuestos utilizando espacios de nombres (Namespaces) y prefijos organizados.
- Realizar consultas y búsquedas precisas de nodos empleando sintaxis XPath (ejes, predicados y funciones).
- Transformar datos estructurados XML a plantillas visuales HTML mediante la aplicación de hojas de estilo XSLT.

---

## 🛠️ Requerimientos Técnicos / Temas Cubiertos
Este proyecto cumple con los estándares exigidos para el aprendizaje integral del formato XML y su uso en el desarrollo backend:

### 1. Sintaxis & Estructura XML Básica
- ✅ **Definición de Documento XML:** Estructura básica con prólogo, comentarios, elementos padre/hijo y atributos tipados en [first.xml](./ARCHIVO/first.xml).
- ✅ **Escape de Caracteres y Entidades:** Demostración de entidades predefinidas (como `&gt;` y `&amp;`) para caracteres especiales en [first.xml](./ARCHIVO/first.xml).

### 2. Validación de Datos (DTD)
- ✅ **DTD Interno:** Declaración e inserción directa de reglas estructurales y entidades en el prólogo del documento XML, ejemplificado en [dtd.xml](./ARCHIVO/dtd.xml).
- ✅ **DTD Externo:** Referencia externa y modularización de la gramática XML, implementado en [biblio.xml](./ARCHIVO/biblio.xml) y definido en [biblioteca.dtd](./ARCHIVO/biblioteca.dtd).

### 3. Validación de Datos (XSD Schema)
- ✅ **Diseño de Esquemas XML Schema:** Creación de esquemas tipados que restringen los datos a tipos específicos (cadenas, enteros) y secuencias obligatorias, definido en [libro.xsd](./ARCHIVO/libro.xsd).
- ✅ **Validación contra XSD:** Vinculación de un esquema XSD a un archivo XML mediante `noNamespaceSchemaLocation`, ejemplificado en [book.xml](./ARCHIVO/book.xml).

### 4. Espacios de Nombres (Namespaces)
- ✅ **Evitar Conflictos de Nombres:** Declaración de espacios de nombres usando el atributo `xmlns` y prefijos para aislar elementos, implementado en [namespace.xml](./ARCHIVO/namespace.xml).
- ✅ **Combinación de Múltiples Esquemas:** Integración de etiquetas procedentes de múltiples espacios de nombres (`lib` y `pers`) en un único archivo XML, demostrado en [multiplenamespace.xml](./ARCHIVO/multiplenamespace.xml).

### 5. Consultas XPath & Transformación XSLT
- ✅ **Selección de Datos mediante XPath:** Documento estructurado con identificadores y nodos listos para la aplicación de consultas XPath jerárquicas, disponible en [xpath.xml](./ARCHIVO/xpath.xml).
- ✅ **Transformación de XML a HTML:** Diseño de una hoja de estilos de transformación que itera sobre registros y genera una tabla visual en HTML, implementada en [transformacion.xsd](./ARCHIVO/transformacion.xsd) (que actúa como plantilla XSLT).

---

## 📂 Estructura del Proyecto
```
be_xml/
│
├── ARCHIVO/
│   ├── biblioteca.dtd          # Declaración externa de DTD (reglas y entidades de biblioteca)
│   ├── biblio.xml              # XML de biblioteca validado externamente con biblioteca.dtd
│   ├── book.xml                # XML de libro validado externamente con libro.xsd
│   ├── dtd.xml                 # XML con declaración y validación interna de DTD
│   ├── first.xml               # Ejemplo de sintaxis básica: prolog, atributos y entidades de escape
│   ├── libro.xsd               # Esquema de validación XSD que restringe elementos de libro
│   ├── multiplenamespace.xml   # Ejemplo de XML combinando múltiples prefijos y Namespaces
│   ├── namespace.xml           # Ejemplo de XML con declaración de Namespace único con prefijo
│   ├── transformacion.xsd      # Hoja de estilo XSLT para transformar la biblioteca XML a una tabla HTML
│   └── xpath.xml               # Documento XML de prueba para consultas jerárquicas XPath
│
├── Temario.md                  # Plan de estudios/syllabus de XML
└── README.md                   # Documentación del repositorio
```

---

## 🚀 Instrucciones de Ejecución y Validación
Para trabajar con los archivos XML y realizar las validaciones correspondientes, se recomienda utilizar herramientas de línea de comandos como **libxml2** (`xmllint`) o extensiones especializadas en tu editor de código.

### 1. Clonar el repositorio
```bash
git clone https://github.com/jltamayocabello-droid/be_xml.git
cd be_xml
```

### 2. Validar Documentos XML por Consola (`xmllint`)
Si tienes instalado `xmllint` (parte del paquete `libxml2`), puedes ejecutar las siguientes comprobaciones:

- **Verificar que un XML está bien formado:**
  ```bash
  xmllint ARCHIVO/first.xml --noout
  ```
- **Validar XML contra su DTD interna:**
  ```bash
  xmllint ARCHIVO/dtd.xml --valid --noout
  ```
- **Validar XML contra su DTD externa:**
  ```bash
  xmllint ARCHIVO/biblio.xml --valid --noout
  ```
- **Validar XML contra su esquema XSD:**
  ```bash
  xmllint --schema ARCHIVO/libro.xsd ARCHIVO/book.xml --noout
  ```

### 3. Visualizar Transformación XSLT en Navegador
El archivo `xpath.xml` incluye la siguiente instrucción de vinculación:
```xml
<?xml-stylesheet type="text/xsl" href="transformacion.xsd"?>
```
Para ver la transformación a HTML:
1. Asegúrate de servir los archivos a través de un servidor local (por ejemplo, la extensión *Live Server* en VS Code o ejecutando `python -m http.server` en la raíz). Esto es necesario debido a las restricciones de seguridad (CORS) de los navegadores modernos.
2. Abre `http://localhost:8000/ARCHIVO/xpath.xml` en tu navegador.
3. Verás los datos del XML presentados en una tabla HTML estructurada.

---

## 📱 Áreas Técnicas Destacadas
| Área Técnica | Conceptos Clave | Descripción |
| :--- | :--- | :--- |
| 📄 **Formato XML** | Estructura jerárquica, Prólogo, Atributos | Metalenguaje extensible que proporciona un formato estandarizado para almacenar e intercambiar datos legibles. |
| 🛡️ **Validación DTD** | Gramática, Elementos, Entidades | Define las reglas de marcado permitidas para los elementos, atributos y entidades del documento. |
| ⚙️ **Esquemas XSD** | xs:schema, Tipos complejos, Tipado rígido | Mecanismo de validación más potente que permite definir tipos de datos, patrones de texto, rangos numéricos y obligatoriedad. |
| 🏷️ **Namespaces** | xmlns, Prefijos únicos | Evita colisiones de nombres al combinar elementos de diferentes vocabularios en un solo documento XML. |
| 🔍 **XPath** | Ejes, Predicados, Selectores jerárquicos | Lenguaje de navegación que permite seleccionar y filtrar elementos y atributos específicos de un árbol XML. |
| 🔄 **XSLT** | Hojas de estilo, xsl:template, Plantillas | Lenguaje de transformación declarativo que procesa documentos XML y los convierte a HTML, texto u otros formatos XML. |

---

## ✒️ Autor
**Jorge Tamayo Cabello**  
*Desarrollador Front-End*

---

## 📄 Licencia
Este repositorio es de carácter estrictamente académico y educativo. Todo el contenido es libre de ser consultado con fines de aprendizaje y referencia técnica.

---

## 🙏 Agradecimientos
- A **Udemy** por la excelente formación en desarrollo de backend mediante el curso de Backend Developer.
- A la **comunidad de desarrollo de software libre** por mantener y estandarizar las especificaciones del ecosistema XML (W3C).