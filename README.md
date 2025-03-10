# prompt-template

A template repository for submitting AI prompts.

## Prompt Schema

The prompt schema defines the structure and metadata for AI prompts in this repository. It ensures consistency and compatibility across all prompts.

### Schema Overview

- **`specVersion`**: The version of the schema (e.g., `1.0.0`).
- **`metadata`**: Metadata about the prompt, including its name, author, and tags.
- **`prompt`**: The core content of the prompt, including the template and variables.
- **`extensions`**: A flexible object for future enhancements.

### Fields

#### Metadata

- **`name`**: A URL-friendly name for the prompt (e.g., `tweet-generator`).
- **`author`**: The author of the prompt (e.g., `@username`).
- **`description`**: A brief description of the prompt's purpose.
- **`tags`**: A list of tags for categorization (e.g., `["marketing", "social-media"]`).
- **`modelCompatibility`**: A list of compatible AI models (e.g., `["gpt-4", "claude-2"]`).
- **`dependencies`**: A map of dependencies (e.g., `{"tweet-writer": "1.0.0"}`).
- **`visibility`**: The visibility of the prompt (`public` or `private`).
- **`createdAt`**: The timestamp when the prompt was created.
- **`updatedAt`**: The timestamp when the prompt was last updated.

#### Prompt

- **`template`**: The template text of the prompt (e.g., `"Write a tweet about {{topic}}"`).
- **`variables`**: A list of variables used in the template.

#### Extensions

- **`extensions`**: A flexible object for experimental or custom fields.

### Example

```json
{
  "specVersion": "1.0.0",
  "metadata": {
    "name": "tweet-generator",
    "author": "@alice",
    "description": "Generates tweets for social media.",
    "tags": ["marketing", "social-media"],
    "modelCompatibility": ["gpt-4", "claude-2"],
    "dependencies": {},
    "visibility": "public",
    "createdAt": "2023-10-01T12:00:00Z",
    "updatedAt": "2023-10-01T12:00:00Z"
  },
  "prompt": {
    "template": "Write a tweet about {{topic}}.",
    "variables": [
      {
        "name": "topic",
        "description": "The topic of the tweet.",
        "type": "string",
        "required": true
      }
    ]
  },
  "extensions": {}
}
```

## Licensing

By submitting a prompt to this repository, you agree to license it under the same terms as this repository (MIT License).
