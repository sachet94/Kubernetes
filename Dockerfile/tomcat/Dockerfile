FROM tomcat:8
ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/student.war /usr/local/tomcat/webapps/student.war
ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/mysql-connector.jar /usr/local/tomcat/lib/mysql-connector.jar
RUN sed -i -e '/org.apache.catalina.webresources/a JAVA_OPTS="-DDBENDPOINT=$DBENDPOINT -DDBNAME=$DBNAME -DDBUSER=$DBUSER -DDBPASS=$DBPASS"' /usr/local/tomcat/bin/catalina.sh
ADD context.xml /usr/local/tomcat/conf/context.xml

