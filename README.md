# Population Pharmacokinetic Report Template

This is a Quarto-based template for pharmacometric reports. Follow the instructions below to render the project successfully.

### **Prerequisites**

#### 1. **Install Quarto**  
- Download and install Quarto from [quarto.org](https://quarto.org).  
- Verify the installation:
   ```bash
   quarto --version
   ```

#### 2. **Set Up Your IDE**  
- **RStudio**:  
   - Ensure you are using **version 2022.07 or later** (Quarto is included).  

- **VS Code**:  
   - Install the **Quarto extension** from the Extensions Marketplace.

#### 3. **LaTeX for PDF Rendering**  
- Install **TinyTeX** (only if you need PDFs):
   ```bash
   quarto install tinytex
   ```


---

### **How to Render the Project**

Once everything is installed, navigate to the project directory and run:

```bash
quarto render
```

This will generate the report in the `report` directory. Open the PDF to ensure everything has rendered correctly.

---

### **Troubleshooting**

If rendering fails, try the following:

1. **Verify LaTeX Installation:**  
   Run `pdflatex` to confirm LaTeX is installed correctly:
   ```bash
   pdflatex --version
   ```

2. **Check Dependencies:**  
   Ensure that all required LaTeX packages are installed:
   ```bash
   tlmgr install tabularray
   ```

3. **Update LaTeX:**  
   Ensure your LaTeX distribution is up-to-date:
   ```bash
   tlmgr update --self --all
   ```

---


### **Project Structure**

```
.
├── _quarto.yml            # Quarto configuration file
├── index.qmd              # Cover page and metadata for the report
├── sections               # Folder containing different sections of the report
│   ├── executive_summary.qmd
│   ├── introduction.qmd
│   ├── methods.qmd
│   ├── results.qmd
│   ├── discussion.qmd
│   └── conclusion.qmd
├── appendices             # Additional information and appendices
│   └── tez.qmd
├── figures                # Figures referenced in the report
│   └── figure1.png
├── data                   # Data files used in the analysis
│   ├── data.csv
│   └── data_preparation.R # Scripts for data preprocessing
├── scripts                # Code for analysis and modeling
│   └── analysis.R
├── custom-template.docx   # Custom Word template for DOCX output (optional)
├── word-template
│   └── v3_Pharmacometrics_Report_Template_Word.docx  # Word template for PMx Report (manual)
├── report                 # Folder for rendered outputs
│   └── PopPK-Report.pdf
└── README.md              # Documentation for the project
```
