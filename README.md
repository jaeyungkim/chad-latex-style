# Chad's Color LaTeX Style (Modernized)

This repository contains a collection of LaTeX style and support files originally put together by Charles I. Jones to make academic papers more readable on‐screen.  The package uses carefully chosen colours, hyperlinks throughout, and sensible defaults for spacing and typography.  In addition to the original files, this repository adds a few conveniences to help you get started quickly.

## Contents

The key files are:

- **`chadstyle.sty`** – the main style file defining colours, fonts, page layout, hyperlink options, and a handful of useful macros.
- **`aernobold.sty` / `aernobold.bst`** – style and bibliography files loosely based on the *American Economic Review* format, but with author names in normal weight instead of bold.
- **`chadskeleton.tex`** – a minimal template demonstrating how to set up your document using the style.  Start here when writing a new paper.
- **`cost04b.tex`** and **`cost040.pdf`** – an example paper compiled with the style.  The PDF shows how the colours and hyperlinks look when printed or displayed on screen.
- **`.gitignore`** – ignores common LaTeX intermediate files such as `.aux`, `.log`, `.out`, etc.

### Optional Improvements

While the original style dates back to 2008, it still compiles cleanly with modern TeX engines.  In this repository we have **already incorporated a number of modernisations** inspired by Pascal Michaillat’s [latex‑paper](https://github.com/pmichaillat/latex-paper) template.  Notably:

* **Improved fonts:** the main text is set in [Source Serif Pro](https://github.com/adobe-fonts/source-serif), the monospaced font is [Source Code Pro](https://github.com/adobe-fonts/source-code-pro), and the mathematics are typeset using a combination of `MnSymbol`, `mathalpha` (Euler calligraphic and Fourier blackboard bold), `bm` and `mathastext`.  These choices yield crisper symbols and a more harmonious look between text and maths.  If you prefer the original Utopia look, you can comment out the font‑related lines in `chadstyle.sty`.

* **Microtype enabled:** the [microtype](https://ctan.org/pkg/microtype) package is now loaded by default to improve kerning and justification.  You no longer need to add it manually.

* **Automatic compilation:** for convenience you can still use `latexmk` or `arara` to automate compilation; a sample `latexmkrc` could be added if desired.

These enhancements should work out of the box with standard `pdflatex`.  Feel free to customise further or revert to the original settings by editing `chadstyle.sty`.

## Usage

1. **Clone or download this repository.**  You can click the **Code** button on GitHub and choose *Download ZIP*, or clone it via git:

   ```bash
   git clone https://github.com/&lt;your_username&gt;/chad-latex-style.git
   ```

2. **Write your paper.**  Use `chadskeleton.tex` as a starting point.  It sets up the colour scheme and defines some handy macros.  Replace the title, author, abstract, and body with your content.

3. **Compile the document.**  If you have a modern TeX distribution installed (e.g. TeX Live 2024 or MiKTeX), run:

   ```bash
   pdflatex chadskeleton.tex
   biber chadskeleton
   pdflatex chadskeleton.tex
   ```

   Alternatively, use `latexmk -pdf chadskeleton.tex` to handle auxiliary runs automatically.  For citation support you may choose `bibtex` or `biber` depending on your bibliography backend (this repository ships a `.bst` file for BibTeX).

4. **Import into Overleaf.**  Overleaf supports GitHub integration.  After pushing this repository to GitHub, follow [Overleaf’s guide](https://www.overleaf.com/learn/how-to/How_do_I_use_Git_and_GitHub_with_Overleaf%3F) to import or link your project.  In summary:
   - From your Overleaf dashboard choose **“New Project” → “Import from GitHub”**.
   - Authorise Overleaf to access your GitHub account if requested.
   - Select the repository you just created.
   - Overleaf will create a new project mirroring the GitHub files.  You can continue editing in Overleaf and synchronise changes via Git.

5. **Customise further.**  Feel free to modify `chadstyle.sty` to suit your needs.  Colours are defined near the top of the file via `\definecolor`.  If you invent new macros or update the style for 2025 and beyond, contributions are welcome—please open a pull request or submit an issue on GitHub.

## License

These files are offered under the permissive MIT License.  See [LICENSE](LICENSE) for details.

---

If you find this style useful, please drop a note to Charles I. Jones and consider citing his work.  Improvements and suggestions are always appreciated!