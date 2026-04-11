Earnings Call Profit Prediction (Text Mining + Portfolio Optimization)

This project builds a profit-maximizing trading strategy using earnings call transcripts and structured financial signals. Instead of optimizing for classification accuracy alone, the model is designed to maximize portfolio-level returns by combining natural language processing with strategic capital allocation.

Overview
Predicts the probability of positive market-adjusted returns from earnings call transcripts
Converts predictions into long/short investment decisions
Optimizes for total profit, with AUC as a secondary metric
Achieved top leaderboard performance (Rank 1) in a competitive setting
Approach
1. Text Modeling (Fast + Interpretable)
TF-IDF vectorization (word + character n-grams)
Focus on front sections of transcripts (earnings summaries & key signals)
Lightweight linear models (Logistic Regression)
2. Feature Engineering
Extracted structured signals from transcripts:
EPS surprise
Revenue surprise
Numerical density, formatting cues (parentheses, “NM”)
Added time-based features:
Year, month, quarter
3. Model Blending
Combined:
Front-text model (primary signal)
Presentation-text model (secondary signal)
Tuned blending weights using time-based validation splits
Profit Optimization (Key Innovation)

Rather than treating predictions equally, the project:

Ranks companies by predicted probability
Allocates capital using tiered position sizing
Balances long vs short exposure
Applies probability sharpening to amplify strong signals

This transforms weak predictive signals into high-profit trading strategies.

Results
Rank 1 leaderboard performance
~$150k simulated profit
AUC ≈ 0.516 (demonstrating profit ≠ accuracy)
Tech Stack
Python (NumPy, Pandas)
scikit-learn (TF-IDF, Logistic Regression)
Regex-based feature extraction
Time-based cross-validation
Key Takeaways
Small predictive edges can generate large profits with proper allocation
Portfolio construction matters more than model complexity
Simple models + strong strategy > complex models without discipline
