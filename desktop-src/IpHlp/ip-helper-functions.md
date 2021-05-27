---
title: IP-Hilfsfunktionen
description: Die folgenden Funktionen rufen Konfigurationseinstellungen für den TCP/IP-Transport auf dem lokalen Computer ab und ändern sie.
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
ms.openlocfilehash: ae19803c25512242b613735a060c7beda8c1df70
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549505"
---
# <a name="ip-helper-functions"></a>IP-Hilfsfunktionen

Die folgenden Funktionen rufen Konfigurationseinstellungen für den TCP/IP-Transport auf dem lokalen Computer ab und ändern sie. Die folgende kategorische Auflistung kann dabei helfen, zu bestimmen, welche Auflistung von Funktionen für eine bestimmte Aufgabe am besten geeignet ist.

-   [**GetNetworkConnectivityHint**](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [**GetNetworkConnectivityHintForInterface**](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [**NotifyNetworkConnectivityHintChange**](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a>Adapterverwaltung

-   [**GetAdapterIndex**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [**GetAdaptersAddresses**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [**GetAdaptersInfo**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [**GetPerAdapterInfo**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [**GetUniDirectionalAdapterInfo**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a>ARP-Verwaltung (Address Resolution Protocol)

-   [**CreateIpNetEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [**CreateProxyArpEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [**DeleteIpNetEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [**DeleteProxyArpEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [**FlushIpNetTable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [**GetIpNetTable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [**SendARP**](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [**SetIpNetEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a>Schnittstellenkonvertierung

-   [**ConvertInterfaceAliasToLuid**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [**ConvertInterfaceGuidToLuid**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [**ConvertInterfaceIndexToLuid**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [**ConvertInterfaceLuidToAlias**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [**ConvertInterfaceLuidToGuid**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [**ConvertInterfaceLuidToIndex**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [**ConvertInterfaceLuidToNameA**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [**ConvertInterfaceLuidToNameW**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [**ConvertInterfaceNameToLuidA**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [**ConvertInterfaceNameToLuidW**](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [**if \_ indextoname**](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [**if \_ nametoindex**](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a>Schnittstellenverwaltung

-   [**GetFriendlyIfIndex**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [**GetIfEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [**GetIfEntry2**](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [**GetIfEntry2Ex**](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [**GetIfStackTable**](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [**GetIfTable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [**GetIfTable2**](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [**GetIfTable2Ex**](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [**GetInterfaceInfo**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [**GetInvertedIfStackTable**](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [**GetIpInterfaceEntry**](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [**GetIpInterfaceTable**](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [**GetNumberOfInterfaces**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [**InitializeIpInterfaceEntry**](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [**SetIfEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [**SetIpInterfaceEntry**](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a>Internetprotokoll (IP) und Internet Control Message Protocol (ICMP)

-   [**GetIcmpStatistics**](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [**GetIpStatistics**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [**Icmp6CreateFile**](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [**Icmp6ParseReplies**](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [**Icmp6SendEcho2**](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [**IcmpCloseHandle**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [**IcmpCreateFile**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [**IcmpParseReplies**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [**IcmpSendEcho**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [**IcmpSendEcho2**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [**IcmpSendEcho2Ex**](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [**SetIpTTL**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a>IP-Adressverwaltung

-   [**AddIPAddress**](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [**CreateAnycastIpAddressEntry**](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [**CreateUnicastIpAddressEntry**](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [**DeleteIPAddress**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [**DeleteAnycastIpAddressEntry**](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [**DeleteUnicastIpAddressEntry**](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [**GetAnycastIpAddressEntry**](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [**GetAnycastIpAddressTable**](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [**GetIpAddrTable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [**GetMulticastIpAddressEntry**](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [**GetMulticastIpAddressTable**](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [**GetUnicastIpAddressEntry**](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [**GetUnicastIpAddressTable**](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [**InitializeUnicastIpAddressEntry**](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [**IpReleaseAddress**](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [**IpRenewAddress**](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [**NotifyStableUnicastIpAddressTable**](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [**SetUnicastIpAddressEntry**](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a>Konvertierung von IP-Adresszeichenfolgen

-   [**RtlIpv4AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [**RtlIpv4AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [**RtlIpv4StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [**RtlIpv4StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a>VERWALTUNG VON IP-Nachbaradressen

-   [**CreateIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [**DeleteIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [**FlushIpNetTable2**](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [**GetIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [**GetIpNetTable2**](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [**ResolveIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [**ResolveNeighbor**](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [**SetIpNetEntry2**](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a>IP-Pfadverwaltung

-   [**FlushIpPathTable**](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [**GetIpPathEntry**](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [**GetIpPathTable**](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a>IP-Routenverwaltung

-   [**CreateIpForwardEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [**CreateIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [**DeleteIpForwardEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [**DeleteIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [**EnableRouter**](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [**GetBestInterface**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [**GetBestInterfaceEx**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [**GetBestRoute**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [**GetBestRoute2**](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [**GetIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [**GetIpForwardTable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [**GetIpForwardTable2**](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [**GetRTTAndHopCount**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [**InitializeIpForwardEntry**](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [**SetIpForwardEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [**SetIpForwardEntry2**](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [**SetIpStatistics**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [**SetIpStatisticsEx**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [**UnenableRouter**](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a>Verwaltung des IP-Tabellenspeichers

-   [**FreeMibTable**](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a>IP-Hilfsprogramm

-   [**ConvertIpv4MaskToLength**](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [**ConvertLengthToIpv4Mask**](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [**CreateSortedAddressPairs**](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [**ParseNetworkString**](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a>Netzwerkkonfiguration

-   [**GetNetworkParams**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a>Benachrichtigung

-   [**CancelMibChangeNotify2**](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [**NotifyAddrChange**](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [**NotifyIpInterfaceChange**](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [**NotifyRouteChange**](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [**NotifyRouteChange2**](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [**NotifyUnicastIpAddressChange**](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="packet-timestamping"></a>Paketzeitstempel

-   [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)
-   [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities)
-   [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)
-   [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange)
-   [**UnregisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/unregisterinterfacetimestampconfigchange)

## <a name="persistent-port-reservation"></a>Persistente Portreservierung

-   [**CreatePersistentTcpPortReservation**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [**CreatePersistentUdpPortReservation**](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [**DeletePersistentTcpPortReservation**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [**DeletePersistentUdpPortReservation**](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [**LookupPersistentTcpPortReservation**](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [**LookupPersistentUdpPortReservation**](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a>Sicherheitsintegrität

-   [**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))
-   [**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))

Diese Funktionen werden nur unter Windows Server 2003 definiert.

> [!Note]  
> Diese Funktionen sind weder unter Windows Vista noch unter Windows Server 2008 verfügbar.

## <a name="teredo-ipv6-client-management"></a>Teredo IPv6-Clientverwaltung

-   [**GetTeredoPort**](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a>Transmission Control Protocol (TCP) und User Datagram Protocol (UDP)

-   [**GetExtendedTcpTable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [**GetExtendedUdpTable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [**GetOwnerModuleFromTcp6Entry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [**GetOwnerModuleFromTcpEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [**GetOwnerModuleFromUdp6Entry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [**GetOwnerModuleFromUdpEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [**GetPerTcp6ConnectionEStats**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [**GetPerTcpConnectionEStats**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [**GetTcpStatistics**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [**GetTcpStatisticsEx**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [**GetTcpStatisticsEx2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [**GetTcp6Table**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [**GetTcp6Table2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [**GetTcpTable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [**GetTcpTable2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [**SetPerTcp6ConnectionEStats**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [**SetPerTcpConnectionEStats**](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [**SetTcpEntry**](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [**GetUdp6Table**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [**GetUdpStatistics**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [**GetUdpStatisticsEx**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [**GetUdpStatisticsEx2**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [**GetUdpTable**](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a>Nicht mehr unterstützte APIs

> [!Note]  
> Diese Funktionen sind veraltet und werden von Microsoft nicht unterstützt.

-   [**AllocateAndGetTcpExTableFromStack**](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [**AllocateAndGetUdpExTableFromStack**](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
