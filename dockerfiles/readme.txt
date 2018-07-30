docker build -t adityaprabhakara/alpine_apache2:1.1 -f Dockerfile .
docker build -t adityaprabhakara/code:1.1 -f Dockerfile.code .



------------------------------------------------
First project
apache

write Dockerfile
git push
jenkins pull from apache2
docker build -t apache2:<build number> -t apache2:latest -f Dockerfile
docker push apache2:<build number>
docker push apache2:latest

--------------------------------------------------------------------
Second project
appcode

write Dockerfile
    FROM 
    COPY service1.war /tomcat/lib
    
checkin dockerfile
checkin of app code


jenkins pull from appcode
build the code
run unit tests
docker build -t appcode:<buildnumber> -t appcode:latest .
docker run appcode:latest .......

kickoff selenium functional testcases
report
docker image push appcode:<buildnumber>
docker image push appcode:latest
