
<img width="493" alt="boligsiden" src="https://user-images.githubusercontent.com/39537120/89758715-bad4d680-dae8-11ea-8e77-c85c02b78373.png">


Scrape all estates at boligsiden.dk in less than a minute:
```
from scraper import BoligScraper

scraper = BoligScraper()
df = scraper.scrape_listings()
```
The scraped data is saved as a dataframe in pickle format in data/scraping_jobs/ .

Before messing around with the dataframe, run the preprocessing process to convert price columns to from string to float:

```
from preprocessor import Preprocessor

preprocessor = Preprocessor()
df = preprocessor.process(df)
```
