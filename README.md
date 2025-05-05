# quarto-p5

**quarto-p5** is a Quarto filter for embedding [p5.js](https://p5js.org/) sketches directly into HTML-based [Quarto](https://quarto.org/) documents. It allows you to define JavaScript code blocks and GLSL shaders in a structured way, automatically injecting the necessary `<script>` tags into the output document.


## Installing

```bash
quarto add paithiov909/quarto-p5
```
This will install the extension under the `_extensions` subdirectory. If you're using version control, you will want to check in this directory.

Then, activate the extension by adding the following lines to the YAML front matter:

```yaml
filters:
  - p5
```


## Usage

To embed a p5.js sketch, define your HTML container, JavaScript sketch, and optional shaders using code blocks. See [example.qmd](https://github.com/paithiov909/quarto-p5/blob/main/example.qmd) for detailed usage.


## Notes

- Missing or invalid shader labels will result in a warning block in the output.
- It does not attempt to validate GLSL or JavaScript syntax.
