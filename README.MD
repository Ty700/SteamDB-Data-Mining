# Steam Game Recommendation System

A comprehensive data mining project analyzing 122,000+ Steam games to build recommendation systems using association rule mining and collaborative filtering techniques.

## 📋 Project Overview

This project explores game recommendation strategies by combining traditional data mining methods (frequent itemsets, association rules) with modern machine learning approaches (matrix factorization). The analysis reveals patterns in game tags, user preferences, and success factors to generate actionable insights for both game developers and players.

**Course:** CSCE 676 - Data Mining & Analysis  
**Institution:** Texas A&M University  
**Semester:** Spring 2026  
**Author:** Tyler Scotti

## 🎯 Objectives

- Identify tag combinations that predict highly-rated games using association rule mining
- Build a collaborative filtering recommendation system despite extreme data sparsity
- Compare pattern-based vs. model-based recommendation approaches
- Analyze free-to-play vs. paid game success patterns
- Generate actionable insights for game developers

## 📊 Dataset

**Source:** [Steam Games Dataset](https://www.kaggle.com/datasets/fronkongames/steam-games-dataset) (Kaggle)

**Size:** 122,611 games with 29 features (after cleaning)

**Key Features:**
- Game metadata: name, release date, price, developers, publishers
- User engagement: positive/negative reviews, recommendations, playtime metrics
- Categorization: 452 unique tags, genres, categories
- Quality metrics: user scores, Metacritic scores

**Notable Characteristics:**
- 452 unique user-generated tags (average 9.6 per game)
- 67.7% of games have reviews; 32.3% are "cold-start" cases
- 23% free-to-play games
- Exponential growth post-2013 (Steam Direct era)

## 🔧 Techniques

### Course Techniques
- **Frequent Itemset Mining:** Apriori algorithm on game tag co-occurrences
- **Association Rule Learning:** Generate rules linking tag combinations to success metrics
- **Clustering:** K-means on game features

### Beyond-Course Techniques
- **Collaborative Filtering:** Matrix factorization using Truncated SVD
- **Content-Based Filtering:** Tag similarity with TF-IDF weighting
- **Hybrid Recommendation:** Combining association rules and collaborative filtering

## 📈 Key Findings (Checkpoint 1 - EDA)

### Data Characteristics
- **Review Sparsity:** Only 40% of games have ≥100 reviews needed for reliable collaborative filtering
- **Price-Quality Independence:** Correlation between price and review quality = 0.03 (essentially zero)
- **Tag Distribution:** Power law with top tags (Indie, Action, Adventure) in 20-30% of games
- **Temporal Trends:** Average price declined from $0.70 (2005) to $0.15 (2025) while quality improved

### Observations
1. Popular games receive both positive AND negative reviews (r=0.82 correlation)
2. Free-to-play games can achieve ratings equal to premium games
3. Market saturation: 25,000 releases in 2024 vs. 500 in 2010
4. Missing tags (32%) correlate strongly with low engagement/abandoned games

## 🔍 Research Questions

1. **RQ1:** What tag combinations most strongly predict highly-rated games?
2. **RQ2:** Can matrix factorization generate meaningful recommendations despite 60% cold-start rate?
3. **RQ3:** How do explicit patterns (association rules) differ from latent patterns (SVD)?
4. **RQ4:** Do free-to-play and paid games exhibit different success patterns?

## 📊 Methodology

### Phase 1: Data Preprocessing
- Tag normalization and filtering (games with ≥3 tags)
- Review filtering (games with ≥100 reviews for collaborative filtering)
- Temporal train/test split (pre-2023 train, 2023+ test)

## 🎓 Educational Value

This project demonstrates:
- Professional data analysis workflow on real-world messy data
- Handling extreme data sparsity (32% missing tags, 60% cold-start games)
- Combining traditional and modern data mining techniques
- Clear documentation and reproducible research practices
- Strategic decision-making based on data characteristics

## 📄 License

This project is for educational purposes as part of CSCE 676 coursework at Texas A&M University.

**Dataset License:** [Kaggle Community License](https://www.kaggle.com/datasets/fronkongames/steam-games-dataset)

## 🙏 Acknowledgments

- **Dataset:** FronKongames (Kaggle)
- **Course:** CSCE 676 - Data Mining & Analysis, Prof. James Caverlee
- **Institution:** Texas A&M University
- **Tools:** scikit-learn, mlxtend, pandas, matplotlib, seaborn

## 📧 Contact

Tyler Scotti  
Texas A&M University  

---

**Last Updated:** February 2026  
**Status:** Checkpoint 1 Complete (EDA) | In Progress
