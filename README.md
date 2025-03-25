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
|opinion|div.js_product-review|opinion|
|opinion ID |[data-entry-id]|opinion_id|
|author |span.user-post__author-name|author|
|recommendation |span.user-post__author-recomendation > em|recommendation|
|number of stars |span.user-post__score-count|stars|
|opinion’s content |div.user-post_text|content|
|list of advantages |div.review-feature__item review-feature__item--positive|pros|
|list of disadvantages |.review-feature__item review-feature__item--negative|cons|
|how many helpful |button.vote-yes[data-total-vote]|vote_yes|
|how many  unhelpful |button.vote-no[data-total-vote]|vote_no|
|publishing date |span.user-post__published > time:nth-child(1)[datetime]|published|
|purchase date |span.user-post__published > time:nth-child(2)[datetime]|purchased|
