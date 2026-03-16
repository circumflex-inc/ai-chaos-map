# AI Chaos Map (AIカオスマップ) - Specification

## Overview
インタラクティブなAIカオスマップ。ブラウザで動的に閲覧できるSPA。
Firebase Hostingで静的サイトとしてデプロイ。

## Domain
- `ai-chaos-map.circumflex.jp` (Cloud DNS で設定)

## Tech Stack
- Pure HTML + CSS + JavaScript (no framework, no build step)
- Single `index.html` + `style.css` + `app.js` + `data.json`
- Firebase Hosting for deployment

## Design
- ダークモード基調（#0a0a0a背景、ネオンカラーアクセント）
- カテゴリごとに色分け
- レスポンシブ（モバイル対応）
- 日本語UI

## Features
1. カテゴリごとにグリッド/カード表示
2. カテゴリクリックでフィルタリング
3. 各社カードにロゴ（favicon API利用）、名前、簡単な説明、公式リンク
4. 検索バー（リアルタイムフィルタ）
5. カテゴリ全体を俯瞰できるマップビュー

## Categories & Data

### 🧠 基盤モデル (Foundation Models)
- OpenAI (GPT-5, o3) - https://openai.com
- Anthropic (Claude 4) - https://anthropic.com
- Google (Gemini 3) - https://deepmind.google
- Meta (Llama 4) - https://ai.meta.com
- Mistral (Mistral Large, Codestral) - https://mistral.ai
- xAI (Grok 3) - https://x.ai
- DeepSeek (DeepSeek-V3, R1) - https://deepseek.com
- Cohere (Command R+) - https://cohere.com
- AI21 Labs (Jamba) - https://ai21.com
- Alibaba (Qwen 3) - https://qwenlm.github.io

### 🖼️ 画像・動画生成 (Image & Video Generation)
- Midjourney - https://midjourney.com
- OpenAI (DALL-E, GPT-4o image) - https://openai.com
- Stability AI (Stable Diffusion) - https://stability.ai
- Flux (Black Forest Labs) - https://blackforestlabs.ai
- Google (Veo 2, Imagen 3) - https://deepmind.google
- Runway (Gen-3) - https://runwayml.com
- Kling (Kuaishou) - https://klingai.com
- Pika - https://pika.art
- Luma AI (Dream Machine) - https://lumalabs.ai
- Ideogram - https://ideogram.ai

### 💻 コーディングAI (AI Coding)
- GitHub Copilot - https://github.com/features/copilot
- Cursor - https://cursor.com
- OpenAI Codex CLI - https://github.com/openai/codex
- Windsurf (Codeium) - https://windsurf.com
- Devin (Cognition) - https://devin.ai
- Replit Agent - https://replit.com
- Tabnine - https://tabnine.com
- Sourcegraph Cody - https://sourcegraph.com/cody
- Augment Code - https://augmentcode.com
- Claude Code (Anthropic) - https://docs.anthropic.com/en/docs/claude-code

### 🤖 AIエージェント (AI Agents)
- OpenAI Operator - https://openai.com
- Anthropic Claude (Computer Use) - https://anthropic.com
- Google Gemini (Project Mariner) - https://deepmind.google
- Manus AI - https://manus.im
- AutoGPT - https://agpt.co
- CrewAI - https://crewai.com
- LangGraph (LangChain) - https://langchain.com
- Microsoft AutoGen - https://microsoft.github.io/autogen
- OpenClaw - https://openclaw.ai

### 🔍 AI検索 (AI Search)
- Perplexity - https://perplexity.ai
- Google (AI Overviews / Gemini) - https://google.com
- OpenAI SearchGPT - https://openai.com
- You.com - https://you.com
- Exa - https://exa.ai
- Brave Search AI - https://brave.com
- Arc Search - https://arc.net

### 🗣️ 音声・TTS (Voice & Speech)
- ElevenLabs - https://elevenlabs.io
- OpenAI (Whisper, Voice) - https://openai.com
- Google (NotebookLM Audio) - https://notebooklm.google
- Assembly AI - https://assemblyai.com
- Deepgram - https://deepgram.com
- Play.ai - https://play.ai
- Cartesia - https://cartesia.ai
- Sesame (CSM) - https://sesame.com

### 🏢 エンタープライズAI (Enterprise AI)
- Palantir AIP - https://palantir.com
- Scale AI - https://scale.com
- Databricks (Mosaic) - https://databricks.com
- Snowflake Cortex - https://snowflake.com
- Salesforce Einstein - https://salesforce.com
- AWS Bedrock - https://aws.amazon.com/bedrock
- Azure AI - https://azure.microsoft.com/ai
- Google Vertex AI - https://cloud.google.com/vertex-ai

### 🛠️ AIインフラ・チップ (AI Infrastructure)
- NVIDIA (H100, B200) - https://nvidia.com
- AMD (MI300X) - https://amd.com
- Groq (LPU) - https://groq.com
- Cerebras (WSE-3) - https://cerebras.ai
- Google (TPU v6) - https://cloud.google.com/tpu
- Intel (Gaudi 3) - https://intel.com
- AWS (Trainium) - https://aws.amazon.com
- SambaNova - https://sambanova.ai

### 📱 ローカルAI・エッジ (Local & Edge AI)
- Ollama - https://ollama.com
- LM Studio - https://lmstudio.ai
- Apple Intelligence - https://apple.com
- Jan - https://jan.ai
- GPT4All - https://gpt4all.io
- llama.cpp - https://github.com/ggml-org/llama.cpp
- MLX (Apple) - https://github.com/ml-explore/mlx

### 🔌 MCP サーバー (MCP Servers) - Developer Tools
- GitHub MCP - https://github.com/modelcontextprotocol/servers
- Playwright MCP (Browser Automation) - https://github.com/anthropics/playwright-mcp
- PostgreSQL MCP - https://github.com/modelcontextprotocol/servers
- Docker MCP - https://github.com/docker/mcp-server
- Linear MCP - https://github.com/linear/linear-mcp
- Sentry MCP - https://github.com/getsentry/sentry-mcp
- Vercel MCP - https://github.com/vercel/mcp

### 🔌 MCP サーバー (MCP Servers) - Data & Productivity
- Google Drive MCP - https://github.com/modelcontextprotocol/servers
- Google Maps MCP - https://github.com/modelcontextprotocol/servers
- Slack MCP - https://github.com/modelcontextprotocol/servers
- Notion MCP - https://github.com/modelcontextprotocol/servers
- Filesystem MCP - https://github.com/modelcontextprotocol/servers
- Memory MCP (Knowledge Graph) - https://github.com/modelcontextprotocol/servers
- Context7 MCP (Docs) - https://github.com/context7/context7-mcp

### 🔌 MCP プラットフォーム (MCP Platforms)
- Anthropic (MCP Creator) - https://anthropic.com
- OpenAI (MCP Adopter) - https://openai.com
- Cloudflare (MCP Hosting) - https://developers.cloudflare.com
- FastMCP (Registry) - https://fastmcp.me
- Smithery (Registry) - https://smithery.ai
- Glama (Registry) - https://glama.ai

### 🎨 デザインAI (AI Design)
- Figma AI - https://figma.com
- Canva Magic Studio - https://canva.com
- Adobe Firefly - https://adobe.com
- Galileo AI - https://galileo.ai
- Framer AI - https://framer.com
- v0 (Vercel) - https://v0.dev

### 🎵 音楽・オーディオAI (Music & Audio AI)
- Suno - https://suno.com
- Udio - https://udio.com
- AIVA - https://aiva.ai
- Boomy - https://boomy.com

### 🔬 科学・研究AI (Science & Research AI)
- AlphaFold 3 (Google) - https://deepmind.google
- Isomorphic Labs - https://isomorphiclabs.com
- Recursion - https://recursion.com
- Insilico Medicine - https://insilico.com

## File Structure
```
ai-chaos-map/
├── index.html        # Main HTML
├── style.css         # Styles
├── app.js            # Interactive logic
├── data.json         # All company/tool data
├── firebase.json     # Firebase config
├── .firebaserc       # Firebase project config
└── SPEC.md           # This file
```
