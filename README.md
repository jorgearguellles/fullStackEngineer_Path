# Full Stack Engineer Hub

> Guía interactiva de aprendizaje para construir aplicaciones de clase mundial — con roadmap, proyectos paso a paso, verificación de progreso y recursos 100% gratuitos.

[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue?style=flat-square&logo=github)](https://TU_USUARIO.github.io/fullstack-engineer-hub)
[![Open Source](https://img.shields.io/badge/Stack-Open%20Source%20First-green?style=flat-square)](https://github.com/TU_USUARIO/fullstack-engineer-hub)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)

---

## ¿Qué es este proyecto?

**Full Stack Engineer Hub** es una aplicación web de una sola página (un archivo HTML autocontenido) que actúa como guía estructurada de aprendizaje para ingenieros full stack. No es un curso — es un **sistema de proyectos reales** con tareas concretas, verificación ejecutable desde la terminal y recursos gratuitos para cada tecnología.

La idea central: en lugar de ver tutoriales pasivamente, el estudiante construye 21 proyectos organizados en 4 dominios de ingeniería, con una guía paso a paso que responde la pregunta más importante que nadie suele responder: **¿cómo sé que lo hice bien antes de marcar la tarea como completa?**

```
┌─────────────────────────────────────────────────────┐
│  🎨 Frontend  ·  ⚙️ Backend  ·  ☁️ Cloud  ·  🤖 AI  │
│                                                     │
│  21 proyectos  ·  18 stacks  ·  107 tareas guiadas  │
│  107 comandos de verificación  ·  60+ recursos OSS  │
└─────────────────────────────────────────────────────┘
```

---

## Demo en vivo

🔗 **[TU_USUARIO.github.io/fullstack-engineer-hub](https://TU_USUARIO.github.io/fullstack-engineer-hub)**

> Reemplaza `TU_USUARIO` con tu nombre de usuario de GitHub después de hacer el deploy.

---

## Contenido del hub

### 4 dominios · 21 proyectos

| Dominio | Proyectos |
|---|---|
| 🎨 **Frontend** | Design System, Analytics Dashboard, PWA E-Commerce, Collaborative Whiteboard, Video Streaming |
| ⚙️ **Backend** | Auth & Identity Service, Notification Engine, GraphQL Gateway, Multi-Tenant SaaS, Event-Driven Orders |
| ☁️ **Cloud & DevOps** | GitOps CI/CD, Serverless Data Pipeline, Multi-Region HA, Zero-Trust Security, FinOps Intelligence |
| 🤖 **AI / ML** | Document RAG Platform, AI Code Reviewer, Multimodal Content Studio, Autonomous Research Agent, AI Tutor |
| ⚡ **Full Stack** | AI-Powered SaaS Platform (monorepo completo) |

### 18 tech stacks cubiertos

`React 19` · `Next.js 14` · `TypeScript` · `Vite + Bun` · `React Native + Expo` · `Node.js 22 + Fastify` · `FastAPI + Python 3.12` · `PostgreSQL + pgvector` · `Redis + BullMQ` · `Kafka` · `Docker + Kubernetes` · `Terraform` · `GitHub Actions + ArgoCD` · `OpenTelemetry + Grafana` · `LangGraph + LangChain` · `Claude API` · `Ollama` · `Hugging Face`

### Por cada tarea se incluye

- **¿Por qué importa?** — contexto real, no solo "qué hace"
- **Pasos concretos** — optimizados para macOS (Homebrew, pnpm, Bun)
- **💡 Tip** — el error más común y cómo evitarlo
- **Comando terminal** — listo para copiar
- **🧪 Verificación** — comando ejecutable + salida esperada exacta
- **📎 Documentación oficial** — links a fuentes gratuitas (sin paywalls)

### Progreso persistente

El progreso se guarda automáticamente en `localStorage`. Al volver al hub después de cerrar el browser, todo el estado se restaura.

---

## Instalación y uso local

### Opción A — directamente en el browser (sin instalación)

```bash
# Descarga el archivo HTML
curl -L https://raw.githubusercontent.com/TU_USUARIO/fullstack-engineer-hub/main/fullstack_engineer.html -o fullstack_engineer.html

# Abre en el browser
open fullstack_engineer.html          # macOS
xdg-open fullstack_engineer.html      # Linux
start fullstack_engineer.html         # Windows
```

### Opción B — clonar el repositorio

```bash
# Clonar
git clone https://github.com/TU_USUARIO/fullstack-engineer-hub.git
cd fullstack-engineer-hub

# Abrir directamente (no necesita servidor)
open fullstack_engineer.html
```

> El proyecto es un archivo HTML autocontenido. No necesita Node.js, servidor ni dependencias instaladas para funcionar.

---

## Deploy en GitHub Pages

El hub está pensado para vivir en GitHub Pages como parte de tu portafolio público.

### Paso 1 — crear el repositorio

```bash
# Crea un repositorio nuevo en github.com/new
# Nombre sugerido: fullstack-engineer-hub
# Visibilidad: Public (necesario para GitHub Pages gratuito)
```

### Paso 2 — subir el archivo

```bash
git init
git add fullstack_engineer.html
git add README.md

git commit -m "feat: add Full Stack Engineer Hub"

git remote add origin https://github.com/TU_USUARIO/fullstack-engineer-hub.git
git branch -M main
git push -u origin main
```

### Paso 3 — activar GitHub Pages

1. Ve a tu repositorio en GitHub
2. **Settings** → **Pages** (menú lateral)
3. En **Source** selecciona: `Deploy from a branch`
4. Branch: `main` · Folder: `/ (root)`
5. Haz click en **Save**

### Paso 4 — renombrar para la URL raíz (opcional)

Si quieres que el hub sea tu página principal (`TU_USUARIO.github.io`):

```bash
# Renombra el repositorio a: TU_USUARIO.github.io
# Settings → General → Repository name
# Luego renombra el archivo HTML:

mv fullstack_engineer.html index.html
git add -A
git commit -m "chore: rename to index.html for root deploy"
git push
```

### Paso 5 — verificar el deploy

```bash
# GitHub Pages tarda ~2 minutos en publicar
# Verifica en:
open https://TU_USUARIO.github.io/fullstack-engineer-hub

# O si usaste el repositorio TU_USUARIO.github.io:
open https://TU_USUARIO.github.io
```

---

## Estructura del proyecto

```
fullstack-engineer-hub/
├── fullstack_engineer.html   # Aplicación completa (autocontenida)
├── README.md                 # Este archivo
└── LICENSE                   # MIT
```

El hub es intencionalmente un solo archivo HTML. Esta decisión de diseño:

- Elimina el paso de instalación — cualquier persona puede abrirlo
- Facilita el deploy en GitHub Pages sin configuración adicional
- Permite compartirlo directamente por mensaje o email
- El `localStorage` del browser persiste el progreso sin necesitar backend

---

## Habilidades técnicas desarrolladas

> Esta sección está dirigida a reclutadores y equipos de ingeniería.

### Ingeniería de Frontend

El desarrollo de este hub implicó construir una SPA completa sin frameworks — solo HTML, CSS y JavaScript vanilla — con arquitectura de componentes, sistema de módulos por datos, renderizado dinámico del DOM y gestión de estado persistente.

**Evidencia técnica:** sistema de tabs, modal con animaciones, malla de proyectos responsive, anillo SVG de progreso animado, filtros por dominio con reactividad, checklist con localStorage, ticker infinito con CSS animations.

### Gestión de datos y arquitectura JavaScript

El hub maneja un grafo de datos complejo: 21 proyectos, 18 stacks, 10 roadmap items, 107 tareas con guías, 107 comandos de verificación, y más de 300 recursos de aprendizaje — todo en estructuras de datos JavaScript bien tipadas, con lookups eficientes y renderizado condicional.

**Evidencia técnica:** separación de `TASK_GUIDE` y `VERIFY_DATA` en constantes independientes (resolviendo el problema real de escape de strings en JS); sistema de IDs por proyecto para localStorage; algoritmo de progreso global con anillo SVG calculado dinámicamente.

### Debugging y resolución de problemas de producción

Durante el desarrollo se encontró y resolvió un bug crítico de JS: template literals anidados con comandos de shell que contenían comillas simples generaban tokens inválidos que silenciosamente impedían la ejecución de todo el script. La solución involucró validación con `node --check`, parseo con state machine y separación arquitectural de los datos.

**Evidencia técnica:** uso de `node --check` para validación de sintaxis JS, parseo de strings con state machine, reescritura de `buildVerifyHTML` con concatenación segura, inyección de `VERIFY_DATA` como JSON serializado.

### Conocimiento del ecosistema full stack moderno

El contenido del hub requirió investigación profunda y síntesis de 107 tareas concretas con pasos exactos para macOS, comandos verificables y links a documentación oficial. Cubre el stack completo de ingeniería moderna de forma integrada.

| Área | Tecnologías dominadas |
|---|---|
| Frontend | React 19, Next.js App Router, TypeScript, Vite, Bun, Vitest, Playwright, Storybook, Radix UI, Tailwind, Framer Motion |
| Mobile | React Native, Expo SDK, NativeWind, Reanimated 3, EAS Build |
| Backend | Node.js, Fastify, FastAPI, tRPC, GraphQL, BullMQ, Prisma, Zod, argon2, JWT, OAuth2/PKCE |
| Bases de datos | PostgreSQL + RLS, Redis, pgvector, Event Sourcing, Kafka |
| Cloud & DevOps | Docker, Kubernetes, Terraform, GitHub Actions, ArgoCD, Helm, Prometheus, OpenTelemetry, Grafana |
| Seguridad | Zero-Trust, Istio + mTLS, HashiCorp Vault, OPA, SPIFFE/SPIRE, HMAC signatures |
| AI / LLM | RAG pipelines, LangGraph agents, pgvector, Claude API, Ollama, RAGAS eval, Browser Use |
| Prácticas | GitOps, CI/CD, Saga pattern, Event Sourcing, CQRS, RBAC, Multi-tenancy, SRE |

### Diseño de producto y UX

El hub resuelve un problema pedagógico real: la ausencia de feedback concreto durante el aprendizaje autodidacta. Cada decisión de diseño responde a una necesidad del estudiante: el panel de verificación `🧪 ¿Cómo sé que llegué?` nació de la pregunta *"¿cómo sabe el estudiante que completó un paso correctamente antes de marcarlo?"*.

**Evidencia técnica:** jerarquía de información en 5 niveles (hub → dominio → proyecto → tarea → verificación), diseño dark mode con CSS variables, paleta de colores semántica por dominio, animaciones de progreso que refuerzan la sensación de avance.

### Iteración y mejora continua

El proyecto pasó por múltiples iteraciones con refactoring significativo: migración completa de `npm` a `pnpm` con validación de sintaxis de cada comando, reescritura del sistema de datos de verificación para eliminar bugs de escape, y adición progresiva de features (checklist → guías → verificación) sin romper funcionalidad existente.

---

## Por qué este proyecto es relevante para un equipo de ingeniería

Un reclutador o tech lead puede verificar en este proyecto:

**Criterio de evaluación → Evidencia en el hub**

- *¿Puede estructurar sistemas complejos de datos?* → TASK_GUIDE con 107 objetos indexados, VERIFY_DATA como JSON separado, lookup eficiente por pid e índice
- *¿Depura problemas no obvios?* → Bug de template literals anidados detectado con node --check, resuelto con parseo por state machine
- *¿Conoce el stack moderno?* → 18 stacks cubiertos con comandos exactos, incluyendo herramientas de 2024-2025 (Bun, LangGraph, pgvector, Browser Use)
- *¿Piensa en el usuario?* → Verificación ejecutable por tarea, persistencia de progreso, feedback visual inmediato
- *¿Itera sin romper?* → Migración npm→pnpm sin errores, refactoring del verify system manteniendo 107 tareas intactas
- *¿Sabe deployar?* → Archivo autocontenido optimizado para GitHub Pages, sin dependencias de servidor

---

## Tecnologías del hub (meta)

El hub en sí mismo fue construido con:

- **HTML5** — estructura semántica, sin frameworks
- **CSS3** — variables CSS, animaciones, grid/flexbox, diseño responsive
- **JavaScript ES2022** — módulos de datos, state machine, DOM manipulation, localStorage API, SVG dinámico
- **Fuente** — JetBrains Mono + Syne (Google Fonts)
- **Deploy** — GitHub Pages (archivos estáticos, cero costo)

---

## Contribuir

Las contribuciones son bienvenidas, especialmente:

- Agregar proyectos para los dominios `cl2–cl5`, `ai2`, `ai3`, `ai5` (actualmente sin guías detalladas)
- Traducir los textos de guías al inglés
- Agregar soporte para Windows (los comandos actuales son para macOS/Linux)
- Mejorar los comandos de verificación con casos edge

```bash
# Fork → clone → branch → PR
git checkout -b feat/add-cl2-guide
# Edita fullstack_engineer.html
# Valida sintaxis JS:
node --check fullstack_engineer.html  # debe retornar sin output (= válido)
git push origin feat/add-cl2-guide
```

---

## Licencia

MIT — úsalo, modifícalo y compártelo libremente. Si lo usas como base para tu propio portafolio, un ⭐ en el repositorio es bienvenido.

---

<div align="center">

Construido como proyecto de portafolio · Ingeniería de Software · 2025

**[Ver demo](https://TU_USUARIO.github.io/fullstack-engineer-hub)** · **[Reportar un bug](https://github.com/TU_USUARIO/fullstack-engineer-hub/issues)** · **[Sugerir un proyecto](https://github.com/TU_USUARIO/fullstack-engineer-hub/issues/new)**

</div>
