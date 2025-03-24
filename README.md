# CeneoScraper
https://www.ceneo.pl/126710499

## Ceneo scraping algorithm
1. Analyse the structure of the web page
2. Sent http request
3. Checking the code of http response
4. Parse the html code of first page wth opinions
5. Extract requred data from parsed code
6. If there are more pages, move to the next page and repeat steps 2-6 for each page
7. Save extracted data

## Analyse the structure of the web page
|Component|Selector|Variable|
|---------|--------|--------|
|opinion ID |[data-entry-id]||
|opinion’s author |.user-post__author-name||
|author’s recommendation |.user-post__author-recomendation > em||
|score expressed in number of stars |.user-post__score-count||
|opinion’s content |.user-post__score-count||
|list of product advantages |.review-feature__item review-feature__item--positive||
|list of product disadvantages |.review-feature__item review-feature__item--negative||
|how many users think that opinion was helpful |button.votes-yes > span||
|how many users think that opinion was unhelpful |button.votes-no > span||
|publishing date |span.user-post__published >time:nth-child(1)[datetime]|
|purchase date |span.user-post__published >time:nth-child(2)[datetime]||
