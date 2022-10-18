# ADCD

Files and utilities making it easier to use ADCD on z/OS

This GIT repository contains the changes I have made to make the ADCD work as I would like.   This covers


- TLS setup
- Keyring setup
- TN3270 setup
- PAGENT for running AT-TLS
- IP V6 configuration
     
## JCL.ZPDT

CERTS
: The definitions from appending E of the ZPDT manual for creating the keystore for X3270 an TLS


## USER.PARMLIB 

BPXPRM00
: Support for additional TCPIP stacks (TCPIP1, TCPIP2, TCPIP3, and TCPIP4).  And support for IP V6, with AF_INET6. 

CONSOLCP
:  Define a console

BPXPRM00
: COnf

## USER.PROCLIB 
CTWTR
: Procedure for collecing CTRACE output and writing it to a dataset

## USER.TCPPARMS

IFCONFIG6
: one line statement to get TCPIP configured for IP V6

IFACE6
: Defines a QDIO interface for IP V6 support

PAGENTCF
: The highlevel ConFiguration file for PAGENT defining AT-TLS

PAGENTCO
: A PAGENT configuration file showing common TLS definitions.   It include all of the cipher specs available - but commented out.

PAGENTEN
: The environment file for PAGENT
PAGENTT
: The PAGENT configuration file for one TCPIP Image

PAGENTTN
:  The configuration file for X3270 and TN3270

TN3270
:  The high level TN3270 configuration file

TNPT2023 
:  The TN3270 configuration file for the TLS port 2023

## USER.VTAMLST
TRLE
: The file containing the VTAM OSA definition used by IP V6 on ADCD and zPDT

## etc
The Unix directory containing 
syslog.conf
:  The file for configuring SYSLOGD 
