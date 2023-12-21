# PlanktoBot 
PlanktoBot is a Slack bot specialised in PlanktoScopes produced by FairScope.
It is AI-powered and helps to enhance your customer support by providing automated assistance to PlanktoScopes users


### .env ###
A file to store all the environment variables. This is a way to centralize these variables and improve performance and security.


### bot_web.py ###
This bot is able to : 
- Listen to event in a specific channel in a slack workspace (PlanktoScope)
- Give threaded messaged
\n
The bot uses a `Langchain` web agent (able to browse the web) and a LLM (`gpt-4`-8k tokens or `gpt-4-1106-preview`-128k tokens) to produce an answer which passes through Langchain and then is posted in the Slack channel.
\n Check the documentation at : https://python.langchain.com/docs/get_started/introduction 

### bot_doc.py ###
- Same as `bot_web.py` but with a limited number of websites to explore ('planktoscope.org/*' & 'docs.planktoscope/community/*')
  
### data.json ###
- In this file we store the timestamp of each message sent in a particular slack channel, it helps to keep track of threads opened by the bot under a client's message so the bot can answer any question any time and not only the last one.
- It is used by the 2 bots 









