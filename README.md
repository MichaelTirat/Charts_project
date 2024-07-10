# Charts_project
Data analysis of spotify's charts in France since December 2016


# PART ONE : DATA EXTRACTION FROM CHARTS
-------------------------------------------------------------------------

First of all, this project require scraping scripts because of the 'cold start' situation : I get all csv files of weekly charts since 2016 until june 2024.

You'll find in this list above the logic of data extraction :
- Create a unique csv file of all charts with a custom date column from the file name
  (weekly charts have only : uri (spotify id of each track) / track_name / track_artist / peak_rank / streams of the week) ====> weekly_charts.csv
- Create a second file by grouping unique uri tracks ===> unique_tracks.csv
- Create a third file by scraping lyrics with Helium & Selenium python libraries form "unique_tracks.csv" on google & genius.com ====> lyrics.csv
- Create a fourth file by requesting spotify's API (3 requests : on ID's track to get the artist's ID, on artist's ID to get the 'class of music', on ID's track to get audio_features informations)
  
