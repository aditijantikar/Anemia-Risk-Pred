# Temporal Hierarchy Analysis of Inflammatory Biomarkers
## Generalizable Framework for Longitudinal Biomarker Relationship Discovery

### Project Overview
This project develops and validates a generalizable analytical framework for identifying temporal relationships between biomarkers in longitudinal health data. Using inflammatory bowel disease (IBD) biomarker data as a demonstration case, we test the **temporal hierarchy hypothesis**: that local tissue inflammation markers exhibit temporal priority over systemic markers of secondary complications.

### Course Context
This project was developed for **BENG 211: Systems Biology and Bioengineering I** at UC San Diego, taught by Dr. Benjamin Smarr.

**Project Team:**
- Pavithra Ramesh
- Aditi Jantikar
- Tejaswini Deshmukh
- Ananya Ramakrishnan

### Scientific Hypothesis

**Primary Hypothesis:**
"In chronic inflammatory conditions, local tissue inflammation markers exhibit temporal priority over systemic markers of secondary complications."

**Testable Predictions:**
1. Local inflammation biomarkers (calprotectin) will precede systemic outcome biomarkers (hemoglobin) with a detectable time lag
2. The temporal lag will be consistent with underlying pathophysiological mechanisms
3. Inflammation severity will correlate with the magnitude of systemic effects (dose-response)
4. The analytical framework will apply to other chronic inflammatory conditions

### Why This Matters

**Clinical Relevance:**
- Early detection: Local markers as leading indicators of systemic complications
- Personalized monitoring: Identify patient-specific temporal patterns
- Intervention timing: Predict when systemic effects will manifest
- Treatment optimization: Adjust therapy before complications develop

**Methodological Innovation:**
- Generalizable framework applicable to multiple diseases
- Discovers temporal relationships without assuming specific lag times
- Handles real-world data challenges (irregular sampling, missing data)
- Provides quantitative metrics for temporal relationships

### Dataset Description

**Data Source:**
Longitudinal biomarker measurements from an IBD patient spanning 1996-2025 (29 years), representing one of the most comprehensive personal biological monitoring datasets available.

**Key Biomarkers Analyzed:**

| Biomarker Level | Marker | Type | Measurements | Clinical Significance |
|-----------------|--------|------|--------------|----------------------|
| Local Inflammation | Fecal Calprotectin | Gut-specific | 223 | Active intestinal inflammation |
| Systemic Inflammation | C-Reactive Protein (CRP) | Body-wide | Variable | Systemic inflammatory response |
| Intermediate Effect | Serum Ferritin | Iron stores | Variable | Body iron depletion |
| Clinical Outcome | Hemoglobin | Anemia marker | 149 | Oxygen-carrying capacity |

**Data Files:**
- `LS Biomarkers Timeseries.csv` - Original time series format (1993-2025)
- `LLM_Biomarkers_Long.csv` - Long format for time series analysis
- `LLM_Biomarkers_Wide.csv` - Wide format for statistical modeling

### Analytical Framework

Our generalizable framework consists of four analytical phases:

**Phase 1: Biomarker Characterization**
- Descriptive statistics and data quality assessment
- Event detection and classification
- Temporal pattern identification

**Phase 2: Cross-Correlation Analysis**
- Systematic testing of multiple time lags (0-12 weeks)
- Identification of optimal temporal relationships
- Statistical significance testing

**Phase 3: Event-Based Analysis**
- Comparison of outcomes following high vs. normal inflammation periods
- Effect size quantification
- Threshold identification

**Phase 4: Dose-Response Modeling**
- Relationship between inflammation severity and systemic impact
- Threshold vs. linear relationship testing
- Predictive model development

### Methods Overview

**Statistical Approaches:**
- Pearson correlation for linear relationships
- Time-lagged cross-correlation for temporal pattern discovery
- Paired statistical tests for event-based comparisons
- Dose-response trend analysis
- ROC analysis for threshold optimization

**Handling Data Challenges:**
- Linear interpolation for irregular sampling intervals
- Missing data strategies
- Multiple comparison corrections
- Sensitivity analysis for robustness

### Generalizability: Application to Other Diseases

This framework can be directly applied to other chronic inflammatory conditions:

| Disease Context | Local Marker | Systemic Marker | Predicted Mechanism |
|-----------------|--------------|-----------------|---------------------|
| Rheumatoid Arthritis | Synovial fluid cytokines | Serum CRP | Joint inflammation → systemic response |
| Chronic Kidney Disease | Urine albumin | Serum creatinine | Glomerular damage → nephron loss |
| COPD | Sputum neutrophils | Systemic inflammatory markers | Airway inflammation → systemic spillover |
| Type 2 Diabetes | HbA1c | Microalbuminuria | Hyperglycemia → microvascular damage |
| Heart Failure | BNP | Troponin/EF | Cardiac stress → myocardial damage |


### Getting Started

**Prerequisites:**
```bash
Python 3.8+
pandas >= 1.3.0
numpy >= 1.21.0
matplotlib >= 3.4.0
seaborn >= 0.11.0
scipy >= 1.7.0
statsmodels >= 0.13.0
```

**Installation:**
```bash
git clone [repository-url]
cd LargeLarryModelers
pip install -r requirements.txt
```

### Technical Skills Demonstrated

**Data Science:**
- Time series analysis and preprocessing
- Cross-correlation and lagged regression
- Event detection and classification
- Statistical hypothesis testing
- Data visualization for biological insights

**Python Tools:**
- pandas: Data manipulation and time series handling
- numpy: Numerical computing and array operations
- scipy: Statistical testing and correlation analysis
- matplotlib/seaborn: Publication-quality visualizations
- statsmodels: Advanced statistical modeling

**Systems Biology:**
- Multi-scale biomarker analysis
- Temporal dynamics in biological systems
- Integration of local and systemic measurements
- Mechanistic interpretation of statistical relationships

### Limitations and Future Directions

**Current Limitations:**
- Single-subject dataset limits population-level generalizability
- Irregular measurement intervals create analytical challenges
- Confounding factors (diet, medication, supplements) not controlled
- Causation cannot be definitively established from observational data

**Future Work:**
- Multi-patient validation cohort
- Include additional intermediate biomarkers (transferrin saturation)
- Machine learning models for personalized lag prediction
- Prospective validation study with standardized measurement intervals
- Application to other chronic inflammatory disease populations

### Educational Value

This project demonstrates:
- Complete workflow from hypothesis to validated findings
- Rigorous statistical methodology for biological data
- Generalizable analytical framework development
- Real-world data handling and quality control
- Scientific communication and visualization

### References

1. Wang, W., et al. (2025). The role of Calprotectin in the diagnosis and treatment of inflammatory bowel disease. International Journal of Molecular Sciences, 26(5), 1996.

2. Mooiweer, E., et al. (2014). Fecal Hemoglobin and Calprotectin Are Equally Effective in Identifying Patients with Inflammatory Bowel Disease with Active Endoscopic Inflammation. Inflammatory Bowel Diseases, 20(2), 307-314.

3. Vavricka, S. R., et al. (2018). The Vampire Study: Significant elevation of faecal calprotectin in healthy volunteers after 300 ml blood ingestion. United European Gastroenterology Journal, 6(7), 1007-1014.

4. Hassan, M., et al. (2024). Correlation of hemoglobin level with new inflammatory markers. Cureus.

5. Logan, M., et al. (2019). The reduction of faecal calprotectin during exclusive enteral nutrition. Alimentary Pharmacology & Therapeutics, 50(6), 664-674.

### Contact

- Aditi Jantikar and Pavithra Ramesh UC San Diego
- Instructor: Dr. Benjamin Smarr

### License

This project is developed for educational purposes as part of BENG 211 coursework at UC San Diego.

### Acknowledgments

- Dr. Benjamin Smarr for dataset access and project guidance
- LS for three decades of meticulous biological data collection
