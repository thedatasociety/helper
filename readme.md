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

## Running a repository locally

Within the repository folder
```bash
# building the image:
repo2docker  --no-run --image-name <repository name>  ./    jupyter lab --ip 0.0.0.0 --NotebookApp.token=''
# runing the image

``` 

### lab-hadoop
```bash
# building the image:
docker rmi lab-hadoop:latest -f
repo2docker --no-run --image-name lab-hadoop  ./ jupyter lab --ip 0.0.0.0 --NotebookApp.token=''
# runing the image
docker run -it -p 8888:8888 -u jovyan -v $(echo ~):$(echo ~)/local-home lab-hadoop jupyter lab --ip 0.0.0.0 --NotebookApp.token=''
``` 



<!-- icons -->

[icon-twitter]:https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/twitter-icon.png
[icon-slack]:https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/slack-icon.png
[icon-github]:https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/github-icon.png
[icon-docker]:https://raw.githubusercontent.com/thedatasociety/lab-hadoop/master/resources/images/docker-icon.png

