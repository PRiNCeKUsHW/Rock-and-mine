# Rock vs Mine Prediction (Sonar Data)

A machine learning project that uses **sonar signals** to predict whether an object under water is a **rock (R)** or a **mine (M)**. It uses a **Logistic Regression** model.

## Dataset

[UCI Sonar Dataset](https://archive.ics.uci.edu/dataset/151/connectionist+bench+sonar+mines+vs+rocks): 208 samples. Each one has 60 numeric features (sonar energy at different frequency bands) and a label of `R` or `M`.

## Workflow

1. Load the data with Pandas (no header row)
2. Explore it: shape, statistics, class balance, group means
3. Split features (columns 0 to 59) and label (column 60)
4. Train/test split (90/10, stratified so both classes are balanced)
5. Train a Logistic Regression model
6. Measure accuracy on training and test data
7. Build a predictive system for a new sonar reading

## Results

| Data | Accuracy |
|------|----------|
| Training | ~83.4% |
| Testing | ~76.2% |

## Tech Stack

- Python
- NumPy, Pandas
- scikit-learn (`LogisticRegression`, `train_test_split`, `accuracy_score`)
- Jupyter Notebook

## How to Run

```bash
git clone https://github.com/PRiNCeKUsHW/Rock-and-mine.git
cd "Rock-and-mine/Rock and Mine ML project"
pip install numpy pandas scikit-learn jupyter
jupyter notebook sonar.ipynb
```

To test a new reading, replace `input_data` in the last cell with 60 values and run it.

## Project Structure

```
Rock and Mine ML project/
├── Copy of sonar data.csv   # Dataset
└── sonar.ipynb              # Analysis, training and prediction
```
