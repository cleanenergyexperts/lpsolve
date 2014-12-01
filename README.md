LPSOLVE
=======

Library containing lpsolve java library.

To use this library in another Maven Project:
---------------------------------------------

Add the following to the pom.xml for releases:

```
<repositories>
    <repository>
        <id>maven.leadoperations.co-release</id>
        <name>AWS S3 Release Repository</name>
        <url>http://maven.leadoperations.co/release</url>
    </repository>
</repositories>
```

or for snapshots:
```
<repositories>
    <repository>
        <id>maven.leadoperations.co-snapshot</id>
        <name>AWS S3 Snapshot Repository</name>
        <url>http://maven.leadoperations.co/snapshot</url>
        <snapshots>
            <enabled>true</enabled>
        </snapshots>
    </repository>
</repositories>
```

Then add the dependency:

```
<dependency>
    <groupId>lpsolve</groupId>
    <artifactId>lpsolve</artifactId>
    <version>5.5.2</version>
</dependency>
```

To upload a new jar to the maven repository:
--------------------------------------------
`mvn deploy:deploy-file -DgroupId=lpsolve -DartifactId=lpsolve -Dversion=5.5.2 -Dpackaging=jar -Dfile=lpsolve55j.jar -DrepositoryId=aws-release -Durl=s3://maven.leadoperations.co/release`

For CloudBees, this worked as follows:
`mvn deploy:deploy-file -DgroupId=lpsolve -DartifactId=lpsolve -Dversion=5.5.2 -Dpackaging=jar -Dfile=lpsolve55j.jar -Durl=dav:https://repository-ce
e.forge.cloudbees.com/release/ -DrepositoryId=cee.forge.cloudbees.com-releases`