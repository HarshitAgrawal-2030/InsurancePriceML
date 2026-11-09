# InsurancePriceML
Predicts a person's health insurance charges from age, BMI, smoking status and other personal details using Linear Regression (pandas, matplotlib, seaborn, scikit-learn).
AI101 Mini-Project · School of AI and Data Engineering, IIT Ropar · Team [25] · Python 3.12

**Team and roles:**
| Member | Entry no. | GitHub handle | Role |
| Harshit Agarwal | 2026EEB1353 |[HarshitAgrawal-2030] |https://github.com/HarshitAgrawal-2030|   | Documentation lead |
| Aryan Hemanth Sawant | 2026MCB1516 | [aryan-s-iitrpr] |https://github.com/aryan-s-iitrpr| | Execution lead |
| Harshit Bansal | 2026ESB1476 | [HarshitBansal-2008] |https://github.com/HarshitBansal-2008| | PPT lead |
| Gajjela Sri Charan | 2026AIB1033 | [sricharan-iitrpr] |https://github.com/sricharan-iitrpr|  | Video lead |
All four members contributed code (see commit history).

**Project structure:**
InsurancePriceML/
├── data/
│   └── insurance.csv                              # Dataset (1,338 rows, 7 columns)
├── notebooks/
│   ├── Insurance_Premium_Linear_Regression.ipynb  # Full pipeline: load, clean, train, evaluate, plot
│   └── insurance.csv                              # Copy read by the notebook
├── Insurance_Premium_Prediction_AI101.pptx        # Project slides (5)
├── expected_output.png                            # Screenshot of a successful run
├── requirements.txt                               # Pinned library versions
├── .gitignore
└── README.md

**Dataset:**
`insurance.csv`, the Medical Cost Personal dataset on Kaggle. It has 1,338 rows and no missing values; the notebook removes 1 duplicate row.
Column	Description
`age`	Age of the person
`sex`	male / female
`bmi`	Body Mass Index
`children`	Number of children covered by the insurance
`smoker`	yes / no
`region`	northeast, northwest, southeast, southwest
`charges`	Insurance cost billed, used as the premium (target).

**Setup:**
Requires Python 3.12 and Git.
  bash
git clone https://github.com/HarshitAgrawal-2030/InsurancePriceML.git
cd InsurancePriceML
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt

**Steps to run:**
Run these commands from the repository folder, with the virtual environment active.
1.Execute the whole notebook:
   bash
   jupyter nbconvert --to notebook --execute notebooks/Insurance_Premium_Linear_Regression.ipynb --output executed_output.ipynb
   
2.Open the results and view the printed metrics and plots:
  bash
   jupyter notebook notebooks/executed_output.ipynb
   
To work interactively instead, run jupyter notebook notebooks/Insurance_Premium_Linear_Regression.ipynb and choose Run > Run All Cells.
The notebook reads 'insurance.csv' by relative path from the 'notebooks' folder, so keep the two files together.

**Expected output:**
The notebook prints the dataset shape, the train/test sizes (1,069 / 268) and these test-set metrics, using 'random_state=42':
| Metric | Test |
| MAE | 4,177.05 |
| MSE | 35,478,020.68 |
| RMSE | 5,956.34 |
| R² | 0.807 |
Example prediction (age 30, male, BMI 27.5, 1 child, non-smoker, southeast): 'Predicted insurance premium: 4,710.51'.
It also draws the charges histogram, the age and smoker charts, an actual vs predicted plot and a residual histogram.
![Expected output](expected_output.png).

**Links:**
Slides: Insurance_Premium_Prediction_AI101.pptx
Video (max 5:00): [Unlisted YouTube or Drive link]

**AI-use disclosure:**
Claude: created the slides, this README and 'requirements.txt' from our notebook and the course briefing. [How the team checked them]
[Any other tool: what it did, how you checked it]
[Confirm: no AI was used to generate the dataset or the results]
