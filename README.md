# CV/Resume Repository

This repository contains my professional CV/resume in multiple formats and languages, tailored for different regions and job markets.

## 📁 Repository Structure

```
├── EU/          # European format CV
├── RU/          # Russian language CV  
├── US/          # US format resume
└── README.md    # This file
```

## 📄 Available Formats

### 🇪🇺 European Version (`EU/`)
- **File**: `CV.tex` → `CV.pdf`
- **Language**: English
- **Format**: European CV standard
- **Target**: European job market

### 🇷🇺 Russian Version (`RU/`)
- **File**: `cv.tex` → `cv.pdf` 
- **Language**: Russian (Русский)
- **Format**: Local standard with Cyrillic support
- **Target**: Russian/CIS job market

### 🇺🇸 US Version (`US/`)
- **File**: `resume_us.tex` → `resume_us.pdf`
- **Language**: English
- **Format**: US resume standard
- **Target**: US job market

## 🛠️ Technologies & Tools

- **LaTeX**: Document typesetting
- **moderncv**: Professional CV class
- **XeLaTeX**: For Russian version (Cyrillic support)
- **PDFLaTeX**: For EU/US versions

## 📋 Prerequisites

To compile the LaTeX files, you need:

```bash
# macOS (via Homebrew)
brew install --cask mactex

# Ubuntu/Debian
sudo apt-get install texlive-full

# Arch Linux
sudo pacman -S texlive-most
```

For the Russian version, ensure XeLaTeX is available (included in most TeX distributions).

## 🚀 Building PDFs

### Compile Individual Versions

```bash
# European version
cd EU/
pdflatex CV.tex

# Russian version (requires XeLaTeX)
cd RU/
xelatex cv.tex

# US version  
cd US/
pdflatex resume_us.tex
```

### Compile All Versions

```bash
# From repository root
for dir in EU RU US; do
  echo "Building $dir version..."
  cd $dir/
  if [ "$dir" = "RU" ]; then
    xelatex *.tex
  else
    pdflatex *.tex
  fi
  cd ..
done
```

## 📝 Customization

Each version is tailored for its target market:

- **Content**: Adjusted for regional preferences and expectations
- **Formatting**: Follows local CV/resume conventions  
- **Language**: Localized where appropriate
- **Contact Info**: Consistent across all versions

## 🔄 Automation

The repository includes:
- **TaskFile.yml**: Task automation (in RU directory)
- **Build artifacts**: Generated PDFs and auxiliary files

## 📧 Contact

**Nursultan Kuandyk**
- Email: n.kuandyk1995@gmail.com
- Phone: +7 747 454 8448
- GitHub: [@lunarnuts](https://github.com/lunarnuts)

## 📄 License

This CV/resume content is personal and proprietary. The LaTeX template structure may be used as reference for educational purposes.

---

*Last updated: September 2025*