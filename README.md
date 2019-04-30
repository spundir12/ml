# ml
# all topics related to ml will be available here
# use below step to use github
1. create a repository 
2. clone the repository in your local machine using below command

   git clone https://github.com/spundir12/ml.git   

3. once repository is created in your local machine create or move your work under that folder
   in my case once repository is created one ml folder is avaialbe in my location there I moved all my old file\folder

4. Add the file\folder using
   
   git add python_eg/

5. Commit Using
   
   git commit -m "add python_eg dir to practice python"
   
6. after step 5, PUSH using
   
   git push origin master


IF file size is larger than 100 mb push will fail 
now we can not solve issue directly becuase file is persisted after commit
to resolve the issue
following steps helped 
git filter-branch --force --index-filter 'git rm --cached -f --ignore-unmatch python_eg/8_SQL/data/imdb.sql'   --tag-name-filter cat -- --all

 git reflog expire --expire=now --all

 git gc --prune=now
 
 git gc --aggressive --prune=now
 
 
 git push --all --force
