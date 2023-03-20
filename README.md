Version Control Lab2
Q1:Create a new project on your local machine then push it to a remote repo
A1:
mkdir lab2git
cd lab2git
git init
git remote add origin https://github.com/Gaser98/lab-2-git-.git
vi README.md
git branch -M main
git add README.md
git commit -m "README.md added"
git config --global push.default current #fixed the conflict between the master and main that made the push fail in the first trial
git push -u origin main
Q2:Create 2 branches (dev,test) and add a file to each then push the changes to the remote repo
A2:
git branch dev
git checkout dev
touch file.txt
git add .
git commit -m "new file added"
git push -u origin dev
git checkout -b test
touch file1.txt
git add .
git commit -m "new file added"
git push -u origin test
Q3:Merge the files on the branches on the main and push the changes to the remote repo
A3:
git checkout main
git merge dev
git merge test
git status #To check changes
git push 
Q4:Create an annotated tag with tagname "v1.7"
A4:
git tag -a v1.7 -m "Release version 1.7"
git push --follow-tags #To push the change as a commit 







