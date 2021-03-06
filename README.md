
# hackbot

hackbot is a chat bot built on the [Hubot][hubot] framework. It was
initially generated by [generator-hubot][generator-hubot], and configured to be
deployed on [Heroku][heroku] to get you up and running as quick as possible.

This README is intended to help get you started. 

[heroku]: http://www.heroku.com
[hubot]: http://hubot.github.com
[generator-hubot]: https://github.com/github/generator-hubot


### Duplicating Repo  

You will need [Git][git] to make a duplicate of this repository. 

move to a new directory  
% mkdir hackbot  
% cd hackbot   
  
Make a bare clone of the repository  
% git clone --bare https://github.com/GridIron/hack-a-thon.git  
 
Mirror-push to your new repository  
% cd hack-a-thon.git  
% git push --mirror https://github.com/your-username/your-new-repo.git   

Remove our temporary local repository  
% cd ..  
% rm -rf hack-a-thon.git     

Now you can make a clone of your new repo  
git clone https://github.com/your-username/your-new-repo.git  

Once you have duplicated this repository. You will need to install [nodejs][nodejs] and [npm][npm] if you haven't already, to get Hubot working. Click the links to download and follow instructions on how to install these tools. 

[git]: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
[nodejs]: https://nodejs.org/
[npm]: http://blog.npmjs.org/post/85484771375/how-to-install-npm

Now you should be able to run your bot locally

### Running hackbot Locally

You can test your hubot by running the following in the top level of your repo

You can start hackbot locally by running:

    % bin/hubot

You'll see some start up output and a prompt:

    [Sat Feb 28 2015 12:38:27 GMT+0000 (GMT)] INFO Using default redis on localhost:6379

Once output has stalled, push enter to generate the following prompt if it is not already present  

    hackbot>

Then you can interact with hackbot by typing `hackbot help`.

    hackbot> hackbot help
    hackbot animate me <query> - The same thing as `image me`, except adds [snip]
    hackbot help - Displays all of the help commands that hackbot knows about.
    ...

### Heroku Integration
You need to install the [Heroku toolbelt][herokut]. Click the link to download and follow the instructions to get this tool. Once this is installed, you will need to make an account with [heroku][herokuaccount] and verify your account. Then do the following in the top level of your repo (Windows users may need to restart their terminal before using Heroku commands):  

% heroku login  
% heroku create my-slackbot-appname  
% heroku config:add HEROKU_URL=http://my-slackbot-appname.herokuapp.com

###Slack Integration
Now one you will need to integrate your hackbot with [Slack][slack] and set some environment
variables. Create an account, create a team, then visit https://yourteamname.slack.com/services/new/hubot to add the Hubot capability. Then you will be presented with an API token. Use this token in the following terminal command:
  
% heroku config:add HUBOT_SLACK_TOKEN=please-place-your-token-here  

Now deploy your bot to heroku

% git push heroku master   

More detailed documentation can be found on the [deploying hubot onto
Heroku][deploy-heroku] wiki page. If you run into any problems, checkout Heroku's [docs][heroku-node-docs].  

[herokut]: https://toolbelt.heroku.com/ 
[slack]: https://slack.com/
[herokuaccount]: https://www.heroku.com/

Now your hackbot should be working fully in your slack team. 
### Scripting

An example script is included at `scripts/example.coffee`, so check it out to
get started, along with the [Scripting Guide](https://hubot.github.com/docs/scripting/).

For more information or examples you can visit  
https://hubot.github.com/docs/  
https://www.npmjs.com/browse/keyword/hubot-scripts  

[scripting-docs]: https://github.com/github/hubot/blob/master/docs/scripting.md

[heroku-node-docs]: http://devcenter.heroku.com/articles/node-js
[deploy-heroku]: https://github.com/github/hubot/blob/master/docs/deploying/heroku.md
