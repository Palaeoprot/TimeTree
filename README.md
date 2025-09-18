# TimeTree 🌳⏰

**A basic method for phylogenetic time calibration and evolutionary analysis**

[![GitHub](https://img.shields.io/badge/GitHub-TimeTree-blue)](https://github.com/Palaeoprot/TimeTree)
[![Python](https://img.shields.io/badge/Python-3.8+-green)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org)
[![License](https://img.shields.io/badge/License-MIT-red)](LICENSE)

---

## 🚀 **Project Overview**

TimeTree is a computational framework designed for phylogenetic time calibration, evolutionary timeline analysis, and large-scale phylogenomic studies

### **Key Capabilities**
- **Multi-source phylogenetic integration** from major databases (NCBI, Ensembl, UniProt)
- **Sophisticated time calibration** using fossil constraints and molecular clock methods  
- **Large-scale tree synthesis** supporting thousands of species across vertebrate clades
- **Interactive visualization** with publication-quality outputs
- **Reproducible workflows** with comprehensive documentation and provenance tracking

---


## 📊 **Features & Functionality**

### **🧬 Core Phylogenetic Operations**
- **Tree Loading & Parsing**: Support for Newick, Nexus, and NeXML formats
- **Multi-tree Synthesis**: Combine phylogenies from different sources and studies
- **Topology Validation**: Automated consistency checking and conflict resolution
- **Branch Length Optimization**: Maximum likelihood and Bayesian approaches

### **⏰ Time Calibration Engine**
- **Fossil Constraint Integration**: Flexible fossil calibration with uncertainty
- **Molecular Clock Models**: Relaxed clocks, local clocks, and rate variation
- **Cross-Validation**: Statistical assessment of calibration accuracy
- **Uncertainty Propagation**: Maintains temporal uncertainty throughout analysis

### **🗄️ Data Integration Hub**
- **UniProt Integration**: Protein sequences and taxonomic data
- **NCBI Taxonomy**: Standardized taxonomic classification
- **Ensembl Genomics**: Gene families and orthology relationships
- **Published Phylogenies**: Integration with major phylogenetic studies

### **📈 Analysis & Visualization**
- **Interactive Tree Viewers**: Web-based exploration of time-calibrated trees
- **Comparative Analyses**: Rate variation, diversification patterns
- **Statistical Testing**: Molecular clock tests, rate correlation analysis
- **Export Formats**: Multiple output formats for downstream analysis

---

## 🛠️ **Installation & Setup**

### **Quick Start**
```bash
# Clone the repository
git clone https://github.com/Palaeoprot/TimeTree.git
cd TimeTree

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter notebook
jupyter notebook TimeTree.ipynb
```

### **Dependencies**
```python
# Core scientific computing
numpy>=1.21.0
pandas>=1.3.0
polars>=0.15.0

# Bioinformatics
biopython>=1.79
ete3>=3.1.2

# Phylogenetics
dendropy>=4.5.0

# Visualization
matplotlib>=3.5.0
seaborn>=0.11.0
plotly>=5.0.0

# API interactions
requests>=2.26.0

# Jupyter ecosystem
jupyter>=1.0.0
ipywidgets>=7.6.0
```

### **System Requirements**
- **Python**: 3.8 or higher
- **Memory**: 4GB RAM minimum (16GB+ recommended for large datasets)
- **Storage**: 2GB free space for cache and outputs
- **Network**: Internet access for API data retrieval

---

## 📖 **Usage Examples**

### **Basic Time Calibration**
```python
from timetree import TimeTreeAnalysis, CalibrationConfig

# Initialize analysis
config = CalibrationConfig(
    fossil_constraints="data/fossils.csv",
    molecular_clock="relaxed_exponential",
    calibration_method="beast2"
)

analysis = TimeTreeAnalysis(config)

# Load phylogenetic data
tree = analysis.load_tree("vertebrate_phylogeny.nwk")
analysis.add_fossil_constraints()

# Perform time calibration
calibrated_tree = analysis.calibrate_tree()
analysis.validate_calibration()

# Generate outputs
analysis.export_tree("calibrated_vertebrates.nwk")
analysis.create_visualization("timeline.html")
```

### **Multi-Source Data Integration**
```python
from timetree import DataIntegrator

# Integrate multiple data sources
integrator = DataIntegrator()
integrator.add_uniprot_data("Mammalia")
integrator.add_ncbi_taxonomy()
integrator.add_published_phylogeny("upham_mammals_2019.tre")

# Synthesize comprehensive dataset
unified_data = integrator.synthesize()
time_calibrated = integrator.apply_temporal_framework()
```

### **Large-Scale Vertebrate Analysis**
```python
from timetree import VertebrateTimeTree

# Initialize vertebrate-specific analysis
vertebrates = VertebrateTimeTree()

# Load major vertebrate clades
vertebrates.load_mammals("upham_et_al_2019")
vertebrates.load_birds("jetz_et_al_2012")  
vertebrates.load_fish("betancur_et_al_2017")
vertebrates.load_amphibians("jetz_pyron_2018")

# Create unified time tree
unified_tree = vertebrates.synthesize_clades()
vertebrates.validate_temporal_consistency()

# Export comprehensive dataset
vertebrates.export_timetree("unified_vertebrates.nwk")
```

---

## 📚 **Scientific Context**

### **Phylogenetic Time Calibration Challenges**
Time-calibrated phylogenies are fundamental to evolutionary biology, enabling researchers to:
- **Date evolutionary events** and understand the timing of diversification
- **Correlate evolution with geological/climatic changes**
- **Perform comparative analyses** across species and clades
- **Inform conservation priorities** based on evolutionary distinctiveness

However, generating reliable time-calibrated trees faces several challenges:
- **Fossil record incompleteness** and dating uncertainties
- **Rate variation** across lineages and through time  
- **Computational scalability** for large phylogenies
- **Integration of disparate data sources** and methodologies

### **TimeTree Solutions**
TimeTree addresses these challenges through:
- **Robust statistical frameworks** for uncertainty quantification
- **Multi-source evidence integration** reducing reliance on single datasets
- **Scalable computational architecture** enabling genome-scale analyses  
- **Transparent methodology** with comprehensive documentation

---

## 🎯 **Use Cases & Applications**

### **Research Applications**
- **Macroevolutionary Studies**: Dating major evolutionary transitions
- **Comparative Genomics**: Evolutionary context for gene family evolution
- **Conservation Biology**: Phylogenetic diversity assessment
- **Paleobiology**: Integration of fossil and molecular evidence
- **Climate-Evolution Studies**: Correlating diversification with environmental change

### **Educational Applications**
- **Graduate Coursework**: Hands-on phylogenetic analysis training
- **Research Training**: Best practices in evolutionary data analysis
- **Workshop Material**: Structured tutorials and examples
- **Reproducible Research**: Template workflows for phylogenetic studies

---

## 📈 **Performance & Scalability**

### **Benchmarking Results**
- **Small datasets** (< 100 species): < 5 minutes complete analysis
- **Medium datasets** (100-1000 species): 15-60 minutes depending on calibration method
- **Large datasets** (1000+ species): Hours to days, optimized for cluster computing
- **Memory efficiency**: Polars-based processing for large dataframes

### **Optimization Features**
- **Intelligent caching** reduces redundant API calls
- **Parallel processing** where computationally feasible
- **Memory management** for large phylogenetic datasets
- **Progressive results** with intermediate checkpoints

---


## 📄 **Citation & References**

### **Citing TimeTree**
If you use TimeTree in your research, please cite:

```bibtex
@software{timetree2025,
  title={TimeTree: A comprehensive toolkit for phylogenetic time calibration and evolutionary analysis},
  author={[Your Name]},
  year={2025},
  url={https://github.com/Palaeoprot/TimeTree},
  version={1.0}
}
```

### **Key References**
- **Upham et al. (2019)**: Mammalian phylogenetic framework - *PLOS Biology* 17(12): e3000494
- **Betancur-R et al. (2017)**: Fish phylogenetic classification - *BMC Evolutionary Biology* 17:162  
- **Jetz et al. (2012)**: Global bird phylogenies - *Nature* 491, 444-448
- **Drummond & Rambaut (2007)**: BEAST phylogenetic software - *BMC Evolutionary Biology* 7:214

### **Data Sources**
- **UniProt Consortium** (2023): Universal protein resource
- **NCBI Taxonomy** (2023): Taxonomic classification database
- **Ensembl** (2023): Comparative genomics resource
- **TimeTree** (Hedges et al.): Timetree of life database

---

## 📊 **Project Status**

### **Current Version**: 1.0.0
### **Development Status**: Active
### **Last Updated**: September 2025

### **Recent Updates**
- ✅ Core time calibration framework
- ✅ Multi-database integration  
- ✅ Interactive visualization tools
- ✅ Comprehensive documentation
- 🔄 Performance optimization (in progress)
- 📋 Additional taxonomic groups (planned)
- 📋 Machine learning enhancements (planned)

---

## 📧 **Contact & Collaboration**

For questions, collaborations, or contributions:
- **GitHub**: [@Palaeoprot](https://github.com/Palaeoprot)
- **Issues**: [Project Issues](https://github.com/Palaeoprot/TimeTree/issues)
- **Discussions**: [Community Forum](https://github.com/Palaeoprot/TimeTree/discussions)

---

## 📜 **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
