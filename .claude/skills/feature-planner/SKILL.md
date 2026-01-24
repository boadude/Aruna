---
name: feature-planner
description: Use when planning a new feature. Creates functional requirement documents from a Product Owner perspective - describing WHAT the user needs, not HOW to implement it technically. Generates a .md file ready for Claude Code's plan mode. (project)
---

# Feature Planner

## Purpose

Transform feature ideas into structured functional requirement documents. This skill writes plans from a **Product Owner perspective** - focusing on user needs, business value, and acceptance criteria. The technical implementation is left to Claude Code's plan mode.

**This is NOT a technical planning tool.** It documents WHAT the user needs to accomplish, not HOW to build it.

## When to Activate

### Automatic Activation
- User says "planificar feature", "crear plan", "documentar requerimiento"
- User describes a new functionality they want
- User mentions "necesito que el sistema...", "quiero que los usuarios puedan..."
- User wants to structure a feature request before implementation
- User wants to add functionality to an existing module

### Detection Keywords
- "planificar", "crear plan", "plan de feature"
- "documentar requerimiento", "especificar feature"
- "funcionalidad nueva", "quiero que pueda..."
- "agregar a...", "modificar...", "extender..."

## Workflow

### Step 1: Understand the Requirement

**Ask the user about the feature:**

If the requirement isn't clear, ask:

```
Para documentar este requerimiento, necesito entender:

1. ¿Qué debe poder hacer el usuario con esta funcionalidad?
2. ¿Quiénes van a usar esta feature? (roles: admin, profesional, asistente, paciente)
3. ¿Hay algún flujo o proceso específico que deba seguir?
4. ¿Existe algún diseño, mockup o referencia visual?
5. ¿Hay alguna restricción o regla de negocio importante?
6. ¿Prioridad? (alta/media/baja)
```

**Capture:**
- Feature name (for the filename)
- User stories or use cases
- Business rules and constraints
- Visual references (if any)
- Priority and context

### Step 2: Identify References (Optional)

If the user mentions existing features or designs as reference, explore to understand:

1. **Visual references**: Screenshots, mockups, or existing screens to use as inspiration
2. **Similar functionality**: Existing features that work similarly
3. **User flows**: How users currently accomplish related tasks

**Note:** This exploration is to understand the FUNCTIONAL context, not to define technical implementation.

### Step 3: Structure the Functional Plan

Using the template at [templates/plan-template.md](templates/plan-template.md), create a functional specification with:

#### 3.1 Metadata
- Feature name
- Date
- Priority
- Module/area of the system

#### 3.2 Overview
- What is this feature?
- Why is it needed? (business value)
- Who will use it? (target users/roles)

#### 3.3 Capacidades por Rol
List what each role should be able to do:

```
### Profesional
- Ver historial de pagos del paciente
- Filtrar por rango de fechas

### Administrador
- Todo lo anterior
- Editar registros de pago
```

Keep it simple - one line per capability.

#### 3.4 Functional Requirements
Describe WHAT the system must do (not HOW):
- What information should be displayed?
- What actions can the user take?
- What should happen when...?
- What validations apply?

#### 3.5 User Flow
Describe the step-by-step journey:
1. User navigates to...
2. User sees...
3. User clicks/selects...
4. System shows/does...
5. User confirms...

#### 3.6 Business Rules
- Constraints and validations
- Permissions by role
- Edge cases and exceptions
- Data rules (required fields, formats, etc.)

#### 3.7 Acceptance Criteria
Testable conditions from the user's perspective:
- [ ] User can see X when Y
- [ ] System prevents Z when W
- [ ] Data appears correctly formatted
- [ ] Feature works for roles A, B, C

#### 3.8 Visual References (if applicable)
- Links to designs/mockups
- Screenshots of similar features
- Notes on UI/UX expectations

#### 3.9 Out of Scope
What this feature does NOT include (to set clear boundaries)

### Step 4: Generate the Plan File

**Create the file:**

1. Identify the module/domain the feature belongs to
2. Create subfolder if it doesn't exist
3. Generate a kebab-case filename from the feature name
4. Save to `.claude/plans/[module]/[feature-name].md`

**Folder organization:**

```
.claude/plans/
├── fichas/                    # Módulo ficha del paciente
│   ├── evoluciones.md
│   ├── sesiones.md
│   └── documentos.md
├── pacientes/                 # Módulo pacientes
│   ├── historial-pagos.md
│   └── importacion-masiva.md
├── calendario/                # Módulo calendario
│   ├── notificaciones.md
│   └── bloqueo-horarios.md
├── settings/                  # Configuración
│   └── integraciones.md
└── general/                   # Features transversales
    └── autenticacion.md
```

**Module mapping:**
| Feature relacionada a... | Carpeta |
|--------------------------|---------|
| Ficha del paciente | `fichas/` |
| Gestión de pacientes | `pacientes/` |
| Citas y agenda | `calendario/` |
| Configuración/Settings | `settings/` |
| Odontología clínica | `odontologia/` |

### Step 5: Present to User

After creating the plan:

1. **Show a summary** of the functional specification
2. **Provide the file path** for reference
3. **Explain next steps**

**Example output:**
```
He documentado el requerimiento para "[Feature Name]" en:
.claude/plans/[module]/[feature-name].md

Resumen:
- Módulo: [module]
- Descripción: [qué podrá hacer el usuario]
- User Stories: [N] historias de usuario
- Criterios de aceptación: [X] criterios definidos

Próximos pasos:
1. Revisa el documento y ajusta si es necesario
2. Cuando esté listo, usa plan mode para implementar
3. Claude Code leerá este archivo y lo traducirá a código
```

## Updating Existing Features

When the user wants to modify or extend an existing feature, follow this decision tree:

### Decision Criteria

| Type | Action | Example |
|------|--------|---------|
| **Bug/fix** | No plan needed, commit with `fix(...)` | "El botón no funciona" |
| **Small enhancement** | Update existing plan with `## Updates` section | "Agregar fecha de vencimiento a recetas" |
| **New significant feature** | Create new plan in same module folder | "Agregar plantillas de recetas predefinidas" |

### How to Decide

Ask yourself:
1. **Does it change the core concept?** → New plan
2. **Is it a natural extension of the same concept?** → Update existing plan
3. **Could it be a standalone feature?** → New plan
4. **Is it just adding a field or small behavior?** → Update existing plan

### Updating an Existing Plan

When adding to an existing plan, append an `## Updates` section at the end:

```markdown
## Updates

### [Date] - [Brief description]

**Cambio solicitado:**
[Description of what changed]

**Nuevos requerimientos:**
- [New requirement 1]
- [New requirement 2]

**Nuevos criterios de aceptación:**
- [ ] [New acceptance criteria]

**Estado:** Pendiente | Implementado
```

### Creating a Related New Plan

When creating a new plan for a related feature:

1. Save in the **same module folder** as the original
2. Reference the original plan if relevant:
   ```markdown
   ## Contexto
   Esta feature extiende el módulo de recetas médicas (ver `recetas-medicas.md`).
   ```
3. Use a descriptive name that reflects the new concept

**Example:**
```
.claude/plans/fichas/
├── recetas-medicas.md           # Original plan
├── plantillas-recetas.md        # New related feature
└── recetas-favoritos.md         # Another related feature
```

### Workflow for Updates

1. **Check if plan exists**: Look in `.claude/plans/[module]/` for existing plans
2. **Evaluate the change**: Small enhancement or new concept?
3. **If update**: Add `## Updates` section to existing plan
4. **If new**: Create new plan with reference to original
5. **Inform user**: Explain why you chose update vs new plan

**Example output for update:**
```
He actualizado el plan existente de recetas médicas:
.claude/plans/fichas/recetas-medicas.md

Agregué la sección "Updates" con:
- Nuevo requerimiento: fecha de vencimiento
- Nuevos criterios de aceptación

El plan original se mantiene como referencia histórica.
```

**Example output for new plan:**
```
He creado un nuevo plan para plantillas de recetas:
.claude/plans/fichas/plantillas-recetas.md

Creé un plan separado porque:
- Es un concepto nuevo (plantillas predefinidas)
- Tiene su propio flujo de usuario
- Podría implementarse de forma independiente

Hace referencia al módulo de recetas médicas existente.
```

## Best Practices

### DO
- Write from the user's perspective, not the developer's
- Use language that a non-technical person would understand
- Focus on WHAT, not HOW
- Include concrete examples and scenarios
- Define clear acceptance criteria
- Specify what's OUT of scope
- Reference existing features as visual/functional examples
- Check for existing plans before creating new ones
- Use `## Updates` section for small enhancements to existing features

### DON'T
- Don't include technical implementation details
- Don't mention specific files, functions, or code patterns
- Don't use technical jargon (queries, mutations, hooks, etc.)
- Don't define database schemas or API endpoints
- Don't specify UI component libraries or frameworks
- Don't make assumptions about technical approach
- Don't create a new plan when an update to existing plan is enough
- Don't use emojis in plan documents

## Example Usage

**User says:**
> "Quiero que los pacientes puedan ver su historial de pagos desde la ficha"

**Skill creates a functional spec with:**
- Overview: Pacientes pueden consultar todos sus pagos realizados
- Capacidades: Profesional puede ver pagos, filtrar por fecha. Admin puede editar.
- Requirements: Lista de pagos con fecha, monto, concepto, estado
- User Flow: Abrir ficha → Ir a pestaña Pagos → Ver listado → Filtrar por fecha
- Business Rules: Solo pagos de la organización actual, ordenados por fecha descendente
- Acceptance Criteria: Usuario ve pagos, puede filtrar, ve totales, etc.

**What it does NOT include:**
- "Crear query en convex/payments.ts"
- "Usar useQuery para obtener datos"
- "Implementar componente PaymentHistoryTable"

## Integration with Plan Mode

The functional spec serves as the **contract** between Product Owner and Developer:

1. **This skill** documents WHAT the user needs (functional)
2. **Plan mode** figures out HOW to build it (technical)

When you enter plan mode with a task, Claude Code will:
1. Read the functional spec from `.claude/plans/`
2. Analyze the codebase for patterns and existing code
3. Create a technical implementation plan
4. Execute the implementation

## Notes

- Plans are saved in `.claude/plans/[module]/` directory
- Write in Spanish (this is a Spanish-speaking product)
- Focus on user value, not technical elegance
- Plans can be version controlled and reviewed by stakeholders
- Update plans if requirements change before implementation
