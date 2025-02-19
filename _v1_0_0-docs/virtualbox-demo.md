---
title: VirtualBox
layout: default
prev_section: aws-demo
next_section: publishing-demo-how-to
category: Miscellaneous
permalink: v1_0_0-docs/virtualbox-demo/
---
## Requirements
* VirtualBox: version 4.3 and up(version 5 and up recommended)
* CPU: faster CPU = faster concept extraction
* Disk: at least 50g
* RAM: at least 28g

## Download
[Ontotext public FTP](ftp://ftp.ontotext.com:/pub/dsp/pub-demo.tar.gz)

## VirtualBox Import
1. Import VM image in VirtualBox by clicking *File* -> *Import Appliance*.
<img src="{{ site.baseurl }}/img/virtualbox/import.png" alt="VirtualBox Import Appliance" style="float:none; margin:10px 0 10px 0" >
2. Select the pub-demo.ova image and click *Next*.
<img src="{{ site.baseurl }}/img/virtualbox/import-select-file.png" alt="VirtualBox Select File" style="float:none; margin:10px 0 10px 0" >
3. Make sure that *Reinitialize the MAC address of all network cards* is NOT selected.
<img src="{{ site.baseurl }}/img/virtualbox/import-overview.png" alt="VirtualBox Import Overview" style="float:none; margin:10px 0 10px 0" >
4. When import process is done, right click on the newly created VM, in the VMs list menu, and select *Headless Start*.
If your version of VirtualBox doesn't have *Headless Start* hold *Shift* button while clicking *Start*, this will start the VM in headless mode.
<img src="{{ site.baseurl }}/img/virtualbox/start.png" alt="VirtualBox VM Start" style="float:none; margin:10px 0 10px 0" >
5. Wait until the machine the state of the VM becomes *Running* and it is accessible(this may take a while, as all services are starting on boot), now you have access to the following services:
* [GraphDB™ Workbench](http://localhost:18080/graphdb)
* [Publishing TAG UI](http://localhost:19101)
* [Publishing NOW UI](http://localhost:19102)
* [Publishing Extractor API](http://localhost:19091/extractor)
* [Publishing Processor API](http://localhost:19098/processor)
* [Publishing Related Reads API](http://localhost:19099/api)
* [Publishing Concept API](http://localhost:19092/concept-api)
* [Publishing Search API](http://localhost:19095/search)
* [Elasticsearch™](http://localhost:19200)

## Access
+ Port: 2222
+ **Service User**:
    + Username: `tomcat`
    + Note: no password, login command:
    `tomcat` or `sudo su - tomcat -s /bin/bash`
+ **Root User**:
    + Username: `root`
    + Password: `ontotext`


#### SSH

```
ssh -p 2222 root@localhost
```

## Usage
See the [Publishing Demo HowTo]({{ site.baseurl }}/v1_0_0-docs/publishing-demo-how-to/) section.
