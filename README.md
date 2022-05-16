# How to Collaborate

These are the steps you need to follow, to allow other to access your locally hosted jupyter notebook (or jupyter lab)

### Do these once:
1) Open a terminal and run `jupyter notebook --generate-config`
2) This will print out in the terminal something like: `Writing default config to: C:\Users\username\.jupyter\jupyter_notebook_config.py`
3) Copy the `C:\Users\username\.jupyter\jupyter_notebook_config.py` part
4) Run the following command in the terminal: `echo "NotebookApp.allow_remote_access = True" >> C:\Users\username\.jupyter\jupyter_notebook_config.py` where `C:\Users\username\.jupyter\jupyter_notebook_config.py` is the path that was printed in the terminal.
5) run `jupyter notebook password` to create a password for jupyter (you will share this password with people you will collaborate!)


6) Create an account at [ngrok](https://dashboard.ngrok.com/signup)
7) Then [download](https://dashboard.ngrok.com/get-started/setup) ngrok depending on you operating system
8) Unzip the zip file
9) Once extracted, run the executable (you might get a warning, please proceed: show more -> run anyway)
10) In the downlad page it will a code snippet you should run in the executable it will be something like `ngrok config add-authtoken 29EfheI8IknZXC9dTivgk6M4jVc_4zGtHaKadsvsdvfsvg2G`
11) Close everything (the terminal, and the executable)

***

### Every time you want to collaborate

1) Start your jupyter notebook or jupyter lab (notice which port jupyter is running on, its usually on port 8888,  localhost:8888 )
2) Run the ngrok executable
3) run `ngrok 8888 --host-headers="localhost:8888"` in the ngrok terminal
4) It will print out something in the terminal, copy and share the url it prints (it will be something like `https://asfdasdga.eu.ngrok.io`

Once you close the ngrok executable, the person or people you shared the url will no longer have access to your jupyter notebook. 
