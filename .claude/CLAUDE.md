# CLAUDE.md — Resumen del repositorio AzureDevOpsRepo

## Propósito del proyecto

Repositorio de prueba creado para **validar la integración entre una herramienta externa y Azure DevOps**. No contiene lógica de negocio ni una aplicación funcional; su único objetivo es confirmar que la conexión con el servicio de Azure DevOps funciona correctamente.

---

## Stack / Lenguajes

| Elemento     | Detalle                              |
|--------------|--------------------------------------|
| Lenguaje     | Shell / Bash (`.sh`)                 |
| Plataforma   | Sin runtime específico requerido     |
| CI/CD target | Azure DevOps Pipelines (implícito)   |

No hay framework, gestor de paquetes ni dependencias externas declaradas.

---

## Estructura de carpetas

```
/
├── README.md      # Descripción breve del repositorio
├── Hello.sh       # Script shell de prueba (primer archivo del repo)
└── .claude/
    └── CLAUDE.md  # Este archivo
```

---

## Archivos principales

### `README.md`
Descripción de una línea:
> "Integración con el azure devops para validar si se integra con el devops"

### `Hello.sh`
Script shell mínimo, contiene únicamente el comentario/texto:
```sh
create a first file repository
```
Su propósito es servir como primer archivo del repositorio para verificar que el flujo de creación y sincronización con Azure DevOps funciona.

---

## Dependencias principales

Ninguna. El repositorio no tiene:
- Archivos de manifiesto (`package.json`, `pom.xml`, `requirements.txt`, `Pipfile`, `go.mod`, etc.)
- Dependencias de sistema declaradas
- Dockerfiles ni archivos de configuración de infraestructura

---

## Instrucciones de ejecución

No hay proceso de build, test ni deploy definido. Para ejecutar el único script presente:

```bash
bash Hello.sh
```

> **Nota:** el contenido actual del script no es un comando válido de Bash; es texto plano descriptivo. Si se pretende usarlo como script ejecutable, deberá añadirse el shebang `#!/usr/bin/env bash` y comandos válidos.

---

## Estado del repositorio

| Indicador             | Valor                     |
|-----------------------|---------------------------|
| Madurez               | Prototipo / sandbox       |
| Tests                 | Ninguno                   |
| CI/CD configurado     | No (sin `.github/` ni `azure-pipelines.yml`) |
| Documentación         | Mínima (README de 1 línea)|
| Listo para producción | No                        |

---

## Convenciones a seguir en este proyecto

Dado que el repositorio está en fase inicial, se recomienda:

1. **Scripts Bash**: incluir siempre `#!/usr/bin/env bash` como primera línea y activar `set -euo pipefail` para robustez.
2. **README**: ampliar con instrucciones de uso reales cuando se agregue funcionalidad.
3. **Pipelines**: añadir `azure-pipelines.yml` cuando se quiera aprovechar la integración con Azure DevOps CI/CD.
4. **Ramas**: seguir la convención `main` como rama principal.
