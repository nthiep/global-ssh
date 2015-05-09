Global-SSH
==========

Description: Global-SSH webservice, application help connect SSH to computer via p2p network, use hole punching create TCP connect and use for SSH

How use Global-SSH:
-------
connect to machine:
<!-- highlight:-d language:console -->
	$gsh [user@]hostname
	hostname can use MAC address
option:
<!-- highlight:-d language:console -->
	Options:
		--version             show program's version number and exit
		-h, --help            show this help message and exit

	Network:
		-J, --join          Join a Domain
		-R, --register      Create new Domain
		-W *, --work=*      Join a Workgroup
		-C *, --create=*    [workgroup] create a Workgroup
		-D *, --delete=*    [workgroup] delete Workgroup
		-L, --logout        logout Domain or Workgroup

	Connect:
		--connect=HOSTNAME  -c [user@]hostname or mac
		-s *, --service=*   [user@]hostname -s service_command
		-p *, --port=*      [user@]hostname -p port
		-c *, --command=*   [user@]hostname -c command
		-i *, --identity=*  [user@]hostname -i identity_file
		-v, --verbose       [user@]hostname -v debugging mode

	Infomation:
		-l, --list          show peer online
		-I, --info          show infomation of machine
		-m *, --mac=*       -I -m hostname

show machines:
<!-- highlight:-d language:console -->
	$ gsh [-l]

connect to other service:
<!-- highlight:-d language:console -->
	$ gsh hostname --port {port}
	this will return local port
to connect use:
<!-- highlight:-d language:console -->
	$ {service} [option] -p {port}


How to install:
-------
use git to clone gsh:
<!-- highlight:-d language:console -->
	$ git clone https://github.com/nthiep/global-ssh.git
or download zip/tar.gz file then extract file.

run setup tool:
<!-- highlight:-d language:console -->
	$ sudo python setup.py install

check service is running:
<!-- highlight:-d language:console -->
	$ sudo service gshd status

About project
-------
This project will build a application tool to connect linux computer behind NAT use hole punching and multi hole punching for symmetric NAT.
Our team: Nguyen Thanh Hiep and Nguyen Huu Dinh

####View details at: https://gssh.github.io