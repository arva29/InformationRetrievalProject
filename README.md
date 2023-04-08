# Information Retrieval Project 2022/23

Project done for the information retrieval course of the master's degree in computer science at the University of Milan

## Topic chosen - Complexity in boardgames (P4)

> *Playing boardgames is a wonderfull hobby that is growing in popularity in the last years. Since 2000, the website BoardGameGeek (BGG) 
provides a complete database about boardgames and users playing boardgames around the world. Users provide also stats and ratings that 
evaluate the popularity of each game according to several criteria, including the game complexity (called weight) (see for example the 
stats for the game Gloomhaven).  
> For many games, either on the producer website or on some community forum (sometimes on the BGG page as well), the Rulebook is also available. 
See for example the games from GMT games that usually provide a pdf rulebook downloadable for each game.  
> Goal of the project is to automatically analyze the rulebooks in order to define appropriate metrics and strategies for automatically evaluate 
the complexity score of the game on the basis of the rules.  
> This score should then compared agains the BGG weight score in order to discuss similarity and differences between the two metrics.*

## Files in the repository

The dataset is created using data from two different sites and this is done with the following 3 notebooks:

- [OrderOfGamersRulebooksScraper](OrderOfGamersRulebooksScraper.ipynb) - Automatically download pdf rulebooks from the [Esoteric Orders of Gamers](https://www.orderofgamers.com/games/) website
- [RulebooksReader](RulebooksReader.ipynb) - Read the pdf downloaded with the previous notebook and extract from each of them name, year, publisher and rules of the game. It then produce a first csv file with the information extracted above.
- [RulesToBGGLinker](RulesToBGGLinker.ipynb) - Using the [BGG API](https://boardgamegeek.com/wiki/page/BGG_XML_API#) it extracts the weight (complexity score) of each game in the csv produced by the previous notebook. It then produce a csv that will be the actual dataset of the project.

In the repository there are two version of the dataset, one is the full dataset extracted by running the notebooks above (about 350 records) while the other, the FILTERED version, is a cleaner version of the dateset where all the records with 0 weight or with a weight voted by less than 50 user have been cut off.

--- https://github.com/LibreOffice/dictionaries
