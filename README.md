pinger2
=======

official pinger2 network monitoring


DESCRIPTION
===========

PingER2 - Ping End-to-end Reporting Tool v2


PREREQUISITES
=============

PingER2 has many prerequisites that must be installed before execution.  PingER2 may install correctly without the prerequisites, but execution behavior will be undefined.

XML::Simple v2.12
	The perl module XML::Simple version 2.12 or higher must be available to PingER2.  The easiest way to handle this is to simply install it as root using the CPAN shell.  If this is impossible, download the XML::Simple distribution from CPAN (XML-Simple-2.12.tar.gz), unpack the contents, and copy the entire XML-Simple-2.12/lib/XML directory to the data directory where PingER2 is installed.  With a standard PingER2 installation this will be /usr/local/share/pinger

ping and ping6
	ping must be installed and available to PingER2.  If ping6 is not available, PingER2 will not be able to operate in IPv6 mode.

dig
	dig (domain information groper) must be available to PingER2 for IPv6 mode.  If dig is unavailable, PingER2 will not function in IPv6 mode.

mail
	mail must be available to PingER2 in order to notify admins of alarms.  If mail is unavailable, alarm notifications will not be sent.

lynx
	The text browser lynx must be installed in order for PingER2 to download the beacon list.

Java v1.4
	To use the interactive configuration tools, Java 1.4 or higher must be installed.

BUILDING / INSTALLING

Once the package is unpacked, use the following commands to make and install it:

	./configure
	make test_prereqs
	make
	make install
	make install_cron ### Only run to make pinger execute automatically

Note 1: By default, PingER2 will install into /usr/local/bin  To specify a different installation path, specify it as an option to ./configure.  For example, to install to /foo/bin:
	./configure --prefix=/foo

Note 2: If test_prereqs gives any error messages, you must resolve these pre-requisite problems before executing PingER2

Note 3: install_cron adds pinger to the cron tab, thereby scheduling it for execution determined by WaitInterval in pinger.xml

STATUS
======

PingER2 2.0.1 is the first release of PingER version 2.

Please send feedback to Warren Matthews: warren.matthews@oit.gatech.edu
