line_cmd_cheatsheet
# docker, git line command cheatsheet

# Docker Hub
Docker Syntax,                     Description
```
docker search <searchterm>              Search Docker Hub for images.
docker pull <user/image>                Downloads an image from Docker Hub.
docker login                            Authenticate to Docker Hub
                                        (or other Docker registry).
docker push <user/image>                Uploads an image to Docker Hub.
                                        You must be authenticated to run this command.
```
# Image and Container InformationPermalink
Docker Syntax,	              Description
```
docker ps                               List all running containers.
docker ps -a                            List all container instances, with their ID
                                        and status.
docker images                           Lists all images on the local machine.
docker history <user/image>             Lists the history of an image.
docker logs [container name or ID]      Displays the logs from a running container.
docker port [container name or ID]      Displays the exposed port of a running container.
docker diff [container name or ID]      Lists the changes made to a container.
```
# Work With Images and ContainersPermalink
Docker Syntax,	Description
```
docker run -it <user/image>               Runs an image, creating a container and
                                          changing the terminal
                                          to the terminal within the container.
docker run -p $HOSTPORT:$CONTAINERPORT -d <user/image>	Run an image in detached mode
                                          with port forwarding.
ctrl+p then ctrl+q                        From within the container’s command prompt,
                                          detach and return to the host’s prompt.
docker attach [container name or ID]      Changes the command prompt
                                          from the host to a running container.
docker start [container name or ID]       Start a container.
docker stop [container name or ID]        Stop a container.
docker rm -f [container name or ID]       Delete a container.
docker rmi [container name or ID]         Delete an image.
docker tag user/image:tag user/image:newtag	Add a new tag to an image.
docker exec [container name or ID]        shell command	Executes a command within a running container.
```
# Image CreationPermalink
Docker Syntax,	Description
```
docker commit <user/image>                Save a container as an image.
docker save <user/image>                  Save an image to a tar archive.
docker build -t sampleuser/ubuntu.        Builds a Docker image
                                          from a Dockerfile
                                          in the current directory.
docker load                               Loads an image from file.
```


# Git CLI
```
git branch				# check work branch
git checkout -b <branch name>		# create a new branch new name locally
git checkout <branch name>		# swich to local work branch
git branch -D <branch name>		# delete a branch
git status 				# show local changes
git diff <file path $ names>		# show file content changes
git checkout <file path & name>		# undo all the file changes(cannot be recovered)
git reset --soft <commit bash>		# unstage commit
git reset --hard <commit bash>		# remove al local changes made (Cannot be undone)
git log					# show branch commit history
git branch -m <old> <new>		# rename a old branch to new
git branch -a				# list all branchs
 git branch -r				# list remote branches
git show-branch				# see the branches and their commites

git pull config pull.rebase false	# merge
git pull config pull.rebase true	# rebase
git pull config pull.ff only		# fast-forward only
git add
git commit -m "some messages"
git push
```

# Run a program at background
```
nohup <exec> > <file.txt> &
tail -f <file.txt>        <or>      tail -n <number> <file.txt>
```
