create a api-key that will allow jenkins to interact with github  -- go to github settings -- developer tools -- and create a token with webook permissions 
grab the api secret key from github and get into manage_jenkins -- configure system -- under github_server - add a secret credential and paste the api here & do a test connection 
now, create a freestly project -- check github project and paste the url 
source code management -- git --paste the same repo url -- we don't need to enter creds bcoz, we added the creds globally 
build triggers -- github hook trigger for git SCM polling 
build  -- add a build step -- invoke gradle script -- use gradle wrapper == task is build 
post build actions -- select archieve the artifactory - add a file that is needed to be archieved - /dist/trainSchedule.zip (in our project)
click save and see if build is working 

now, goto git master branch and commit the changes and chweck if build is triggered automatically on your jenkins server 
