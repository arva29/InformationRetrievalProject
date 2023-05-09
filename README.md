# Information Retrieval Project 2022/23

Project done for the information retrieval course of the master's degree in computer science at the University of Milan

## Topic chosen - Complexity in boardgames (P4)

> <p align="justify"> Playing boardgames is a wonderful hobby that is growing in popularity in the last years. Since 2000, the website BoardGameGeek (BGG) provides a complete database about boardgames and users playing boardgames around the world. Users provide also stats and ratings that evaluate the popularity of each game according to several criteria, including the game complexity (called weight) (see for example the stats for the game Gloomhaven).  
> For many games, either on the producer website or on some community forum (sometimes on the BGG page as well), the Rulebook is also available. See for example the games from GMT games that usually provide a pdf rulebook downloadable for each game.
> Goal of the project is to automatically analyze the rulebooks in order to define appropriate metrics and strategies for automatically evaluate the complexity score of the game on the basis of the rules.  
> This score should then compared against the BGG weight score in order to discuss similarity and differences between the two metrics. </p>

## Files in the repository

The dataset is created using data from two different sites and this is done with the following 2 notebooks:

- [OrderOfGamersRulebooksScraper](OrderOfGamersRulebooksScraper.ipynb) - Automatically download pdf rulebooks from the [Esoteric Orders of Gamers](https://www.orderofgamers.com/games/) website
- [RulebooksReader](RulebooksReader.ipynb) - Read the pdf downloaded with the previous notebook and extract from each of them name, year, publisher and rules of the game. Then, using the [BGG API](https://boardgamegeek.com/wiki/page/BGG_XML_API#) it extracts the weight (complexity score) of each game . It then produce a csv that will be the actual dataset of the project.

The [boardgame_dataset](boardgame_dataset.csv) is the dataset generated by the [RulebooksReader notebook](RulebooksReader.ipynb) and it is the datset used for the complexity analysis. The core of the project is developed in the [BoardGameComplexityAnalysis notebook](BoardGameComplexityAnalysis.ipynb) (that is a colaboratory notebook due to some issues between a library and M1 chips)

The [hyph_en_US.dic](hyph_en_US.dic) file is a file used in the main notebook for the division into syllables of text. It is the file utilized by the LibreOffice Foundation to permorm the hyphenation in their applications and could be found in their [GitHub repository](https://github.com/LibreOffice/dictionaries).

The last file is the project report with the explanation and result of the work done.
