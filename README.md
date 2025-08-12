# Chad & Pascal's Modern LaTeX Style

This repository contains a collection of LaTeX style and support files that combines the best of two excellent academic paper templates: Charles I. Jones's original color LaTeX style and Pascal Michaillat's modern latex-paper enhancements. The package uses carefully chosen colours, hyperlinks throughout, modern typography, and sensible defaults for spacing to make academic papers more readable both on-screen and in print.

## Contents

The key files are:

- **`chadstyle.sty`** – the main style file combining Chad's color scheme and layout with Pascal's modern font and typography enhancements.
- **`aernobold.sty` / `aernobold.bst`** – style and bibliography files loosely based on the *American Economic Review* format, but with author names in normal weight instead of bold.
- **`chadskeleton.tex`** – a minimal template demonstrating how to set up your document using the style. Start here when writing a new paper.
- **`cost04b.tex`** and **`cost040.pdf`** – an example paper compiled with the style. The PDF shows how the colours and hyperlinks look when printed or displayed on screen.
- **`.gitignore`** – ignores common LaTeX intermediate files such as `.aux`, `.log`, `.out`, etc.

### Combined Features

This style merges **Chad Jones's** excellent color scheme and hyperlink system with **Pascal Michaillat's** modern typography and font improvements:

**From Chad's original style:**
* Carefully chosen color palette for on-screen readability
* Comprehensive hyperlink system throughout the document
* Sensible spacing and layout defaults
* Useful macros for academic writing

**From Pascal's latex-paper template:**
* **Improved fonts:** main text in [Source Serif Pro](https://github.com/adobe-fonts/source-serif), monospaced font in [Source Code Pro](https://github.com/adobe-fonts/source-code-pro), and mathematics using `MnSymbol`, `mathalpha` (Euler calligraphic and Fourier blackboard bold), `bm` and `mathastext`
* **Enhanced typography:** microtype package for improved kerning and justification
* **Modern LaTeX practices:** T1 encoding, better font handling, and contemporary package usage

The result is a style that combines Chad's proven readability approach with Pascal's typographic refinements, creating documents that look excellent both on screen and in print.

## Usage

1. **Clone or download this repository.** You can click the **Code** button on GitHub and choose *Download ZIP*, or clone it via git:

   ```bash
   git clone https://github.com/<your_username>/chad-pascal-latex-style.git
   ```

2. **Write your paper.** Use `chadskeleton.tex` as a starting point. It sets up the combined color scheme and typography. Replace the title, author, abstract, and body with your content.

3. **Compile the document.** If you have a modern TeX distribution installed (e.g. TeX Live 2024 or MiKTeX), run:

   ```bash
   pdflatex chadskeleton.tex
   biber chadskeleton
   pdflatex chadskeleton.tex
   ```

   Alternatively, use `latexmk -pdf chadskeleton.tex` to handle auxiliary runs automatically. For citation support you may choose `bibtex` or `biber` depending on your bibliography backend (this repository ships a `.bst` file for BibTeX).

4. **Import into Overleaf.** Overleaf supports GitHub integration. After pushing this repository to GitHub, follow [Overleaf's guide](https://www.overleaf.com/learn/how-to/How_do_I_use_Git_and_GitHub_with_Overleaf%3F) to import or link your project.

5. **Customise further.** Feel free to modify `chadstyle.sty` to suit your needs. Colours are defined near the top of the file via `\definecolor`. If you prefer the original fonts, you can comment out the font-related sections.

## License

These files are offered under the permissive MIT License. See [LICENSE](LICENSE) for details.

---

If you find this style useful, please consider crediting both Charles I. Jones for the original color LaTeX style and Pascal Michaillat for the modern typography enhancements. Improvements and suggestions are always appreciated!
