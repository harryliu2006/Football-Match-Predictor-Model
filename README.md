# Premier League Match Predictor

A small project where I scraped four seasons of English Premier League (EPL) data and built a machine learning model to predict match outcomes.

---

## Workflow
1. **Scrape Data** – Used `requests` + `BeautifulSoup` to collect fixtures, results, and stats.  
2. **Clean & Prepare** – Converted raw tables into a single dataset (`matches_full.csv`) with rolling averages and team encodings.  
3. **Train Model** – Used **XGBoost** to classify matches as home win, draw, or away win.  
4. **Evaluate** – Model reached **~55% precision**, which is only slightly better than random guessing. This shows how unpredictable football outcomes can be - teams often get dominated in the flow of the game but land one shot on goal and end up scoring (We see this in Real Madrid Champions League Wins in recent years) and how limited four seasons of data are. Nevertheless, it was still a valuable exercise in building the full pipeline: scraping raw data, engineering features, training a model, and evaluating results.  

---

## Insights
- Rolling averages of goals, shots, and expected goals (xG) were the most useful features.  
- Limited data (only 4 seasons) and the chaotic nature of football outcomes kept accuracy modest.  
- Still, the project shows how data and ML can capture meaningful patterns.  

---

## Tools Used
- Python (`pandas`, `numpy`, `scikit-learn`, `xgboost`)  
- Web scraping (`requests`, `beautifulsoup4`)  
- Visualization (`matplotlib`)  

---

## Try It Out
- `scraping.ipynb` → collects and saves EPL match data  
- `PLpredictor.ipynb` → trains and evaluates the ML model  

---

## Future Ideas
- Add more seasons and competitions for a bigger dataset  
- Try different models (logistic regression, ensembles, deep learning)  
- Explore match context (lineups, injuries, home crowd) for richer predictions  
