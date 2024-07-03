 
# LaTeX Formula Renderer

This script allows you to render LaTeX formulas into PNG images using a Python script. It leverages LaTeX and dvipng to create high-quality images of mathematical formulas.

## Installation

### Prerequisites

The script requires Python, LaTeX, and dvipng. You need to install these tools on your system before running the script.

1. **Python Installation:**
   Ensure that Python is installed on your system. You can download it from [python.org](https://www.python.org/downloads/).

2. **LaTeX and dvipng Installation:**
   Install LaTeX and dvipng on your system. The installation commands depend on your operating system.

   - **For Ubuntu/Debian:**
     ```
     sudo apt-get install texlive texlive-latex-extra texlive-fonts-recommended dvipng
     ```
   - **For macOS:**
     Use [MacTeX](http://www.tug.org/mactex/) distribution which includes dvipng.
     ```
     brew install --cask mactex
     ```
   - **For Windows:**
     Install MiKTeX from [MiKTeX.org](https://miktex.org/download). dvipng is included.

3. **Python Libraries:**
   Install required Python libraries using pip.
   ```
   pip install matplotlib Pillow
   ```

## Usage

1. **Prepare your LaTeX formula:**
   Write your LaTeX formula as a string. For example:
   ```python
   latex_formula = r"\[F={\frac{1}{4\pi\varepsilon_{0}}}{\frac{q q^{\prime}}{r^{2}}}\]"
   ```

2. **Run the script:**
   Use the `render_latex` function to render your LaTeX formula into a PNG image.
   ```python
   render_latex(latex_formula)
   ```

3. **View the generated image:**
   The script will attempt to display the image using PIL. If it cannot display the image, it will save the image as 'formula.png' in the current directory.

## Additional Notes

- The script creates temporary files (`temp.tex`, `temp.aux`, `temp.dvi`, `temp.log`) during execution. These files are cleaned up after the image is generated.
- Customize the output filename and DPI by modifying the arguments in the `render_latex` function call.

## Troubleshooting

- If you encounter issues with LaTeX compilation, check the output logs for any errors related to your LaTeX syntax or missing packages.
- Ensure all installation steps are correctly followed and that all dependencies are installed.

 
