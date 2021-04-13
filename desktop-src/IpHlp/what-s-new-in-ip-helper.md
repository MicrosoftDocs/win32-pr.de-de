---
description: Neues in IP Helper
ms.assetid: fa9d72d0-2f9c-433d-b05a-8423664b2e3e
title: Neues in IP Helper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2c1a6eebb3e9e785e8988b822df0b2a80ae6eba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349018"
---
# <a name="whats-new-in-ip-helper"></a>Neues in IP Helper

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 und Windows Server 2012

Die folgenden Features wurden den IP-Hilfsskripts unter Windows 8 und Windows Server 2012 hinzugefügt.

Eine Funktion, die Verlaufs Schätzungen der Vergangenheit für eine Netzwerkverbindung abruft. Weitere Informationen finden Sie unter

-   [**Getipnetworkconnectionbandwiddermates**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates)

Eine-Struktur, die Informationen zu den verfügbaren Bandbreiten Schätzungen und zugeordneten Varianz enthält, die vom TCP/IP-Stapel bestimmt werden. Weitere Informationen finden Sie unter

-   [**NL- \_ Bandbreiten \_ Informationen**](/windows/desktop/api/Nldef/ns-nldef-nl_bandwidth_information)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

Die folgenden Features wurden den IP-Hilfsskripts unter Windows 7 und Windows Server 2008 R2 hinzugefügt.

Funktionen, die eine Ethernet-Adresse zwischen einem binären Format und einem Zeichen folgen Format für die Mac-Adresse des Ethernet konvertieren. Weitere Informationen finden Sie unter

-   [**Rtlethernetadresssstostring**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetaddresstostringa)
-   [**Rtlethernetstringdienst Address**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetstringtoaddressa)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 und Windows Vista SP1

Die folgenden Funktionen wurden den IP Helper-APIs unter Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) hinzugefügt.

Eine Funktion, die mit IPv4 und dem ICMP (Internet Control Message Protocol) funktioniert. Weitere Informationen finden Sie unter

-   [**IcmpSendEcho2Ex**](/windows/desktop/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)

## <a name="windows-vista"></a>Windows Vista

Die folgenden Gruppen von Funktionen wurden den IP-Hilfsobjekten unter Windows Vista und höher hinzugefügt.

Funktionen, die sowohl mit IPv6 als auch mit IPv4 für die Schnittstellen Konvertierung funktionieren. Weitere Informationen finden Sie unter

-   [**Convertinterfacealiastoluid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [**Convertinterfaceguidtoluid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [**Convertinterfakeingedextoluid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [**Convertinterfakeluidtoguid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [**Convertinterfakeluidumindex**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [**Convertinterfakeluidtonamea**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [**Convertinterfakeluidtonamew**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [**Convertinterfakenametoluida**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [**Convertinterfakenametoluidw**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [**If \_ indextoname**](/windows/desktop/api/Netioapi/nf-netioapi-if_indextoname)
-   [**Wenn \_ nametoindex**](/windows/desktop/api/Netioapi/nf-netioapi-if_nametoindex)

Funktionen, die für die Schnittstellen Verwaltung sowohl mit IPv6 als auch mit IPv4 funktionieren. Weitere Informationen finden Sie unter

-   [**GetIfEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getifentry2)
-   [**Getifstacktable**](/windows/desktop/api/Netioapi/nf-netioapi-getifstacktable)
-   [**GetIfTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2)
-   [**GetIfTable2Ex**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2ex)
-   [**Getinvertedifstacktable**](/windows/desktop/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [**Getipinterfaceentry**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [**Getipinterfaketable**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [**Initializeipinterfaceentry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [**""-Interfaceentry "**](/windows/desktop/api/Netioapi/nf-netioapi-setipinterfaceentry)

Funktionen, die für die IP-Adressverwaltung sowohl mit IPv6 als auch mit IPv4 funktionieren. Weitere Informationen finden Sie unter

-   [**"Kreateanycastipaddressentry"**](/windows/desktop/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [**"Kreateunicastipaddressentry"**](/windows/desktop/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [**Deleteanycastipaddressentry**](/windows/desktop/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [**Deleteunicastipaddressentry**](/windows/desktop/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [**Getanycastipaddressentry**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [**Getanycastipadresssstable**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [**Getmulticastipaddressentry**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [**Getmulticastipadresssstable**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [**Getunicastipaddressentry**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [**Getunicastipadresssstable**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [**Initializeunicastipaddressentry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [**Notifystableunicastipadresssstable**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [**"Setup"**](/windows/desktop/api/Netioapi/nf-netioapi-setunicastipaddressentry)

Eine Funktion, die sowohl mit IPv6 als auch mit IPv4 zur Verwaltung von IP-Tabellen Arbeitsspeicher funktioniert. Weitere Informationen finden Sie unter

-   [**Frei wählbar**](/windows/desktop/api/Netioapi/nf-netioapi-freemibtable)

Funktionen, die sowohl mit IPv6 als auch mit IPv4 für IP-Nachbar Adressverwaltung funktionieren. Weitere Informationen finden Sie unter

-   [**CreateIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipnetentry2)
-   [**DeleteIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [**FlushIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-flushipnettable2)
-   [**GetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetentry2)
-   [**GetIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnettable2)
-   [**ResolveIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [**Resolveneighbor**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [**SetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipnetentry2)

Funktionen, die für die IP-Pfad Verwaltung sowohl mit IPv6 als auch mit IPv4 funktionieren. Weitere Informationen finden Sie unter

-   [**Flushippathtable**](/windows/desktop/api/Netioapi/nf-netioapi-flushippathtable)
-   [**Getippathentry**](/windows/desktop/api/Netioapi/nf-netioapi-getippathentry)
-   [**Getippathtable**](/windows/desktop/api/Netioapi/nf-netioapi-getippathtable)

Funktionen, die für die IP-Routen Verwaltung sowohl mit IPv6 als auch mit IPv4 funktionieren. Weitere Informationen finden Sie unter

-   [**CreateIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [**DeleteIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [**GetBestRoute2**](/windows/desktop/api/Netioapi/nf-netioapi-getbestroute2)
-   [**GetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [**GetIpForwardTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [**Initializeipforwardentry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [**SetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [**"* Tipstatisticsex"**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)

Funktionen, die für die Benachrichtigung sowohl mit IPv6 als auch mit IPv4 funktionieren. Weitere Informationen finden Sie unter

-   [**CancelMibChangeNotify2**](/windows/desktop/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [**Notizyipinterfacechange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [**NotifyRouteChange2**](/windows/desktop/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [**Notifyunicastipadresssschange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

Hilfsfunktionen für die Verwendung von IP-Adressen. Weitere Informationen finden Sie unter

-   [**ConvertIpv4MaskToLength**](/windows/desktop/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [**ConvertLengthToIpv4Mask**](/windows/desktop/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [**"Kreatesortedadresssspairs"**](/windows/desktop/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [**Parameeworkstring**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

Funktionen, die mit dem Transmission Control Protocol (TCP) und dem User Datagram Protocol (UDP) funktionieren, um die IPv6-oder IPv4-TCP-Verbindungstabelle oder die UDP-listenertabelle abzurufen. Weitere Informationen finden Sie unter

-   [**GetTcp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [**GetTcp6Table2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [**GetTcpTable2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [**GetUdp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudp6table)

Funktionen, die mit dem Transmission Control Protocol (TCP) funktionieren, um erweiterte TCP-Statistiken für eine Verbindung abzurufen. Weitere Informationen finden Sie unter

-   [**GetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [**Getpertcpconnectionestats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [**SetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [**Setpertcpconnectionestats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)

Neue Funktionen, die für die Teredo-IPv6-Client Verwaltung funktionieren. Weitere Informationen finden Sie unter

-   [**Getteredoport**](/windows/desktop/api/Netioapi/nf-netioapi-getteredoport)
-   [**Notifyteredoportchange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [**Notifystableunicastipadresssstable**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

Hilfsfunktionen, die Konvertierungen zwischen IP-Adressen und Zeichen folgen Darstellungen von IP-Adressen bereitstellen. Weitere Informationen finden Sie unter

-   [**RtlIpv4AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [**RtlIpv4AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [**RtlIpv4StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [**RtlIpv4StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [**RtlIpv6AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [**RtlIpv6AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [**RtlIpv6StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [**RtlIpv6StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

Funktionen, die permanente Reservierungen für einen aufeinander folgenden Block von TCP-oder UDP-Ports auf dem lokalen Computer bereitstellen. Weitere Informationen finden Sie unter

-   [**"Kreatepersistenttcpportreservation"**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [**"Kreatepersistentudpportreservation"**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [**Deletepersistenttcpportreservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [**Deletepersistentudpportreservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [**Lookuppersistenttcpportreservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [**Lookuppersistentudpportreservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="windows-server-2003"></a>Windows Server 2003

Die folgenden Funktionen wurden den IP Helper-APIs unter Windows Server 2003 und höher hinzugefügt:

-   [**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))
-   [**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))

## <a name="windows-xp-sp2"></a>Windows XP SP2

Die folgenden Funktionen wurden den IP Helper-APIs unter Windows XP mit Service Pack 2 (SP2) und höher hinzugefügt:

-   [**Getownermodulefromtcpentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [**GetOwnerModuleFromTcp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [**Getownermodulefromudpentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [**GetOwnerModuleFromUdp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)

 

 
