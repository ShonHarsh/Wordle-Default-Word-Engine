# Wordle-Default-Word-Creator

This robot is in regards to the game Wordle.  It aims to create guesses to use in the game.

**Build_LetterFrequency** - This routine reads Data\Input\Letter-Frequency.xlsx, stores the data in a dictionarysString Letter, double Frequency> and sorts them by frequency descending.

**Build_WordFrequency** - This routine reads the source word document Data\Input\Words-Source.xlsx, removes all words that are not five characters in length, removes all words that do not have unique characters (For example: keep "Heart" but not "Bleed"), and writes the list to Data\Output\Word-List.xlsx.

**Note** This routine reads over 320k records and processes them so it is expensive.  On a Intel i9 3Ghz it took 13:42 minutes.

#### //ToDo
1. Filter words based on Wordle validity by testing words
1. Use the frequency dictionary in the output from the Build_WordFrequency routine in order to give each word a weight.
1. Calculate unique letter guess groups based on weight.
1. Test words for validity against the game and remove words that are not accepted

### GETTING STARTED

After making a pull request or downloading the project, open the Main.xaml in UiPath Studio.  The robot can be run with the play button in the ribbon and the result can be seen in output panel.

### DETAILS

**Project Format:** Windows, C#

**GitHub:** https://github.com/ShonHarsh/Wordle-Default-Word-Engine

**Rreference Sources**
1. Letter-Frequency - https://en.wikipedia.org/wiki/Letter_frequency
1. Word-Source - https://github.com/dwyl/english-words

### SAMPLE OUTPUT

```
03/29/2024 16:37:49 => [Debug] Debug started for file: Main
03/29/2024 16:37:49 => [Info] Wordle-Default-Word-Engine execution started
03/29/2024 16:37:49 => [Info] Wordle-Default-Word-Engine.Main.Begin;
03/29/2024 16:37:49 => [Info] Wordle-Default-Word-Engine.Build_LetterFrequency.Begin;
03/29/2024 16:37:49 => [Info] Wordle-Default-Word-Engine.Read_InputDocumentLetterFrequency.Begin;
03/29/2024 16:37:49 => [Info] Wordle-Default-Word-Engine.Read_InputDocumentLetterFrequency.ReadDataTable;
03/29/2024 16:37:49 => [Info] Wordle-Default-Word-Engine.Read_InputDocumentLetterFrequency.End;
03/29/2024 16:37:50 => [Info] Wordle-Default-Word-Engine.Calculate_LetterSchema.Begin;
03/29/2024 16:37:50 => [Info] Wordle-Default-Word-Engine.Calculate_LetterSchema.End;
03/29/2024 16:37:50 => [Info] Wordle-Default-Word-Engine.Build_LetterFrequency.End;
03/29/2024 16:37:50 => [Info] Wordle-Default-Word-Engine.Build_WordFrequency.Begin;
03/29/2024 16:37:50 => [Info] Wordle-Default-Word-Engine.Read_InputDocumentWords.Begin;
03/29/2024 16:37:53 => [Info] Wordle-Default-Word-Engine.Read_InputDocumentWords.End;
03/29/2024 16:37:53 => [Info] Wordle-Default-Word-Engine.Remove_InvalidWords.Begin;
03/29/2024 16:48:48 => [Info] Wordle-Default-Word-Engine.Remove_InvalidWords.End;
03/29/2024 16:48:48 => [Info] Wordle-Default-Word-Engine.Remove_RepeatingLetterWords.Begin;
03/29/2024 16:51:21 => [Info] Wordle-Default-Word-Engine.Remove_RepeatingLetterWords.End;
03/29/2024 16:51:21 => [Info] Wordle-Default-Word-Engine.Write_WordListFiltered.Begin;
03/29/2024 16:51:31 => [Info] Wordle-Default-Word-Engine.Write_WordListFiltered.End;
03/29/2024 16:51:31 => [Info] Wordle-Default-Word-Engine.Build_WordFrequency.End;
03/29/2024 16:51:31 => [Info] Wordle-Default-Word-Engine.Main.OperationCompleted;
03/29/2024 16:51:31 => [Info] Wordle-Default-Word-Engine.Main.End;
03/29/2024 16:51:31 => [Info] Wordle-Default-Word-Engine execution ended in: 00:13:42
```

### ARCHITECTURE REQUIREMENTS

A standard UiPath, Studio to Orchestrator cloud setup is the base of operation.  It is easy to setup and free.
1. An Orchestrator connection - Visit https://cloud.uipath.com/ and authenticate or sign up.
2. [UiPath Studio](https://www.uipath.com/product/studio) is used to run the robot.  Note that Studio Web can be used directly in Orchestrator but I recommend installing the Studio IDE application.

### GIT NOTES

Clone the project to develop or change it.

`git clone https://github.com/ShonHarsh/Wordle-Default-Word-Engine`

### LINKS
- [UiPath Automation Platform](https://www.uipath.com/)
- [UiPath Studio](https://www.uipath.com/product/studio)
- [Shon Harsh Website 127.0.0.1](https://shonharsh.github.io/curriculum-vitae/index.html)
- [This.GitHub](https://github.com/shonharsh)
- [LinkedIn](https://www.linkedin.com/in/shonharsh/)
