# deck_converter

This program converts decks (into) the format used by XMage. 
It can also automatically convert all standard land cards
of those decks to use a specific edition to match your 
preferences.

## Supported Formats

The program understands decks as exported by the sites:

* http://tappedout.net/mtg-deck-builder/edh/
* http://www.mtgsalvation.com/forums/the-game/commander-edh/204408-commander-decklist-database
* https://www.mtggoldfish.com/metagame/commander

## Notes and Limitations

The program uses a database extracted from the database used 
by XMage. **This is not included, yet, therefore you currently 
cannot use this program :(**

At the moment you will need to define things before compilation
in the `Defines.h`:

* the path to the directory with the images available to you, 
  so you the program can determine what alternatives you have,
* the path to the database, and
* the edition you want to use for lands. **Not setting this
  will crash the program.**

## Usage

`deck_converter <in-file>`

... where `<in-file>` specifies the file to convert.

## Technical Notes

tappedout.net uses `x [tab] name`, while mtgsalvation.com and 
mtggoldfish.com are simply using `x name`. In both cases X is the number
detailling how often that card is in the deck.
