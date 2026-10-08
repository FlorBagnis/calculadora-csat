# 📊 Calculadora de Métricas CSAT

<img width="786" height="839" alt="image" src="https://github.com/user-attachments/assets/9f5391c2-da40-4d63-b48b-d63401aab941" />

Aplicación web desarrollada como proyecto personal para que los equipos de **Customer Support** puedan entender, seguir y mejorar su métrica de satisfacción del cliente (**CSAT**).

La idea surgió a partir de mi experiencia como **Support Guru en Tiendanube**, donde el CSAT era una de las métricas con las que se medía el desempeño. Primero armé una calculadora en **Excel** para controlar mi propio porcentaje y saber cuántas valoraciones positivas necesitaba para llegar al objetivo. La compartí con mis compañeros para que pudieran entender las métricas, y decidí llevarla a **HTML** para que cualquier persona de soporte pueda usarla desde el navegador, sin descargar archivos ni depender de Excel.

> ⚙️ **Propósito:** Convertir las valoraciones de los clientes en un objetivo accionable: saber en cualquier momento cuál es mi CSAT actual y cuántas valoraciones positivas me faltan para alcanzar la meta (94%, 96%, 100%, la que me pidan).

---

<p align="center">
  <a href="https://florbagnis.github.io/calculadora-csat/">
    <img src="https://img.shields.io/badge/Ver_Demo-Abrir_Herramienta-ff69b4?style=for-the-badge&logo=github&logoColor=white" alt="Ver Demo" />
  </a>
</p>

---

## 🔄 Del Excel a la web

| | Excel (original) | Versión web |
|---|---|---|
| **Cómo se usa** | Se descarga y se abre en Excel | Se abre desde un link, en cualquier dispositivo |
| **Objetivo de CSAT** | Celda editable | Campo editable + botones de objetivos frecuentes |
| **Para compartir** | Hay que enviar el archivo | Alcanza con pasar el link |
| **Seguimiento** | Se conserva manualmente en el archivo | Permite exportar los resultados en PDF |
| **Presentación** | Depende del formato de Excel | Reporte PDF adaptado al modo claro u oscuro |

> 💡 **Por qué la migré:** el Excel me servía a mí y a mi equipo cercano, pero un archivo es difícil de compartir y de mantener. En formato web, cualquier persona de soporte puede usarla al instante para superarse en sus métricas y conservar un registro de sus resultados.

📥 También dejé disponible la versión original en Excel: [`Calculadora_de_Metricas_corregida.xlsx`](./Calculadora_de_Metricas_corregida.xlsx)

---

## 🚀 Demo

🔗 https://florbagnis.github.io/calculadora-csat/

---

## 📂 Repositorio

🔗 https://github.com/FlorBagnis/calculadora-csat

---

## 🧮 ¿Cómo se calcula?

Se ingresan las valoraciones **negativas** y **positivas** y el **objetivo** de CSAT:

* **Total** = negativas + positivas
* **% actual** = positivas ÷ total
* **Positivas necesarias** = negativas × objetivo ÷ (1 − objetivo), redondeado hacia arriba
* **Positivas extra que faltan** = positivas necesarias − positivas actuales (mínimo 0)

**Ejemplos** (con objetivo del 94%):

| Negativas | Positivas | % actual | Positivas que faltan |
|:---:|:---:|:---:|:---:|
| 1 | 25 | 96,15% | 0 |
| 1 | 10 | 90,91% | 6 |
| 3 | 40 | 93,02% | 7 |

> ℹ️ Con un objetivo del **100%** no puede haber valoraciones negativas: si ya hay al menos una, la herramienta lo indica en lugar de mostrar un número engañoso.

---

## 📄 Exportación y seguimiento

La calculadora permite **exportar los resultados obtenidos en formato PDF**, facilitando el seguimiento de las métricas de Customer Experience y la conservación de un registro de cada cálculo.

El reporte permite llevar un control de los principales datos de la medición y **se adapta visualmente al modo claro u oscuro** utilizado en la herramienta, manteniendo una presentación consistente y legible.

Esta funcionalidad transforma la calculadora en algo más que una herramienta de cálculo: permite **consultar, alcanzar y registrar objetivos de CSAT**.

---

### 📚 Objetivos del proyecto

Durante este desarrollo se aplicaron y consolidaron conceptos como:

* **Lógica interactiva con JavaScript (ES6+):** manipulación dinámica del DOM, captura de eventos y cálculo en tiempo real.
* **Modelado de reglas de negocio:** traducción de una métrica de soporte (CSAT) a fórmulas que indican un objetivo concreto y alcanzable, incluyendo casos límite como objetivos con decimales o del 100%.
* **Migración de una herramienta de Excel a la web:** llevar la lógica de fórmulas (suma, porcentaje, redondeo y condicionales) a JavaScript manteniendo los mismos resultados.
* **Generación de reportes en PDF:** incorporación de una opción para exportar los resultados de la calculadora y conservar un registro de las métricas obtenidas.
* **Adaptación visual del reporte:** generación del PDF respetando el modo claro u oscuro utilizado en la herramienta.
* **HTML5 semántico:** estructuración accesible y limpia de formularios, inputs numéricos y etiquetas.
* **CSS3 moderno y diseño responsive:** maquetación adaptable mediante Grid, Flexbox y Media Queries, con soporte automático para modo claro y oscuro.
* **Validación de entradas de usuario:** prevención de errores en valores vacíos, negativos, decimales y objetivos fuera de rango.
* **UX/UI orientada a soporte:** interfaz simple y veloz, pensada para consultar la métrica en segundos durante la jornada.
* **Control de versiones y publicación:** gestión de commits en **Git/GitHub** con publicación en **GitHub Pages**.

---

## ✨ Funcionalidades

- Cálculo del **% de CSAT actual** en tiempo real.
- **Objetivo editable** de 1% a 100%, con decimales (por ejemplo 94,5%).
- Botones de **objetivos frecuentes**: 90%, 92%, 94%, 95%, 96%, 98% y 100%.
- Cálculo de las **positivas necesarias** y de cuántas **faltan sumar** para llegar a la meta.
- Mensaje claro según el resultado (objetivo alcanzado o cuántas valoraciones faltan).
- 📄 **Exportación de métricas en PDF** para guardar y llevar un registro de los resultados obtenidos.
- 🌓 El reporte PDF se adapta automáticamente al **modo claro u oscuro** seleccionado en la herramienta.
- Interfaz intuitiva, responsive y con **modo oscuro automático**.
- Sin instalación, sin registro y sin enviar datos a ningún servidor: todo se calcula en el navegador.

---

## 🛠️ Tecnologías utilizadas

- HTML5
- CSS3
- JavaScript (vanilla)
- Microsoft Excel (versión original)
- Git
- GitHub y GitHub Pages
- Visual Studio Code

---

## 🔗 Proyectos relacionados

* 💳 [Cuota Nube – Calculadora de Tasas](https://calculadora-tiendanube.vercel.app/): otra herramienta que desarrollé para equipos de soporte, validada con el equipo de Producto de Tiendanube. ([Ver código](https://github.com/FlorBagnis/calculadora-tiendanube))

---

¿Te sirvió? Dejale una ⭐ al repo.

---

## 📄 Licencia

Distribuido bajo licencia MIT. Ver el archivo `LICENSE`.

### 👩‍💻 Autora

**Florencia Bagnis**

* 💼 [LinkedIn](https://www.linkedin.com/in/florencia-bagnis)
* 💻 [Portfolio](https://florbagnis.github.io/Portfolio-FlorBagnis/)
* 💌 [florenciasoledadbagnis@gmail.com](mailto:florenciasoledadbagnis@gmail.com)

<br>

> 📊 Herramienta desarrollada para ayudar a equipos de Customer Support a entender y mejorar sus métricas de CSAT, combinando lógica frontend en JavaScript con mi experiencia en Customer Experience, Technical Support y seguimiento de indicadores de calidad.
