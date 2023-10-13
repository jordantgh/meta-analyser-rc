# Meta-Analyser

## Overview

<p>
  <img src="assets/image.jpg" alt="AppScreenShot" width="200" />
</p>

This is a tool designed to partially automate data search and extraction from scientific literature as well as facilitate its pre-cleaning. It performs searches of PubMed Central open access articles (using the normal PMC search syntax) and automatically retrieves supplementary files. It includes a processing workflow that attempts to parse out discrete data frames from often inconsistently formatted .xlsx and .csv files provided with academic publications. Users can preview data files and select the ones they want to process. Once processing is complete, the user again has the opportunity to further refine the data by filtering unwanted tables and selecting specific data features. The data is stored in a local SQLite database.

CURRENTLY A WORK IN PROGRESS!

I have gotten it to a point where it can facilitate my own work (being familiar as I am with its quirks, patient with its sluggishness, etc), but it is not by any means ready for prime time. I offer it publicly now to allow any motivated and helpful people who are perhaps interested in the concept try it out and let me know if they run into any specific issues (besides that it's slow, the UI is ugly, etc).

## Features

- Search for scientific articles based on a query
- Download supplementary files linked to the articles
- Process tables from supplementary files and store them in a local SQLite database
- Filter tables using a custom query engine that provides a "pubmed like" search syntax 

## WIP Features

- OpenAI header row detection (the most common edge case not handled by my table parser is non-header header rows containing irrelevant text)
- Session saving - save not only the final processed tables in a DB, but the entire app state (which papers you initially searched, which you excluded) will be able to be saved. This allows you to retrace your steps, or revise them.

