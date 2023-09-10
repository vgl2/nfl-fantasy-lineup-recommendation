# nfl-fantasy-lineup-recommendation
Sample recommendation model to predict recommended lineups to use for fantasy football. All of the data has been provided by NFL FastR https://www.nflfastr.com/


This version only predicts for the following positions:
1. QB
2. RB
3. WR
4. TE
5. FLEX, RB/WR/TE or W/R/T (dependent on how it's named on your platforms)

Future versions will take into account D/ST and kickers.

Requirements:
Packages that need to be installed:
1. Numpy/Pandas
2. CatBoost - more info about catboost at https://www.catboost.ai
3. nfl_data_py - more info about nfl_data_py at https://github.com/cooperdff/nfl_data_py
4. sleeper-py - sleeper API  more info about sleeper-py at https://pypi.org/project/sleeper-py/
5. espn_api - espn API more info about espn_api at https://pypi.org/project/espn-api/
6. yahoo_fantasy_api - Yahoo fantasy API more info about yahoo_fantasy_api at https://pypi.org/project/yahoo-fantasy-api/

Once these packages are installed, the models can be run as a standalone without the API hookups. However, in order to link with sleeper, espn, or yahoo you must need the following:

### ESPN 
Note - This can only be run locally at the moment - this cannot be run on the cloud that does not have a remote desktop feature
1. leagueId - This can be found in the URL when logged into your account (e.g. https://fantasy.espn.com/football/team?leagueId=XXXX&teamId=YYYY&seasonId=ZZZZ where XXXX is the leagueId)
2. teamId - This can be found in the URL when logged into your account (e.g. https://fantasy.espn.com/football/team?leagueId=XXXX&teamId=YYYY&seasonId=ZZZZ where YYYY is the teamId)
3. seasonId - This can be found in the URL when logged into your account (e.g. https://fantasy.espn.com/football/team?leagueId=XXXX&teamId=YYYY&seasonId=ZZZZ where ZZZZ is the seasonId)
4. espn_s2 - Please look at this link to learn how to find your espn_s2 value - https://cran.r-project.org/web/packages/ffscrapr/vignettes/espn_authentication.html
5.  SWID - Please look at this link to learn how to find your SWID value - https://cran.r-project.org/web/packages/ffscrapr/vignettes/espn_authentication.html

### Sleeper
Note - This can be run locally and on the cloud.
1. username - Username of the account - Note: This is not your team name
2. leagueID - Can be found when you go to the league settings
3. season - the specific year that you're checking

### Yahoo
Note - Not all features have been tested. Please raise issues on bugs that you find but it should be functional. Also, this program will only work for the most recent season. Further modifications are needed in order for it to work on prior seasons. 

1. Path to json file containing the yahoo secret key/access token combination file - The contents will look like {access_token:XXXX,customer_key:YYYY,customer_secret:ZZZZ} where these are unique values. More information can be found at https://github.com/mattdodge/yahoofantasy under installation and autheneticaton for steps in generatng a yahoo oauth key. #Please do not share this file with anyone! 
2. league id - This can be found in the Scoring & Settings section of your fantasy football home page.
3. team name - This is the name of your team

Please raise any issues (e.g. bugs) via Github and please direct any questions and comments at vgl2@uw.edu. Lastly, please let me know if there are any platforms that you might want to be added in the future for predictions. 
