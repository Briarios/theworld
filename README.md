ok so

After much trials and tribulations of living in China i have found a rather simple solution to get over the GFW
without the use of a VPN, what you need is shown below and relevent links to them, you are of course able to swear and whinge
all you like as it may or may notbe frustrating for some of you. So lets Get started!

For all Users

go here http://dnscrypt.org/

and download the files you need for your OS ( click on the green button at the top right hand side) 
once you have downloaded it please follow the instructions on the site and you should be good in installing the software.

If you download the linux/OSX versions please ensure you have downloaded libsodium as well, it is a required package.
also make sure you have downloaded the build-essentials and m4 (just incase)

-------------------

libsodium --> http://download.libsodium.org/libsodium/releases/

when using wget ensure you use the http:// instead of https:// as it will break.


with libsodium just do the standard ./configure && make && make check && make install 

to install the program

-------------------

With dnscrypt you can do the same thing ./configure && make && make check && make install

to install the program, however if you need to install it on a RaspberryPi please ensure you have the ./configure --host=armv6l set otherwise it will break and you will end in tears. (note: i can't remember the correct switch so read --help first )

-------------------

windows users just follow the websites instructions on how to install it. 

-------------------

once installed follow the website instructions and set your interface dns to 127.0.0.1 and ensure that dnscrypt is running and you should be sweet. 

after installing dnscrypt

you will need to edit your hosts file

at either /etc/hosts file in linux/OSX or C:\Windows\System32\drivers\etc\hosts file in Windows flavours

and you will need to add in the ip addresses of the hosts.txt file which is in the same git as this readme

these ip addresses are addresses of youtube's many caching servers around the world. 

these ip addresses should provide usefullness when youtube goes full https

------------------

after you have done all that there is one last thing you need to do 

you need to install firefox or chrome and then go here https://www.eff.org/https-everywhere

to install an addon that allows you to view https versions of some websites. 

Note: not all websites you visit that have been blocked will have a https version. Also At this stage, even though youtube have a https site, they do not yet have their video caching servers on https and because it is on http the GFW will send a TCP RST to disconnect the session. as of 15-09-2013 I have sent them a feedback form asking for them to do https but at this stage unlikely it will get done. 

-------------------

so in all all websites should become visible again after doing this hack, but please remember that the GFW may update to block https in the future or start blocking websites or do null route injection to prevent people accessing websites altogether. some websites may need a vpn like the youtube videos so if you know anyone working in youtube/google please tell them to hurry up :P or if your a gifted coder maybe you can find a way to route the http video servers over a https link and then inject the code into the youtube website. 

Best o'luck to ye

Briarios.

