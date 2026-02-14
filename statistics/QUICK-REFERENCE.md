# Statistics Quick Reference

A quick lookup guide for common statistics concepts and formulas.

## Mean, Median, Mode

| Measure | Formula | Use Case |
|---------|---------|----------|
| Mean | $\frac{\sum x_i}{n}$ | Center of data |
| Median | Middle value | When outliers present |
| Mode | Most frequent | Most common value |

### Relationship (Pearson's Formula)

For moderately skewed distributions:
$$\text{Mode} \approx 3(\text{Median}) - 2(\text{Mean})$$

## Spread

| Measure | Formula | Interpretation |
|---------|---------|-----------------|
| Range | Max - Min | Total spread |
| Variance | $\sigma^2 = \frac{\sum(x_i - \bar{x})^2}{n}$ | Average squared deviation |
| Std Dev | $\sigma = \sqrt{\text{Variance}}$ | Typical deviation |
| IQR | Q3 - Q1 | Range of middle 50% |

### IQR (Interquartile Range) Details

- **Q1**: 25th percentile (1st quartile)
- **Q3**: 75th percentile (3rd quartile)
- **IQR = Q3 - Q1**: Resistant to outliers

**Outlier Detection:**
- Lower whisker: $Q1 - 1.5 × \text{IQR}$
- Upper whisker: $Q3 + 1.5 × \text{IQR}$
- Any value outside these bounds is an outlier

## Probability Rules

```
1. 0 ≤ P(A) ≤ 1
2. P(A) + P(not A) = 1
3. P(A or B) = P(A) + P(B) - P(A and B)
4. P(A and B) = P(A) × P(B|A)
5. P(A|B) = P(A and B) / P(B)
```

## Standard Normal Distribution (Z-scores)

| Z-score | % within range |
|---------|---|
| ±1σ | 68% |
| ±2σ | 95% |
| ±3σ | 99.7% |

## Hypothesis Testing

- **Null Hypothesis (H₀)**: No effect or no difference
- **Alternative Hypothesis (H₁)**: There is an effect or difference
- **Type I Error (α)**: Rejecting true null hypothesis
- **Type II Error (β)**: Failing to reject false null hypothesis
- **P-value**: Probability of observed results if H₀ is true
- **Significance level**: Usually α = 0.05

## Python Libraries

```
numpy      - Numerical computation
scipy      - Scientific computing (stats module)
pandas     - Data manipulation
matplotlib - Visualization
seaborn    - Statistical visualization
statsmodels - Statistical modeling
```

## Common Distributions Reference

| Distribution | When to use | Parameters |
|---|---|---|
| Normal | Natural phenomena | μ, σ |
| Binomial | Success/failure repeated | n, p |
| Poisson | Count of events | λ |
| Exponential | Time between events | λ |
| Uniform | Equal likelihood | a, b |