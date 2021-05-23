Motivation <br>
Building a labelled dataset to build an algorithm to tag pieces of fiction. The internet is forever but people may eventually not what a username of theirs associated with a fanfic publicly, so I deleted the original repo and am recreating it with the scripts to build a dataset but there no longer any actual fanfics nor is there a dataset. I believe in giving credit where credit is due, do I won't disassociate usernames from fics, however I also believe in a person's right to be forgotten so I'm not creating a repo that at its core would have data that could be used to trace back to someone.

Table of Contents <br>
[Necessary Libraries](#libraries) <br>
[Files in the Repository](#repofiles) <br>
[Instructions for downloading fanfics from Archive of Our Own (AO3)](#ficdownloading) <br>
[Notes on the fics I'm choosing](#chosenfics) <br>
[Notes on fanfic processing](#ficprocessing) <br>
[Notes on manual tag processing](#tagprocessing) <br>

<a name="libraries">Necessary Libraries</a> <br>
Pandas <br>
NumPy <br>
BeautifulSoup <br>
OS <br>
SQLAlchemy <br>

<a name="repofiles">Files in the Repository w/ Summary</a> <br>
ETLPipeline.ipynb: jupyter notebook with ETL pipeline for AO3 fanfics <br>
README.md: documentation file <br>
tagClustering folder: <br>
  allTags.csv: CSV file with from additionalTags column grouped <br>
  FandomGenreCWTagClustering.xlsx: Excel file with tags with grouped tags, fandoms, and fandom genres in separate sheets <br>
  fandomGenreTags.csv: CSV file with tags of the genres for the fandoms column grouped <br>
  fandomTags.csv: CSV file with tags from fandoms column grouped <br>

Files created by script: <br>
UniqueList_fandom.csv: CSV file created from the fandom column <br>
UniqueList_additionalTags.csv: CSV file created from the additionalTags column <br>

<a name="ficdownloading">Instructions for downloading fanfics from Archive of Our Own (AO3)</a>: <br>
AO3 has handy download buttons in each fic, however since I am bulk downloading fics I choose to install Flamebyrd's AO3 Ebook Download Helper tool (https://random.fangirling.net/scripts/ao3_downloader). <br>

<a name="chosenfics">Notes on the chosen fics</a>: <br>
I'm downloading fics based on fandoms I know well that are inclusive with diverse characters from typically underrepresented communities (people with disabilities, people of color, queer people, etc)</a>. <br>

<a name="ficprocessing">Notes on fic processing</a>: <br>
There is certain formatting that won't process correctly and the story_text will come back blank. This happens in about 3% of the fics. I am working on figuring out how to retrieve these differently formatted fics. <br>

<a name="tagprocessing">Notes on manual tag processing</a>: <br>
I have included my current tag processing document to help with your own tag clustering and to keep labelling as consistent as possible since two people are likely to categorize things differently. <br>

Sources for code adapted and used: <br>
Stripping code found here: https://stackoverflow.com/questions/7984169/remove-trailing-newline-from-the-elements-of-a-string-list <br>
Merge fanfics back in a single row: https://stackoverflow.com/questions/39646345/pandas-merging-rows-with-the-same-value-and-same-index <br>
Convert list to string: https://www.geeksforgeeks.org/python-program-to-convert-a-list-to-string/ <br>
Flattened list of lists: https://stackoverflow.com/questions/952914/how-to-make-a-flat-list-out-of-list-of-lists <br>
