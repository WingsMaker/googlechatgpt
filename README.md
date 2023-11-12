# googlechatgpt
ChatGPT alike Google Chat using PaLM api ( v1 not v2 )

![WhatsApp Image 2023-11-12 at 21 17 32_f8cef1a1](https://github.com/WingsMaker/googlechatgpt/assets/32192638/aa4d3630-3eed-4d63-b8aa-30f64916e7b9)

# Requirements
- Google Gmail account ( where your android playstore account is )
- Google PaLM api key , see [https://beta.openai.com/account/api-keys](https://makersuite.google.com)
- Telegram chatbot token, see https://t.me/BotFather

  

# Getting Started - Google App Script Project
[1] Goto https://script.google.com/home , click "New Project" 

[2] Write the scripts, copy paste from below template url :

https://raw.githubusercontent.com/WingsMaker/chatgptbot/main/googleappscript.txt

[3] Rename the project

Click on the "Untitled project" to rename the project as something else. Example, "googlechatgpt".

![image](https://github.com/WingsMaker/googlechatgpt/assets/32192638/c0feefc6-fef8-47ea-af0f-ba8c0b39d2d2)


[4] Deploy as google web app

In the Google App Script project, go to "Publish" in the top navigation bar. 
Under "Deploy as web app", select "Deploy". This will open a pop-up window. 
Your web app URL will be listed in the "Current web app URL" field.

Click on the "Deploy - New Deployment"

![image](https://user-images.githubusercontent.com/32192638/209758084-a48fdfd0-4eb8-45be-af04-1642c3c05ed8.png)

Click "Select type - Web App"

![image](https://user-images.githubusercontent.com/32192638/209758240-b3d00b5c-09de-4355-be1d-b6193269409f.png)

Fill in the form and click "Deploy".
( for more see https://www.youtube.com/watch?v=-AlstV1PAaA )

![image](https://user-images.githubusercontent.com/32192638/209758768-29dda612-80c7-425e-8a39-e3e80d2fe5bc.png)

Copy the web app url to the clipboard for later use.

[5] Update the values of weburi in the script.

Remove the substrings "https://script.google.com/macros/s/" and "/exec" of url. Copy the result to clipboard.
Change the value of statement, paste the weburi address into here.

var weburi  = "__paste_here__";

[6] Update the values of token in the script.

Find your Telegram chatbot token by logging into the BotFather in Telegram, selecting your bot, and clicking the "API Token" button.
( see https://www.youtube.com/watch?v=aNmRNjME6mE )
Change the value of statement, paste the bot token into here.

var token = "__replace_here__";

[7] Update the values of apiKey in the script.

The api secret key for Chat GPT is located in the My Apps page of your Chat GPT dashboard.
( for more see https://www.youtube.com/watch?v=DFmmiYlbgX0 )
Change the value of statement, paste the api secret key into here.

var apiKey = "__replace_here__";

[8] Save the script and REDO the deployment process in step 4 

since the code has been changed, need to update the value of webappUrl in [7].

[9] Run the "start_bot" function for only once to make sure actual telegram bot able to callback this google web app.

![image](https://github.com/WingsMaker/chatgptbot/assets/32192638/416ecbda-30bb-4d63-adb3-d3a24da7822f)

Your telegram bot is ready !


