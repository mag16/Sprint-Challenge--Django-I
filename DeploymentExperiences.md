My first issue in deploying to Heroku came when app would not deploy due to a suggestion by heroku.  was given the suggestion to "DISABLE_COLLECTSTATIC" and did (first to config vars then via terminal).  App got deployed.  Real problems for me started with migrations.  Keep getting the error "no module named corsheaders found" with my heroku logs giving my an error at path '/' with a 503.  added a '/' path to urls.py.  Did a pip3 install instead for cors header. The fixed worked and was able to 'migrate' migrations to heroku.  I only have a completed back end so just need a quick front end to be able to load properly but deployment works.  MVP.

Changes to my settings.py made deployment possible.  added Whitenoise middleware(line 70), STATIC_ROOT (line 147), change to databases (line 104).

Procfile attempts.  Took a while but got it to load.  My heroku deployment works now.


My links:
https://introdjango-djorg.herokuapp.com/admin
https://github.com/mag16/IntroDjango--djorg