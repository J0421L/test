# Resume

[![deploy](../../actions/workflows/deploy.yml/badge.svg?branch=main)](../../actions/workflows/deploy.yml)

This is my one-page resume, written in LaTeX.
You can view the latest version at <https://aragorn1025.github.io/resume/>.

Feel free to use it as a template for your own resume!

## How to Use

1. Fork this repository.
2. Set your name by adding a repository variable `AUTHOR_NAME` (for example, `Aragorn_Dai`) in **Settings → Secrets and variables → Actions → Variables**.
   The PDF will be named `<AUTHOR_NAME>_Resume.pdf`.
3. Enable GitHub Actions in the **Actions** tab of your fork.
4. Enable GitHub Pages in **Settings → Pages**, and set **Source** to **GitHub Actions**.
5. Create a branch, and edit `resume.tex` with your own information.
6. Open a pull request to `main` of your fork, and merge it.
   Make sure the base repository is your fork, not this repository.

Once the workflow finishes, your resume will be available at `https://<your-username>.github.io/<repository>/`.

## Layout Options

The layout is defined in `resume.cls`, so `resume.tex` only holds the content.

```latex
\documentclass[
    10pt,
    margin            = {0.5in},
    section_separator = {1.6em},
    item_separator    = {0.4em},
    point_separator   = {0.15em},
]{resume}
```

| Option | Default | Description |
|---|---|---|
| `margin` | `0.5in` | Page margin |
| `section_separator` | `1.2em` | Space above each section title |
| `item_separator` | `0.4em` | Space above each experience, education, or skill entry |
| `point_separator` | `0.1em` | Space between bullet points |

Other options, such as the font size `10pt`, are passed to the `article` class.

See `resume.tex` for a complete example.

## License

The template, including `resume.cls`, the `Dockerfile`, and the workflow, is licensed under the [MIT License](LICENSE).
The personal information and resume content in `resume.tex` are not covered by this license, so please replace them with your own.
