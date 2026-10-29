# Breast-cancer death risk calculator (women aged ≥70 years, breast-conserving surgery)

Web calculator for the predicted cumulative incidence of breast-cancer death (other-cause death as a competing event)
at 3, 5 and 10 years after diagnosis, with a 10-year incidence curve and the model-based risk group.
Xiangya Hospital of Central South University.

- Model: CoxBoost-FG (likelihood-based boosting of the Fine–Gray subdistribution hazard).
- Development data: Surveillance, Epidemiology, and End Results (SEER) Program, Incidence – SEER Research Data,
  17 Registries, Nov 2025 Sub (2000–2023).
- The model includes year of diagnosis; the calculator uses 2023, the most recent year of the development data.

## Files

`index.html` (welcome page and prediction page), `model.js` (model parameters), `logo.png`.
`model.js` contains only aggregate model parameters (coefficients, the means and standard deviations used for
standardisation, and baseline cumulative subdistribution hazards on a monthly grid); it contains no patient-level
data. All calculations run in the visitor's browser; nothing that is entered is sent or stored.

## Intended use

For research and education only; not intended to guide treatment decisions for individual patients. Developed in
women aged ≥70 years with T1–T2, N0–N1 or Nx invasive ductal carcinoma treated with breast-conserving surgery
(diagnosed 2010–2023); internal validation only.
