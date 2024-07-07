# Feminist books data project: The process
 This is a repository with the notebooks and tables used in my 'feminist books project', which analyses the Penguin Random House catalogue of books in Spanish. You can check it out [here](https://anaemepe.github.io/feminist-books-project/).

In this first project my aim was to understand the evolution of books about feminism in recent years. There was a huge wave of books on feminism some years ago and I 
feel it is no longer the case. So my initial question was: Are there more or less new books about feminism now compared to five years ago? 

I focused on one country, Spain, where I come from, and the leading publishing house, Penguin Random House. I limited the analysis to the number of books, years and related genres in order to show a glimpse of the current situation and trends.

The main findings are:
- Penguin's online collection of Spanish books contains 118 labelled "feminist". The company publishes 1,800 new titles each year.
- There are only 3 titles in the current collection published before 2014.
- Related genres are sometimes surprising: for example, there are way more feminist books also labelled "influencers' books" than LGBTIQ literature.

The data collection process consisted of, first, scraping Penguin Random House feminist collection [pages](https://www.penguinlibros.com/es/136-libros-feministas) to obtain the titles and links. Then, I scraped each book's page and collected publication years and related genres. Each book page looked like [this](https://www.penguinlibros.com/es/audiolibros-de-economia-politica-y-actualidad/288520-audiolibro-teoria-king-kong-9788439740247?mot_tcid=ed8fb4c9-2c99-48b5-8a42-46a909bfec6a). There were 118 of them so running the code took some time. 

After collecting the data, I placed it in two different dataframes, one with the books (title, author, year, link) and another with the genres. I chose to have two because most of the books are under several genres so there was a huge risk of distributing them in the wrong places. I also wasn't interested in knowing which book had what related genres, but in a more global reading, so it made even more sense to keep them separately. 

I then exported them as tables in csv format as I wanted to keep the scraping notebook for scraping. Pandas `value_counts` showed me some duplicates in the books dataframe and I cleaned the csv manually following the information shown in the scraping notebook. I then opened a second notebook only to analyse the tables as dataframes. Then, I input the results of the analysis into charts using Datawrapper. 

- Here is the [scraping notebook](https://github.com/anaemepe/feminist-books-process#:~:text=draft4Project1%20%2D%20Penguin.ipynb).
- Here is the [analysis notebook](https://github.com/anaemepe/feminist-books-process/blob/main/draft5Project1.ipynb).
- Here is the [books table](https://github.com/anaemepe/feminist-books-process#:~:text=2%20hours%20ago-,booksPRH_clean.csv,-Uploading%20files).
- Here is the [related genres table](https://github.com/anaemepe/feminist-books-process/blob/main/booksPRH_genres.csv).

## A section about new skills, etc

I've grown a lot in scraping, along with a little passion/obsession for it. I've also learnt to use scatterplots creatively and the whole workflow process.

## A section about things I tried

My initial plan was to analyse the words used in the titles and build a classification. Many titles refer to body parts, the natural world, and motherhood or its absence.
However, this required deeper qualitative analysis and several editorial decisions, so I chose not to go down that road for the time being. 

I also tried to scrape the descriptions of each book for the same aim but when Penguin blocked me I accepted that it was time to pass to something else. Before this, my pre-initial plan was to also scrape the second largest publishing house in Spain and compare results. Time limitation was also the reason not to pursue this plan. 

In the visualisation part, I tried to include more 'related genres' comparisons so the squares in the graph would look like little books - which was the idea I had in mind for that visual. But things got confusing pretty quickly. 

If I had developed this project in a newsroom, I would have **definitely** contacted Penguin Random House for comments and questions about their data. 
