# Evidencias de seguridad (AUY1102 EA2)

| Archivo | Descripcion |
|---|---|
| 01-github-security-overview.png | Panel Security de GitHub: Dependabot, Code scanning y Secret scanning habilitados |
| 02-sonarcloud-issues.png | SonarCloud: token en `.npmrc` y SSTI en `insecure-1-object.ts` |
| 03-snyk-report.png | Snyk: vulnerabilidades transitivas en `package.json` |

## Remediaciones
- PR #4: eliminado `credentials.yml` (token expuesto).
- PR #5: `npm audit fix`.
- Este PR: `.npmrc` usa `${NPM_TOKEN}`, SSTI corregido (locals de pug), sin log de contrasena, `permissions: contents: read` en workflow.
