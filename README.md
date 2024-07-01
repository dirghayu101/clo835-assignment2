# Setup:
- wget https://raw.githubusercontent.com/sojoudian/clo835_s24/master/project-2/app.py
- git init && git add . && git commit -m "setup." && git remote add origin git@github.com:dirghayu101/clo835-assignment2.git && git push -u origin main
- docker kill $(docker ps -q) && docker rm -f $(docker ps -a -q) #can remove f flag, or can use just the second half.
- docker run --name clo835-assignment-2 -d -p 127.0.0.1:3030:3030 clo835-assignment-2
- 
- 