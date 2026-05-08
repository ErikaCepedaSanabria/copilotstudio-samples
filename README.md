# ✨🦋 Copilot Studio Samples — by Erika Cepeda 🦋✨

> Una colección de **agentes de Microsoft Copilot Studio** listos para clonar, personalizar y desplegar. Cada agente es una historia diferente: productividad, ventas, eventos… todos con IA generativa en el centro. 🌸

<p align="center">
  <i>✨ Agents that spark joy · Powered by Microsoft Copilot Studio 🤖 · Built with ❤️ by Erika Cepeda ✨</i>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/erikacepeda/">
    <img src="https://img.shields.io/badge/LinkedIn-Erika%20Cepeda-C865F7?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Erika Cepeda" />
  </a>
  &nbsp;
  <img src="https://img.shields.io/badge/Platform-Microsoft%20Copilot%20Studio-742774?style=for-the-badge&logo=microsoftcopilot&logoColor=white" alt="Copilot Studio" />
  &nbsp;
  <img src="https://img.shields.io/badge/Powered%20by-GPT--5%20%26%20Azure%20OpenAI-FF6B6B?style=for-the-badge&logo=openai&logoColor=white" alt="GPT-5" />
  &nbsp;
  <img src="https://img.shields.io/badge/Made%20with-%F0%9F%A6%8B%20%26%20%F0%9F%8C%B8-F7C8E0?style=for-the-badge" alt="Made with butterflies and flowers" />
</p>

---

## 🌺 Agentes disponibles

| 🦋 Agente | Descripción | Idioma |
|---|---|---|
| [🗓️ Recomendador de sesiones](#️-recomendador-de-sesiones) | Recomienda sesiones del Power Platform Madrid 2026 según tus gustos y disponibilidad | 🇪🇸 Español |
| [💼 Sales Specialist – Microsoft Cloud](#-sales-specialist--microsoft-cloud) | Cualifica oportunidades comerciales y recomienda soluciones Microsoft con metodología BANT+ | 🇪🇸 Español |

---

## 🗓️ Recomendador de sesiones

> *Tu guía personal para el Power Platform Madrid 2026* ✨

El **Recomendador de sesiones** es tu asistente para el evento **Power Platform Madrid 2026**. Antes de que empieces a elegir sesiones al azar, este agente te hace las preguntas correctas — temática, nivel, formato, idioma y disponibilidad horaria — y te entrega un plan personalizado con los mejores tracks para ti.

### ¿Qué hace? 🌸

- 🎯 **Recomienda de 3 a 6 sesiones priorizadas** adaptadas a tu perfil
- ⚡ **Modo agenda express**: solo 3 preguntas y ya tienes tu plan
- 📋 Para cada sesión incluye: título, hora, track, ponentes, por qué encaja contigo y un consejo para aprovecharla al máximo
- 🔍 Grounded en la agenda oficial del evento y en la página pública de Eventbrite
- 💬 Transparente cuando la agenda no especifica nivel o idioma — nunca inventa datos

### Arquitectura 🌷

```
Recomendador de sesiones/
├── agent.mcs.yml                    # Instrucciones del agente (GPT-5)
├── settings.mcs.yml                 # Configuración de acceso y auth
├── icon.png                         # Icono del agente
├── knowledge/
│   ├── files/                       # Agenda oficial Power Platform Madrid 2026
│   └── *.mcs.yml                    # Fuente Eventbrite y agenda del evento
└── topics/
    ├── RecomendarSesionesEvento.mcs.yml   # Flujo principal de recomendación
    ├── RecomendarSesionesExpress.mcs.yml  # Modo agenda express (3 preguntas)
    ├── Greeting.mcs.yml
    ├── Fallback.mcs.yml
    └── ...                          # Topics estándar de sistema
```

### Pruébalo con prompts como 🦋

- _"Quiero sesiones sobre Power Automate nivel intermedio por la mañana"_
- _"Dame una agenda express para el evento"_
- _"¿Qué sesiones hay sobre Copilot Studio?"_
- _"Soy desarrollador/a y busco sesiones técnicas avanzadas"_

---

## 💼 Sales Specialist – Microsoft Cloud

> *Tu co-piloto comercial para el ecosistema Microsoft* 🚀

El **Sales Specialist – Microsoft Cloud** es un agente experto en cualificación comercial con metodología **BANT+** y recomendación de soluciones Microsoft. Habla como un consultor senior de Devoteam: directo, profesional, centrado en valor de negocio — no en características técnicas.

### ¿Qué hace? 🌻

| Capacidad | Detalle |
|---|---|
| 🎯 **Cualificación BANT+** | Budget · Authority · Need · Timeline + Sector, tamaño y competencia |
| 💡 **Recomendaciones priorizadas** | Máximo 3 soluciones con valor de negocio y próximo paso concreto |
| 📊 **Ficha de cualificación** | Formato estructurado con nivel de cualificación (Alta/Media/Baja) |
| 🤝 **Gestión competitiva** | Posicionamiento vs Google Workspace, AWS y Salesforce |
| 📄 **Análisis de RFPs** | Si compartes un briefing, extrae los campos BANT+ automáticamente |

### Portfolio Microsoft cubierto 🌸

| Área | Soluciones |
|---|---|
| **Productividad** | Microsoft 365, Copilot for M365 |
| **Seguridad** | Sentinel, Defender XDR, Purview, Entra |
| **Datos & IA** | Fabric, Azure OpenAI, Copilot Studio, Power BI |
| **Infraestructura** | Azure IaaS/PaaS, Arc, GitHub/Azure DevOps |
| **CRM & Automatización** | Dynamics 365, Power Platform, Microsoft Viva |

### Arquitectura 🌷

```
Sales Specialist – Microsoft Cloud/
├── agent.mcs.yml                    # Instrucciones BANT+ y portfolio (GPT-5)
├── settings.mcs.yml                 # Auth y acceso
├── connectionreferences.mcs.yml     # Referencias de conexión
├── icon.png                         # Icono del agente
└── topics/
    ├── MenuPrincipal.mcs.yml              # Menú de entrada al agente
    ├── CualificarOportunidad.mcs.yml      # Flujo BANT+ completo
    ├── RecomendarSolucion.mcs.yml         # Motor de recomendación
    ├── GenerarResumen.mcs.yml             # Ficha de cualificación
    ├── CierreComercial.mcs.yml            # Próximo paso y cierre
    ├── Greeting.mcs.yml
    ├── Fallback.mcs.yml
    └── ...                               # Topics estándar de sistema
```

### Pruébalo con prompts como 🦋

- _"Tengo un cliente del sector Retail, unos 500 empleados, que quiere mejorar su seguridad"_
- _"¿Cómo me posiciono frente a Google Workspace en una cuenta Enterprise?"_
- _"Ayúdame a cualificar esta oportunidad: [descripción]"_
- _"El cliente tiene un RFP, te lo paso para que extraigas el BANT+"_

---

## 🚀 Cómo desplegar cualquier agente

### Prerrequisitos 🌸

- [ ] Tenant **Microsoft 365** con licencia de Copilot Studio
- [ ] Acceso a **Copilot Studio** → [aka.ms/copilotstudio](https://aka.ms/copilotstudio)
- [ ] Extensión **Copilot Studio para VS Code** → [instalar aquí](https://marketplace.visualstudio.com/items?itemName=ms-CopilotStudio.vscode-copilotstudio)
- [ ] **VS Code** (versión estable más reciente)
- [ ] **Git** instalado localmente

### Pasos ✨

**1. Clona este repositorio**
```bash
git clone https://github.com/erikacepeda/copilotstudio-samples.git
cd copilotstudio-samples
```

**2. Abre en VS Code**
```bash
code .
```

**3. Crea un nuevo agente en Copilot Studio**
1. Ve a [Copilot Studio](https://aka.ms/copilotstudio) e inicia sesión.
2. Haz clic en **Crear** → **Nuevo agente**.
3. Dale un nombre y completa el asistente de configuración.

**4. Clona tu agente localmente con la extensión**
1. En VS Code, abre el panel de **Copilot Studio** en la barra lateral.
2. Haz clic en **Sign in** y autentica con tu cuenta Microsoft 365.
3. Selecciona el **Environment** donde creaste el agente.
4. Localiza tu agente y haz clic en **Clone** para descargarlo localmente.

**5. Copia los archivos del agente elegido**

Copia la carpeta completa del agente que quieres desplegar en tu carpeta local, reemplazando los archivos existentes:

```
[Nombre del agente]/
├── agent.mcs.yml        ← copiar y reemplazar
├── knowledge/           ← copiar carpeta completa
└── topics/              ← copiar carpeta completa
```

**6. Aplica los cambios desde la extensión**
1. En VS Code, abre el panel de **Copilot Studio**.
2. Haz clic en **Apply Changes** para publicar los cambios en Copilot Studio.
3. Espera la confirmación de que los cambios se aplicaron correctamente.

**7. Prueba en Copilot Studio**
1. Ve a [Copilot Studio](https://aka.ms/copilotstudio) y navega a tu agente.
2. Haz clic en **Test** para abrir el panel de chat de prueba.
3. ¡Empieza a conversar! 🦋

---

## ✨ Personalización

| Qué cambiar | Dónde |
|---|---|
| Instrucciones del agente / persona | `agent.mcs.yml` → `instructions` |
| Fuentes de conocimiento | `knowledge/` — añade o edita archivos `.knowledge.mcs.yml` |
| Topics de conversación | `topics/` — añade o edita archivos `.mcs.yml` |
| Auth y control de acceso | `settings.mcs.yml` |
| Icono del agente | Reemplaza `icon.png` (512×512 PNG recomendado) |
| Modelo de IA | `agent.mcs.yml` → `aISettings.model.modelNameHint` |

---

## 🌺 Sobre la autora

<p align="center">
  <b>Erika Cepeda</b> — Microsoft AI & Copilot Studio enthusiast 🦋<br/>
  Construyendo agentes que hacen la vida más fácil (y más bonita ✨)
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/erikacepeda/">
    <img src="https://img.shields.io/badge/%F0%9F%A6%8B%20Sígueme%20en%20LinkedIn-C865F7?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Erika Cepeda" />
  </a>
</p>

---

## 📄 Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).

---

<p align="center">
  🌸🦋✨ Hecho con amor para la comunidad Microsoft ✨🦋🌸
</p>
