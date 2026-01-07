# 🤖 Asistente Virtual CloudNote Pro

Asistente virtual inteligente de soporte técnico construido con React, TypeScript y LangChain. Este proyecto es una **práctica educativa** que simula un sistema de soporte automatizado para CloudNote Pro, una aplicación ficticia de toma de notas.

El asistente utiliza un clasificador híbrido (reglas + LLM) para determinar si las consultas están dentro del dominio de soporte, manteniendo memoria conversacional para respuestas contextualizadas.

---

## ✨ Características

### 🎨 Interfaz de Usuario
- Diseño moderno con gradientes, glassmorphism y animaciones
- **Tema claro/oscuro** con transiciones fluidas
- **Mensajes formateados** con soporte para listas y negritas
- **Auto-scroll** inteligente
- Indicador de "escribiendo..." en tiempo real
- Diseño responsive

### 🧠 Inteligencia Artificial
- **Clasificación híbrida** (reglas + LLM) para filtrar consultas
- **Memoria conversacional** que mantiene el contexto
- Integración con **Groq** (modelo `llama-3.1-8b-instant`)
- Respuestas contextualizadas basadas en el historial
- Manejo inteligente de errores

---

## 🛠 Tecnologías

### Frontend

- **React 18.3** - Biblioteca UI
- **TypeScript 5.5** - Lenguaje tipado
- **Tailwind CSS 3.4** - Framework de estilos
- **Vite** - Build tool
- **Lucide React** - Iconos

### Backend/IA

- **LangChain** - Framework para aplicaciones LLM
- **@langchain/groq** - Integración con Groq
- **Groq Cloud** - Inferencia LLM (llama-3.1-8b-instant)

---

## 🚀 Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/tu-usuario/cloudnote-assistant.git
cd cloudnote-assistant
```

### 2. Instalar dependencias

```bash
npm install
```

### 3. Configurar variables de entorno

Crea un archivo `.env` en la raíz:

```env
VITE_GROQ_API_KEY=tu_api_key_aqui
```

> **Nota:** Obtén tu API key en [console.groq.com](https://console.groq.com/keys)

### 4. Iniciar aplicación

```bash
npm run dev
```

La app estará disponible en `http://localhost:5173`

---

## 📁 Estructura del Proyecto

```
src/
├── components/          # Componentes React
│   ├── chat/           # Componentes del chat
│   └── layout/         # Layout principal
├── context/            # Context API (Tema)
├── services/           # Lógica del asistente
│   ├── assistantService.ts
│   ├── conversationMemory.ts
│   ├── domainFilter.ts
│   └── llmService.ts
├── config/             # Configuración
├── types/              # Tipos TypeScript
└── App.tsx
```

---

## 💡 Uso

**Consultas IN_DOMAIN** (el asistente responde):
- "No puedo sincronizar mis notas"
- "¿Cómo inicio sesión en CloudNote?"
- "¿Cómo comparto una nota?"

**Consultas OUT_OF_DOMAIN** (respuesta automática):
- "¿Qué tiempo hace hoy?"
- "Suma 2 + 2"

---

## 📝 Licencia

MIT License - Este es un proyecto educativo de práctica.

---

**Hecho con ❤️ como proyecto de aprendizaje**