# Exircise10-Solution
Exircise 10 User the NewAPI and the requests module to fetch the daily news relative to different topics. Go to: https://newsapi.org/ and explore the various options to build you application

    import requests
    import json

    query = input("What type of news are interested in? ")
    url = f"https://newsapi.org/v2/everything?q={query}&from=2023-01-28&sortBy=publishedAt&apiKey=dbe57b028aeb41e285a226a94865f7a7"
    r = requests.get(url)
    ews = json.loads(r.text)
    # print(news, type(news))
    for article in news["articles"]:
    print(article["title"])
    print(article["description"])
     print("--------------------------------------")
  