job1: 
if developer push to dev branch then jenkins will fetch from dev branch and deploy on the docker container

job2:
if developer push to master branch then jenkins will fetch from master branch and deploy on the docker container
, both the master docker contauiner and the dev docker container are different

job3:
jenkins will check whether the website runnign porperly , if the build is successfull, it will merge both the master and the dev branch .



steps:

1. first of all make a new dir in windows 

2. initialize it as git repo , then go to its hooks dir and add there a file of psot-commit 

3. in github , set up the hooks for the repo

4. write the html code in the git repo

5. make 2 branches one is master and the other is the dev

5. finally in the jenkins add job 1 that will push the file to dev branch in the github, then jenkins will fetch from the github dev branch

and deploy on the docker container .

6. use the poll SCM trigger to automatically done the job and also launch the docker container , by adding command in the execute hell


7. now make another job and this time trigger the master branch of the same repo with

 selecting " remotely do the job "and also launch the docker container by adding command int eh execute shell


8. after that make another job that will make quality assurance by selecting run the job after the job2 will be finished.


