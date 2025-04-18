# Smart Todo TUI

A minimalistic terminal user interface (TUI) todo app with AI assistance. Manage your tasks efficiently with natural language processing and a clean terminal interface.

## Features

### Standard Mode

The standard mode provides an interactive terminal interface for managing your tasks:

- Create, edit, and delete tasks
- Set due dates, priorities, and tags
- Sort tasks by name, creation date, or due date
- Filter tasks by status, tags, or search terms
- View detailed task information

### AI-Assisted Modes

Smart Todo TUI offers two AI-powered modes for enhanced productivity:

#### Quick AI Add Mode

Quickly add tasks using natural language:

```
./smartodo ai-add "Schedule a meeting with the team for next Tuesday at 2pm with high priority"
```

The AI will parse your request and create a properly formatted task with the correct due date, priority, and tags.

#### Interactive AI Chat Mode

Engage in a conversation with the AI assistant to manage your tasks:

```
./smartodo ai-chat
```

In this mode, you can:

- Use natural language to create, edit, and delete tasks
- Ask for task recommendations and organization suggestions
- Perform operations on selected tasks
- Receive AI-powered insights about your task list

## Usage

### Standard Mode Commands

When you run `./smartodo` without arguments, it enters an interactive REPL with single-letter commands:

```
j/k or ↓/↑ - Navigate up and down the task list
a - Add a new task (prompts for details)
d - Delete the selected task
e - Edit the selected task (prompts for new details)
m - Toggle task status (done/pending)
s - Sort tasks by name or date
/ - Search tasks
q - Quit the application
```

### Command-Line Arguments

```
# Start AI chat mode
./smartodo ai-chat

# Quick add a task with AI
./smartodo ai-add "Schedule a meeting with the team for next Tuesday at 2pm"
```

### AI Chat Commands

In AI chat mode, you can use natural language commands like:

- "Add a task to call mom tomorrow"
- "Show me all my high priority tasks"
- "Mark the selected task as done"
- "Reschedule my meeting with John to next Friday"
- "What tasks are due this week?"
- "Help me organize my work tasks"

## Installation

### Prerequisites

- C compiler (gcc or clang)
- libcurl
- ncurses
- cJSON
- OpenAI API key (for AI features)

### Building from Source

```bash
# Clone the repository
git clone https://github.com/yourusername/smart-todo-tui.git
cd smart-todo-tui

# Navigate to the src directory and build
cd src
make

# Set your OpenAI API key (required for AI features)
export OPENAI_API_KEY="your-api-key-here"

# Run the application
./smartodo
```

## Configuration

Tasks are stored in `$HOME/.todo-app/tasks.json`.

## License

MIT
