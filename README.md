# Open WebUI 👋

![GitHub stars](https://img.shields.io/github/stars/open-webui/open-webui?style=social)
![GitHub forks](https://img.shields.io/github/forks/open-webui/open-webui?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/open-webui/open-webui?style=social)
![GitHub repo size](https://img.shields.io/github/repo-size/open-webui/open-webui)
![GitHub language count](https://img.shields.io/github/languages/count/open-webui/open-webui)
![GitHub top language](https://img.shields.io/github/languages/top/open-webui/open-webui)
![GitHub last commit](https://img.shields.io/github/last-commit/open-webui/open-webui?color=red)
![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Follama-webui%2Follama-wbui&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)
[![Discord](https://img.shields.io/badge/Discord-Open_WebUI-blue?logo=discord&logoColor=white)](https://discord.gg/5rJgQTnV4s)
[![](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/tjbck)

Open WebUI is an [extensible](https://github.com/open-webui/pipelines), feature-rich, and user-friendly self-hosted WebUI designed to operate entirely offline. It supports various LLM runners, including Ollama and OpenAI-compatible APIs. For more information, be sure to check out our [Open WebUI Documentation](https://docs.openwebui.com/).

![Open WebUI Demo](./demo.gif)

## Key Features of Open WebUI ⭐

- 🚀 **Effortless Setup**: Install seamlessly using Docker or Kubernetes (kubectl, kustomize or helm) for a hassle-free experience with support for both `:ollama` and `:cuda` tagged images.

- 🤝 **Ollama/OpenAI API Integration**: Effortlessly integrate OpenAI-compatible APIs for versatile conversations alongside Ollama models. Customize the OpenAI API URL to link with **LMStudio, GroqCloud, Mistral, OpenRouter, and more**.

- 🧩 **Pipelines, Open WebUI Plugin Support**: Seamlessly integrate custom logic and Python libraries into Open WebUI using [Pipelines Plugin Framework](https://github.com/open-webui/pipelines). Launch your Pipelines instance, set the OpenAI URL to the Pipelines URL, and explore endless possibilities. [Examples](https://github.com/open-webui/pipelines/tree/main/examples) include **Function Calling**, User **Rate Limiting** to control access, **Usage Monitoring** with tools like Langfuse, **Live Translation with LibreTranslate** for multilingual support, **Toxic Message Filtering** and much more.

- 📱 **Responsive Design**: Enjoy a seamless experience across Desktop PC, Laptop, and Mobile devices.

- 📱 **Progressive Web App (PWA) for Mobile**: Enjoy a native app-like experience on your mobile device with our PWA, providing offline access on localhost and a seamless user interface.

- ✒️🔢 **Full Markdown and LaTeX Support**: Elevate your LLM experience with comprehensive Markdown and LaTeX capabilities for enriched interaction.

- 🎤📹 **Hands-Free Voice/Video Call**: Experience seamless communication with integrated hands-free voice and video call features, allowing for a more dynamic and interactive chat environment.

- 🛠️ **Model Builder**: Easily create Ollama models via the Web UI. Create and add custom characters/agents, customize chat elements, and import models effortlessly through [Open WebUI Community](https://openwebui.com/) integration.

- 🐍 **Native Python Function Calling Tool**: Enhance your LLMs with built-in code editor support in the tools workspace. Bring Your Own Function (BYOF) by simply adding your pure Python functions, enabling seamless integration with LLMs.

- 📚 **Local RAG Integration**: Dive into the future of chat interactions with groundbreaking Retrieval Augmented Generation (RAG) support. This feature seamlessly integrates document interactions into your chat experience. You can load documents directly into the chat or add files to your document library, effortlessly accessing them using the `#` command before a query.

- 🔍 **Web Search for RAG**: Perform web searches using providers like `SearXNG`, `Google PSE`, `Brave Search`, `serpstack`, `serper`, `Serply`, `DuckDuckGo`, `TavilySearch`, `SearchApi` and `Bing` and inject the results directly into your chat experience.

- 🌐 **Web Browsing Capability**: Seamlessly integrate websites into your chat experience using the `#` command followed by a URL. This feature allows you to incorporate web content directly into your conversations, enhancing the richness and depth of your interactions.

- 🎨 **Image Generation Integration**: Seamlessly incorporate image generation capabilities using options such as AUTOMATIC1111 API or ComfyUI (local), and OpenAI's DALL-E (external), enriching your chat experience with dynamic visual content.

- ⚙️ **Many Models Conversations**: Effortlessly engage with various models simultaneously, harnessing their unique strengths for optimal responses. Enhance your experience by leveraging a diverse set of models in parallel.

- 🔐 **Role-Based Access Control (RBAC)**: Ensure secure access with restricted permissions; only authorized individuals can access your Ollama, and exclusive model creation/pulling rights are reserved for administrators.

- 🌐🌍 **Multilingual Support**: Experience Open WebUI in your preferred language with our internationalization (i18n) support. Join us in expanding our supported languages! We're actively seeking contributors!

- 🌟 **Continuous Updates**: We are committed to improving Open WebUI with regular updates, fixes, and new features.

Want to learn more about Open WebUI's features? Check out our [Open WebUI documentation](https://docs.openwebui.com/features) for a comprehensive overview!

## 🔗 Also Check Out Open WebUI Community!

Don't forget to explore our sibling project, [Open WebUI Community](https://openwebui.com/), where you can discover, download, and explore customized Modelfiles. Open WebUI Community offers a wide range of exciting possibilities for enhancing your chat interactions with Open WebUI! 🚀

## How to Install 🚀

### Installation via Python pip 🐍

Open WebUI can be installed using pip, the Python package installer. Before proceeding, ensure you're using **Python 3.11** to avoid compatibility issues.

1. **Install Open WebUI**:
   Open your terminal and run the following command to install Open WebUI:

   ```bash
   pip install open-webui
   ```

2. **Running Open WebUI**:
   After installation, you can start Open WebUI by executing:

   ```bash
   open-webui serve
   ```

This will start the Open WebUI server, which you can access at [http://localhost:8080](http://localhost:8080)

### Quick Start with Docker 🐳

> [!NOTE]  
> Please note that for certain Docker environments, additional configurations might be needed. If you encounter any connection issues, our detailed guide on [Open WebUI Documentation](https://docs.openwebui.com/) is ready to assist you.

> [!WARNING]
> When using Docker to install Open WebUI, make sure to include the `-v open-webui:/app/backend/data` in your Docker command. This step is crucial as it ensures your database is properly mounted and prevents any loss of data.

> [!TIP]  
> If you wish to utilize Open WebUI with Ollama included or CUDA acceleration, we recommend utilizing our official images tagged with either `:cuda` or `:ollama`. To enable CUDA, you must install the [Nvidia CUDA container toolkit](https://docs.nvidia.com/dgx/nvidia-container-runtime-upgrade/) on your Linux/WSL system.

### Installation with Default Configuration

- **If Ollama is on your computer**, use this command:

  ```bash
  docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
  ```

- **If Ollama is on a Different Server**, use this command:

  To connect to Ollama on another server, change the `OLLAMA_BASE_URL` to the server's URL:

  ```bash
  docker run -d -p 3000:8080 -e OLLAMA_BASE_URL=https://example.com -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
  ```

- **To run Open WebUI with Nvidia GPU support**, use this command:

  ```bash
  docker run -d -p 3000:8080 --gpus all --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:cuda
  ```

### Installation for OpenAI API Usage Only

- **If you're only using OpenAI API**, use this command:

  ```bash
  docker run -d -p 3000:8080 -e OPENAI_API_KEY=your_secret_key -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
  ```

### Installing Open WebUI with Bundled Ollama Support

This installation method uses a single container image that bundles Open WebUI with Ollama, allowing for a streamlined setup via a single command. Choose the appropriate command based on your hardware setup:

- **With GPU Support**:
  Utilize GPU resources by running the following command:

  ```bash
  docker run -d -p 3000:8080 --gpus=all -v ollama:/root/.ollama -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:ollama
  ```

- **For CPU Only**:
  If you're not using a GPU, use this command instead:

  ```bash
  docker run -d -p 3000:8080 -v ollama:/root/.ollama -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:ollama
  ```

Both commands facilitate a built-in, hassle-free installation of both Open WebUI and Ollama, ensuring that you can get everything up and running swiftly.

After installation, you can access Open WebUI at [http://localhost:3000](http://localhost:3000). Enjoy! 😄

### Other Installation Methods

We offer various installation alternatives, including non-Docker native installation methods, Docker Compose, Kustomize, and Helm. Visit our [Open WebUI Documentation](https://docs.openwebui.com/getting-started/) or join our [Discord community](https://discord.gg/5rJgQTnV4s) for comprehensive guidance.

### Troubleshooting

Encountering connection issues? Our [Open WebUI Documentation](https://docs.openwebui.com/troubleshooting/) has got you covered. For further assistance and to join our vibrant community, visit the [Open WebUI Discord](https://discord.gg/5rJgQTnV4s).

#### Open WebUI: Server Connection Error

If you're experiencing connection issues, it’s often due to the WebUI docker container not being able to reach the Ollama server at 127.0.0.1:11434 (host.docker.internal:11434) inside the container . Use the `--network=host` flag in your docker command to resolve this. Note that the port changes from 3000 to 8080, resulting in the link: `http://localhost:8080`.

**Example Docker Command**:

```bash
docker run -d --network=host -v open-webui:/app/backend/data -e OLLAMA_BASE_URL=http://127.0.0.1:11434 --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

### Keeping Your Docker Installation Up-to-Date

In case you want to update your local Docker installation to the latest version, you can do it with [Watchtower](https://containrrr.dev/watchtower/):

```bash
docker run --rm --volume /var/run/docker.sock:/var/run/docker.sock containrrr/watchtower --run-once open-webui
```

In the last part of the command, replace `open-webui` with your container name if it is different.

Check our Migration Guide available in our [Open WebUI Documentation](https://docs.openwebui.com/tutorials/migration/).

### Using the Dev Branch 🌙

> [!WARNING]
> The `:dev` branch contains the latest unstable features and changes. Use it at your own risk as it may have bugs or incomplete features.

If you want to try out the latest bleeding-edge features and are okay with occasional instability, you can use the `:dev` tag like this:

```bash
docker run -d -p 3000:8080 -v open-webui:/app/backend/data --name open-webui --add-host=host.docker.internal:host-gateway --restart always ghcr.io/open-webui/open-webui:dev
```

## What's Next? 🌟

Discover upcoming features on our roadmap in the [Open WebUI Documentation](https://docs.openwebui.com/roadmap/).

## License 📜

This project is licensed under the [MIT License](LICENSE) - see the [LICENSE](LICENSE) file for details. 📄

## Support 💬

If you have any questions, suggestions, or need assistance, please open an issue or join our
[Open WebUI Discord community](https://discord.gg/5rJgQTnV4s) to connect with us! 🤝

## Star History

<a href="https://star-history.com/#open-webui/open-webui&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=open-webui/open-webui&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=open-webui/open-webui&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=open-webui/open-webui&type=Date" />
  </picture>
</a>

---

Created by [Timothy Jaeryang Baek](https://github.com/tjbck) - Let's make Open WebUI even more amazing together! 💪


```
open-webui
├─ .dockerignore
├─ .eslintignore
├─ .eslintrc.cjs
├─ .git
│  ├─ HEAD
│  ├─ config
│  ├─ description
│  ├─ hooks
│  │  ├─ applypatch-msg.sample
│  │  ├─ commit-msg.sample
│  │  ├─ fsmonitor-watchman.sample
│  │  ├─ post-update.sample
│  │  ├─ pre-applypatch.sample
│  │  ├─ pre-commit.sample
│  │  ├─ pre-merge-commit.sample
│  │  ├─ pre-push.sample
│  │  ├─ pre-rebase.sample
│  │  ├─ pre-receive.sample
│  │  ├─ prepare-commit-msg.sample
│  │  └─ update.sample
│  ├─ index
│  ├─ info
│  │  └─ exclude
│  ├─ objects
│  │  ├─ info
│  │  └─ pack
│  │     ├─ pack-f060fb32a741711fd4737bec41e51f5b8adf2dc4.idx
│  │     └─ pack-f060fb32a741711fd4737bec41e51f5b8adf2dc4.pack
│  ├─ packed-refs
│  └─ refs
│     ├─ heads
│     │  ├─ dev
│     │  └─ main
│     ├─ remotes
│     │  └─ origin
│     │     └─ HEAD
│     └─ tags
├─ .gitattributes
├─ .github
│  ├─ FUNDING.yml
│  ├─ ISSUE_TEMPLATE
│  │  ├─ bug_report.md
│  │  └─ feature_request.md
│  ├─ dependabot.yml
│  ├─ pull_request_template.md
│  └─ workflows
│     ├─ build-release.yml
│     ├─ deploy-to-hf-spaces.yml
│     ├─ docker-build.yaml
│     ├─ format-backend.yaml
│     ├─ format-build-frontend.yaml
│     ├─ integration-test.yml
│     ├─ lint-backend.disabled
│     ├─ lint-frontend.disabled
│     └─ release-pypi.yml
├─ .gitignore
├─ .prettierignore
├─ .prettierrc
├─ CHANGELOG.md
├─ CODE_OF_CONDUCT.md
├─ Caddyfile.localhost
├─ Dockerfile
├─ INSTALLATION.md
├─ LICENSE
├─ Makefile
├─ README.md
├─ TROUBLESHOOTING.md
├─ backend
│  ├─ .dockerignore
│  ├─ .gitignore
│  ├─ data
│  │  └─ readme.txt
│  ├─ dev.sh
│  ├─ open_webui
│  │  ├─ __init__.py
│  │  ├─ alembic.ini
│  │  ├─ apps
│  │  │  ├─ audio
│  │  │  │  └─ main.py
│  │  │  ├─ images
│  │  │  │  ├─ main.py
│  │  │  │  └─ utils
│  │  │  │     └─ comfyui.py
│  │  │  ├─ ollama
│  │  │  │  └─ main.py
│  │  │  ├─ openai
│  │  │  │  └─ main.py
│  │  │  ├─ retrieval
│  │  │  │  ├─ loaders
│  │  │  │  │  ├─ github_loader.py
│  │  │  │  │  └─ main.py
│  │  │  │  ├─ main.py
│  │  │  │  ├─ models
│  │  │  │  │  └─ colbert.py
│  │  │  │  ├─ utils.py
│  │  │  │  ├─ vector
│  │  │  │  │  ├─ connector.py
│  │  │  │  │  ├─ dbs
│  │  │  │  │  │  ├─ chroma.py
│  │  │  │  │  │  ├─ milvus.py
│  │  │  │  │  │  ├─ opensearch.py
│  │  │  │  │  │  ├─ pgvector.py
│  │  │  │  │  │  └─ qdrant.py
│  │  │  │  │  └─ main.py
│  │  │  │  └─ web
│  │  │  │     ├─ bing.py
│  │  │  │     ├─ brave.py
│  │  │  │     ├─ duckduckgo.py
│  │  │  │     ├─ google_pse.py
│  │  │  │     ├─ jina_search.py
│  │  │  │     ├─ main.py
│  │  │  │     ├─ searchapi.py
│  │  │  │     ├─ searxng.py
│  │  │  │     ├─ serper.py
│  │  │  │     ├─ serply.py
│  │  │  │     ├─ serpstack.py
│  │  │  │     ├─ tavily.py
│  │  │  │     ├─ testdata
│  │  │  │     │  ├─ bing.json
│  │  │  │     │  ├─ brave.json
│  │  │  │     │  ├─ google_pse.json
│  │  │  │     │  ├─ searchapi.json
│  │  │  │     │  ├─ searxng.json
│  │  │  │     │  ├─ serper.json
│  │  │  │     │  ├─ serply.json
│  │  │  │     │  └─ serpstack.json
│  │  │  │     └─ utils.py
│  │  │  ├─ socket
│  │  │  │  ├─ main.py
│  │  │  │  └─ utils.py
│  │  │  └─ webui
│  │  │     ├─ internal
│  │  │     │  ├─ db.py
│  │  │     │  ├─ migrations
│  │  │     │  │  ├─ 001_initial_schema.py
│  │  │     │  │  ├─ 002_add_local_sharing.py
│  │  │     │  │  ├─ 003_add_auth_api_key.py
│  │  │     │  │  ├─ 004_add_archived.py
│  │  │     │  │  ├─ 005_add_updated_at.py
│  │  │     │  │  ├─ 006_migrate_timestamps_and_charfields.py
│  │  │     │  │  ├─ 007_add_user_last_active_at.py
│  │  │     │  │  ├─ 008_add_memory.py
│  │  │     │  │  ├─ 009_add_models.py
│  │  │     │  │  ├─ 010_migrate_modelfiles_to_models.py
│  │  │     │  │  ├─ 011_add_user_settings.py
│  │  │     │  │  ├─ 012_add_tools.py
│  │  │     │  │  ├─ 013_add_user_info.py
│  │  │     │  │  ├─ 014_add_files.py
│  │  │     │  │  ├─ 015_add_functions.py
│  │  │     │  │  ├─ 016_add_valves_and_is_active.py
│  │  │     │  │  ├─ 017_add_user_oauth_sub.py
│  │  │     │  │  └─ 018_add_function_is_global.py
│  │  │     │  └─ wrappers.py
│  │  │     ├─ main.py
│  │  │     ├─ models
│  │  │     │  ├─ auths.py
│  │  │     │  ├─ chats.py
│  │  │     │  ├─ feedbacks.py
│  │  │     │  ├─ files.py
│  │  │     │  ├─ folders.py
│  │  │     │  ├─ functions.py
│  │  │     │  ├─ groups.py
│  │  │     │  ├─ knowledge.py
│  │  │     │  ├─ memories.py
│  │  │     │  ├─ models.py
│  │  │     │  ├─ prompts.py
│  │  │     │  ├─ secrets.py
│  │  │     │  ├─ tags.py
│  │  │     │  ├─ tools.py
│  │  │     │  └─ users.py
│  │  │     └─ utils.py
│  │  ├─ config.py
│  │  ├─ constants.py
│  │  ├─ data
│  │  │  └─ readme.txt
│  │  ├─ env.py
│  │  ├─ main.py
│  │  ├─ migrations
│  │  │  ├─ README
│  │  │  ├─ env.py
│  │  │  ├─ script.py.mako
│  │  │  ├─ util.py
│  │  │  └─ versions
│  │  │     ├─ 1af9b942657b_migrate_tags.py
│  │  │     ├─ 242a2047eae0_update_chat_table.py
│  │  │     ├─ 3ab32c4b8f59_update_tags.py
│  │  │     ├─ 4ace53fd72c8_update_folder_table_datetime.py
│  │  │     ├─ 6a39f3d8e55c_add_knowledge_table.py
│  │  │     ├─ 7e5b5dc7342b_init.py
│  │  │     ├─ 922e7a387820_add_group_table.py
│  │  │     ├─ af906e964978_add_feedback_table.py
│  │  │     ├─ c0fbf31ca0db_update_file_table.py
│  │  │     ├─ c29facfe716b_update_file_table_path.py
│  │  │     ├─ c69f45358db4_add_folder_table.py
│  │  │     └─ ca81bd47c050_add_config_table.py
│  │  ├─ static
│  │  │  ├─ assets
│  │  │  │  └─ pdf-style.css
│  │  │  ├─ favicon.png
│  │  │  ├─ fonts
│  │  │  │  ├─ NotoSans-Bold.ttf
│  │  │  │  ├─ NotoSans-Italic.ttf
│  │  │  │  ├─ NotoSans-Regular.ttf
│  │  │  │  ├─ NotoSans-Variable.ttf
│  │  │  │  ├─ NotoSansJP-Regular.ttf
│  │  │  │  ├─ NotoSansJP-Variable.ttf
│  │  │  │  ├─ NotoSansKR-Regular.ttf
│  │  │  │  ├─ NotoSansKR-Variable.ttf
│  │  │  │  ├─ NotoSansSC-Regular.ttf
│  │  │  │  └─ NotoSansSC-Variable.ttf
│  │  │  ├─ logo.png
│  │  │  ├─ splash.png
│  │  │  └─ user-import.csv
│  │  ├─ storage
│  │  │  └─ provider.py
│  │  ├─ test
│  │  │  ├─ __init__.py
│  │  │  ├─ apps
│  │  │  │  └─ webui
│  │  │  └─ util
│  │  │     ├─ abstract_integration_test.py
│  │  │     └─ mock_user.py
│  │  └─ utils
│  │     ├─ access_control.py
│  │     ├─ logo.png
│  │     ├─ misc.py
│  │     ├─ oauth.py
│  │     ├─ payload.py
│  │     ├─ pdf_generator.py
│  │     ├─ response.py
│  │     ├─ schemas.py
│  │     ├─ security_headers.py
│  │     ├─ task.py
│  │     ├─ tools.py
│  │     ├─ utils.py
│  │     └─ webhook.py
│  ├─ requirements.txt
│  ├─ start.sh
│  └─ start_windows.bat
├─ confirm_remove.sh
├─ cypress
│  ├─ data
│  │  └─ example-doc.txt
│  ├─ e2e
│  │  ├─ chat.cy.ts
│  │  ├─ documents.cy.ts
│  │  ├─ registration.cy.ts
│  │  └─ settings.cy.ts
│  ├─ support
│  │  ├─ e2e.ts
│  │  └─ index.d.ts
│  └─ tsconfig.json
├─ cypress.config.ts
├─ demo.gif
├─ docker-compose.a1111-test.yaml
├─ docker-compose.amdgpu.yaml
├─ docker-compose.api.yaml
├─ docker-compose.data.yaml
├─ docker-compose.gpu.yaml
├─ docker-compose.yaml
├─ docs
│  ├─ CONTRIBUTING.md
│  ├─ README.md
│  ├─ SECURITY.md
│  └─ apache.md
├─ hatch_build.py
├─ i18next-parser.config.ts
├─ kubernetes
│  ├─ helm
│  │  └─ README.md
│  └─ manifest
│     ├─ base
│     │  ├─ kustomization.yaml
│     │  ├─ ollama-service.yaml
│     │  ├─ ollama-statefulset.yaml
│     │  ├─ open-webui.yaml
│     │  ├─ webui-deployment.yaml
│     │  ├─ webui-ingress.yaml
│     │  ├─ webui-pvc.yaml
│     │  └─ webui-service.yaml
│     └─ gpu
│        ├─ kustomization.yaml
│        └─ ollama-statefulset-gpu.yaml
├─ package-lock.json
├─ package.json
├─ postcss.config.js
├─ pyproject.toml
├─ run-compose.sh
├─ run-ollama-docker.sh
├─ run.sh
├─ scripts
│  └─ prepare-pyodide.js
├─ src
│  ├─ app.css
│  ├─ app.d.ts
│  ├─ app.html
│  ├─ lib
│  │  ├─ apis
│  │  │  ├─ audio
│  │  │  │  └─ index.ts
│  │  │  ├─ auths
│  │  │  │  └─ index.ts
│  │  │  ├─ chats
│  │  │  │  └─ index.ts
│  │  │  ├─ configs
│  │  │  │  └─ index.ts
│  │  │  ├─ evaluations
│  │  │  │  └─ index.ts
│  │  │  ├─ files
│  │  │  │  └─ index.ts
│  │  │  ├─ folders
│  │  │  │  └─ index.ts
│  │  │  ├─ functions
│  │  │  │  └─ index.ts
│  │  │  ├─ groups
│  │  │  │  └─ index.ts
│  │  │  ├─ images
│  │  │  │  └─ index.ts
│  │  │  ├─ index.ts
│  │  │  ├─ knowledge
│  │  │  │  └─ index.ts
│  │  │  ├─ memories
│  │  │  │  └─ index.ts
│  │  │  ├─ models
│  │  │  │  └─ index.ts
│  │  │  ├─ ollama
│  │  │  │  └─ index.ts
│  │  │  ├─ openai
│  │  │  │  └─ index.ts
│  │  │  ├─ prompts
│  │  │  │  └─ index.ts
│  │  │  ├─ retrieval
│  │  │  │  └─ index.ts
│  │  │  ├─ streaming
│  │  │  │  └─ index.ts
│  │  │  ├─ tools
│  │  │  │  └─ index.ts
│  │  │  ├─ users
│  │  │  │  └─ index.ts
│  │  │  └─ utils
│  │  │     └─ index.ts
│  │  ├─ components
│  │  │  ├─ AddFilesPlaceholder.svelte
│  │  │  ├─ ChangelogModal.svelte
│  │  │  ├─ OnBoarding.svelte
│  │  │  ├─ admin
│  │  │  │  ├─ Evaluations
│  │  │  │  │  ├─ FeedbackMenu.svelte
│  │  │  │  │  ├─ Feedbacks.svelte
│  │  │  │  │  └─ Leaderboard.svelte
│  │  │  │  ├─ Evaluations.svelte
│  │  │  │  ├─ Functions
│  │  │  │  │  ├─ FunctionEditor.svelte
│  │  │  │  │  └─ FunctionMenu.svelte
│  │  │  │  ├─ Functions.svelte
│  │  │  │  ├─ Settings
│  │  │  │  │  ├─ Audio.svelte
│  │  │  │  │  ├─ Connections
│  │  │  │  │  │  ├─ AddConnectionModal.svelte
│  │  │  │  │  │  ├─ ManageOllamaModal.svelte
│  │  │  │  │  │  ├─ OllamaConnection.svelte
│  │  │  │  │  │  └─ OpenAIConnection.svelte
│  │  │  │  │  ├─ Connections.svelte
│  │  │  │  │  ├─ Database.svelte
│  │  │  │  │  ├─ Documents.svelte
│  │  │  │  │  ├─ Evaluations
│  │  │  │  │  │  ├─ ArenaModelModal.svelte
│  │  │  │  │  │  └─ Model.svelte
│  │  │  │  │  ├─ Evaluations.svelte
│  │  │  │  │  ├─ General.svelte
│  │  │  │  │  ├─ Images.svelte
│  │  │  │  │  ├─ Interface.svelte
│  │  │  │  │  ├─ Models.svelte
│  │  │  │  │  ├─ Pipelines.svelte
│  │  │  │  │  └─ WebSearch.svelte
│  │  │  │  ├─ Settings.svelte
│  │  │  │  ├─ Users
│  │  │  │  │  ├─ Groups
│  │  │  │  │  │  ├─ AddGroupModal.svelte
│  │  │  │  │  │  ├─ Display.svelte
│  │  │  │  │  │  ├─ EditGroupModal.svelte
│  │  │  │  │  │  ├─ GroupItem.svelte
│  │  │  │  │  │  ├─ Permissions.svelte
│  │  │  │  │  │  └─ Users.svelte
│  │  │  │  │  ├─ Groups.svelte
│  │  │  │  │  ├─ UserList
│  │  │  │  │  │  ├─ AddUserModal.svelte
│  │  │  │  │  │  ├─ EditUserModal.svelte
│  │  │  │  │  │  └─ UserChatsModal.svelte
│  │  │  │  │  └─ UserList.svelte
│  │  │  │  └─ Users.svelte
│  │  │  ├─ chat
│  │  │  │  ├─ Artifacts.svelte
│  │  │  │  ├─ Chat.svelte
│  │  │  │  ├─ ChatControls.svelte
│  │  │  │  ├─ ChatPlaceholder.svelte
│  │  │  │  ├─ Controls
│  │  │  │  │  ├─ Controls.svelte
│  │  │  │  │  └─ Valves.svelte
│  │  │  │  ├─ MessageInput
│  │  │  │  │  ├─ CallOverlay
│  │  │  │  │  │  └─ VideoInputMenu.svelte
│  │  │  │  │  ├─ CallOverlay.svelte
│  │  │  │  │  ├─ Commands
│  │  │  │  │  │  ├─ Knowledge.svelte
│  │  │  │  │  │  ├─ Models.svelte
│  │  │  │  │  │  └─ Prompts.svelte
│  │  │  │  │  ├─ Commands.svelte
│  │  │  │  │  ├─ FilesOverlay.svelte
│  │  │  │  │  ├─ InputMenu.svelte
│  │  │  │  │  └─ VoiceRecording.svelte
│  │  │  │  ├─ MessageInput.svelte
│  │  │  │  ├─ Messages
│  │  │  │  │  ├─ Citations.svelte
│  │  │  │  │  ├─ CitationsModal.svelte
│  │  │  │  │  ├─ CodeBlock.svelte
│  │  │  │  │  ├─ CodeExecutionModal.svelte
│  │  │  │  │  ├─ CodeExecutions.svelte
│  │  │  │  │  ├─ ContentRenderer.svelte
│  │  │  │  │  ├─ Error.svelte
│  │  │  │  │  ├─ Markdown
│  │  │  │  │  │  ├─ KatexRenderer.svelte
│  │  │  │  │  │  ├─ MarkdownInlineTokens.svelte
│  │  │  │  │  │  └─ MarkdownTokens.svelte
│  │  │  │  │  ├─ Markdown.svelte
│  │  │  │  │  ├─ Message.svelte
│  │  │  │  │  ├─ MultiResponseMessages.svelte
│  │  │  │  │  ├─ Name.svelte
│  │  │  │  │  ├─ ProfileImage.svelte
│  │  │  │  │  ├─ RateComment.svelte
│  │  │  │  │  ├─ ResponseMessage
│  │  │  │  │  │  └─ WebSearchResults.svelte
│  │  │  │  │  ├─ ResponseMessage.svelte
│  │  │  │  │  ├─ Skeleton.svelte
│  │  │  │  │  └─ UserMessage.svelte
│  │  │  │  ├─ Messages.svelte
│  │  │  │  ├─ ModelSelector
│  │  │  │  │  └─ Selector.svelte
│  │  │  │  ├─ ModelSelector.svelte
│  │  │  │  ├─ Overview
│  │  │  │  │  ├─ Flow.svelte
│  │  │  │  │  └─ Node.svelte
│  │  │  │  ├─ Overview.svelte
│  │  │  │  ├─ Placeholder.svelte
│  │  │  │  ├─ Settings
│  │  │  │  │  ├─ Account
│  │  │  │  │  │  └─ UpdatePassword.svelte
│  │  │  │  │  ├─ Account.svelte
│  │  │  │  │  ├─ Advanced
│  │  │  │  │  │  └─ AdvancedParams.svelte
│  │  │  │  │  ├─ Audio.svelte
│  │  │  │  │  ├─ Chats.svelte
│  │  │  │  │  ├─ General.svelte
│  │  │  │  │  ├─ Interface.svelte
│  │  │  │  │  ├─ Personalization
│  │  │  │  │  │  ├─ AddMemoryModal.svelte
│  │  │  │  │  │  ├─ EditMemoryModal.svelte
│  │  │  │  │  │  └─ ManageModal.svelte
│  │  │  │  │  └─ Personalization.svelte
│  │  │  │  ├─ SettingsModal.svelte
│  │  │  │  ├─ ShareChatModal.svelte
│  │  │  │  ├─ ShortcutsModal.svelte
│  │  │  │  ├─ Suggestions.svelte
│  │  │  │  ├─ TagChatModal.svelte
│  │  │  │  └─ Tags.svelte
│  │  │  ├─ common
│  │  │  │  ├─ Badge.svelte
│  │  │  │  ├─ Banner.svelte
│  │  │  │  ├─ Checkbox.svelte
│  │  │  │  ├─ CodeEditor.svelte
│  │  │  │  ├─ Collapsible.svelte
│  │  │  │  ├─ ConfirmDialog.svelte
│  │  │  │  ├─ DragGhost.svelte
│  │  │  │  ├─ Drawer.svelte
│  │  │  │  ├─ Dropdown.svelte
│  │  │  │  ├─ FileItem.svelte
│  │  │  │  ├─ FileItemModal.svelte
│  │  │  │  ├─ Folder.svelte
│  │  │  │  ├─ Image.svelte
│  │  │  │  ├─ ImagePreview.svelte
│  │  │  │  ├─ Loader.svelte
│  │  │  │  ├─ Marquee.svelte
│  │  │  │  ├─ Modal.svelte
│  │  │  │  ├─ Overlay.svelte
│  │  │  │  ├─ Pagination.svelte
│  │  │  │  ├─ RichTextInput.svelte
│  │  │  │  ├─ SVGPanZoom.svelte
│  │  │  │  ├─ Selector.svelte
│  │  │  │  ├─ SensitiveInput.svelte
│  │  │  │  ├─ Sidebar.svelte
│  │  │  │  ├─ SlideShow.svelte
│  │  │  │  ├─ Spinner.svelte
│  │  │  │  ├─ Switch.svelte
│  │  │  │  ├─ Tags
│  │  │  │  │  ├─ TagInput.svelte
│  │  │  │  │  └─ TagList.svelte
│  │  │  │  ├─ Tags.svelte
│  │  │  │  ├─ Textarea.svelte
│  │  │  │  ├─ Tooltip.svelte
│  │  │  │  └─ Valves.svelte
│  │  │  ├─ icons
│  │  │  │  ├─ AdjustmentsHorizontal.svelte
│  │  │  │  ├─ ArchiveBox.svelte
│  │  │  │  ├─ ArrowDownTray.svelte
│  │  │  │  ├─ ArrowLeft.svelte
│  │  │  │  ├─ ArrowPath.svelte
│  │  │  │  ├─ ArrowRight.svelte
│  │  │  │  ├─ ArrowRightCircle.svelte
│  │  │  │  ├─ ArrowUpCircle.svelte
│  │  │  │  ├─ ArrowsPointingOut.svelte
│  │  │  │  ├─ BarsArrowUp.svelte
│  │  │  │  ├─ Bolt.svelte
│  │  │  │  ├─ BookOpen.svelte
│  │  │  │  ├─ Bookmark.svelte
│  │  │  │  ├─ BookmarkSlash.svelte
│  │  │  │  ├─ ChartBar.svelte
│  │  │  │  ├─ ChatBubble.svelte
│  │  │  │  ├─ ChatBubbleOval.svelte
│  │  │  │  ├─ ChatBubbles.svelte
│  │  │  │  ├─ Check.svelte
│  │  │  │  ├─ ChevronDown.svelte
│  │  │  │  ├─ ChevronLeft.svelte
│  │  │  │  ├─ ChevronRight.svelte
│  │  │  │  ├─ ChevronUp.svelte
│  │  │  │  ├─ ChevronUpDown.svelte
│  │  │  │  ├─ Clipboard.svelte
│  │  │  │  ├─ CloudArrowUp.svelte
│  │  │  │  ├─ Cog6.svelte
│  │  │  │  ├─ Cube.svelte
│  │  │  │  ├─ Document.svelte
│  │  │  │  ├─ DocumentArrowDown.svelte
│  │  │  │  ├─ DocumentArrowUpSolid.svelte
│  │  │  │  ├─ DocumentChartBar.svelte
│  │  │  │  ├─ DocumentDuplicate.svelte
│  │  │  │  ├─ Download.svelte
│  │  │  │  ├─ EllipsisHorizontal.svelte
│  │  │  │  ├─ EllipsisVertical.svelte
│  │  │  │  ├─ EyeSlash.svelte
│  │  │  │  ├─ FloppyDisk.svelte
│  │  │  │  ├─ FolderOpen.svelte
│  │  │  │  ├─ GarbageBin.svelte
│  │  │  │  ├─ GlobeAlt.svelte
│  │  │  │  ├─ GlobeAltSolid.svelte
│  │  │  │  ├─ Headphone.svelte
│  │  │  │  ├─ Heart.svelte
│  │  │  │  ├─ Info.svelte
│  │  │  │  ├─ Keyboard.svelte
│  │  │  │  ├─ Lifebuoy.svelte
│  │  │  │  ├─ LightBlub.svelte
│  │  │  │  ├─ Link.svelte
│  │  │  │  ├─ LockClosed.svelte
│  │  │  │  ├─ MagnifyingGlass.svelte
│  │  │  │  ├─ Map.svelte
│  │  │  │  ├─ MenuLines.svelte
│  │  │  │  ├─ Merge.svelte
│  │  │  │  ├─ Mic.svelte
│  │  │  │  ├─ Minus.svelte
│  │  │  │  ├─ Pencil.svelte
│  │  │  │  ├─ PencilSolid.svelte
│  │  │  │  ├─ PencilSquare.svelte
│  │  │  │  ├─ Plus.svelte
│  │  │  │  ├─ QuestionMarkCircle.svelte
│  │  │  │  ├─ Search.svelte
│  │  │  │  ├─ Share.svelte
│  │  │  │  ├─ Sparkles.svelte
│  │  │  │  ├─ SparklesSolid.svelte
│  │  │  │  ├─ Star.svelte
│  │  │  │  ├─ User.svelte
│  │  │  │  ├─ UserCircleSolid.svelte
│  │  │  │  ├─ UserPlusSolid.svelte
│  │  │  │  ├─ UsersSolid.svelte
│  │  │  │  ├─ Wrench.svelte
│  │  │  │  ├─ WrenchSolid.svelte
│  │  │  │  └─ XMark.svelte
│  │  │  ├─ playground
│  │  │  │  ├─ Chat
│  │  │  │  │  └─ Messages.svelte
│  │  │  │  ├─ Chat.svelte
│  │  │  │  ├─ Completions.svelte
│  │  │  │  └─ Notes.svelte
│  │  │  └─ workspace
│  │  │     ├─ Knowledge
│  │  │     │  ├─ CreateKnowledgeBase.svelte
│  │  │     │  ├─ ItemMenu.svelte
│  │  │     │  ├─ KnowledgeBase
│  │  │     │  │  ├─ AddContentMenu.svelte
│  │  │     │  │  ├─ AddTextContentModal.svelte
│  │  │     │  │  └─ Files.svelte
│  │  │     │  └─ KnowledgeBase.svelte
│  │  │     ├─ Knowledge.svelte
│  │  │     ├─ Models
│  │  │     │  ├─ ActionsSelector.svelte
│  │  │     │  ├─ Capabilities.svelte
│  │  │     │  ├─ FiltersSelector.svelte
│  │  │     │  ├─ Knowledge
│  │  │     │  │  └─ Selector.svelte
│  │  │     │  ├─ Knowledge.svelte
│  │  │     │  ├─ ModelEditor.svelte
│  │  │     │  ├─ ModelMenu.svelte
│  │  │     │  └─ ToolsSelector.svelte
│  │  │     ├─ Models.svelte
│  │  │     ├─ Prompts
│  │  │     │  ├─ PromptEditor.svelte
│  │  │     │  └─ PromptMenu.svelte
│  │  │     ├─ Prompts.svelte
│  │  │     ├─ Tools
│  │  │     │  ├─ ToolMenu.svelte
│  │  │     │  └─ ToolkitEditor.svelte
│  │  │     ├─ Tools.svelte
│  │  │     └─ common
│  │  │        ├─ AccessControl.svelte
│  │  │        ├─ AccessControlModal.svelte
│  │  │        ├─ ManifestModal.svelte
│  │  │        └─ ValvesModal.svelte
│  │  ├─ constants.ts
│  │  ├─ i18n
│  │  │  ├─ index.ts
│  │  │  └─ locales
│  │  │     ├─ ar-BH
│  │  │     │  └─ translation.json
│  │  │     ├─ bg-BG
│  │  │     │  └─ translation.json
│  │  │     ├─ bn-BD
│  │  │     │  └─ translation.json
│  │  │     ├─ ca-ES
│  │  │     │  └─ translation.json
│  │  │     ├─ ceb-PH
│  │  │     │  └─ translation.json
│  │  │     ├─ cs-CZ
│  │  │     │  └─ translation.json
│  │  │     ├─ da-DK
│  │  │     │  └─ translation.json
│  │  │     ├─ de-DE
│  │  │     │  └─ translation.json
│  │  │     ├─ dg-DG
│  │  │     │  └─ translation.json
│  │  │     ├─ en-GB
│  │  │     │  └─ translation.json
│  │  │     ├─ en-US
│  │  │     │  └─ translation.json
│  │  │     ├─ es-ES
│  │  │     │  └─ translation.json
│  │  │     ├─ fa-IR
│  │  │     │  └─ translation.json
│  │  │     ├─ fi-FI
│  │  │     │  └─ translation.json
│  │  │     ├─ fr-CA
│  │  │     │  └─ translation.json
│  │  │     ├─ fr-FR
│  │  │     │  └─ translation.json
│  │  │     ├─ he-IL
│  │  │     │  └─ translation.json
│  │  │     ├─ hi-IN
│  │  │     │  └─ translation.json
│  │  │     ├─ hr-HR
│  │  │     │  └─ translation.json
│  │  │     ├─ hu-HU
│  │  │     │  └─ translation.json
│  │  │     ├─ id-ID
│  │  │     │  └─ translation.json
│  │  │     ├─ ie-GA
│  │  │     │  └─ translation.json
│  │  │     ├─ it-IT
│  │  │     │  └─ translation.json
│  │  │     ├─ ja-JP
│  │  │     │  └─ translation.json
│  │  │     ├─ ka-GE
│  │  │     │  └─ translation.json
│  │  │     ├─ ko-KR
│  │  │     │  └─ translation.json
│  │  │     ├─ languages.json
│  │  │     ├─ lt-LT
│  │  │     │  └─ translation.json
│  │  │     ├─ ms-MY
│  │  │     │  └─ translation.json
│  │  │     ├─ nb-NO
│  │  │     │  └─ translation.json
│  │  │     ├─ nl-NL
│  │  │     │  └─ translation.json
│  │  │     ├─ pa-IN
│  │  │     │  └─ translation.json
│  │  │     ├─ pl-PL
│  │  │     │  └─ translation.json
│  │  │     ├─ pt-BR
│  │  │     │  └─ translation.json
│  │  │     ├─ pt-PT
│  │  │     │  └─ translation.json
│  │  │     ├─ ro-RO
│  │  │     │  └─ translation.json
│  │  │     ├─ ru-RU
│  │  │     │  └─ translation.json
│  │  │     ├─ sr-RS
│  │  │     │  └─ translation.json
│  │  │     ├─ sv-SE
│  │  │     │  └─ translation.json
│  │  │     ├─ th-TH
│  │  │     │  └─ translation.json
│  │  │     ├─ tk-TM
│  │  │     │  └─ translation.json
│  │  │     ├─ tk-TW
│  │  │     │  └─ translation.json
│  │  │     ├─ tr-TR
│  │  │     │  └─ translation.json
│  │  │     ├─ uk-UA
│  │  │     │  └─ translation.json
│  │  │     ├─ ur-PK
│  │  │     │  └─ translation.json
│  │  │     ├─ vi-VN
│  │  │     │  └─ translation.json
│  │  │     ├─ zh-CN
│  │  │     │  └─ translation.json
│  │  │     └─ zh-TW
│  │  │        └─ translation.json
│  │  ├─ index.ts
│  │  ├─ stores
│  │  │  └─ index.ts
│  │  ├─ types
│  │  │  └─ index.ts
│  │  ├─ utils
│  │  │  ├─ _template_old.ts
│  │  │  ├─ characters
│  │  │  │  └─ index.ts
│  │  │  ├─ index.ts
│  │  │  ├─ marked
│  │  │  │  ├─ extension.ts
│  │  │  │  └─ katex-extension.ts
│  │  │  ├─ rag
│  │  │  │  └─ index.ts
│  │  │  └─ transitions
│  │  │     └─ index.ts
│  │  └─ workers
│  │     └─ pyodide.worker.ts
│  └─ tailwind.css
├─ static
│  ├─ assets
│  │  ├─ fonts
│  │  │  ├─ Archivo-Variable.ttf
│  │  │  ├─ InstrumentSerif-Italic.ttf
│  │  │  ├─ InstrumentSerif-Regular.ttf
│  │  │  ├─ Inter-Variable.ttf
│  │  │  └─ Mona-Sans.woff2
│  │  └─ images
│  │     ├─ adam.jpg
│  │     ├─ earth.jpg
│  │     ├─ galaxy.jpg
│  │     └─ space.jpg
│  ├─ audio
│  │  └─ greeting.mp3
│  ├─ doge.png
│  ├─ favicon.png
│  ├─ manifest.json
│  ├─ opensearch.xml
│  ├─ pyodide
│  │  └─ pyodide-lock.json
│  ├─ robots.txt
│  ├─ static
│  │  ├─ favicon.png
│  │  ├─ splash-dark.png
│  │  └─ splash.png
│  ├─ themes
│  │  ├─ rosepine-dawn.css
│  │  └─ rosepine.css
│  └─ user.png
├─ svelte.config.js
├─ tailwind.config.js
├─ test
│  └─ test_files
│     └─ image_gen
│        └─ sd-empty.pt
├─ tsconfig.json
├─ update_ollama_models.sh
├─ uv.lock
└─ vite.config.ts

```