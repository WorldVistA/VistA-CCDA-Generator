# VistA-CCDA-Generator

This VistA CCD-A Generator project is for Health Level 7 (HL7) Clinical Document Architecture (CDA) XML-based patient data output for exchange from World Vista systems.

After installing Docker Desktop and WorldVistA EHR, you can follow this [YouTube Video](https://studio.youtube.com/video/nK2yi22AyC8/) for the rest.

# Pre-Installation Requirements

[Docker Desktop](https://hub.docker.com/editions/community/docker-ce-desktop-windows/) or [Docker Engine](https://docs.docker.com/engine/install/ubuntu/) for linux

[WorldVistA EHR](https://hub.docker.com/r/worldvista/worldvista-ehr)

[M-Web-Server by Sam Habiel](https://github.com/shabiel/M-Web-Server/) [Add Services Below]

[VISTA XML Processing Utilities by Sam Habiel](https://github.com/shabiel/VISTA-xml-processing-utilities) [If you are not on World VistA only]

# Installation

World VistA Installation

`docker run -d -p 2222:22 -p 8001:8001 -p 8080:8080 -p 9430:9430 -p 9080:9080 --name=wv worldvista/worldvista-ehr`

`docker exec -it wv su - wv

Add M-Web-Server Services 

`mumps -dir`

`WV> S DUZ=1`

`WV> D ^XUP`

 Press 'Enter' back to prompt

`WV> d addService^%webutils("GET","resources/*","FILESYS^%webapi")`

`WV> d addService^%webutils("GET","ccda/{patientId}","wsCCDA^C0CDA")`

Clone VistA-CCDA-Generator

`git clone https://github.com/WorldVistA/VistA-CCDA-Generator/`

Move clone to the (p)atches folder

`cd VistA-CCDA-Generator`

`cd src`

`cp *.m ~/p/`

For missing CDA.xsl error

`cd ~/www`

`mkdir css`

`cd css`

`wget http://syn.vistaplex.org/css/CDA.xsl`
