# Personalize Existing Workflow Rules 

**DO THIS:** Help user modify team workflow rules 

## Step-by-Step Workflow

### 1. Identify Rule to Personalize
```bash
# List all rule files (use tree if available, otherwise find)
tree .cursor/rules -I '_|node_modules' || find .cursor/rules -name "*.mdc" -type f | grep -v "/_/"
```

### 2. Read Current Rule
```bash
cat .cursor/rules/_core/persona.mdc  # Or target file
```

### 3. Modify the Rule
```bash
cp .cursor/rules/_core/persona.mdc .cursor/rules/_core/persona-onewordtodescribenewpersona.mdc #or target file
```
Make specific changes based on user needs in the new copied file .cursor/rules/_core/persona-onewordtodescribenewpersona.mdc.


## Common Personalizations

### Less Aggressive Workflow Execution
Create in `_core/persona-patient.mdc`:
```markdown
**You are a helpful, patient developer assistant.**
- Ask for clarification when needed
- Explain reasoning before major changes
- Wait for approval on destructive operations
```

### More Verbose Workflow Communication
Replace in `_core/communication-verbose.mdc`:
```markdown
# Communication Style
- Explain reasoning behind decisions
- Include context and alternatives
- Describe implications of changes
```

### Different Package Manager in Workflows
Replace in `_core/standards-different.mdc`:
```markdown
# Package Managers
- **Default:** Use `npm` unless specified otherwise.

## Example Session
```bash
# 1. Edit persona to be less autonomous
cp .cursor/rules/_core/persona.mdc .cursor/rules/_core/persona-patient.mdc #or target file
vi .cursor/rules/_core/persona-patient.mdc

# Disable the old rule rule type = manual
vi .cursor/rules/_core/persona.mdc
```

