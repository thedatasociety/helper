# helper<!-- ds header -->
<div align="center">
 <img src="https://avatars3.githubusercontent.com/u/47368510?s=200&v=4" width="100px">
 <h3>The Data Science and Engineering Society </h3>
 <hr/>
 <a href="https://github.com/thedatasociety" target="_blank">
   <img src="https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/github-icon.png" width="30px" alt="github organization">
 </a>
 <a href="https://hub.docker.com/search?q=thedatasociety&type=image"  target="_blank" >
   <img src="https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/docker-icon.png" width="30px" alt="our docker hub organization">
 </a>
 <a href="https://thedatasociety.slack.com" target="_blank" >
   <img src="https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/slack-icon.png" width="30px" alt="our slack">
 </a>
 <a href="https://twitter.com/thedatasociety" target="_blank">
   <img src="https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/twitter-icon.png" width="30px" alt="our twitter">
 </a>
 <a href="https://quiltdata.com/package/thedatasociety/" target="_blank">
   <img src="https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/quilt-icon.png" width="30px" alt="quilt packages">
 </a> 
</div>
<!-- /ds header -->

## Running a thedatasociety's repository locally

Install minimal packages:
```
sudo apt install python3-pip
sudo pip3 install jupyter-repo2docker
```

Clone the repository. Enter the folder. Within the repository folder, run:

```bash
# removing image if it exists
docker rmi ${PWD##*/}:latest -f
# building the image:
repo2docker  --no-run --image-name ${PWD##*/}  ./  jupyter lab 
# running the built image
docker run -it -p 8888:8888 -v $(echo ~):$(echo ~)/local-home ${PWD##*/} jupyter lab --ip 0.0.0.0 --NotebookApp.token=''  --no-browser
``` 

or 
```bash
docker rmi ${PWD##*/}:latest -f && 
repo2docker  --no-run --image-name ${PWD##*/}  ./  jupyter lab  &&
docker run -it -p 8888:8888 -v $(echo ~):$(echo ~)/local-home ${PWD##*/} jupyter lab --ip 0.0.0.0 --NotebookApp.token=''  --no-browser
```
http://localhost:8888


<!-- icons -->

[icon-twitter]:https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/twitter-icon.png
[icon-slack]:https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/slack-icon.png
[icon-github]:https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/github-icon.png
[icon-docker]:https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/docker-icon.png

