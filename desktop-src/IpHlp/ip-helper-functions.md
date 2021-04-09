---
description: Mit den folgenden Funktionen werden die Konfigurationseinstellungen für den TCP/IP-Transport auf dem lokalen Computer abgerufen und geändert.
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
title: Funktionen des IP-Hilfsprogramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c8bff21f41c04bb5aecf505b251fbbe2f8bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760477"
---
# <a name="ip-helper-functions"></a>IP-Hilfsfunktionen

Mit den folgenden Funktionen werden die Konfigurationseinstellungen für den TCP/IP-Transport auf dem lokalen Computer abgerufen und geändert. Die folgende kategorische Auflistung kann helfen, zu bestimmen, welche Sammlung von Funktionen für eine bestimmte Aufgabe am besten geeignet ist.

-   [**Getnetworkconnectivityhint**](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [**Getnetworkconnectivityhintforinterface**](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [**Notifynetworkconnectivityhintchange**](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a>Adapter Verwaltung

-   [**GetAdapterIndex**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [**Getadaptersadressen**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [**Getadaptersinfo**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [**Getperadapterinfo**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [**Getunidirectionaladapterinfo**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a>Address Resolution Protocol (ARP)-Verwaltung

-   [**"Kreateipnetentry"**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [**"Kreateproxyarpentry"**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [**Deleteipnetentry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [**Deleteproxyarpentry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [**Flushipnettfähig**](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [**Getipnettfähig**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [**Sendarp**](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [**"-Netentry"**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a>Schnittstellen Konvertierung

-   [**Convertinterfacealiastoluid**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [**Convertinterfaceguidtoluid**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [**Convertinterfakeingedextoluid**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [**Convertinterfakeluidesalias**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [**Convertinterfakeluidtoguid**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [**Convertinterfakeluidumindex**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [**Convertinterfakeluidtonamea**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [**Convertinterfakeluidtonamew**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [**Convertinterfakenametoluida**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [**Convertinterfakenametoluidw**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [**If \_ indextoname**](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [**Wenn \_ nametoindex**](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a>Schnittstellen Verwaltung

-   [**Getfriendlyifindex**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [**Getif-Eintrag**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [**GetIfEntry2**](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [**GetIfEntry2Ex**](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [**Getifstacktable**](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [**Getiftbar**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [**GetIfTable2**](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [**GetIfTable2Ex**](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [**Getinterfacetten Info**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [**Getinvertedifstacktable**](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [**Getipinterfaceentry**](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [**Getipinterfaketable**](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [**Getnumofintergesichter**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [**Initializeipinterfaceentry**](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [**"Eintrag"**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [**""-Interfaceentry "**](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a>Internetprotokoll (IP) und Internet Control Message Protocol (ICMP)

-   [**GetIcmpStatistics**](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [**GetIpStatistics**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [**Icmp6CreateFile**](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [**Icmp6ParseReplies**](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [**Icmp6SendEcho2**](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [**Icmpclosehandle**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [**Icmpkreatefile**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [**Icmpparamesereplies**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [**Icmpsendecho**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [**IcmpSendEcho2**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [**IcmpSendEcho2Ex**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [**"Abgleichen"**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a>IP-Adressverwaltung

-   [**Addipaddress**](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [**"Kreateanycastipaddressentry"**](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [**"Kreateunicastipaddressentry"**](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [**Deleteipaddress**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [**Deleteanycastipaddressentry**](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [**Deleteunicastipaddressentry**](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [**Getanycastipaddressentry**](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [**Getanycastipadresssstable**](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [**Getipaddrtable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [**Getmulticastipaddressentry**](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [**Getmulticastipadresssstable**](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [**Getunicastipaddressentry**](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [**Getunicastipadresssstable**](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [**Initializeunicastipaddressentry**](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [**Ipreleaseaddress**](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [**Iprenewaddress**](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [**Notifystableunicastipadresssstable**](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [**"Setup"**](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a>Konvertieren von IP-Adressen

-   [**RtlIpv4AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [**RtlIpv4AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [**RtlIpv4StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [**RtlIpv4StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a>IP-Nachbar Adressverwaltung

-   [**CreateIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [**DeleteIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [**FlushIpNetTable2**](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [**GetIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [**GetIpNetTable2**](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [**ResolveIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [**Resolveneighbor**](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [**SetIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a>IP-Pfad Verwaltung

-   [**Flushippathtable**](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [**Getippathentry**](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [**Getippathtable**](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a>IP-Routen Verwaltung

-   [**"Kreateipforwardentry"**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [**CreateIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [**Deleteipforwardentry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [**DeleteIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [**Enablerouter**](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [**Getbestinterface**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [**Getbestinterfaceex**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [**Getbestroute**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [**GetBestRoute2**](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [**GetIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [**Getipforwardtable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [**GetIpForwardTable2**](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [**Getrttandhopcount**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [**Initializeipforwardentry**](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [**"Gtipforwardentry"**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [**SetIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [**""-Statistik**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [**"* Tipstatisticsex"**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [**Unenablerouter**](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a>Speicherverwaltung für IP-Tabellen

-   [**Frei wählbar**](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a>IP-Hilfsprogramm

-   [**ConvertIpv4MaskToLength**](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [**ConvertLengthToIpv4Mask**](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [**"Kreatesortedadresssspairs"**](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [**Parameeworkstring**](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a>Netzwerkkonfiguration

-   [**Getnetworkparameams**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a>Benachrichtigung

-   [**CancelMibChangeNotify2**](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [**Notifyaddrchange**](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [**Notizyipinterfacechange**](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [**Notifyroutechange**](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [**NotifyRouteChange2**](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [**Notifyunicastipadresssschange**](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="persistent-port-reservation"></a>Persistente Port Reservierung

-   [**"Kreatepersistenttcpportreservation"**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [**"Kreatepersistentudpportreservation"**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [**Deletepersistenttcpportreservation**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [**Deletepersistentudpportreservation**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [**Lookuppersistenttcpportreservation**](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [**Lookuppersistentudpportreservation**](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a>Sicherheitsintegrität

-   [**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))
-   [**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))

Diese Funktionen werden nur auf Windows Server 2003 definiert.

> [!Note]  
> Diese Funktionen sind unter Windows Vista und Windows Server 2008 nicht verfügbar.

## <a name="teredo-ipv6-client-management"></a>Teredo-IPv6-Client Verwaltung

-   [**Getteredoport**](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [**Notifyteredoportchange**](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [**Notifystableunicastipadresssstable**](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a>Transmission Control Protocol (TCP) und User Datagram Protocol (UDP)

-   [**Getextende dtcptable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [**Getextendedudptable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [**GetOwnerModuleFromTcp6Entry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [**Getownermodulefromtcpentry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [**GetOwnerModuleFromUdp6Entry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [**Getownermodulefromudpentry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [**GetPerTcp6ConnectionEStats**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [**Getpertcpconnectionestats**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [**GetTcpStatistics**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [**Gettcpstatisticsex**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [**GetTcpStatisticsEx2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [**GetTcp6Table**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [**GetTcp6Table2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [**GetTcpTable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [**GetTcpTable2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [**SetPerTcp6ConnectionEStats**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [**Setpertcpconnectionestats**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [**Settcpentry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [**GetUdp6Table**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [**GetUdpStatistics**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [**Getudpstatisticsex**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [**GetUdpStatisticsEx2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [**Getudptable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a>Nicht mehr unterstützte APIs

> [!Note]  
> Diese Funktionen sind veraltet und werden von Microsoft nicht unterstützt.

-   [**"Zuweisung von" "" "".**](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [**"Zuweisung von" "" "".**](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
