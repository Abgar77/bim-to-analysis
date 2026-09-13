# BIM-to-Analysis Workflow and Design Surrogate

Independent verification of a four-storey braced steel frame, taking a Revit structural model through Oasys GSA and comparing the results against first-principles Eurocode 3 design calculations.

Base structure: 4-storey braced steel office building, 24.5 x 32.5 m on plan, 22 m tall, S355, with a central transfer truss at first floor carrying the internal columns. Originally designed as coursework at Imperial College London.

What this does
Rebuilds the frame as a Revit structural model with a coordinated analytical representation.
Exports to Oasys GSA and runs linear static, buckling eigenvalue and P-delta analyses.
Reconciles GSA's results against the original Python Eurocode 3 checks, resolving each discrepancy to a cause.
Returns member utilisations to Revit as shared parameters via Dynamo.
Generates a parametric dataset of frame variants and trains a surrogate model predicting utilisation, deflection and steel tonnage.
Repository layout
Path	Contents
baseline/	Frozen reference: member register, load take-down, Python design checks
revit/	Revit model, exported schedules, drawing set, Dynamo scripts
gsa/	GSA models, section mapping database, exported results
sweep/	Parametric generation scripts and dataset
surrogate/	Notebooks, trained models, extrapolation study
report/	Verification report
Status

In progress.

Author

Abgar Ivanyan - MEng Civil Engineering, Imperial College LondonIndependent verification of a four-storey braced steel frame, taking a Revit structural model through Oasys GSA and comparing the results against first-principles Eurocode 3 design calculations.
