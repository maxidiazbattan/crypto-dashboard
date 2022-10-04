![crypto_dash.jpg](https://github.com/maxidiazbattan/crypto-dashboard/blob/main/assets/crypto%20dash.jpg?raw=true)


# Crypto-dashboard

In this repo, I have created a dashboard with Dash, a Python framework that allows you to create web apps in pure Python, for more info you can check the documentation here, https://dash.plotly.com/. For this project I used Defi and Yahoo Finance Api's, to obtain the data, I had to use Defi because Yahoo allowed me to make very few requests, so I had to change my strategy when assembling the graphs. For the three area plots I used Defi, and for the candlestick Yahoo Finance, I had to store the data in dataframes and export them to avoid problems with the requests. Data cleaning was done with pandas. In the following link, you can see the final result, https://cryptodashboardwdash.herokuapp.com/ (it takes a bit to load the first time because it's dormant at Heroku Servers). I hope you like it, and the instructions to use it are below.

# Heroku Deployment

## Copy this repo to your own personal one
1. On https://github.com/new, create a new repository  
2. In your terminal, in your home directory, clone the repo
3. `cd` into the repository that is created and you should see all the files now.
4. Then, connect this cloned repo to your new personal repo made in Step 1: `git remote set-url origin https://www.github.com/{your-username}/crypto-dashboard.git` (be sure to change your username and remove the curly braces)
5. Run `git push origin main` to push the local repo to remote. You should now see this same code in your personal `crypto-dashboard` repo.

## Run Application
1. Run command in terminal `python app.py` (or your app name)
2. Preview web page in browser '/'

## Deploy to Heroku
1. Install Heroku CLI: 
- For WSL users, run `sudo curl https://cli-assets.heroku.com/install.sh | sh`. 
- For Mac users, run `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"` if you don't have Homebrew installed, then `brew tap heroku/brew && brew install heroku`. 

This could take a few minutes. In the meantime...

2. Create a free account on Heroku https://signup.heroku.com/login
3. Create a `requirements.txt` file with all your non-standard dependencies (based on any libraries you are importing), separated by a newline. In our case, they are `Flask` w/ a capital F. Note that libraries like `os` are standard imports, so they don't need to be included.
4. Create a `Procfile`, which has the command that Heroku will use to run your app: `web: python app.py` (see documentation https://devcenter.heroku.com/articles/getting-started-with-python#define-a-procfile)
5. Add + commit all changed files with git
6. Log in to Heroku: `heroku login -i`
5. Create a Heroku app: `heroku create`. This will create a new URL and associated host for you.
6. Push your code to Heroku: `git push heroku main`. This actually pushes your code to Heroku's remote repository. You may get an error at this point relating to a buildpack. That means that Heroku can't figure out on its own what primary language your code is written in. You should be able to resolve this with `heroku buildpacks:set heroku/python`.
7. Open your app with your new URL: `heroku open`. Click the link to open if it doesn't open on its own. It shouldn't work, because it doeesn't have any environment variables (remember, your `.env` file is not in your git repository!)
8. Go to https://dashboard.heroku.com/apps and click your App, then go to Settings, and click "Reveal Config Vars"
9. Run `heroku open` or refresh the URL if you have it open. 
10. That's it, your app it's deployed, congrats!


# Built With

* [Python](https://docs.python.org/3/) - Programming language
* [Pandas](https://pandas.pydata.org/docs/) - Data manipulation python library
* [Plotly](https://plotly.com/python/) - Graphing python library
* [Dash](https://dash.plotly.com/) - Dashboard python library


# Author

* **Maximiliano Diaz Battan** 

