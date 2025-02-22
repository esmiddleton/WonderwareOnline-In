Publisher Diagnostics
=====================

Typical control network architectures create a lot of obstacles for publishing data to AVEVA Insight. To help diagnose problems with network and/or on-premises components working with AVEVA Insight, use the Powershell scripts.

DMZ
---
Although these tools can be useful in other architectures, they assume the Publisher is deployed behind a DMZ which protects against general Internet access and that a web proxy, such as AVEVA's [DMZ Secure Link](https://insight.connect.aveva.com/Downloads/InsightPublisher/DMZSecureLink.zip "free DMZ Secure Link download"), is installed on a Windows system within the DMZ. 

Tutorial
--------
There is also a [brief video tutorial](https://www.youtube.com/watch?v=5ABdq7KvQDU "Watch") describing the architecture and network configuration

Publisher Network Diagnostics
-----------------------------

A full diagnostics script to use to report on most network and Publisher-related configuration information which:

1. Displays network configuration information
1. Displays configuration settings for AVEVA Publishers and DMZ Secure Link
1. Reports the results of various communications tests to help pinpoint the cause of problems
1. Where feasible, includes interpretation of the cause and offers recommendations
1. Is a succinct way to describe communication problems when working with Technical Support and IT

Example output from running this script on the Publisher node and on the DMZ Secure Link node are also included. These results are based on the configuration described in the tutorial and use the same IP addresses shown there and in the summary illustration below.

Getting Help
------------
If you need help getting publishing to work, there are a lot of details specific to your environment that you need to share. ![This worksheet](https://github.com/esmiddleton/Wonderware-Online-InSight/blob/master/Publishing/Insight%20Publishing%20Topology%20Worksheet.xlsx) can help capture many of those details. Some will not apply, but even capturing the fact that they don't apply can be a help. Complete the "Customer" tab and share it with whoever is providing assistance. See the "Example" tab to see what information is expected. 

Manual Tests
------------
The core of the more comprehensive "PublisherNetworkDiagnostics.ps1" script is a few Powershell commands to test ports and HTTP requests. For those who want to do their own targeted tests, the "ManualPublisherTests.ps1" provides some useful examples/reference.
![Example Network for Insight](https://user-images.githubusercontent.com/20399082/75187015-01cb3d00-56fe-11ea-8bb4-4c3a325bce2a.PNG)
