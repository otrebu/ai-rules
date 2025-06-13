# Create Executable TypeScript Scripts with Node

**Your task: Create new, executable TypeScript scripts within a `scripts` directory, runnable with `node`.**

## Directory Check

Check if the `scripts/` directory exists:

```bash
ls -la scripts 2>/dev/null || echo "scripts/ directory not found - will create it"
```

Follow these steps precisely:

1.  **Ensure `scripts` Directory:** If it doesn't already exist, create a `scripts/` directory in the project root.
2.  **Create Script File:** Inside the `scripts/` directory, create your new TypeScript file (e.g., `scripts/my-new-script.ts`).
3.  **Add Env node Shebang:** Make the first line of your script: `#!/usr/bin/env -S node --experimental-strip-types`
4.  **Write TypeScript Code:** Implement the script's logic in TypeScript. Ensure the code is compatible with Node.js execution environments.
5.  **Make Executable:** After saving the script, make it executable by running the command: `chmod +x scripts/your-script-name.ts` (replace `your-script-name.ts` with the actual filename).

**REMEMBER: The final script must be a TypeScript file located in the `scripts/` directory, start with the `#!/usr/bin/env -S node --experimental-strip-types` shebang, and be executable (`chmod +x`).**
