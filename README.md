# Acoustic Indices Parametrisation

This repository provides a reproducible workflow for evaluating how different parameters —sampling frequency (`fs`), window size (`NFFT`), and window overlap (`Overlap`)— affect multiple acoustic index comparisons. This repository includes codefor the calculation of acoustic indices with 432 parameter iterations, the computation of non-metric multidimensional scaling (nMDS) and derived multivariate descriptors, and the assessment of the parametrisation influence using Bayesian models. In addition, we include code for a dashboard to visualize the influence of parametrisation on the nMDS, 10 audio file examples for each habitat studied, and the complete acoustic index computations for the full list of audio files.
We present examples from  both **terrestrial** and **underwater** soundscapes.

---

## 📁 Repository Structure

```text
acousticindices_parametrisation/
├── code_matlab_acousticindices/      # MATLAB scripts to compute acoustic indices
│   ├── terrestrial/
│   └── underwater/
├── code_r_glmm/                      # R scripts for Bayesian GLMM analysis
│   ├── terrestrial/
│   └── underwater/
├── code_r_multivariate/              # R scripts for NMDS & multivariate descriptors
│   ├── terrestrial/
│   └── underwater/
├── code_r_nMDS_dashboard/            # R Scripts to create a local dashboard
│   ├── terrestrial/
│   └── underwater/
├── outcome_acousticindices/          # Output: Acoustic indices as CSV
│   ├── terrestrial/
│   └── underwater/
├── outcome_multivariate/             # Output: nMDS plots and descriptors
│   ├── terrestrial/
│   └── underwater/
├── outcome_glmm/                     # Output: Bayesian model summaries and plots
│   ├── terrestrial/
│   └── underwater/
└── wav_directory/                    # Input audio recordings
│   ├── terrestrial/
│        ├── Bushland/
│        └── Urban/
│   └── underwater/
│        ├── Pocillopora/
│        └── Non-Pocillopora/                    

---

## 🎯 Project Goals

- Evaluate the influence of FFT parameters on ecoacoustic indices.
- Assess the stability of multivariate descriptors under different parameter settings.
- Contribute to standardisation in ecoacoustic analyses.

---

## 🧮 Acoustic Indices Computed

- **H** – Acoustic Entropy
- **ACI** – Acoustic Complexity Index
- **AEI** – Acoustic Evenness Index   
- **ADI** – Acoustic Diversity Index  
- **NDSI** – Normalised Difference Soundscape Index  

---

## 📈 Analyses Performed

- **Multivariate Ordination**: NMDS using `vegan`
- **Multivariate Descriptors**:
  - Centroid Distance
  - Habitat Dispersion
  - Kernel Density Overlap
  - Bhattacharyya Coefficient
- **Bayesian Generalized Linear Mixed Model**

---

## 🌐 Interactive Dashboards

Explore the parametrisation effects on the nMDS results online:

🌳 **Terrestrial NMDS Dashboard**  
👉 [https://juancarlosazofeifasolano.shinyapps.io/nmds_dashboard_terrestrial/](https://juancarlosazofeifasolano.shinyapps.io/nmds_dashboard_terrestrial/)

🌊 **Underwater NMDS Dashboard**  
👉 [https://juancarlosazofeifasolano.shinyapps.io/nmds_dashboard_underwater/](https://juancarlosazofeifasolano.shinyapps.io/nmds_dashboard_underwater/)

---

## 🚀 How to Use This Repository

### 1. Clone the Repository

```bash
git clone https://github.com/juancarlosazofeifasolano/acousticindices_parametrisation.git

### 2. Run MATLAB Scripts

For computing the the acoustic indices (H, ACI, AEI, ADI, NDSI) with the 432 unique iterations:
- Navigate to `code_matlab_acousticindices/`
- Use **MATLAB Desktop** or **[MATLAB Online](https://matlab.mathworks.com/)** to open and run `.mlx` Live Scripts for computing acoustic indices
- Results are saved automatically under `outcome_acousticindices/`

> ✅ All MATLAB scripts are set up to:
> - Use **relative paths** for seamless portability

### 3. Run R Scripts

For computing the ordination analyses and Bayesian models. Results from the full list of audio files are already included in the folders:
- Multivariate analyses: located in `code_r_multivariate/`
- Bayesian GLMMs (via `brms`): located in `code_r_glmm/`

> ✅ All R scripts are set up to:
> - Use **relative paths** for seamless portability
> - Automatically check and install any **missing R packages**

---

## 📝 Citation

This repository is part of a PhD research project focused on the **acoustic monitoring of ecosystems**.

Citation details will be added once the associated publications are available.

Author: Juan Carlos Azofeifa-Solano  
Institution: Centre for Marine Science and Technology, Curtin University, Australian Institute of Marine Science
Supervisors: Christine Erbe, Miles J. G. Parsons, Robert McCauley, Rohan Brooker
Colaborators: James Kemp

---

## 📬 Contact

For questions, collaborations, or feedback:

- Open an [issue on GitHub](https://github.com/juancarlosazofeifasolano/acousticindices_parametrisation/issues)


