# OAuth-Sample-App

# Instructions for Building and Running the Project

Get your OAuth application registered in Facebook Developer account and obtain App ID and App Secret values. The OAuth redirection endpoint of the client application is https://localhost:8443/OAuthApp/callback . Above is valid if you host this web application in a web server (tomcat) running in port 8443. Once you download/clone this project, you need to modify the following two files;

  1.   /src/main/java/com/mycompany/oauthapp/servlet/OAuthCallbackListener.java

This has following code.

final String REDIRECT_URI = "https://localhost:8443/OAuthApp/callback"; final String CLIENT_ID = "2226000597678052"; final String CLIENT_SECRET = "f9cfc064c00394b9b4a28b3f2df31814";

Put your App ID, App Secret and the correct Redirect Uri in above.

  2.  /src/main/webapp/index.jsp

This has following code.

var appid = "2226000597678052"; var redirecturi = "https://localhost:8443/OAuthApp/callback";

Put your App ID and Redirect Uri above

After the above changes, build the project with Maven. (eg: mvn clean install). Once you have got the OAuthApp.war file in the target directory, deploy it in a web server (eg: tomcat). You can access the application with the URL https://localhost:(port)/OAuthApp

You need to configure HTTPS on your server in order to run this application.

For more details about message flow visit my blog post 
