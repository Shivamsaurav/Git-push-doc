# Git-push-doc

If this error appears

"remote: Support for password authentication was removed on August 13, 2021.
 Please use a personal access token instead.
 remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
 fatal: unable to access 'https://github.com/saigowthamr/react-fileupload.git/':
 The requested URL returned error: 403 "
 
 Solution: 
 
 This error tells that for security reasons GitHub removes the password-based authentication from August 13, 2021.

 To fix the error, follow the below steps:

 Step 1: Open GitHub.com, click on your profile picture, then click on settings.

 Step 2: Now, scroll to the bottom of a page and click on the Developer settings tab.

 Step 3: Now, click on Personal access tokens and generate a new token by giving the name and expiration date, etc.

 Step 4: Once you successfully generated the Personal access token copy it.

 Step 5: Now, open the Git repository where you got the error and remove the current origin by running the following command.
 
          #git remote remove origin
          
 Step 6: Add the new origin by using the following command in your terminal.
          
          #git remote add origin https://<PERSONALACCESSTOKEN>@github.com/<USERNAME>/<REPO>.git
          
 Atlast -----> git push --set-upstream origin main

