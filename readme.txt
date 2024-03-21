
** See: OAAppStore jpackage/readme.txt

New runtime versions of OAAppStore are stored in the oaappstore-run github repo.

Each version will be stored under a new github tag.
    ex: 3.2.1

Set version (multiple places):
    src/main/java/com/viaoa/appstore/resource/values.properties
    pom.xml

   
To run as executable jar file
    1: copy files (not directories) from oaappstore-run/executable-jar to a directory on users computer
    2: java -jar oaAppStore.jar single
    
    
        