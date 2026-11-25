# Dissecting Games

Cards to help you analyze a game from different perspectives.

Card data (XML files) to work together with https://github.com/csongorb/cardsimulator.

## Structure

This repository holds **content only**. Everything that displays the cards comes from [cardsimulator](https://github.com/csongorb/cardsimulator), included as a git submodule (pinned to a commit).

- `cards/cardset.xml`: title, repository and public address (used by the QR codes in PDFs)
- `cards/cardCategories.xml`, `cards/cards.xml`: the cards
- `texts/`: documents linked from the cards
- `index.html`: tiny loader, identical in every card set
- `.github/workflows/deploy.yml`: publishes the site to GitHub Pages on every push to `main`
- `.github/workflows/update-cardsimulator.yml`: manual run (workflow_dispatch) that bumps the `cardsimulator` submodule to the newest commit on `main` and pushes the pointer to `main`
- `cardsimulator/`: the simulator (submodule)

Run locally with any static web server (the XML can't be loaded from `file://`).

Update the simulator: run the *Update cardsimulator submodule* workflow on GitHub Actions, or locally with the help of your Git client.

## Version-History

### Todos

- ?

### Release 2.0 (Work in Progress)

Structure:

- matches cardsimulator v0.5
- restructured the main architecture, separated into
	- cardsimulator
	- dissectinggames (that includes cardsimulator as submodule)
- this repository is now content only
	- card visualisation comes from `cardsimulator`
	- tiny loader `index.html`
	- GitHub Pages deploy workflow

Content:

- shortened descriptions to make cards more readable 
- category "Examples" renamed to "Case Studies"
- new color palette for the categories
- new case studies: Clair Obscur: Expedition 33, Outer Wilds
- book links point to the book's Wikipedia article (or its Goodreads page when there is none) instead of Amazon
- task "Write one sprint as the projectmanager…" tagged "Business" instead of "Questions"

### Release 1.1.1 (26. March 2021)

- minor re-arrangement of the cards in the rows

### Release 1.1 (17. September 2019)

- added new example cards

### Release 1.0 (20. March 2018)

- added cards
	- added question cards
	- added task cards

## Credits

- **Csongor Baranyai**  
	- csongorb (at) gmail (dot) com  
	- [csongorb.com](http://www.csongorb.com)

Additional design / content / coding:

- **Haneyeh Sam**
	- [haniyehsam.itch.io](https://haniyehsam.itch.io/)
- **Christoph Maureder**
	- [christophmaureder.me](https://christophmaureder.me/)
- **Adrian Ace Köhlmoos**
	- [ace2win.itch.io](https://ace2win.itch.io)

Additional input:

- **Sebastian Stamm**
	- [www.the-stamm.com/](http://www.the-stamm.com/)
- **Florian Berger**
	- [florian-berger.de/](http://florian-berger.de/)

## License

[![Creative Commons License](https://i.creativecommons.org/l/by-nc/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc/4.0/)
This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0/).

All other media (images, software, etc.) remain the property of their copyright holders.
