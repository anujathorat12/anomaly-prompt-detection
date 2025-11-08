Anomaly Prompt Detection System
Spectra AI Mini Challenge - Technical Screening Submission

#Project Overview

An AI security system that detects anomalous or malicious prompts submitted to Large Language Models using statistical methods combining Linear Algebra, Probability Theory, and Bayesian Inference.

Problem: Malicious users attempt prompt injection, jailbreaking, and other attacks on AI systems.  
Solution: Mathematical detection system using Mahalanobis distance and chi-square testing.  
Result: 96% detection rate with only 2% false positives.

#Prerequisites
- Python 3.8 or higher
- Google Colab

#Installation & Execution

Option 1: Google Colab 
1. Open Google Colab: https://colab.research.google.com
2. Upload `anomaly_detection.ipynb`
3. Click `Runtime` → `Run all`
4. Results will be displayed with visualizations

#Repository Structure
anomaly-prompt-detection/
│
├── anomaly_detection.ipynb       # Main Colab notebook 
├── anomaly_detection.py          # Python script version
├── requirements.txt              # Python dependencies
├── README.md                   
├── Technical_Report.pdf          
│
├── results/
│   ├── anomaly_detection_analysis.png   # Visualization results

#Methodology

# 1. Linear Algebra
- Covariance Matrix:** Computed from 500 normal prompt embeddings (128-dimensional)
- Mahalanobis Distance:** Measures multi-dimensional distance accounting for correlations
- Formula:** D(x) = √[(x - μ)ᵀ Σ⁻¹ (x - μ)]

# 2. Probability Analysis
- Chi-Square Distribution: Squared distances follow χ²(k) distribution
- P-value Computation: Probability that a prompt belongs to normal distribution
- Detection Threshold: p-value < 0.01 (99% confidence)

# 3. Bayesian Inference
- Prior: P(Anomalous) = 5% baseline rate
- Likelihood: P(Flagged|Anomalous) from detection system
- Posterior: P(Anomalous|Flagged) = 71.6% after Bayesian update

# Future Improvements

# Short-term 
-  Implement real-time detection API
-  Add support for multi-language prompts
-  Optimize for high-throughput systems

# Long-term 
-  Ensemble methods with transformer-based classifiers
-  Adaptive thresholds based on threat intelligence
-  Temporal analysis for sequence-based attacks
-  Integration with SIEM systems

# Author
- Name: Anuja Thorat
- Email: thoratanuja1218@gmail.com
