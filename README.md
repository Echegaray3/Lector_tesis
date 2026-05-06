# Clasificador Estado del Arte — Tesis Doctoral

**Investigador:** Juan Diego Espinosa  
**Institución:** UPV CIGIP  
**Tema de tesis:** Arquitecturas de agentes inteligentes basados en LLMs para la orquestación de procesos industriales de producción

## Características

- ⭐ **Destacar papers** — marcar papers importantes con estrella para acceso rápido
- 🏷️ **Traducción de títulos al español** — traducción automática de títulos mediante Claude API
- 📂 **Importar desde Zotero CSV** — importar y deduplicar papers desde exports de Zotero
- 🤖 **Clasificación con IA** — uso de Claude o GPT-4o para clasificación automática
- 💾 **Persistencia local** — todo guardado en localStorage del navegador

## Uso

Accede al clasificador en: https://echegaray3.github.io/estado-del-arte/

## Archivos

- `clasificador_estado_del_arte.html` — herramienta principal (SPA standalone)
- `Estado del Arte.csv` — dataset de 434 papers académicos
- `PROYECTO_GUIA.md` — documentación del proyecto
- `index.html` — redirección a la herramienta principal

## Estructura de datos

Los papers se almacenan en `localStorage` bajo la clave `thesis_db_v2`:

```json
{
  "classified": { "0": { "llm": "No", "rea": "MADRL", ... } },
  "decisions": { "0": { "decision": "keep", "starred": true, ... } },
  "translations": { "0": { "abEs": "...", "tiEs": "..." } }
}
```

## Funcionalidades principales

### ⭐ Destacar Papers
- Botón ★ en cada fila para marcar como favorito
- Filtro "★ Solo destacados" en la barra lateral
- Persiste en localStorage

### 🏷️ Traducción de Títulos
- Botón "🏷 Títulos ES" en el header
- Traduce títulos al español en lotes de 20
- Se muestra bajo el título inglés en la tabla

### 📂 Importar Zotero CSV
- Botón "📂 Zotero CSV" para cargar archivos
- Deduplicación inteligente por DOI y título
- Papers importados usan IDs a partir de 10000

## API

Soporta Anthropic Claude y OpenAI GPT-4o. Configurar la API key en el header.

