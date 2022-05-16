# How to Collaborate

These are the steps you need to follow, to allow others to access your locally hosted jupyter notebook (or jupyter lab)

### Do these once:
1) Open a terminal and run `jupyter notebook --generate-config`
2) This will print out in the terminal something like: `Writing default config to: C:\Users\username\.jupyter\jupyter_notebook_config.py`
3) Locate and open with a text editor the file `C:\Users\username\.jupyter\jupyter_notebook_config.py`
4) Within the file locate the comment: `c.NotebookApp.allow_remote_access = False` and change it to `c.NotebookApp.allow_remote_access = True` then save and close.
5) run `jupyter notebook password` to create a password for jupyter (you will share this password with people you will collaborate!) I propose the team agrees to have a common password
6) Run `pip install jupyter_contrib_nbextensions` to install jupyter extentions
<br><br>


7) Create an account at [ngrok](https://dashboard.ngrok.com/signup)
8) Then [download](https://dashboard.ngrok.com/get-started/setup) ngrok depending on you operating system
9) Unzip the zip file
10) Once extracted, run the executable (you might get a warning*, please proceed: show more -> run anyway)
11) In the downlad page it will create a code snippet you should run in the executable it will be something like `ngrok config add-authtoken 29EfheI8IknZXC9dTivgk6M4jVc_4zGtHaKadsvsdvfsvg2G`
12) Close everything (the terminal, and the executable)

\*In case you are on Windows you might need to do the following for the ngrok executable to Bypass Microsoft Defender SmartScreen prevented an unrecognized app from starting
- Right-click on the file.
- Select Properties.
- Make sure you are in the General tab.
- Press the Unblock button.
- Click Apply/OK and exit.
The file will be unblocked.

***

### Every time you want to collaborate

1) Start your jupyter notebook or jupyter lab (notice which port jupyter is running on, its usually on port 8888,  localhost:8888 )
2) Run the ngrok executable
3) run `ngrok http 8888` in the ngrok terminal
4) It will print out something in the terminal, copy and share the url it prints (it will be something like ` https://5f74-2a02-85f-f0f5-2300-653e-4c82-42ed-782c.eu.ngrok.io`

Once you close the ngrok executable, the person or people you shared the url will no longer have access to your jupyter notebook. 
