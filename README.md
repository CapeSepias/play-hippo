![PlayHippo Logo](https://raw.githubusercontent.com/jbloemendal/play-hippo/master/public/images/logo.png)
#PlayHippo Service Module
The service module wraps Hippo CMS 10.2.0 dependencies and provides a singelton helper tool class PlayHippoTool with which
you can access Hippo repository using HST ContentBeans (see for example: model.HippoGoGreenNewsDocument and controllers.HomeController).


##Add hippo service module dependency (build.sbt):

```
resolvers += (
  "Play Hippo Repository" at "http://jbloemendal.github.io/play-hippo/releases/"
)

libraryDependencies ++= Seq(
  "org.onehippo" % "playhippo_2.11" % "1.1",
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


##org.onehippo.playhippo.services.PlayHippoTool Usage
See https://github.com/jbloemendal/play-hippo/blob/master/module/app/org/onehippo/playhippo/services/PlayHippoTool.java

[https://playframework.com/](https://playframework.com/)<br/>
[http://www.onehippo.org/](http://www.onehippo.org/)<br/>
[http://www.onehippo.org/7_8/library/development/check-out-go-green-from-subversion.html](http://www.onehippo.org/7_8/library/development/check-out-go-green-from-subversion.html)<br/>
http://jannisbloe.blogspot.nl/2016/05/integrating-play-framework-and-hippo-cms.html
