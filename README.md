# rundeck-plugins
How can you run this plugin in development mode?
To do this, you must have a docker installed on your machine and simply run a rundeck image
```
docker run --name local-rundeck -p 4440:4440 -v $(pwd)/rundeck:/home/rundeck/libext rundeck/rundeck:3.3.8        
```
As a prerequisite you must install in your gitpyton image initially
```
pip install gitpython==2.1.15
```
Then to perform the build you must distribute as follows
```
zip -r gke-plugin.zip . && mv gke-plugin.zip ../rundeck

zip -r git-plugin.zip . && mv git-plugin.zip ../rundeck

zip -r new-plugin.zip . && mv new-plugin.zip ../rundeck
````

have fun