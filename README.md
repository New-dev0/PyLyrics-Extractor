# PyLyrics Extractor

You can now get lyrics for a song just by passing in the song name without an artist name and my lyrics extracting algorithm will do the rest of the job for you.

It fetches, extracts and returns the song's title and song lyrics from various websites autocorrecting the song names for the misspelled names along the way.  

## Motivation

While I was searching for a Python library to extract lyrics for songs to integrate it into my WhatsApp and Slack chatbot, I couldn't find any libraries or APIs which could only accept song names. The APIs and libraries I tested required the accurate spelling of song names and artist name to be passed in for fetching the song lyrics. And even after passing all of these information, there were still some song lyrics which weren't available in their APIs and libraries. 

This is the reason why I had to write an algorithm for fetching and scraping song lyrics from various websites even for any misspelled song name passed-in by the user.

## Requirements

* You will need an API Key and Engine ID of Google Custom Search JSON API.
  * Create your new custom search engine here to get your Engine ID: https://cse.google.com/cse/create/new
  * Visit here to get your API key: https://developers.google.com/custom-search/v1/overview
* Python installed on your machine.
* BeautifulSoup and Requests library.

## How to use

1. Import this module in your Python program.
'''
from lyrics_extractor import Song_Lyrics
'''

2. Assign a Variable to the Class by passing in the Google Custom Search JSON API key and Engine ID received after creating a custom search engine.
'''extract_lyrics = Song_Lyrics(GCS_API_KEY, GCS_ENGINE_ID)
'''

3. Get the title and the lyrics for the song by passing in the song name in the class function.
''' 
song_title, song_lyrics = extract_lyrics.get_lyrics("Shape of You")
'''

4. If you got the title and the lyrics for the song correctly then change the song name 'Shape of you' and try again with any misspelled song name like 'Shaep fo you'.

5. Voila! You have received your requested song lyrics even after passing in a misspelled song name.

### How to Contribute:
1. Fork this repository.
2. Clone it onto your local machine and test if everything works correctly before making any changes.
2. Make the appropriate changes.
3. Test it.
4. Test it again.
5. If everything's fine, open a pull request.

We will be more than happy to review your Pull Requests. So go for it and contribute to this awesome open source community.

If your Pull Request is accepted, you will surely get credits here.

### Contributors
* Rishabh Agrawal

### Copyright Information
I have only been extracting lyrics for Educational Purposes only. The chatbots I mentioned at the start are all being used for Non-commercial Purposes.

If you are planning to use this library for commercial purposes then I request you to have a look at the terms and policies of these websites and scrape lyrics only from sites which allow their content to be scraped and used commercially.

At the end I would say do respect the website's servers and please don't bombard with a lot of requests at once else you are bound to get an error.