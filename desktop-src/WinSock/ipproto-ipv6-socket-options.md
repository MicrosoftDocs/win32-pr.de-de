---
description: In den folgenden Tabellen werden IPPROTO \_ IPV6-Socketoptionen beschrieben, die für Sockets gelten, die für die IPv6-Adressfamilie (AF \_ INET6) erstellt wurden. Weitere Informationen zum Abrufen und Festlegen von Socketoptionen finden Sie auf den Referenzseiten der Funktionen getsockopt und setsockopt.
ms.assetid: 65f8f7a4-757b-43a3-9d47-b115754c89d6
title: IPPROTO_IPV6-Socketoptionen
ms.topic: article
ms.date: 10/07/2019
ms.openlocfilehash: 86f8156f91e5f7e185319224e06d7bf54e87c6da
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444251"
---
# <a name="ipproto_ipv6-socket-options"></a>IPPROTO \_ IPV6-Socketoptionen

In den folgenden Tabellen werden **IPPROTO \_ IPV6-Socketoptionen** beschrieben, die für Sockets gelten, die für die IPv6-Adressfamilie (AF \_ INET6) erstellt wurden. Weitere Informationen zum Abrufen und Festlegen von Socketoptionen finden Sie auf den Referenzseiten der Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Um Protokolle aufzulisten und unterstützte Eigenschaften für jedes installierte Protokoll zu ermitteln, verwenden Sie die Funktion [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)oder [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

Einige Socketoptionen erfordern mehr Erklärung, als diese Tabellen vermitteln können. diese Optionen enthalten Links zu zusätzlichen Informationen.

## <a name="options"></a>Optionen

| Option | get | set | Optval-Typ | BESCHREIBUNG |
|-|-|-|-|-|
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | ja | ja | DWORD (boolesch) | Gibt an, ob die [**LPFN_WSARECVMSG -Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) optionale Steuerdaten zurückgeben soll, die die ursprüngliche Eingangsschnittstelle enthalten, an der das Paket für Datagrammsockets empfangen wurde. Diese Option wird mit IPv6-Übergangstechnologien (z.B. 6to4-, ISATAP- und Teredo-Tunnel) verwendet, die Adresszuweisung und automatisches Host-zu-Host-Tunneling für Unicast-IPv6-Datenverkehr bereitstellen, wenn IPv6-Hosts IP4-Netzwerke durchlaufen müssen, um andere IPv6-Netzwerke zu erreichen. IPv6-Pakete werden als IPv4-Pakete getunnelt gesendet. Mit dieser Option kann die ursprüngliche IPv4-Schnittstelle, an der das Paket empfangen wurde, in der [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) zurückgegeben werden.  |
| IPV6_ADD_IFLIST | | ja | DWORD (IF_INDEX) | Fügt der IFLIST, die der **option IP_IFLIST** zugeordnet ist, einen Schnittstellenindex hinzu. |
| IPV6 \_ MITGLIEDSCHAFT HINZUFÜGEN \_ | | ja | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Verbinden Sie den Socket mit der angegebenen Multicastgruppe auf der angegebenen Schnittstelle.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| IPV6_DEL_IFLIST | | ja | DWORD (IF_INDEX) | Entfernt einen Schnittstellenindex aus der IFLIST, die der **option IP_IFLIST** zugeordnet ist. Einträge können nur von der Anwendung entfernt werden. Beachten Sie daher, dass Einträge möglicherweise veraltet sind, sobald eine Schnittstelle entfernt wird. |
| IPV6 \_ DROP \_ MEMBERSHIP | | ja | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Belassen Sie die angegebene Multicastgruppe von der angegebenen Schnittstelle.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| IPV6_GET_IFLIST | ja | | DWORD[] (IF_INDEX[]) | Ruft die aktuelle IFLIST ab, die der **option IP_IFLIST** zugeordnet ist. Gibt einen Fehler zurück, wenn **IP_IFLIST** nicht aktiviert ist. |
| IPV6 \_ HDRINCL | ja | ja | DWORD(boolean) | Gibt an, dass die Anwendung den IPv6-Header für alle ausgehenden Daten bereitstellt. Wenn der *optval-Parameter* beim Aufruf von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **1** festgelegt ist, ist die Option aktiviert. Wenn *optval* auf **0** festgelegt ist, ist die Option deaktiviert. Der Standardwert ist „deaktiviert“. Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). Ein TCP/IP-Dienstanbieter, der SOCK RAW unterstützt, \_ sollte auch IPV6 \_ HDRINCL unterstützen. |
| IPV6 \_ HOPLIMIT | ja | ja | DWORD (boolesch) | Gibt an, dass Hopinformationen (TTL) in der [**funktion LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) zurückgegeben werden sollen. Wenn *optval* beim Aufruf von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **1** festgelegt ist, ist die Option aktiviert. Wenn auf **0** festgelegt ist, ist die Option deaktiviert.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| IPV6_IFLIST | ja | ja | DWORD (boolesch) | Ruft den **IP_IFLIST** Zustand des Sockets ab oder legt diese fest. Wenn diese Option auf TRUE festgelegt ist, ist der Empfang von Datagrammen auf Schnittstellen beschränkt, die sich in der IFLIST befinden. Für andere Schnittstellen empfangene Datagramme werden ignoriert. IFLIST wird leer gestartet. Verwenden Sie **IP_ADD_IFLIST** und **IP_DEL_IFLIST,** um die IFLIST zu bearbeiten. |
| IPV6 \_ JOIN \_ GROUP | | ja | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Identisch mit IPV6 \_ ADD \_ MEMBERSHIP |
| IPV6 \_ LEAVE \_ GROUP | | ja | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Identisch mit IPV6 \_ DROP \_ MEMBERSHIP |
| IPV6 \_ MTU | ja | | DWORD | Ruft die Schätzung des Pfads mtu des Systems ab. Socket muss verbunden sein. |
| IPV6 \_ MTU \_ DISCOVER | ja | ja | DWORD (**PMTUD \_ STATE**) | Ruft den MTU-Ermittlungsstatus des Pfads für den Socket ab oder legt den Pfad fest. Der Standardwert ist **IP \_ PMTUDISC \_ NOT \_ SET**. Für Streamsockets führen **IP \_ PMTUDISC \_ NOT \_ SET** und **IP \_ PMTUDISC \_ DO** die Pfad-MTU-Ermittlung durch. **IP-Adresse \_ PMTUDISC \_ DONT** und **IP \_ PMTUDISC \_ PROBE** deaktivieren die PFAD-MTU-Ermittlung. Wenn Datagrammsockets auf **IP \_ PMTUDISC \_ DO** festgelegt sind, führt der Versuch, Pakete zu senden, die größer als die PFAD-MTU sind, zu einem Fehler. Wenn ip **\_ PMTUDISC \_ DONT** festgelegt ist, werden Pakete gemäß der MTU-Schnittstelle fragmentiert. Wenn ip **\_ PMTUDISC \_ PROBE** festgelegt ist, führt der Versuch, Pakete zu senden, die größer als die MTU der Schnittstelle sind, zu einem Fehler.  |
| IPV6 \_ \_ MULTICAST-HOPS | ja | ja | DWORD | Ruft den TTL-Wert ab, der dem IPv6-Multicastdatenverkehr auf dem Socket zugeordnet ist, oder legt ihn fest. Es ist unzulässig, die Tl auf einen Wert größer als 255 zu setzen.  Diese Option ist nur für Datagramm- und Unformatiertocket gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| IPV6 \_ MULTICAST \_ IF | ja | ja | DWORD | Ruft die ausgehende Schnittstelle zum Senden von IPv6-Multicastdatenverkehr ab oder legt diese fest. Diese Option ändert nicht die Standardschnittstelle für den Empfang von IPv6-Multicastdatenverkehr. Diese Option ist für mehrfach vernetzte Computer wichtig.  Der Eingabewert zum Festlegen dieser Option ist ein 4-Byte-Schnittstellenindex der gewünschten ausgehenden Schnittstelle in Host-Byte-Reihenfolge. Die [**GetAdaptersAddresses-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) kann verwendet werden, um die Informationen zum Schnittstellenindex zu erhalten. Wenn *optval beim* Aufruf von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **NULL** festgelegt ist, wird die IPv6-Standardschnittstelle verwendet. Wenn *optval* 0 (null) ist, wird die Standardschnittstelle für den Empfang von Multicast zum Senden von Multicastdatenverkehr angegeben.  Beim Abrufen dieser Option gibt *optval* den aktuellen Standardschnittstellenindex zum Senden von Multicast-IPv6-Datenverkehr in Host-Byte-Reihenfolge zurück. |
| \_IPV6-MULTICASTSCHLEIFE \_ | ja | ja | DWORD (boolean) | Gibt an, dass auf dem Socket gesendete Multicastdaten an den Socket-Empfangspuffer gesendet werden, wenn sie auch in der Ziel-Multicastgruppe verbunden sind. Wenn *optval* beim Aufruf von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **1** festgelegt ist, ist die Option aktiviert. Wenn diese Option **auf 0 festgelegt** ist, ist die Option deaktiviert.  Diese Option ist nur für Datagramm- und Unformatiertocket gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| [IPV6 \_ PKTINFO](ipv6-pktinfo.md) | ja | ja | DWORD (boolean) | Gibt an, dass Paketinformationen von der funktion LPFN_WSARECVMSG [**(WSARecvMsg) zurückgegeben werden**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) sollen. |
| [\_IPV6-SCHUTZEBENE \_](ipv6-protection-level.md) | ja | ja | INT | Ermöglicht die Einschränkung eines Sockets auf einen angegebenen Bereich, z. B. Adressen mit dem gleichen lokalen Linkpräfix oder standortortspräfix. Stellt verschiedene Einschränkungsstufen und Standardeinstellungen zur Seite. Weitere [Informationen finden Sie unter IPV6-SCHUTZEBENE. \_ \_ ](ipv6-protection-level.md) |
| IPV6 \_ RECVIF | ja | ja | DWORD (boolean) | Gibt an, ob der IP-Stapel den Steuerungspuffer mit Details darüber auffüllen soll, welche Schnittstelle ein Paket mit einem Datagrammsocket empfangen hat. Wenn dieser Wert true ist, gibt die [**funktion LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) optionale Steuerungsdaten zurück, die die Schnittstelle enthalten, an der das Paket für Datagrammsockes empfangen wurde. Mit dieser Option kann die IPv6-Schnittstelle, an der das Paket empfangen wurde, in der [**WSAMSG-Struktur zurückgegeben**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) werden.  Diese Option ist nur für Datagramm- und Unformatiertocket gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| IPV6 \_ RECVTCLASS | ja | ja | DWORD (boolean) | Gibt an, ob der IP-Stapel den Steuerungspuffer mit einer Nachricht auffüllen soll, die das IPv6-Headerfeld der Traffic-Klasse für ein empfangenes Datagramm enthält. Wenn dieser Wert true ist, gibt die [**funktion LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) optionale Steuerungsdaten zurück, die den IPv6-Headerfeldwert der Traffic Class des empfangenen Datagramms enthalten.  Mit dieser Option kann das IPv6-Headerfeld der Traffic Class des empfangenen Datagramms in der [**WSAMSG-Struktur zurückgegeben**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) werden. Der zurückgegebene Nachrichtentyp ist IPV6 \_ TCLASS. Alle DSCP- und ECN-Bits des Felds Traffic Class werden zurückgegeben.  Diese Option ist nur für Datagrammsockets gültig (der Sockettyp muss SOCK \_ DGRAM sein).  |
| IPV6 \_ \_ UNICAST-HOPS | ja | ja | DWORD | Ruft den aktuellen TTL-Wert ab, der dem IPv6-Socket für Unicastdatenverkehr zugeordnet ist, oder legt ihn fest. Es ist unzulässig, die Tl auf einen Wert größer als 255 zu setzen. |
| IPV6 \_ UNICAST \_ IF | ja | ja | DWORD (IF \_ INDEX) | Ruft die ausgehende Schnittstelle zum Senden von IPv6-Datenverkehr ab oder legt sie fest. Diese Option ändert nicht die Standardschnittstelle für den Empfang von IPv6-Datenverkehr. Diese Option ist für mehrfach vernetzte Computer wichtig.  Der Eingabewert zum Festlegen dieser Option ist ein 4-Byte-Schnittstellenindex der gewünschten ausgehenden Schnittstelle in Host-Byte-Reihenfolge. Die [**GetAdaptersAddresses-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) kann verwendet werden, um die Informationen zum Schnittstellenindex zu erhalten. Wenn *optval* 0 (null) ist, wird die Standardschnittstelle zum Senden von IPv6-Datenverkehr auf nicht angegeben festgelegt.  Beim Abrufen dieser Option gibt *optval* den aktuellen Standardschnittstellenindex zum Senden von IPv6-Datenverkehr in Host-Byte-Reihenfolge zurück. |
| IPV6_USER_MTU | ja | ja | DWORD | Ruft eine Obergrenze für die IP-Schicht-MTU (in Bytes) für den angegebenen Socket ab oder legt diese fest. Wenn der Wert höher als die Schätzung des Mtu-Pfadpfads des Systems ist (den Sie auf einem verbundenen Socket abrufen können, indem Sie die Option **IPV6_MTU** Socket abfragen), hat die Option keine Auswirkungen. Wenn der Wert niedriger ist, werden ausgehende Pakete, die größer als dieser sind, fragmentiert oder können abhängig vom Wert von **IPV6_DONTFRAG.** Der Standardwert ist **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Zur Typsicherheit sollten Sie die [**Funktionen WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) und [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) verwenden, anstatt die Socketoption direkt zu verwenden. |
| IPV6 \_ V6ONLY | ja | ja | DWORD (boolean) | Gibt an, ob ein für die AF INET6-Adressfamilie erstellter Socket \_ nur auf IPv6-Kommunikation beschränkt ist. Sockets, die für die AF INET6-Adressfamilie erstellt wurden, können sowohl für die IPv6- als auch für \_ die IPv4-Kommunikation verwendet werden. Einige Anwendungen möchten die Verwendung eines Sockets, der für die AF INET6-Adressfamilie erstellt wurde, möglicherweise auf \_ IPv6-Kommunikation beschränken. Wenn dieser Wert ungleich 0 (standard unter Windows) ist, kann ein für die AF INET6-Adressfamilie erstellter Socket nur zum Senden und Empfangen von \_ IPv6-Paketen verwendet werden. Wenn dieser Wert 0 (null) ist, kann ein Socket, der für die AF INET6-Adressfamilie erstellt wurde, zum Senden und Empfangen von Paketen an und von einer \_ IPv6-Adresse oder einer IPv4-Adresse verwendet werden. Die Möglichkeit der Interaktion mit einer IPv4-Adresse setzt die Verwendung von IPv4-zugeordneten Adressen voraus. Diese Socketoption wird unter Windows Vista oder höher unterstützt. |

## <a name="windows-support-for-ipproto_ipv6-socket-options"></a>Windows-Unterstützung für IPPROTO \_ IPV6-Socketoptionen

| Option | Windows 8 | Windows Server 2012 | Windows 7 | WindowsServer 2008 | Windows Vista |
|-|-|-|-|-|-|
| URSPRÜNGLICHE \_ \_ IP-ANKUNFT, \_ WENN | x | x | x | | |
| IPV6_ADD_IFLIST | Ab Windows 10 Version 1803 | | | | |
| IPV6 \_ MITGLIEDSCHAFT HINZUFÜGEN \_ | x | x | x | x | x |
| IPV6_DEL_IFLIST | Ab Windows 10 Version 1803 | | | | |
| IPV6 \_ DROP \_ MEMBERSHIP | x | x | x | x | x |
| IPV6_GET_IFLIST | Ab Windows 10 Version 1803 | | | | |
| IPV6 \_ HDRINCL | x | x | x | x | x |
| IPV6 \_ HOPLIMIT | x | x | x | x | x |
| IPV6_IFLIST | Ab Windows 10 Version 1803 | | | | |
| IPV6 \_ JOIN \_ GROUP | x | x | x | x | x |
| IPV6 \_ LEAVE \_ GROUP | x | x | x | x | x |
| IPV6 \_ \_ MULTICAST-HOPS | x | x | x | x | x |
| IPV6 \_ MULTICAST \_ IF | x | x | x | x | x |
| IPV6 \_ \_ MULTICAST-SCHLEIFE | x | x | x | x | x |
| IPV6 \_ PKTINFO | x | x | x | x | x |
| [\_IPV6-SCHUTZEBENE \_](ipv6-protection-level.md) | x | x | x | x | x |
| IPV6 \_ RECVIF | x | x | x | x | x |
| IPV6 \_ \_ UNICAST-HOPS | x | x | x | x | x |
| IPV6 \_ UNICAST \_ IF | x | x | x | x | x |
| IPV6 \_ V6ONLY | x | x | x | x | x |

<br/>

| Option | Windows Server 2003 | Windows XP |
|-|-|-|
| URSPRÜNGLICHE \_ \_ IP-ANKUNFT, \_ WENN | | |
| IPV6_ADD_IFLIST | | |
| IPV6– \_ MITGLIEDSCHAFT \_ HINZUFÜGEN | x | x |
| IPV6_DEL_IFLIST | | |
| IPV6 \_ DROP \_ MEMBERSHIP | x | x |
| IPV6_GET_IFLIST | | |
| IPV6 \_ HDRINCL x | x |
| IPV6 \_ HOPLIMIT x | x |
| IPV6_IFLIST | | |
| IPV6 \_ JOIN \_ GROUP | x | x |
| IPV6 \_ LEAVE \_ GROUP | x | x |
| \_IPV6-MULTICAST-HOPS \_ | x | x |
| IPV6 \_ MULTICAST \_ IF | x | x |
| \_IPV6-MULTICASTSCHLEIFE \_ | x | x |
| IPV6 \_ PKTINFO | x | x |
| [\_IPV6-SCHUTZEBENE \_](ipv6-protection-level.md) | x | x |
| IPV6 \_ RECVIF | | |
| IPV6 \_ \_ UNICAST-HOPS | x | x |
| IPV6 \_ UNICAST \_ IF | | |
| IPV6 \_ V6ONLY | | |

## <a name="remarks"></a>Hinweise

Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Headerdateien geändert, und die **IPPROTO \_ IPV6-Ebene** wird in der *Headerdatei Ws2def.h* definiert, die automatisch in der *Winsock2.h-Headerdatei* enthalten ist. Die **IPPROTO \_ IPV6-Socketoptionen** werden in der *Headerdatei Ws2ipdef.h* definiert, die automatisch in der *Ws2tcpip.h-Headerdatei* enthalten ist. Die *Headerdateien Ws2def.h* und *Ws2ipdef.h* sollten nie direkt verwendet werden.

Die IP \_ ORIGINAL \_ ARRIVAL \_ IF-Socketoption wird unter Windows Server 2008 R2 sowie unter Windows 7 unterstützt.

## <a name="requirements"></a>Requirements (Anforderungen)

| Anforderung | Wert |
|-|-|
| Header | <dl> <dt>Ws2def.h (einschließlich Winsock2.h); </dt> <dt>Winsock2.h unter Windows Server 2003 und Windows XP</dt> </dl> |
