# AI Code Reviewer

AI-powered code review tool for GitHub pull requests.


## Configuration

The tool uses GitHub Action inputs for configuration. The following inputs are available:

- `GITHUB_TOKEN`: GitHub token for API access
- `OPENAI_API_KEY`: OpenAI API key
- `OPENAI_API_MODEL`: OpenAI model to use
- `exclude`: Comma-separated list of patterns to exclude from review

## Features

- Reviews pull requests using OpenAI's GPT-4 API.
- Provides intelligent comments and suggestions for improving your code.
- Filters out files that match specified exclude patterns.
- Easy to set up and integrate into your GitHub workflow.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
