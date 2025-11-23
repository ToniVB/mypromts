# 📘 GPT Template

---

## Name

**Qué es:** El título visible del GPT.  
**Cómo hacerlo efectivo:** Debe ser **corto, claro y específico**. Idealmente en inglés si es técnico.  
**Ejemplo:** `NCR Translator & Organizer`

---

## Description

**Qué es:** Resumen breve (máx. 2–3 frases) de lo que hace el GPT.  
**Cómo hacerlo efectivo:** Debe transmitir **qué hace** y **para quién está pensado**.  
**Ejemplo:**  
"Generates and translates Non-Conformity Reports (NCRs) from Spanish drafts into clear, professional English for international clients."

---

## Instructions

**Qué es:** El núcleo del GPT. Aquí defines el comportamiento, estilo y reglas.  
**Cómo hacerlo efectivo:**

- Usa un **lenguaje directo y en segunda persona** (“Debes…”).
- Divide en **Propósito**, **Reglas principales**, **Formato de salida**.
- Añade ejemplos de entrada/salida si son críticos.

**Ejemplo:**

```plaintext
Purpose: Translate and organize NCRs from Spanish to English with formal engineering tone.  
Main Rules:  
- No colloquial expressions.  
- Ensure precision and clarity.  
- Keep sentences short and direct.  

Output Structure:  
1. Title  
2. Problem Description  
3. Evidence (if applicable)  
4. Corrective Action  

Example:  
Input (ES): "El soporte instalado no corresponde al plano 2D aprobado."  
Output (EN):  
Non-Conformity Report  
Description: The installed support does not match the approved 2D drawing.  
Corrective action: Replace with compliant support according to drawing ref. XXX.  
```

## Conversation Starters / Iniciadores de conversación

**Qué es:** Frases que aparecen como **botones sugeridos** para arrancar una conversación con el GPT.  
**Cómo hacerlo efectivo:**

- Piensa en **preguntas típicas** o tareas clave.
  
- Haz que sean **variadas** (traducción, resumen, redacción).
  

**Ejemplo:**

- "Traducir este borrador de NCR al inglés"
  
- "Revisar si este NCR está claro para cliente"
  
- "Generar estructura de NCR a partir de notas"
  

## Knowledge / Conocimiento

**Qué es:** Archivos o datos adicionales que subes (manuales, normas, PDFs, bases de datos).  
**Cómo hacerlo efectivo:**

- Incluye solo lo **relevante** para el GPT.
  
- Manténlo actualizado (versiones de documentos, normas técnicas).
  

**Ejemplo:**

- PDF con procedimiento de NCR interno.
  
- Plantilla estándar de NCR en inglés.
  

## Model / Modelo

**Qué es:** El motor de IA que usará el GPT.  
**Cómo hacerlo efectivo:**

- GPT-4o o GPT-4o-mini para tareas con contexto y precisión.
  
- GPT-4o es mejor para **documentación crítica, traducción técnica y formalidad**.
  
- GPT-4o-mini si necesitas velocidad para borradores simples.
  

## Functions / Funciones

**Qué es:** Bloques de código (en Python u otro) que amplían el GPT para tareas automáticas.  
**Cómo hacerlo efectivo:**

- Define **inputs y outputs claros**.
  
- Usa funciones cuando necesites **automatización repetitiva** (ejemplo: formatear un NCR automáticamente).
  
  $$
  def format_ncr(title, description, evidence=None, corrective_action=None):
  ncr = f"**Non-Conformity Report**\n"
  ncr += f"Title: {title}\n"
  ncr += f"Description: {description}\n"
  if evidence:
  ncr += f"Evidence: {evidence}\n"
  ncr += f"Corrective Action: {corrective_action}\n"
  return ncr
  $$

python

```python
def format_ncr(title, description, evidence=None, corrective_action=None):
 ncr = f"**Non-Conformity Report**\n"
 ncr += f"Title: {title}\n"
 ncr += f"Description: {description}\n"
 if evidence:
 ncr += f"Evidence: {evidence}\n"
 ncr += f"Corrective Action: {corrective_action}\n"
 return ncr
```

## Actions / Acciones

**Qué es:** Integraciones externas (APIs, Notion, Gmail, etc.).  
**Cómo hacerlo efectivo:**

- Define **qué servicio conecta** y **para qué lo usas**.
  
- Úsalo solo si aporta **flujo de trabajo real** (ejemplo: guardar NCR en Notion automáticamente).
  

**Ejemplo:**

- Action para subir NCRs a Notion en tabla de control de calidad.
  
- Action para enviar NCR al correo del cliente.
