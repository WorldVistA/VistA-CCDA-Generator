# VistA-CCDA-Generator

This VistA CCD-A Generator project is for Health Level 7 (HL7) Clinical Document Architecture (CDA) XML-based patient data output for exchange from World Vista systems.

# Pre-Installation Requirements

[Docker Desktop](https://hub.docker.com/editions/community/docker-ce-desktop-windows/) or [Docker Engine](https://docs.docker.com/engine/install/ubuntu/) for linux


[WorldVistA EHR](https://hub.docker.com/r/worldvista/worldvista-ehr)


[M-Web-Server by Sam Habiel](https://github.com/shabiel/M-Web-Server/) [Add Services Below]

`S DUZ=1`

`D ^XUP`

`d addService^%webutils("GET","resources/*","FILESYS^%webapi")`

`d addService^%webutils("GET","ccda/{patientId}","wsCCDA^C0CDA")`


[VISTA XML Processing Utilities by Sam Habiel](https://github.com/shabiel/VISTA-xml-processing-utilities) [If you are not on World VistA only]

# Installation

`git clone https://github.com/WorldVistA/VistA-CCDA-Generator/`

`cp *.m ~/p/`

wget http://syn.vistaplex.org/css/CDA.xsl
