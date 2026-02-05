# mmWave oscillators database

## Authors

[**Gustavo M. Hama**](mailto:gustavo.misawa-hama@univ-grenoble-alpes.fr)¹⁺²  
**Antônio A. L. de Souza**³  
**Ariana L. C. Serrano**²  
**Florence Podevin**¹  
**Sylvain Bourdel**¹  

### Affiliations

| | |
| :--- | :--- |
| <img src="images/TIMA_logo.png" alt="TIMA Logo" height="40"> | ¹ Univ. Grenoble Alpes, Grenoble INP, CNRS, TIMA, 38000 Grenoble, France |
| <img src="images/USP.png" alt="USP Logo" height="60"> | ² Laboratory of Microelectronics, University of São Paulo, São Paulo 05508-010, Brazil |
| <img src="images/UFPB_logo.png" alt="UFPB Logo" height="60"> | ³ Department of Electrical Engineering, Federal University of Paraíba, João Pessoa 58051-900, Brazil |

---

## 📊 Overview

This repository contains a comprehensive database gathering performance data from various research papers on mmWave oscillators. It is designed to assist researchers and designers in benchmarking and comparing state-of-the-art results in integrated technologies.

## 📝 Citation

If you use this database for your research, please cite it as:
> Gustavo M. Hama et al., "mmWave Oscillators Database," [Online]. Available: https://github.com/Gustavo-Hama/mmWave_oscillators_database

---

## 🔬 Database Schema & Parameter Definitions

The following table describes the parameters analyzed for each entry in the database:

| Parameter | Description |
| :--- | :--- |
| **DOI** | Digital Object Identifier for direct access to the source paper. |
| **Title** | The full title of the research publication. |
| **Main claim** | The primary innovation or contribution of the work. |
| **Where** | The publication venue (e.g., IEEE JSSC, T-MTT). |
| **Year** | The year the paper was published. |
| **Tech. Node** | The semiconductor process node (e.g., 28nm, 65nm). |
| **Process Technology** | The specific process used (e.g., CMOS, BiCMOS, SiGe). |
| **Tech. $f_T$ (GHz)** | Transition frequency of the transistors in the technology. |
| **Tech. $f_{max}$ (GHz)** | Maximum frequency of oscillation of the transistors. |
| **Buffers?** | Indicates if output buffers are included in the design/measurements. |
| **No. cores** | Total number of oscillator cores used (multicore or single core). |
| **Core area ($mm^2$)** | Physical area of the oscillator core only. |
| **Chip area ($mm^2$)** | Total die area, including pads and peripherals. |
| **Fundamental oscillator?** | Whether the output is the base frequency or a harmonic. |
| **$f_{osc}$ (GHz)** | The center operating oscillation frequency. |
| **Continuous?** | Indicates if the tuning is analog/continuous or discrete. |
| **FTR (%)** | Frequency Tuning Range as a percentage of the center frequency. |
| **$P_{DC}$ (mW)** | Power consumption of the oscillator core alone. |
| **Total $P_{DC}$ (mW)** | Total DC power consumption including all auxiliary circuits (e.g., buffers). |
| **$P_{out}$ (dBm)** | Measured output power of the oscillator. |
| **Efficiency (%)** | DC-to-RF power conversion efficiency. |
| **$\Delta f$ (MHz)** | The frequency offset used for the reported Phase Noise. |
| **$PN@ \Delta f$ (dBc/Hz)** | Phase Noise measured at the reported offset frequency. |
| **$PN@ 10\text{ MHz}$ (dBc/Hz)** | Phase Noise extrapolated for a 10 MHz offset. |
| **$FOM@ 10\text{ MHz}$ (dBc/Hz)** | Standard Figure of Merit calculated at a 10 MHz offset. |
| **$FOM_T@ 10\text{ MHz}$ (dBc/Hz)** | Figure of Merit including Tuning Range ($FTR$) at a 10 MHz offset. |

### Figure of Merit (FOM) Definitions

* **FOM ($FOM@10\,\text{MHz}$)**:  
  The standard Figure of Merit for VCOs, typically calculated as:
  
  $$
  FOM = PN_{10\,\text{MHz}} - 20\log_{10}\left(\frac{f_{osc}}{10 \text{ MHz}}\right) + 10\log_{10}\left(\frac{P_{DC}}{1 \text{ mW}}\right)
  $$

  where $PN_{10\,\text{MHz}}$ is the phase noise at a 10 MHz offset, $f_{osc}$ is the oscillation frequency, and $P_{DC}$ is the core DC power consumption.

* **Tuning Range Figure of Merit ($FOM_T@10\,\text{MHz}$)**:  
  An extended Figure of Merit that incorporates the Frequency Tuning Range ($FTR$):
  
  $$
  FOM_T = FOM + 20\log_{10}\left(\frac{FTR (\%)}{10}\right)
  $$

  where $FTR$ is the frequency tuning range expressed as a percentage of the center frequency.

---

## 🚀 How to Contribute

Contributions are welcome! If you would like to add a design to the database, please contact us by email.

## Acknowledgments

| | |
| :--- | :--- |
| <img src="images/NF_France_2030.png" alt="France 2030 NF-YACARI Logo" height="100"> | Part of this work was funded by the French National Research Agency (ANR-22-PEFT-0005) as part of France 2030 and the NF-YACARI project. |