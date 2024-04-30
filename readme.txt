

github Project used to hold OAAppStore installer and any Java Application created using OABuilder.
The windows installer will load the latest release of OAAppStore

All OABuilder Apps are then stored in the following root direcorties:

Runtime directory files, ex: server.ini, client.ini, single.ini
    https://github.com/ViaOA/oaappstore-run/raw/master/appstore
examples:
    com/viaoa/oaappstore/version.ini 
    com/viaoa/oaappstore/single.ini 

Jar file and dependency jar files:
    https://github.com/ViaOA/oaappstore-run/raw/master/jarstore

examples:
com/viaoa/oa-core-3.7.7.jar
com/viaoa/oa-jfc-3.7.7.jar
com/viaoa/dependency-uber-1.0.0.jar
 
OAAppStore uses the same directory sturcture on Windows, where it was installed.
 
=========================================


Adding / Updating a project to OAAppStore

** using oatemplate as an example

build the project (mvn install)

update files:
    OAAppStore-Run\appstore\com\viaoa\oatemplate
        version.ini
            update with changes (version, release, file names, etc) 

copy the new target\oatemplate-0.0.1.jar file (not oatemplate.jar, which is an uber jar) to
    OAAppStore-Run\jarstore\com\viaoa\oatemplate

commit project OAAppStore-Run









** See: OAAppStore jpackage/readme.txt

New runtime versions of OAAppStore are stored in the oaappstore-run github repo.



For MS Windows, use windows\windows-installer\OAAppStore.msi 
    https://github.com/ViaOA/oaappstore-run/tree/master/windows-installer   
   
   
   
   
To manually run  (NOTE: *** this needs to be updated ***)

    1: copy files (not directories) from oaappstore-run/executable-jar to a directory on users computer
         https://github.com/ViaOA/oaappstore-run/tree/master/executable-jar   
    2: read version.ini to find other jar files to download, from the "../jarstore" directory, and copy to the same directory as #1.
         https://github.com/ViaOA/oaappstore-run/tree/master/jarstore   
    
    
    3: java -cp *.jar com.viaoa.oaappstore.control.StartupController single
    
    



        