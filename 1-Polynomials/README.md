# MathTrackX: Polynomials, Functions and Graphs

Study Materials based on the **University of Adelaide MathTrackX** curriculum.

## Course Overview

This is the first course in the MathTrackX XSeries Program, designed to provide a solid foundation in mathematical fundamentals. The course covers 4 weeks of content plus assessment preparation.

## Course Structure

| Week | Topic | Key Concepts |
|------|-------|--------------|
| **Week 1** | Numbers | Natural, integers, rationals, reals, inequalities, intervals |
| **Week 2** | Linear Functions | Coordinate plane, slope, linear equations, graphing |
| **Week 3** | Polynomials | Degree, operations, quadratics, graphing polynomials |
| **Week 4** | Functions & Graphs | Domain, range, continuity, composition, transformations |

## Study Materials

| File | Description | Pages (approx.) |
|------|-------------|-----------------|
| `study-material.tex` | Complete study material following the 4-week structure | ~30 pages |
| `cheatsheet.tex` | One-page quick reference (landscape A4) | 1 page |
| `exercises.tex` | Practice problems with solutions for all 4 weeks | ~20 pages |
| `mock-exams.tex` | Three 60-minute mock exams with solutions | ~25 pages |

## Learning Outcomes

By the end of this course, you will be able to:

- Distinguish between integers, rational numbers, and real numbers
- Simplify expressions and apply arithmetic rules
- Use inequalities and interval notation
- Plot points and understand the coordinate plane
- Graph linear functions and determine slope and intercepts
- Solve linear equations in various contexts
- Identify polynomials and their properties
- Solve quadratic equations using factoring, completing the square, or the quadratic formula
- Graph polynomials and identify roots, turning points, and end behavior
- Determine domain and range of functions
- Understand continuity and identify discontinuities
- Construct new functions through composition and operations
- Apply transformations to function graphs

## Compilation Instructions

### Prerequisites

Install a LaTeX distribution:

- **Linux (Ubuntu/Debian)**: `sudo apt install texlive-full`
- **Linux (Arch)**: `sudo pacman -S texlive-most`
- **macOS**: Install [MacTeX](https://www.tug.org/mactex/)
- **Windows**: Install [MiKTeX](https://miktex.org/) or [TeX Live](https://www.tug.org/texlive/)

### Compiling to PDF

#### Option 1: Command Line (pdflatex)

```bash
cd 1-Polynomials

# Compile each document (run twice for TOC/references)
pdflatex study-material.tex && pdflatex study-material.tex
pdflatex cheatsheet.tex
pdflatex exercises.tex && pdflatex exercises.tex
pdflatex mock-exams.tex && pdflatex mock-exams.tex
```

#### Option 2: Using latexmk (Recommended)

```bash
latexmk -pdf study-material.tex
latexmk -pdf cheatsheet.tex
latexmk -pdf exercises.tex
latexmk -pdf mock-exams.tex
```

#### Option 3: Compile All at Once

```bash
for f in *.tex; do
    pdflatex "$f" && pdflatex "$f"
done
```

#### Option 4: Using an IDE

- **TeXstudio**: Open file and press F5 to compile
- **VS Code + LaTeX Workshop**: Open file and save (auto-compiles)
- **Overleaf**: Upload all `.tex` files to a new project

### Cleaning Auxiliary Files

```bash
rm -f *.aux *.log *.out *.toc *.synctex.gz *.fls *.fdb_latexmk
# Or using latexmk:
latexmk -c
```

## Study Guide

### Recommended Order

1. **Read** `study-material.pdf` week by week
2. **Practice** with `exercises.pdf` after each week (attempt problems before checking solutions)
3. **Review** using `cheatsheet.pdf` for quick revision
4. **Test yourself** with mock exams under timed conditions (60 minutes each)
5. **Identify weak areas** and revisit relevant sections

### Week-by-Week Focus

**Week 1: Numbers**
- Master number classification (N, Z, Q, R)
- Practice fraction arithmetic
- Understand inequality rules (especially sign reversal)
- Become fluent with interval notation

**Week 2: Linear Functions**
- Memorize slope formula: m = (y2-y1)/(x2-x1)
- Know all forms: slope-intercept, point-slope, standard
- Practice finding equations from points or slope
- Understand parallel (same slope) and perpendicular (negative reciprocal)

**Week 3: Polynomials**
- Identify degree, leading coefficient, constant term
- Master special products: (a+b)², (a-b)², (a+b)(a-b)
- Memorize quadratic formula and discriminant rules
- Understand end behavior based on degree and leading coefficient

**Week 4: Functions & Graphs**
- Always check for domain restrictions (division by zero, square roots)
- Remember composition order: (f∘g)(x) = f(g(x)) - apply g first
- Know transformation rules: +k up, -h right, negative reflects
- Polynomials are always continuous

## Troubleshooting

**Problem**: Missing package errors
```
! LaTeX Error: File `tcolorbox.sty' not found.
```
**Solution**: Install the full TeX distribution or the specific package

**Problem**: PGFPlots version issues
**Solution**: Remove `\pgfplotsset{compat=1.18}` or update pgfplots

**Problem**: Compilation takes too long
**Solution**: Use `pdflatex` with `-interaction=nonstopmode` flag

## About MathTrackX

MathTrackX is an XSeries Program from the University of Adelaide offered through edX. This course "Polynomials, Functions and Graphs" is the first in the series, designed to build foundational mathematical skills for further study.

**Official course**: [MathTrackX on edX](https://www.edx.org/learn/math/university-of-adelaide-mathtrackx-polynomials-functions-and-graphs)

---

*Materials created for educational purposes based on the MathTrackX curriculum.*
