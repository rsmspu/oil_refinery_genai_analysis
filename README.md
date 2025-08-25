# oil_refinery_genai_analysis
A case study on Multimodal anomaly detection in Oil rigs sensor data

**Introduction:**

Large scale oil refieneries are equipped with heavy machinery(boilers, engines, turbines, etc.) and are continuoly monitored by thousands of sensors for process efficiency,
environmental safety, and predictive maintenance purposes. The data generated here would be both structured and unstructured, sensors capture monitoring data and operators 
log their observations during their regular visits.

**Objective:**
Design and demonstrate a prototype system that detects anomalies in oil rig operations by combining sensor time series data and operator text logs.

**Problem Statement:**
1. Detect Anomalies in sensor data
2. Correlate anomalies with operator logs
3. Summarise the results and generate insights, so that there is no additional cost involved.
4. Deploy it for better utilization and data based value generation

We built a complete, enterprise-grade AI pipeline for oil rig anomaly detection, text correlation, and predictive maintenance - ready for production deployment.

**Project Components Overview:**
Here is the technical architecture design for this project:
<img width="1010" height="307" alt="image" src="https://github.com/user-attachments/assets/16a6fab6-e61e-4826-9cae-f5256935cb92" />

Module Deep Dive:
**Module 0: Synthetic Raw Data Generation**
Here are the key variations oil rig synthetic data includes:
**Sensor Data Variations:**


**Temporal Patterns:**

1. Daily cycles: Higher activity during day shifts (6 AM - 6 PM)
2. Weekly patterns: Reduced operations during weekends
3. Seasonal effects: Temperature variations, weather impact on offshore operations
4. Maintenance windows: Planned shutdowns every 30-90 days

**Equipment-Specific Patterns:**

1. Pumps: Flow rate correlates with pressure differential
2. Compressors: Power consumption increases with outlet pressure
3. Generators: Voltage/frequency stability with load variations
4. Separators: Level control cycles, pressure vessel dynamics

**Anomaly Types:**

1. Gradual degradation: Bearing wear, fouling, corrosion (weeks to months)
2. Sudden failures: Seal ruptures, electrical faults, blockages
3. Oscillations: Mechanical looseness, control instability
4. Drift: Sensor calibration issues, process parameter shifts

**Operator Log Variations:**


**Content Types:**

1. Maintenance logs: Scheduled/unscheduled repairs, part replacements
2. Operational notes: Process adjustments, production rates
3. Safety observations: Near-misses, safety system tests
4. Environmental logs: Weather conditions, emissions monitoring

**Language Variations:**
1. Technical terminology vs. colloquial descriptions
2. Different levels of detail (terse vs. verbose)
3. Varying expertise levels among operators
4. Abbreviations and industry-specific jargon
   
**Module 1: Data Preprocessing & Quality Assessment**

**Purpose:** Transform raw sensor data and operator logs into analysis-ready format
**Key Features:**

✅ Automated data ingestion and validation

✅ Quality assessment with 4-metric scoring (Completeness, Consistency, Validity, Anomalies)

✅ Smart missing data handling (KNN, interpolation, forward-fill)

✅ Advanced feature engineering (75+ time series features)

✅ Equipment-specific normalization and scaling


**Module 2: Multi-Method Anomaly Detection**

**Purpose:** Detect equipment anomalies using ensemble of advanced algorithms
**Key Features:**

✅ Isolation Forest: Fast, scalable unsupervised detection

✅ Statistical Methods: Z-score, IQR, MAD detection

✅ Matrix Profile: Pattern-based anomaly identification

✅ Change Point Detection: Structural break identification

✅ Ensemble Scoring: Weighted combination for robust results

**Module 3: NLP Text Correlation**

**Purpose:** Correlate sensor anomalies with operator communications using AI
**Key Features:**

✅ BERT Embeddings: Semantic understanding of operator logs

✅ Temporal Correlation: Time-window based anomaly-log matching

✅ Topic Modeling: Automatic discovery of communication themes

✅ Similarity Analysis: Cosine similarity for semantic matching

✅ Equipment Mapping: Smart resolution of equipment references

✅ Pattern Analysis: Equipment, temporal, and severity patterns

**Module 4: AI-Powered Insight Generation**

**Purpose:** Generate actionable insights and predictive maintenance recommendations
**Key Features:**

✅ Predictive Modeling: ML-based failure prediction (30-day horizon)

✅ Risk Assessment: Multi-factor equipment risk scoring

✅ Generate Insights: GPT/Claude powered analysis and recommendations

After all these modules are developed, an app can is built using streamlit for users to input simulated/real data and get the reports generated to be shared with plants.


