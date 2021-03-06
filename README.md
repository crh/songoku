Son Goku
===

This is an example project that uses the [Maven Release Plugin](https://github.com/github/maven-plugins) , [GitHub Downloads Plugin](https://github.com/github/maven-plugins) and [Github Site Plugin](https://github.com/github/maven-plugins)

# Getting started

* Fork this project
* Update the `pom.xml` file `<url>` element to be the address of your fork
* Optionally update `<scm>` and `<developers>` section as well to have the information for your fork
* Add the following to your Maven `settings.xml` file (update with your GitHub login name and password):

```xml
  <profiles>
    <profile>
      <id>github</id>
      <properties>
        <github.global.userName>user</github.global.userName>
        <github.global.password>password</github.global.password>
      </properties>
    </profile>  
  </profiles>

  <activeProfiles>
    <activeProfile>github</activeProfile>
  </activeProfiles>
```

* Add the following to your Maven `settings.xml` file (update with your Repository Manager login name and password):

```xml
  <servers>
    <server>
      <id>foobar</id>
      <username>user</username>
      <password>password</password>
    </server>
  </servers>
```

* TODO

** update pom.xml for distribution management
** assembly => download

# Using Maven Release Plugin

```
   $mvn release:prepare
   $mvn release:perform
```

# Using GitHub Download Plugin

```
  $mvn clean install ghDownloads:upload
```

# Using GitHub Page Plugin

```
  $mvn site
```

The generated site will be committed to the [gh-pages branch](https:///github.com/crh/songoku/tree/gh-pages) and visible [here](http://crh.github.com/songoku/).

# Inspired by

  + https://github.com/kevinsawicki/github-maven-example

# References:

+ https://github.com/github/maven-plugins
+ https://github.com/kevinsawicki/github-maven-example
+ https://github.com/blog/945-github-maven-plugins
+ http://www.sonatype.com/people/2009/09/maven-tips-and-tricks-using-github/
+ http://www.owengriffin.com/posts/2010/04/15/Releasing_Maven_projects_to_Github.html
