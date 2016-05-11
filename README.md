#PlayHippo Service Module
The service module wraps hippo cms 10.2.0 dependencies and provides a singelton helper tool class PlayHippo with which
you can access Hippo repository using HST contentbeans, facilitating HippoBeans (see for example: controllers.HomeController and model.HippoGoGreenNewsDocument).


##Add hippo service module dependency (build.sbt):

```
resolvers += (
  "Play Hippo Repository" at "http://jbloemendal.github.io/play-hippo/releases/"
)

libraryDependencies ++= Seq(
  "org.onehippo" % "playhippo_2.11" % "1.0",
  ...
)
```


##Configure your repository (conf/application.conf)
```
hippo.rmi.uri = "rmi://localhost:1099/hipporepository"
hippo.rmi.user = "admin"
hippo.rmi.password = "admin"
```


##Enable rmi connections
http://www.onehippo.org/library/concepts/content-repository/repository-deployment-settings.html


##org.onehippo.playhippo.services.PlayHippo Usage
```
public static HstQuery createQuery(String folderPath)

public static HippoFolderBean createFolder(String newFolderNodePath, String hippoStdFolderNodeType, String folderName)

public static HippoBean newDocument(String folderNodePath, String documentType, String newDocumentNodeName)

public static Session getSession()

```

1 [https://playframework.com/](https://playframework.com/)<br/>
2 [http://www.onehippo.org/](http://www.onehippo.org/)<br/>
3 [http://www.onehippo.org/7_8/library/development/check-out-go-green-from-subversion.html](http://www.onehippo.org/7_8/library/development/check-out-go-green-from-subversion.html)


