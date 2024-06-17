# Feature Score Calculator Module

## Overview

The Feature Score Calculator module is designed to calculate Fisher's scores for features in a dataset, facilitating feature selection and analysis tasks. This module preprocesses data, computes Fisher's scores for each feature with respect to a target variable, and provides scaled scores for interpretation.

## Features

- Preprocesses dataset:
  - Converts non-numeric features using label encoding.
  - Handles missing values by replacing with column means.
  - Standardizes numeric features for consistency.

- Computes Fisher's scores:
  - Calculates the score for each feature based on its mean and variance across different classes of the target variable.
  - Scales scores to a 0-100 range for easier interpretation.

## Usage

### Installation

1. Clone the repository:
   ```
   git clone <repository_url>
   ```

2. Install required dependencies:
   ```
   pip install -r requirements.txt
   ```

### Example

```python
import pandas as pd
from feature_score_calculator import FeatureScoreCalculator

# Load your dataset
data = pd.read_csv('your_dataset.csv')

# Initialize FeatureScoreCalculator
target_variable = 'Target'
feature_names = data.columns.drop(target_variable)
fsc = FeatureScoreCalculator(data, target_variable, feature_names)

# Display feature scores
fsc.display_scores()
```

### Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn

## Contributors

- Sanjay (sanjaykabaddi5858@gmail.com)
  
## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by Fisher's discriminant analysis.
- Built with scikit-learn and pandas.

---
