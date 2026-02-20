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

## 🧩 Análisis del modelo propuesto
Incluya un análisis sobre:
- Cómo se estructura el modelo entregado
- Cómo representa las necesidades del cliente
- Qué supuestos se tomaron

## 📈 Diagrama final entregado
> (Inserte aquí una imagen o enlace al modelo-final.drawio / .asta / PDF)

## 📋 Tabla de actores, entidades o componentes (si aplica)

| Nombre del elemento | Tipo | Descripción | Responsable |
|---------------------|------|-------------|-------------|
| Ej: Paciente        | Actor | Usuario que agenda una cita médica | Cliente |

## 🔍 Investigación complementaria
### Tema investigado:
(Ej: Buenas prácticas BPMN, comparación TOGAF vs C4, principios de seguridad STRIDE, etc.)

### Resumen:
Describa en 2–3 párrafos lo investigado, citando fuentes cuando sea necesario. Incluya cómo se relaciona con el taller.

## 📚 Referencias
- [1] Apellido, Nombre. *Título*. Año. URL o DOI.
- [2] Fuente oficial BPMN: https://www.omg.org/spec/BPMN/

---

_Este documento hace parte de la entrega del taller X del curso AREM (Arquitectura Empresarial) - Universidad de La Sabana._
