# correlation_matthews_js
A lightweight, zero-dependency JavaScript utility for calculating evaluation metrics for machine learning models. Optimized for **imbalanced datasets** using the Confusion Matrix and Matthews Correlation Coefficient (MCC).

## Features

- **Matthews Correlation Coefficient (MCC):** Provides a balanced evaluation of binary classification, accurately handling class imbalance.
- **Confusion Matrix:** Fast, single-pass (`O(n)`) computation of TP, TN, FP, and FN.
- **Zero Dependencies:** Written in pure, modern JavaScript.

## Usage

```javascript
const calculateMcc = require('./calculateMcc');

// Ground truth and model predictions
const yTrue =;
const yPred =;

try {
    const mcc = calculateMcc(yTrue, yPred);
    console.log(`MCC Score: ${mcc.toFixed(4)}`); // Output value between -1.0 and +1.0
} catch (error) {
    console.error(`Error: ${error.message}`);
}
```

## Formula

$$MCC = \frac{TP \times TN - FP \times FN}{\sqrt{(TP + FP)(TP + FN)(TN + FP)(TN + FN)}}$$

## License

This project is licensed under the MIT License.
