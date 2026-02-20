# Informe Técnico del Taller

## Nombre del Taller
_Taller1 - Modelado BPMN del proceso de Recolección y Consolidación de Información Académica para encuesta Autoevaluación Institucional y por Programas._

## Integrantes del equipo
| Nombre | Correo Electrónico |
|---|---|
| Valentina Alejandra López Romero | valentinalopro@unisabana.edu.co |
| Mariana Valle Moreno | marianavamo@unisabana.edu.co |
| Laura Camila Rodriguez Leon | laurarodleo@unisabana.edu.co |

## Descripción general del trabajo

El objetivo del taller fue seleccionar un proceso real del cliente asignado y modelarlo utilizando la notación BPMN, representando fielmente su funcionamiento actual (modelo AS-IS).

El proceso escogido corresponde a la **Recolección y Consolidación de Información Académica para la Encuesta de Autoevaluación Institucional y por Programas**, la cual es considerada una de las mediciones más importantes que realiza la universidad. Este instrumento constituye un insumo fundamental para dar respuesta a los lineamientos establecidos por el Consejo Nacional de Acreditación (CNA), ya que no solo permite identificar oportunidades de mejora, sino que también sirve como soporte estratégico para la toma de decisiones y el aseguramiento de la calidad institucional.

El alcance definido de este proceso comprende desde el envío de la citación al director de programa hasta la recepción, validación y consolidación de un archivo Excel con la información académica requerida para la planeación de la implementación de la encuesta, incluyendo listados de materias, salones, horarios y profesores disponibles por semestre para su aplicación de manera satisfactoria.

El trabajo se desarrolló a partir del análisis del contexto suministrado por el cliente, identificando actividades, responsables, puntos de decisión y posibles reprocesos presentes en el flujo actual.

## Proceso de desarrollo 

Para el modelado del proceso se siguieron los siguientes pasos:

### 1. Delimitación del alcance  

A través del contexto proporcionado por el cliente se identificó que el macroproceso de la encuesta incluía múltiples subprocesos. Por esta razón, se decidió acotar el análisis únicamente al flujo relacionado con la citación, la reunión explicativa y la recepción de información académica por parte de los directores de cada programa.

### 2. Identificación de actores  

Una vez delimitado el proceso, se identificaron los actores principales involucrados en el flujo:

- **Coordinadora de Encuestas**
- **Director de Programa**

Esta separación nos permitió asignar responsabilidades claras a cada actor.

### 3. Estructuración del flujo  

Posteriormente, se procedió a listar y organizar las actividades que componen el proceso, identificando la secuencia lógica en la que ocurren. Entre las principales actividades modeladas se encuentran:

- Envío de citación  
- Validación de disponibilidad  
- Programación de reunión  
- Envío del formato Excel  
- Diligenciamiento del formato por parte del director  
- Validación manual del formato recibido  
- Consolidación final de la información  

Adicionalmente, se identificaron puntos de decisión que requerían la incorporación de *gateways exclusivos*, especialmente en los casos de validación de disponibilidad y verificación del formato del archivo.

### 4. Modelado en herramienta BPMN  

Finalmente, se realizó el modelo en la herramienta **Miro**, donde se estructuraron las actividades, eventos y gateways conforme al estándar BPMN.

Una vez definidos los elementos principales del flujo, se ajustaron detalles técnicos del diagrama, tales como:

- Incorporación de eventos de mensaje para representar el envío y recepción de correos electrónicos.  
- Uso de eventos de temporizador cuando la siguiente acción no ocurre de manera inmediata.    

Estos ajustes permitieron mejorar la claridad del modelo y asegurar una representación más precisa del proceso real.

## Análisis del modelo propuesto

### 1. Estructura y Representación del Modelo

El modelo representa el proceso de Recolección y Consolidación de Información Académica para la encuesta de Autoevaluación Institucional y por Programas diferenciando claramente las responsabilidades entre la Coordinadora de Encuestas y el Director de Programa. El flujo inicia con el envío de la citación y finaliza cuando la información se encuentra consolidada y lista para continuar con la planeación logística, lo que permite delimitar con precisión el alcance del proceso dentro del macroproceso de la aplicación de la encuesta institucional.

Desde el punto de vista estructural, el diagrama incorpora eventos de mensaje para representar el intercambio de correos electrónicos, un evento intermedio de temporizador que modela la espera entre la programación y la realización de la reunión, y puntos de decisión que permiten evidenciar situaciones reales del proceso, como la validación de disponibilidad de agenda y la verificación del formato del archivo Excel completado por los directores de programa.

El modelo no solo describe las actividades del proceso, sino que también hace visibles los reprocesos que forman parte de su ejecución real. La necesidad de solicitar nuevos horarios cuando no existe disponibilidad para concretar la reunión con los directores de programa, así como la obligación de ajustar manualmente el formato del archivo Excel recibido, evidencian claramente la carga operativa actual. Según lo indicado por el cliente, la información enviada por los directores no se encuentra estandarizada; cada uno remite los datos en el formato que considera conveniente, lo que genera inconsistencias, campos incompletos y errores que deben corregirse manualmente antes de su consolidación. De esta manera, el diagrama cumple con uno de los propósitos fundamentales del modelado BPMN: **hacer explícitos los puntos críticos, los cuellos de botella y las dependencias que pueden afectar la eficiencia y la calidad del proceso**.

Desde la perspectiva de Arquitectura Empresarial, el proceso evidencia oportunidades de mejora en la forma en que se organiza, se gestiona la información y se apoya en la tecnología:
- El flujo actual presenta varias repeticiones y retrocesos que podrían disminuirse si existieran mecanismos de coordinación más estructurados, especialmente en la programación de reuniones y en la entrega de información.
- La información académica se valida de manera manual, lo que aumenta la probabilidad de errores, inconsistencias o formatos distintos entre programas.
- El proceso depende principalmente del correo electrónico y de archivos Excel independientes, lo que limita su nivel de automatización y trazabilidad. Esto sugiere que, incluso sin adquirir nuevas plataformas, podrían integrarse mejor las herramientas institucionales ya disponibles para hacer el proceso más ágil y controlado.

### 2. Diferencias con el caso base y justificaciones  

El caso base trabajado en clase, correspondiente al proceso de agendamiento de citas médicas de la Clínica Salud Viva, presenta un nivel de digitalización significativamente mayor. En dicho escenario, el paciente interactúa con un sistema de citas en línea que valida disponibilidad en tiempo real, almacena información automáticamente en una base de datos y genera confirmaciones de manera automática por correo electrónico o mensaje de texto. En otras palabras, el flujo está soportado por una plataforma tecnológica integrada que reduce la intervención manual.

En contraste, el proceso modelado para la universidad depende de coordinación manual entre actores, validaciones realizadas de forma individual y consolidación manual de información en archivos Excel. A diferencia del caso base, no existe una plataforma centralizada que gestione disponibilidad ni una base de datos que capture la información en tiempo real. Esto genera iteraciones adicionales, retrabajos y mayor carga operativa en la Coordinadora de Encuestas.

En consecuencia, mientras el caso base representa un proceso digitalmente maduro y automatizado, el proceso universitario refleja una operación funcional pero manual, con oportunidades claras de optimización. Esta comparación resulta fundamental para formular futuras propuestas de mejora desde la Arquitectura Empresarial teniendo en cuenta el contexto organizacional y tecnológico de la univerisdad.

## Diagrama final entregado
<p align="center">
  <img src="./BPMN_Real_Client.jpg" alt="Modelo BPMN - Recolección y Consolidación de Información Académica para la Encuesta de Autoevaluación Institucional y por Programas de la Universidad de la Sabana" width="100%"/>
</p>

## 📋 Tabla de actores, entidades o componentes (si aplica)

| Nombre del elemento            | Tipo            | Descripción                                                                 | Responsable                  |
|---------------------------------|-----------------|-----------------------------------------------------------------------------|------------------------------|
| Coordinadora de Encuestas      | Actor           | Encargada de coordinar citaciones, validar información y consolidar datos | Coordinadora de Encuestas       |
| Director de Programa           | Actor           | Responsable de enviar disponibilidad y diligenciar información académica  |  Director de Programa     |
| Formato Excel                  | Objeto de datos | Archivo enviado para diligenciamiento de información académica            | Director de Programa        |
| Excel Consolidado              | Objeto de datos | Archivo maestro con información validada y lista para planeación logística | Coordinadora de Encuestas   |

## 🔍 Investigación complementaria
### Tema investigado:
(Ej: Buenas prácticas BPMN, comparación TOGAF vs C4, principios de seguridad STRIDE, etc.)

### Resumen:
Describa en 2–3 párrafos lo investigado, citando fuentes cuando sea necesario. Incluya cómo se relaciona con el taller.

## 📚 Referencias
- [1] Apellido, Nombre. *Título*. Año. URL o DOI.
- [2] Fuente oficial BPMN: https://www.omg.org/spec/BPMN/

---

_Este documento hace parte de la entrega del taller 1 del curso AREM (Arquitectura Empresarial) - Universidad de La Sabana._
