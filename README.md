# Rough-and-ready grounded theory coder

A Python tool that reads text files containing interview transcripts and uses an LLM to simulate the work of an ethnographer doing ethnographic coding based on grounded theory. Transcripts are first divided into segments (there is an entire literature on how to do this, so we start by   The output is – provisionally – a list of codes and the in-vivo quotes the codes are attached to, plus some justification for the coding choice made by the LLM. 

## Main challenge

Yudhanjaya: 

> Grounded theory with LLMs is tricky because they are inherently biased towards categorization. For grounded theory, you need to prompt the model to act as a pure inductive coder, which means almost force-pushing it into negative space and then comparing outputs. I personally would use Gemini Pro (not flash) because its forced "thinking" process will come in handy.

On the other hand, categorization is also useful to map the ethnographic data onto a concept space that intended readers understand easily – this is on e way to understand the "rough-and-ready" in this little project.



## Key Features

* Works on simple text files. Some pre-processing might be needed but is not part of this repo.
* Intended final output is a network of co-occurring codes or, in a good scenario, a [semantic social network](https://doi.org/10.1177/1525822X20908236). In successive iterations I intend to add some JSON structured output to build a graph from.

## Use Cases

Rapid production of some insights from interviews or other contributions. For example: 

1. Ask the same question for several informants, like "As a politician, how do you experience economic reform? What needs to be in place for you to attempt it yourself?"
2. Use the software to map out the individual responses in terms of ethnographic codes, and look for patterns.

Not suitable for academic publication, as speed is prioritized over rigor.

## Installation

### Prerequisites
- Python 3.7 or higher
- An Anthropic API key (get one at [console.anthropic.com](https://console.anthropic.com))

### Setup Steps

1. **Install Python dependencies:**
```bash
pip install anthropic beautifulsoup4 fuzzywuzzy python-levenshtein
```

2. **Set up your API key:**
Create a file named `api_key.txt` in the project directory and add your Anthropic API key:
```
your-anthropic-api-key-here
```

3. **Prepare input files:**
Create an `Input/` folder and add your text files containing sci-fi book reviews/summaries.

## Usage

To do.

## Input Requirements

To do.

## Output Format

To do.

### Real Example Output

To do.

## File Structure

To do.

## How It Works

To do.

### Data Models

To 
## Troubleshooting

### Common Issues

**"No module named 'anthropic'"**
```bash
pip install anthropic beautifulsoup4 fuzzywuzzy python-levenshtein
```

**"API key not found"**
- Ensure `api_key.txt` exists in the project directory
- Check that the file contains only your API key (no extra spaces/newlines)
- Verify your API key is valid at [console.anthropic.com](https://console.anthropic.com)

**"Folder path does not exist"**
- Create an `Input/` folder in the project directory
- Add your text files to this folder
- Ensure the folder name is exactly `Input` (case-sensitive)

**No extractions found**
- Ensure your text files contain clear references to sci-fi books and economic concepts
- Check that files are not empty or corrupted
- Verify files contain actual book reviews or summaries, not just metadata

**API errors or timeouts**
- Check your internet connection
- Verify your Anthropic API key has sufficient credits
- The tool automatically retries failed requests


## License

This project is provided as-is for research and educational purposes.

## Support

For issues, questions, or contributions, please refer to the project documentation or create an issue in the project repository.
