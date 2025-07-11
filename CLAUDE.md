# Gitmoji Pre-commit Hook Project

## Overview
This project implements a git pre-commit hook that automatically appends relevant emojis to commit messages using an LLM API (specifically designed for Ollama with gemma3n model).

## Project Structure
- `hello.txt` - Test file containing sample text
- `.git/hooks/prepare-commit-msg` - Main git hook script that processes commit messages

## How It Works
The `prepare-commit-msg` hook automatically enhances commit messages by:
1. Intercepting commit messages before they're finalized
2. Sending the commit message to an LLM API for emoji suggestion
3. Appending the suggested emoji to the commit message

## Setup Requirements
Set these environment variables:
- `LLM_API_URL` - URL to your Ollama API endpoint (required to enable the hook)
- `LLM_MODEL` - Model name to use (e.g., "gemma3n")

## Hook Behavior
- Only processes regular commits (not merges, squashes, etc.)
- Skips empty messages or comments (starting with #)
- Makes API call to `/api/generate` endpoint
- Safely handles API failures
- Appends emoji with proper spacing

## Example Usage
```bash
# Set up environment
export LLM_API_URL="http://localhost:11434"
export LLM_MODEL="gemma3n"

# Make a commit - emoji will be added automatically
git commit -m "Fix authentication bug"
# Results in: "Fix authentication bug🔒"
```

## Recent Commits
The project shows active development with emoji-enhanced commit messages:
- `cleanup job`
- `modify test file📝`
- `adding a test file`
- `Clean up test file🧹`
- `Test commit with LLM_API_URL🧪`

## Testing
To test the hook:
1. Set required environment variables
2. Make a commit
3. Verify emoji appears in commit message
4. Check `git log` to see emoji-enhanced history

## Commands
- **Run tests**: No specific test framework detected
- **Build**: No build process required (bash script)
- **Lint**: No linting configured