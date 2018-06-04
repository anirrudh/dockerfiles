## Docker File Repositry.
![alt text](https://www.docker.com/sites/default/files/horizontal.png "Docker Logo")
### authored by @anirrudh. 

The sole purpose for this repository is to host a load of dockerfiles that have been written by me
for various purposes. I envision this being a repo that people are able to fork and build their own
docker files on. 

The file structure has 2 folders: OS and Languages. 

The OS folder will contain OS templates as well as images catered to specific disciplines. These will
be based on both the Ubuntu and CentOS images. 

The Lamgugages folder will contain base images created specifically for development in that specific
language, with additional useful tools installed. 

### Running the Images, and creating Containers.
Remember, with docker you must first understand that an image is only the "loaded", vanilla version
of the file on docker. You can create *many* containers from many images. 

(Future usage): Inseretion of script to check for image sizes. 

##### Image initalization. 
'''sh 
docker image build -f /path/to/dockerfile .
'''

After the image initializes, you need to look at the images that have been built to obtain the
image id. Use command
'''sh
docker images
'''
to see the running images. Get the image ID of the image that you want to build. This will allow the
container to be done. 

##### Containerization
To now spin up a container based on that image, we can simply use the following command: 
'''sh
docker run -i -t *insert_image_id* 
'''

Then, you should be logged into the contianer! yay! 

