1.	fork the repo
2.	git clone <’link to repository’>
3.	cd <’name of cloned folder’ >
4.	mkdir your-code
5.	cd your-code/
6.	touch about-me.md
7.	open file with notepad with notepad about-me.md and add 'My name is **your name**'  
8.	git add about-me.md
9.	git status
10.	It will tell you that there is a new file:   about-me.md
11.	git commit -m 'added file'
12.	git status
13.	git push origin master
14.	git pull origin master
15.	open file with notepad with notepad about-me.md and add 'I am from **your country**'  
16.	git add about-me.md
17.	git commit -m 'added nationality'
18.	git push origin master
19.	git pull origin master
20.	open file with notepad with notepad about-me.md and add 'I am a student of the Data Bootcamp'  
21.	git add about-me.md
22.	git commit -m 'added info about bootcamp'
23.	git push origin master
24.	git log 
25.	Copy the commit prior to your recent commit (‘added nationality’)
26.	Press Q to escape
27.	git reset --hard 32a63d7d09589d80a8ff614be85d854792798aee
28.	If you go to your repo on github you will see:
•	My name is <your name> I am from <your country> I am a student of the Data Bootcamp
•	But if you check the local .md file you will have the previous version as we did a reset: My name is <your name> I am from <your country>
29.	git checkout -b conflict
30.	In this conflict brach alter the about me file by adding 'I work as **your job**'
31.	notepad about-me.md and make the change
32.	In the conflict branch do git add .
33.	git commit -m 'added my job' 
34.	git pull origin master
35.	you will have a conflict as you are trying to pull into the conflict branch the version that is on the remote master branch (My name is <your name> I am from <your country> I am a student of the Data Bootcamp) and in the local conflict branch you have a different version and git does not know which one to keep
36.	if you do 'git diff master conflict' it will show you the differences between the two 

37.	if you now open the about-me file you will see the two versions
38.	we want to keep the version that we have in the master branch so update the about-me file with My name is <your name> I am from <your country> I am a student of the Data Bootcamp
39.	git add .
40.	git commit -m 'resolving conflicts with master branch'
41.	if you run git status it should be now ok 
42.	if you run git push origin conflict you should now be able to see in the github repo the two branches (master and conflict) with the same text in the about-me file 
43.	git checkout master 
44.	git merge conflict


