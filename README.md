# TikTok Scraper in Python with Selenium & Google Sheets
This is an unofficial tool for collecting TikTokers' metadata (in this case, average views for the latest 30 TikToks, engagement rate and engagement rate by reach).

## Background
I collab with a lot of TikTokers for work, and it had been a pain in the ass collecting each video's views, likes, comments, shares, etc., and then copy paste them in a google spreadsheet over and over again. So I made this scraper to fetch (and calculate) the data I need, and I wanted to share it with people who may also be interested in it :)

## Getting Started
To start use the scrapper follow the instruction below.

### Selenium
The script uses Selenium and Chrome Webdriver to auto open a web browser and visit TikTok.
```sh
- pip install selenium
```
Download Chrome Webdriver (https://chromedriver.chromium.org/downloads), put the webdriver in /usr/local/bin

### gspread
```sh
- pip install gspread
```

### Google Sheets API
To access spreadsheets via Google Sheets API you need to authenticate and authorize your application.
- Instruction -> https://docs.gspread.org/en/latest/oauth2.html
- YouTube Guide -> https://www.youtube.com/watch?v=bu5wXjz2KvU

Remember to substitute the credentials file directory with yours in the script.

## Use the scrapper
Run the script in Terminal, enter the spreadsheet name and the worksheet name.
```sh
- python3 update_tiktokers.py
```

## Result Example
![image](https://user-images.githubusercontent.com/49832190/188074532-1ffa3149-8fc3-444d-985e-8e1ff34bdec0.png)

- ER: Engagement Rate, (likes+comments+shares)/followers
- ER by Reach: (likes+comments+shares)/views
