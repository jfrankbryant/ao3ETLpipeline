Motivation
Building a labelled dataset to build an algorithm to tag pieces of fiction. The internet is forever but people may eventually not what a username of theirs associated with a fanfic publicly, so I deleted the original repo and am recreating it with the scripts to build a dataset but there no longer any actual fanfics nor is there a dataset. I believe in giving credit where credit is due, do I won't disassociate usernames from fics, however I also believe in a person's right to be forgotten so I'm not creating a repo that at its core would have data that could be used to trace back to someone.

Table of Contents
[Necessary Libraries](#libraries)
[Files in the Repository](#repofiles)
[Instructions for downloading fanfics from Archive of Our Own (AO3)](#ficdownloading)
[Notes on the fics I'm choosing](#chosenfics)
[Notes on fanfic processing](#ficprocessing)
[Notes on manual tag processing](#tagprocessing)

<a name="libraries">Necessary Libraries</a>
Pandas
NumPy
BeautifulSoup
OS
SQLAlchemy

<a name="repofiles">Files in the Repository w/ Summary</a>
ETLPipeline.ipynb: jupyter notebook with ETL pipeline for AO3 fanfics
README.md: documentation file
tagClustering folder:
  allTags.csv: CSV file with from additionalTags column grouped
  FandomGenreCWTagClustering.xlsx: Excel file with tags with grouped tags, fandoms, and fandom genres in separate sheets
  fandomGenreTags.csv: CSV file with tags of the genres for the fandoms column grouped
  fandomTags.csv: CSV file with tags from fandoms column grouped

Files created by script:
UniqueList_fandom.csv: CSV file created from the fandom column
UniqueList_additionalTags.csv: CSV file created from the additionalTags column

<a name="ficdownloading">Instructions for downloading fanfics from Archive of Our Own (AO3)</a>:
AO3 has handy download buttons in each fic, however since I am bulk downloading fics I choose to install Flamebyrd's AO3 Ebook Download Helper tool (https://random.fangirling.net/scripts/ao3_downloader).

<a name="chosenfics">Notes on the chosen fics</a>:
I'm downloading fics based on fandoms I know well that are inclusive with diverse characters from typically underrepresented communities (people with disabilities, people of color, queer people, etc)</a>.

<a name="ficprocessing">Notes on fic processing</a>:
There is certain formatting that won't process correctly and the story_text will come back blank. This happens in about 3% of the fics. I am working on figuring out how to retrieve these differently formatted fics.

<a name="tagprocessing">Notes on manual tag processing</a>:
I have included my current tag processing document to help with your own tag clustering and to keep labelling as consistent as possible since two people are likely to categorize things differently.

Sources for code adapted and used:
Stripping code found here: https://stackoverflow.com/questions/7984169/remove-trailing-newline-from-the-elements-of-a-string-list
Merge fanfics back in a single row: https://stackoverflow.com/questions/39646345/pandas-merging-rows-with-the-same-value-and-same-index
Convert list to string: https://www.geeksforgeeks.org/python-program-to-convert-a-list-to-string/
Flattened list of lists: https://stackoverflow.com/questions/952914/how-to-make-a-flat-list-out-of-list-of-lists
