# Child-GI-Bill-calculator
Simple GI Bill calculator for you to see how much it will cover and what you (or they) will need to pay out of pocket for up to four years of school for your kids or spouse.

Don't forget that the GI Bill has a total of 36 months available. One academic year = 9 months. The calculator won't let you allocate more than 36 TOTAL months. 

PACKAGES NEEDED FOR THIS TO WORK
* streamlit
* pandas
* requests
* beautifulsoup4
* google-generativeai
* openai
* anthropic

If you use the Docker container, the requirements.txt has all that in the build file so it gets pulled and installed into the container. Docker Desktop is FREE use it unless you are using a different container software. 

FEATURES
* Save and re-load your inputs! Saving outputs a JSON file that has all the relevent data input in it so you can come back to your work. Default save is to your 'Downloads' folder.
* AI integration includes Ollama, Gemini, OpenAI, and Anthropic APIs. Make sure you create your API key first if using one of the cloud providers. If using Ollama, you have the choice in the dropdown under the URL to select the model depending on what you have installed.
* Copy and paste the URL for the tuition page of the school and the AI agent will pull relevent costs out and directly into the calculator. 
* AI makes mistakes, make sure it pulls the right numbers from the university or college tuition page correctly before blindly trusting it.
* The 'Student Covers Years' is intended to integrate burden sharing costs if you decide to NOT give one of your kids or spouse all of your GI bill. It calculates in half year increments.

KNOWN ISSUES
* The AI extractor has some known issues when the tuition data is in menus that expand on the webpage. Working to troubleshoot it so the extractor is reliable.
* BAH calculator doesn't pull info with the AI agent. You have to manually use the BAH Calculator on the DTMO website.
  
TO DO LIST
* Work BAH calculator integration for each school to properly pull the MHA rate for the school. The official .mil site doesn't allow API access 
* Add the options of GI Bill extensions when keeping that single month for yourself which can be used by the service member to get things like vocational training
* Yellow ribbon school integration.
* Test Apple Container build for the Docker container to ensure the OCI-compliant build works directly on Apple Silicon.
