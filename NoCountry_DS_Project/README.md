# CORAZONADA - Soluciones basadas en Datos

¡Bienvenido al proyecto **C23-114-Data**! Este es nuestro MVP (Producto Mínimo Viable) para mejorar la gestión hospitalaria a través del análisis de datos.

## 🚀 Instalación y Configuración

Para ejecutar este proyecto localmente, sigue estos pasos:

1. Clona este repositorio:
   ```bash
   git clone https://github.com/No-Country-simulation/c23-14-data.git




---
# 📂 Estructura del respositorio
---

```bash
c23-14-data/
├── data/                  # Conjunto de datos
├── src/                   # Jupyter notebooks con análisis exploratorio, modelado y interfaces
├── Presentación/          # Modelo de negocio, tareas del equipo y presentación de venta
├── Models/                # Modelos entrenados y sus pesos
├── requirements.txt       # Dependencias del proyecto
├── README.md              # Documentación del repositorio
```
# 📝 Descripción y Objetivo del Proyecto
## Situación Inicial
Los hospitales y centros de salud  enfrentan dificultades para gestionar el flujo de pacientes, especialmente en áreas críticas como la cardiología. La falta de previsión en el proceso de altas puede ocasionar:

- Sobrecarga en los recursos hospitalarios.
- Prolongación innecesaria de la hospitalización.
- Decisiones poco informadas que afectan la eficiencia y calidad del servicio.
  
Esto resulta en costos adicionales, planificación deficiente de altas y uso ineficiente de los recursos. Además, la alta subjetividad en el proceso de altas puede derivar en altas prematuras o inapropiadas, lo que aumenta el riesgo de reingresos hospitalarios, complicaciones posteriores e incluso fallecimientos.

Estos reingresos innecesarios no solo afectan la salud de los pacientes, sino que también contribuyen a la sobrecarga del sistema de salud.

## Objetivo General
El proyecto busca desarrollar un sistema básico que ofrezca una predicción preliminar de las altas de pacientes, utilizando un modelo de inteligencia artificial entrenado con datos históricos de pacientes cardiológicos. El objetivo es mejorar la gestión hospitalaria, optimizar los recursos y reducir los reingresos innecesarios

---


# ETAPAS 

## Datos
Los datos fueron recolectados de pacientes admitidos en el **Hero DMC Heart Institute**, Ludhiana, Punjab, India, entre el **1 de abril de 2017** y el **31 de marzo de 2019**. El conjunto de datos incluye:

- **14,845** ingresos de **12,238** pacientes
- **1,921** pacientes con múltiples ingresos

**Enlace del conjunto de datos**: [Hospital Admissions Data](https://www.kaggle.com/datasets/ashishsahani/hospital-admissions-data?select=table_headings.csv)

## Diccionario de Datos

| **Campo**                            | **Descripción**                                   |
|--------------------------------------|---------------------------------------------------|
| **SNO**                              | Número de serie del paciente                       |
| **MRD No.**                          | Número de admisión del paciente                    |
| **D.O.A**                            | Fecha de admisión                                 |
| **D.O.D**                            | Fecha de alta                                    |
| **AGE**                              | Edad del paciente                                 |
| **GENDER**                           | Género del paciente                               |
| **RURAL**                            | Indicador de localidad (Rural (R) / Urbano (U))   |
| **TYPE OF ADMISSION**                | Tipo de admisión (Emergencia / OPD)               |
| **month year**                       | Mes y año de la admisión                          |
| **DURATION OF STAY**                 | Duración de la estadía                            |
| **duration of intensive unit stay**  | Duración de la estadía en la unidad intensiva     |
| **OUTCOME**                          | Resultado del tratamiento (Ej. Recuperado)        |
| **SMOKING**                          | Indicador de si el paciente fuma (Sí/No)          |
| **ALCOHOL**                          | Indicador de si el paciente consume alcohol (Sí/No)|
| **DM**                               | Diabetes Mellitus (Sí/No)                         |
| **HTN**                              | Hipertensión (Sí/No)                              |
| **CAD**                              | Enfermedad Arterial Coronaria (Sí/No)             |
| **PRIOR CMP**                        | Miocardiopatía previa (Sí/No)                     |
| **CKD**                              | Enfermedad Renal Crónica (Sí/No)                  |
| **HB**                               | Niveles de Hemoglobina                            |
| **TLC**                              | Conteo total de leucocitos                        |
| **PLATELETS**                        | Conteo de plaquetas                               |
| **GLUCOSE**                          | Niveles de glucosa                                |
| **UREA**                              | Niveles de urea                                  |
| **CREATININE**                       | Niveles de creatinina                             |
| **BNP**                               | Péptido natriurético tipo B                       |
| **RAISED CARDIAC ENZYMES**           | Enzimas cardíacas elevadas                        |
| **EF**                               | Fracción de eyección (Ejection Fraction)          |
| **SEVERE ANAEMIA**                   | Indicador de anemia severa (Sí/No)                |
| **ANAEMIA**                          | Indicador de anemia (Sí/No)                       |
| **STABLE ANGINA**                    | Angina estable (Sí/No)                            |
| **ACS**                              | Síndrome coronario agudo (Sí/No)                  |
| **STEMI**                            | Infarto de miocardio con elevación del ST (Sí/No) |
| **ATYPICAL CHEST PAIN**              | Dolor torácico atípico (Sí/No)                    |
| **HEART FAILURE**                    | Insuficiencia cardíaca (Sí/No)                    |
| **HFREF**                            | Insuficiencia cardíaca con fracción de eyección reducida |
| **HFNEF**                            | Insuficiencia cardíaca con fracción de eyección normal |
| **VALVULAR**                         | Enfermedad valvular (Sí/No)                       |
| **CHB**                              | Bloqueo cardíaco completo (Sí/No)                 |
| **SSS**                              | Síndrome de seno enfermo (Sí/No)                  |
| **AKI**                              | Lesión renal aguda (Sí/No)                        |
| **CVA INFRACT**                      | Infarto cerebrovascular (Sí/No)                   |
| **CVA BLEED**                        | Sangrado cerebrovascular (Sí/No)                  |
| **AF**                               | Fibrilación auricular (Sí/No)                     |
| **VT**                               | Taquicardia ventricular (Sí/No)                   |
| **PSVT**                             | Taquicardia supraventricular paroxística (Sí/No)  |
| **CONGENITAL**                       | Enfermedad cardíaca congénita (Sí/No)             |
| **UTI**                              | Infección del tracto urinario (Sí/No)             |
| **NEURO CARDIOGENIC SYNCOPE**        | Síncope neurocardiogénico (Sí/No)                 |
| **ORTHOSTATIC**                      | Hipotensión ortostática (Sí/No)                   |
| **INFECTIVE ENDOCARDITIS**           | Endocarditis infecciosa (Sí/No)                   |
| **DVT**                              | Trombosis venosa profunda (Sí/No)                 |
| **CARDIOGENIC SHOCK**                | Shock cardiogénico (Sí/No)                        |
| **SHOCK**                            | Shock (Sí/No)                                     |
| **PULMONARY EMBOLISM**               | Embolia pulmonar (Sí/No)                          |
| **CHEST INFECTION**                  | Infección torácica (Sí/No)                        |

---
## Análisis y hallazgos clave

---

## 🌐 MODELO E INTERFACES

El modelo de predicción fue entrenado utilizando **Random Forest**, un algoritmo de aprendizaje automático que se adapta muy bien a problemas de clasificación. Este modelo fue seleccionado por ofrecer las mejores métricas en términos de precisión y rendimiento para el conjunto de datos disponible.

Para la interfaz de usuario, utilizamos **Streamlit**, una herramienta que facilita la creación de aplicaciones interactivas de datos de manera rápida y eficiente. Posteriormente, la aplicación fue desplegada en **Render**, lo que permitió que estuviera disponible en línea.

Puedes acceder al modelo y las interfaces a través de la siguiente plataforma:

[Acceder al Modelo y las Interfaces](https://c23-14-data-hospitalia.onrender.com)


# 📚 Recursos
- **Modelo de negocio**: [Presentación de ventas](./Presentación)
- **Análisis exploratorio de datos**: Jupyter Notebooks en la carpeta `src/`
- **Modelos entrenados**: Encuentra los modelos en la carpeta `Models/`




# 🛠 **Stack de Tecnologías y Herramientas**

(Tecnologías y herramientas a utilizar en el proyecto)

---

<table>
  <tr>
    <th>Librería/Herramienta</th>
    <th>Logo</th>
    <th>Descripción</th>
  </tr>
  <tr>
    <td><strong>Pandas</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/e/ed/Pandas_logo.svg" width="40"></td>
    <td>Librería de Python para manipulación y análisis de datos.</td>
  </tr>
  <tr>
    <td><strong>Matplotlib</strong></td>
    <td align="center"><img src="https://matplotlib.org/stable/_static/logo2_compressed.svg" width="40"></td>
    <td>Librería usada para la generación de gráficos en dos dimensiones.</td>
  </tr>
  <tr>
    <td><strong>Seaborn</strong></td>
    <td align="center"><img src="https://seaborn.pydata.org/_images/logo-tall-lightbg.svg" width="40"></td>
    <td>Librería de Python creada sobre Matplotlib, usada para crear gráficos estadísticos.</td>
  </tr>
  <tr>
    <td><strong>Jupyter</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" width="40"></td>
    <td>Software gratuito, estándares abiertos y servicios web para informática interactiva en todos los lenguajes de programación.</td>
  </tr>
  <tr>
    <td><strong>Visual Studio Code</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/9/9a/Visual_Studio_Code_1.35_icon.svg" width="40"></td>
    <td>Editor de código fuente.</td>
  </tr>
  <tr>
    <td><strong>Colaboratory con Python</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/d/d0/Google_Colaboratory_SVG_Logo.svg" width="40"></td>
    <td>Plataforma de Google basada en Jupyter Notebooks, junto con las librerías de Python para análisis de datos como Pandas y Matplotlib.</td>
  </tr>
  <tr>
    <td><strong>Power BI</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/c/cf/New_Power_BI_Logo.svg" width="40"></td>
    <td>Herramienta líder en el mercado para crear visualizaciones de datos avanzadas, informes interactivos y paneles de control.</td>
  </tr>
  <tr>
    <td><strong>Canva</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/e/ec/Canva_Logo.svg" width="40"></td>
    <td>Plataforma de diseño gráfico y composición de imágenes.</td>
  </tr>
  <tr>
    <td><strong>PowerPoint</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/1/19/Microsoft_PowerPoint_2013-2019_logo.svg" width="40"></td>
    <td>Microsoft PowerPoint (PPT) es un software de ofimática diseñado para realizar presentación de diapositivas.</td>
  </tr>
  <tr>
    <td><strong>Python</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/c/c3/Python-logo-notext.svg" width="40"></td>
    <td>Lenguaje de programación utilizado para análisis de datos y desarrollo de aplicaciones.</td>
  </tr>
  <tr>
    <td><strong>GitHub</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/9/91/Octicons-mark-github.svg" width="40"></td>
    <td>Plataforma de desarrollo colaborativo para proyectos de software.</td>
  </tr>
  <tr>
    <td><strong>Miro</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/41/Miro_logo.svg/2560px-Miro_logo.svg.png" width="40"></td>
    <td>Para la planificación de los sprints.</td>
  </tr>
  <tr>
    <td><strong>Google Drive</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/d/da/Google_Drive_logo.png" width="40"></td>
    <td>Servicio de alojamiento y sincronización de archivos.</td>
  </tr>
  <tr>
    <td><strong>Google Meet</strong></td>
    <td align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/5/5c/Google_Meet_icon_%282020%29.svg" width="40"></td>
    <td>Herramienta utilizada para las videollamadas y reuniones.</td>
  </tr>
  <tr>
    <td><strong>Streamlit</strong></td>
    <td align="center"><img src="https://streamlit.io/images/brand/streamlit-logo-primary-colormark-darktext.svg" width="40"></td>
    <td>Herramienta de código abierto diseñada para crear aplicaciones web interactivas y visualizaciones de datos de manera rápida y sencilla utilizando Python.</td>
  </tr>
</table>


---







## 👥 Equipo

<table>
  <tr>
    <td align="center">
      <img src="https://avatars.githubusercontent.com/u/123048093?s=400&u=50613e4d8debc804f14d21504c9db1ad60edf0c5&v=4" width="150" height="150" alt="Pablo Luberriaga"><br>
      <strong>Pablo Luberriaga</strong><br>
      <em>Data Analyst</em><br>
      <a href="https://www.linkedin.com/in/pabloluberriaga/" target="_blank">
        <img src="https://cdn.jsdelivr.net/npm/simple-icons@v9/icons/linkedin.svg" width="20">
      </a>
      <a href="https://github.com/pablolube" target="_blank">
        <img src="https://cdn.jsdelivr.net/npm/simple-icons@v9/icons/github.svg" width="20">
      </a>
    </td>
    <td align="center">
      <img src="https://avatars.githubusercontent.com/u/176251377?v=4" width="150" height="150" alt="Estefania Garrido"><br>
      <strong>Estefanía Garrido</strong><br>
      <em>Data Scientist</em><br>
      <a href="https://www.linkedin.com/in/estefan%C3%ADa-garridoz/" target="_blank">
        <img src="https://cdn.jsdelivr.net/npm/simple-icons@v9/icons/linkedin.svg" width="20">
      </a>
      <a href="https://github.com/Estefaniagz" target="_blank">
        <img src="https://cdn.jsdelivr.net/npm/simple-icons@v9/icons/github.svg" width="20">
      </a>
    </td>
    <td align="center">
      <img src="https://avatars.githubusercontent.com/u/145939303?v=4" width="150" height="150" alt="Saúl Cova"><br>
      <strong>Saúl Cova</strong><br>
      <em>Data Scientist</em><br>
      <a href="https://www.linkedin.com/in/sa%C3%BAl-cova-008830145" target="_blank">
        <img src="https://cdn.jsdelivr.net/npm/simple-icons@v9/icons/linkedin.svg" width="20">
      </a>
      <a href="https://github.com/saulcova3" target="_blank">
        <img src="https://cdn.jsdelivr.net/npm/simple-icons@v9/icons/github.svg" width="20">
      </a>
    </td>
  </tr>
</table>
