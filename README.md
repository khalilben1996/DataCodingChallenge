# Data-Engineering-Coding-Challenge



##  Challenge - News Content Collect and Store
  The goal of this coding challenge is to create a solution that crawls for articles from a news website [THEGUARDIAN.COM], cleanses the response, stores it in a mongo database, then makes it available to search via an API.

### Requirements
  * python (Flask==1.1.1,requests, pymongo, dnspython)
  * Docker (for the api)
  
## Technologies used
  * Flask
  * pymongo

 
### Install
1. clone the project
	`git clone https://github.com/MenoIy/Gemography-Data-Engineering-Coding-Challenge-t.git`
2. cd into project directory
	`cd United-remote_Backend_challenge`
3. Run scrapy (to scrap news from website)
   `scrapy crawl collector`
4. Build docker image of the API
	`docker build -t collectorapp .`
5. Run the docker container
	`docker run -it -d -p 8100:8100 collectorapp`



Now the API is working on [http://localhost:8100/](http://localhost:8100/)


## Bonus

  * search the articles' text by keyword.
  
   ('/') keyword=key
   
                    ex : localhost:8100/keyword=US news