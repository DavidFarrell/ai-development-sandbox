
# AI Development Sandbox

Safe Docker environment for AI-assisted development with Claude Code and OpenCode.

## Quick Start

1. **Build the container:**
   ```bash
   cd ~/git/ai-sandbox
   docker-compose build
   ```

2. **Start the development environment:**
   ```bash
   docker-compose run --rm dev-sandbox bash
   ```

3. **Inside the container, you'll be at `/workspace/projects`:**
   ```bash
   # Check you're in the right place
   pwd  # should show /workspace/projects

   # Clone or work with your projects
   git clone https://github.com/yourusername/yourproject.git
   cd yourproject

   # Start Claude Code or OpenCode
   claude
   opencode
   ```

4. **When done, exit:**
   ```bash
   exit
   ```

## What's Persistent

- **Authentication**: Claude Code and OpenCode login credentials
- **Settings**: MCP configurations, user preferences
- **Projects**: All your code in the `projects/` directory
- **SSH Keys**: For GitHub access (read-only)

## Features

- **Isolated Environment**: Safe sandbox separate from your main system
- **Sudo Access**: Install packages as needed with `sudo apt install`
- **Both AI Tools**: Claude Code and OpenCode pre-installed
- **Development Tools**: Git, Node.js, Python, build tools included

The `--rm` flag automatically removes the container when you exit, keeping things clean.

### quickstart:
docker-compose run --rm dev-sandbox bash