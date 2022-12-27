![crypto_dash.jpg](https://github.com/maxidiazbattan/crypto-dashboard/blob/main/assets/crypto%20dash.jpg?raw=true)


# Crypto-dashboard

In this repo, I have created a dashboard with Dash, a Python framework that allows you to create web apps in pure Python, for more info you can check the documentation here, https://dash.plotly.com/. For this project I used Defi and Yahoo Finance Api's, to obtain the data, I had to use Defi because Yahoo allowed me to make very few requests, so I had to change my strategy when assembling the graphs. For the three area plots I used Defi, and for the candlestick Yahoo Finance, I had to store the data in dataframes and export them to avoid problems with the requests. Data cleaning was done with pandas. In the following link, you can see the final result, https://crypto-dashboard-33bn.onrender.com/ (it takes a bit to load the first time because it's dormant at Render Servers). I hope you like it, and the instructions to use it are below.


# Render Deployment

## Copy this repo to your own personal one
1. On https://github.com/new, create a new repository  
2. In your terminal, in your home directory, clone the repo
3. `cd` into the repository that is created and you should see all the files now.
4. Then, connect this cloned repo to your new personal repo made in Step 1: `git remote set-url origin https://www.github.com/{your-username}/covid-dashboard.git` (be sure to change your username and remove the curly braces)
5. Run `git push origin main` to push the local repo to remote. You should now see this same code in your personal `covid-dashboard` repo.

## Deploy to Render
1. Go to https://render.com/ and create a new account free account. 
2. Once your account was created, click on the "new" button and select web service.
3. Connect your GitHub account and click install.
4. Select the repo you want to deploy, in this case, the repo previously cloned, and click connect.
5. Choose a name for your app, the rest of the options can be the default, with the exception of "Start Command", here we have to change $ gunicorn app:app to $ gunicorn app_name:server. Where app_name it's the name of your app. 
6. If everything it's correct, click on Create Web Service.
7. And that's it, after a couple of minutes, your app it's deployed, congrats!


# Built With

* [Python](https://docs.python.org/3/) - Programming language
* [Pandas](https://pandas.pydata.org/docs/) - Data manipulation python library
* [Plotly](https://plotly.com/python/) - Graphing python library
* [Dash](https://dash.plotly.com/) - Dashboard python library


# Author

* **Maximiliano Diaz Battan** 

