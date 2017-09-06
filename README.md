# Bradamsa

Bradamsa is a [Burp Suite](http://www.portswigger.net/burp/) extension for [Radamsa](https://code.google.com/p/ouspg/wiki/Radamsa), a well-known fuzzer made by the [Oulu University Secure Programming Group](https://www.ee.oulu.fi/research/ouspg/). Inspired by [burp-radamsa](https://github.com/Raz0r/burp-radamsa), this plugin allows to generate Intruder payloads using Radamsa.

Download the latest release from [HERE](https://github.com/ikkisoft/bradamsa/releases).

**Mix (B)urp Suite + (Radamsa) and you get crashes!**   

![Bradamsa Tab](http://i.imgur.com/ZdVE9Ow.png "Bradamsa Tab")

## Features

* Java-based plugin using native Burp Suite extension APIs 
* Intruder payloads generator using Radamsa (sniper attack type only)
* Support for Radamsa v0.3 options
* Options validation directly from within Burp Suite 

![Options validation](http://i.imgur.com/TVvE71Y.png "Options validation")

## How To Use It

1.  Install Radamsa from [Hatlp GIT](http://haltp.org/git/radamsa.git) or the official [Google project page ](https://code.google.com/p/ouspg/downloads/list)

```
$ git clone http://haltp.org/git/radamsa.git
$ cd radamsa
$ make
$ sudo make install
```

```
$ curl https://ouspg.googlecode.com/files/radamsa-0.3.tar.gz | tar -zxvf - && cd radamsa-0.3 && make && sudo make install && man radamsa
```

2. From the _Extender_ tab in Burp Suite,  add [bradamsa.jar](https://github.com/ikkisoft/bradamsa/releases) 
3. Open the _Bradamsa_ tab and configure Radamsa. For more details, please refer to the official [Radamsa page](https://code.google.com/p/ouspg/wiki/Radamsa) or type ```$ radamsa --help``` in your terminal
4.  Send a request to Burp Intruder
5.  In Payload → Payload Sets → Payload type, select "Extension-generated"
6.  In Payload → Payload Options → Select generator, choose "Bradamsa" from the drop down list
7.  Finish to configure Burp Intruder and start fuzzing  

![Payload Generator](http://i.imgur.com/POZPRss.png "Payload Generator")
