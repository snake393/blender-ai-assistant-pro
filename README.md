[![Download](docs/download-button.svg)][download-url]

# blender-ai-assistant-pro
**Talk to Blender — inspect, build and edit scenes through conversation.**

A Blender addon with a built-in AI assistant and a local Model Context Protocol (MCP) server: describe the change in plain language and it reads your scene, creates objects, edits materials and carries out multi-step tasks under your approval. A companion chat panel keeps the conversation, previews and tasks next to your viewport, while external MCP clients such as OpenCode connect to the same tools through an authenticated local endpoint.

[download-url]: https://github.com/snake393/blender-ai-assistant-pro/

![License](https://img.shields.io/badge/license-MIT-blue) ![Language](https://img.shields.io/badge/language-Python-3776AB?logo=python&logoColor=white) ![Platform](https://img.shields.io/badge/platform-Windows_x64-0078D6?logo=windows&logoColor=white) ![MCP](https://img.shields.io/badge/Model_Context_Protocol-server-8A2BE2) ![Blender](https://img.shields.io/badge/Blender-4.2%2B-E87D0D?logo=blender&logoColor=white) ![Release](https://img.shields.io/badge/release-1.0.0-98D85B)

## 🤔 Why
Repeating the same menus and clicks in Blender — renaming, arranging, re-texturing — eats the hours you wanted to spend designing. This addon lets you say what you want instead: the assistant inspects the scene first, proposes concrete operations and applies them step by step with your approval. Iteration takes messages rather than menu paths, and you keep working in Blender the whole time.

## ⚖️ Without / With

| Without | With |
|---|---|
| Scene context gathered by hand in the outliner | Scene and object inspection gives the assistant context before it acts |
| Object, material and layout edits repeated manually | Multi-step briefs executed as supervised scene operations |
| Custom glue code to link AI tools to Blender | Built-in MCP server with an authenticated local endpoint for OpenCode and other clients |
| Locked to a single AI vendor | OpenAI, Anthropic Claude, Google Gemini, OpenRouter, OpenCode Zen, Ollama or custom endpoints |

## 🚀 Quick Start
1. Get the latest Windows x64 bundle from the [Download][download-url] page.
2. Download mcp-for-blender-pro.zip from Releases.
3. In Blender, open Edit → Preferences → Get Extensions → menu → Install from Disk.
4. Select the ZIP, enable mcp-for-blender-pro, then open 3D Viewport → N → MCP Pro.
5. Choose a provider, add your connection details and select a model.
6. Send a message in Blender or click Open Studio Window.

> **Note:** the bundle targets Windows x64 with Blender 4.2 or later. Keep Blender open while you use the chat panel or an external MCP client.

## ✨ Features
- **Inspect** scenes and objects before any change, so every suggestion starts from real context.
- **Create** primitives, lights and cameras; move, duplicate, parent and delete objects; assign materials.
- **Capture** viewport screenshots and let image-capable models review the result visually.
- **Search** Poly Haven, Sketchfab and Poly Pizza libraries and import an asset after your approval.
- **Run** a single assistant for quick edits or a manager–worker–reviewer team for structured jobs.
- **Connect** OpenCode and other MCP clients to 21 scene tools over an authenticated local endpoint.
- **Switch** the main interface between English, German, French, Spanish and Chinese.

## 🧠 How it works
The addon runs a local MCP server that exposes 21 supervised scene tools — inspection, creation, editing, screenshots, bpy API lookups and scene export — plus a chat panel that talks to it directly. Every mutating step passes approval, cancellation and named undo, and external clients such as OpenCode reach the same tools through an authenticated Streamable HTTP endpoint.

## 🧪 Usage
> Inspect this scene and explain its object structure before making any changes.

> Create a simple product-display scene with a pedestal, a camera and three lights. Give the pedestal a matte blue material.

> Duplicate the selected object into a neatly spaced row of five and show the viewport.

## 🔧 Configuration

| Setting | Options | Notes |
|---|---|---|
| Provider | OpenAI, Anthropic Claude, Google Gemini, OpenRouter, OpenCode Zen, Ollama, custom API | Custom endpoints speak OpenAI Chat Completions, Anthropic Messages or Ollama protocols |
| Model | any tool-calling model from the provider catalog | Image-capable models can also read viewport screenshots |
| Saved connections | multiple per provider, each with its own key | Keep work and personal keys separate |
| Mode | single assistant or team chain | Teams split work into manager, worker and reviewer roles; tasks run sequentially |
| Interface language | English, German, French, Spanish, Chinese | Applies to the main interface |
| Safety | approvals, cancellation after the current step, named undo steps | Python tool validation filters disallowed operations; it is not a security sandbox |

## 🩺 Troubleshooting / FAQ
**The panel does not appear in Blender.** Confirm Blender 4.2+ on Windows x64, then reinstall via *Get Extensions → Install from Disk* and enable the addon in preferences.

**The assistant replies but does nothing.** Pick a model with tool-calling support — plain chat models can describe steps but cannot drive scene tools.

**Screenshots come back ignored.** Viewport snapshots need an image-capable model.

**A team task is stuck.** A blocked task gets a single correction attempt; a second failed review stops the workflow, and the task board shows what was returned.

**Where are my keys stored?** In your user settings on this machine. Chat history lasts for the current session, and the panel authenticates every request to Blender locally.

> **Tip:** launch OpenCode Portable straight from the sidebar — the Blender connection arrives configured, and OpenCode handles its own provider sign-in and model selection.

## 🤝 Contributing
Issues and pull requests are welcome — bug reports, tool ideas and documentation fixes all help the project grow. If this addon saved you time, please give it a star ⭐ so other Blender artists can discover it.

## Keywords
blender mcp server · mcp for blender · blender ai assistant · blender ai addon · ai for blender · blender copilot · blender chatgpt · blender claude · blender openai · blender gemini · blender ollama · blender llm · blender agents · multi-agent blender · blender automation · blender scripting · blender python · bpy api · blender api · 3d modeling · 3d automation · 3d workflow · scene generation · ai materials · ai textures · viewport screenshot · blender addon · blender extension · blender plugin · model context protocol · mcp integration · opencode blender · ai tools for blender · chat in blender · blender workflow · Краш · Кринж · Имба · Чиллить · Вайб · Рофл · Стэнить · Тильт · Скуф · Альтушка · Пикми · Нормис · NPC · Войс · Шеймить · Фармить · Шипперить · Бэнгер · Жиза · Чиназес

## License
Released under the [MIT](./LICENSE) license.
