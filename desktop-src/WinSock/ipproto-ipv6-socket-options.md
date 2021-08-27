---
description: In den folgenden Tabellen werden IPPROTO \_ IPV6-Socketoptionen beschrieben, die für Sockets gelten, die für die IPv6-Adressfamilie (AF \_ INET6) erstellt wurden. Weitere Informationen zum Abrufen und Festlegen von Socketoptionen finden Sie auf den Referenzseiten der Funktionen getsockopt und setsockopt.
ms.assetid: 65f8f7a4-757b-43a3-9d47-b115754c89d6
title: IPPROTO_IPV6-Socketoptionen
ms.topic: article
ms.date: 10/07/2019
ms.openlocfilehash: 0a6612e9d494325a40cf7b00803dbd13ead68def094383cb3faa50e0160ef932
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097750"
---
# <a name="ipproto_ipv6-socket-options"></a>IPPROTO \_ IPV6-Socketoptionen

In den folgenden Tabellen werden **IPPROTO \_ IPV6-Socketoptionen** beschrieben, die für Sockets gelten, die für die IPv6-Adressfamilie (AF \_ INET6) erstellt wurden. Weitere Informationen zum Abrufen und Festlegen von Socketoptionen finden Sie auf den Referenzseiten der Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Um Protokolle aufzulisten und unterstützte Eigenschaften für jedes installierte Protokoll zu ermitteln, verwenden Sie die Funktion [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)oder [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

Einige Socketoptionen erfordern mehr Erklärung, als diese Tabellen vermitteln können. diese Optionen enthalten Links zu zusätzlichen Informationen.

## <a name="options"></a>Optionen

| Option | get | set | Optval-Typ | BESCHREIBUNG |
|-|-|-|-|-|
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | Ja | Ja | DWORD (boolesch) | Gibt an, ob die [**WSARecvMsg-Funktion (LPFN_WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) optionale Steuerdaten zurückgeben soll, die die ursprüngliche Eingangsschnittstelle enthalten, an der das Paket für Datagrammsockets empfangen wurde. Diese Option wird mit IPv6-Übergangstechnologien (z.B. 6to4-, ISATAP- und Teredo-Tunnel) verwendet, die eine Adresszuweisung und automatisches Host-zu-Host-Tunneling für Unicast-IPv6-Datenverkehr bereitstellen, wenn IPv6-Hosts IP4-Netzwerke durchlaufen müssen, um andere IPv6-Netzwerke zu erreichen. IPv6-Pakete werden als IPv4-Pakete getunnelt gesendet. Mit dieser Option kann die ursprüngliche IPv4-Schnittstelle, an der das Paket empfangen wurde, in der [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) zurückgegeben werden.  |
| IPV6_ADD_IFLIST | | Ja | DWORD (IF_INDEX) | Fügt der IFLIST, die der **option IP_IFLIST** zugeordnet ist, einen Schnittstellenindex hinzu. |
| IPV6 \_ MITGLIEDSCHAFT HINZUFÜGEN \_ | | Ja | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Verbinden Sie den Socket mit der angegebenen Multicastgruppe auf der angegebenen Schnittstelle.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| IPV6_DEL_IFLIST | | Ja | DWORD (IF_INDEX) | Entfernt einen Schnittstellenindex aus der IFLIST, die der **option IP_IFLIST** zugeordnet ist. Einträge können nur von der Anwendung entfernt werden. Beachten Sie daher, dass Einträge möglicherweise veraltet sind, sobald eine Schnittstelle entfernt wird. |
| IPV6 \_ DROP \_ MEMBERSHIP | | Ja | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Belassen Sie die angegebene Multicastgruppe von der angegebenen Schnittstelle.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| IPV6_GET_IFLIST | Ja | | DWORD[] (IF_INDEX[]) | Ruft die aktuelle IFLIST ab, die der **option IP_IFLIST** zugeordnet ist. Gibt einen Fehler zurück, wenn **IP_IFLIST** nicht aktiviert ist. |
| IPV6 \_ HDRINCL | Ja | Ja | DWORD(boolean) | Gibt an, dass die Anwendung den IPv6-Header für alle ausgehenden Daten bereitstellt. Wenn der *optval-Parameter* beim Aufruf von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **1** festgelegt ist, ist die Option aktiviert. Wenn *optval* auf **0** festgelegt ist, ist die Option deaktiviert. Der Standardwert ist „deaktiviert“. Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). Ein TCP/IP-Dienstanbieter, der SOCK RAW unterstützt, \_ sollte auch IPV6 \_ HDRINCL unterstützen. |
| IPV6 \_ HOPLIMIT | Ja | Ja | DWORD (boolesch) | Gibt an, dass Hopinformationen (TTL) in der [**funktion LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) zurückgegeben werden sollen. Wenn *optval* beim Aufruf von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **1** festgelegt ist, ist die Option aktiviert. Wenn auf **0** festgelegt ist, ist die Option deaktiviert.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| IPV6_IFLIST | Ja | Ja | DWORD (boolesch) | Ruft den **IP_IFLIST** Zustand des Sockets ab oder legt diese fest. Wenn diese Option auf TRUE festgelegt ist, ist der Empfang von Datagrammen auf Schnittstellen beschränkt, die sich in der IFLIST befinden. Für andere Schnittstellen empfangene Datagramme werden ignoriert. IFLIST wird leer gestartet. Verwenden Sie **IP_ADD_IFLIST** und **IP_DEL_IFLIST,** um die IFLIST zu bearbeiten. |
| IPV6 \_ JOIN \_ GROUP | | Ja | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Identisch mit IPV6 \_ ADD \_ MEMBERSHIP |
| IPV6 \_ LEAVE \_ GROUP | | Ja | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Identisch mit IPV6 \_ DROP \_ MEMBERSHIP |
| IPV6 \_ MTU | Ja | | DWORD | Ruft die Schätzung des Pfads mtu des Systems ab. Socket muss verbunden sein. |
| IPV6 \_ MTU \_ DISCOVER | Ja | Ja | DWORD (**PMTUD \_ STATE**) | Ruft den MTU-Ermittlungsstatus des Pfads für den Socket ab oder legt den Pfad fest. Der Standardwert ist **IP \_ PMTUDISC \_ NOT \_ SET.** Für Streamsockets führen **IP \_ PMTUDISC \_ NOT \_ SET** und **IP \_ PMTUDISC \_ DO** die Pfad-MTU-Ermittlung durch. **IP-Adresse \_ PMTUDISC \_ DONT** und **IP \_ PMTUDISC \_ PROBE** deaktivieren die PFAD-MTU-Ermittlung. Wenn Datagrammsockets auf **IP \_ PMTUDISC \_ DO** festgelegt sind, führt der Versuch, Pakete zu senden, die größer als die PFAD-MTU sind, zu einem Fehler. Wenn ip **\_ PMTUDISC \_ DONT** festgelegt ist, werden Pakete gemäß der MTU-Schnittstelle fragmentiert. Wenn ip **\_ PMTUDISC \_ PROBE** festgelegt ist, führt der Versuch, Pakete zu senden, die größer als die MTU der Schnittstelle sind, zu einem Fehler.  |
| IPV6 \_ \_ MULTICAST-HOPS | Ja | Ja | DWORD | Ruft den TTL-Wert ab, der IPv6-Multicastdatenverkehr auf dem Socket zugeordnet ist, oder legt den Wert fest. Es ist unzulässig, die Gültigkeitsdauer auf einen Wert größer als 255 festzulegen.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| IPV6 \_ MULTICAST \_ IF | Ja | Ja | DWORD | Ruft die ausgehende Schnittstelle zum Senden von IPv6-Multicastdatenverkehr ab oder legt sie fest. Diese Option ändert nicht die Standardschnittstelle für den Empfang von IPv6-Multicastdatenverkehr. Diese Option ist für mehrfach vernetzten Computer wichtig.  Der Eingabewert zum Festlegen dieser Option ist ein 4-Byte-Schnittstellenindex der gewünschten ausgehenden Schnittstelle in host-Bytereihenfolge. Die [**GetAdaptersAddresses-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) kann verwendet werden, um die Schnittstellenindexinformationen abzurufen. Wenn *optval* beim Aufruf von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **NULL** festgelegt ist, wird die IPv6-Standardschnittstelle verwendet. Wenn *optval* 0 (null) ist, wird die Standardschnittstelle für den Empfang von Multicast zum Senden von Multicastdatenverkehr angegeben.  Beim Abrufen dieser Option gibt *optval* den aktuellen Standardschnittstellenindex zum Senden von Multicast-IPv6-Datenverkehr in Host-Bytereihenfolge zurück. |
| IPV6 \_ \_ MULTICAST-SCHLEIFE | Ja | Ja | DWORD (boolesch) | Gibt an, dass multicast-Daten, die am Socket gesendet werden, an den Empfangspuffer der Sockets wiederholt werden, wenn sie auch in der Multicastzielgruppe verknüpft sind. Wenn *optval* beim Aufruf von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **1** festgelegt ist, ist die Option aktiviert. Wenn auf **0** festgelegt ist, ist die Option deaktiviert.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| [IPV6 \_ PKTINFO](ipv6-pktinfo.md) | Ja | Ja | DWORD (boolesch) | Gibt an, dass Paketinformationen von der [**WSARecvMsg-Funktion (LPFN_WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) zurückgegeben werden sollen. |
| [\_IPV6-SCHUTZEBENE \_](ipv6-protection-level.md) | Ja | Ja | INT | Aktiviert die Einschränkung eines Sockets auf einen angegebenen Bereich, z. B. Adressen mit demselben lokalen Linkpräfix oder lokalen Standortpräfix. Stellt verschiedene Einschränkungsstufen und Standardeinstellungen bereit. Weitere Informationen finden Sie [unter IPV6 \_ PROTECTION \_ LEVEL.](ipv6-protection-level.md) |
| IPV6 \_ RECVIF | Ja | Ja | DWORD (boolesch) | Gibt an, ob der IP-Stapel den Steuerungspuffer mit Details darüber auffüllen soll, welche Schnittstelle ein Paket mit einem Datagrammsocket empfangen hat. Wenn dieser Wert true ist, gibt die [**WSARecvMsg-Funktion (LPFN_WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) optionale Steuerdaten zurück, die die Schnittstelle enthalten, an die das Paket für Datagrammsockets empfangen wurde. Mit dieser Option kann die IPv6-Schnittstelle, an der das Paket empfangen wurde, in der [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) zurückgegeben werden.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| IPV6 \_ RECVTCLASS | Ja | Ja | DWORD (boolesch) | Gibt an, ob der IP-Stapel den Steuerungspuffer mit einer Nachricht auffüllen soll, die das IPv6-Headerfeld der Datenverkehrsklasse in einem empfangenen Datagramm enthält. Wenn dieser Wert true ist, gibt die [**WSARecvMsg-Funktion (LPFN_WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) optionale Steuerdaten zurück, die den IPv6-Headerfeldwert der Traffic Class des empfangenen Datagramms enthalten.  Mit dieser Option kann das IPv6-Headerfeld der Datenverkehrsklasse des empfangenen Datagramms in der [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) zurückgegeben werden. Der zurückgegebene Nachrichtentyp ist IPV6 \_ TCLASS. Alle DSCP- und ECN-Bits des Felds Traffic Class werden zurückgegeben.  Diese Option ist nur für Datagrammsockets gültig (der Sockettyp muss SOCK \_ DGRAM sein).  |
| IPV6 \_ \_ UNICAST-HOPS | Ja | Ja | DWORD | Ruft den aktuellen TTL-Wert ab, der IPv6-Socket für Unicastdatenverkehr zugeordnet ist, oder legt den aktuellen TTL-Wert fest. Es ist unzulässig, die Gültigkeitsdauer auf einen Wert größer als 255 festzulegen. |
| IPV6 \_ UNICAST \_ IF | Ja | Ja | DWORD (IF \_ INDEX) | Ruft die ausgehende Schnittstelle zum Senden von IPv6-Datenverkehr ab oder legt sie fest. Diese Option ändert nicht die Standardschnittstelle für den Empfang von IPv6-Datenverkehr. Diese Option ist für mehrfach vernetzten Computer wichtig.  Der Eingabewert zum Festlegen dieser Option ist ein 4-Byte-Schnittstellenindex der gewünschten ausgehenden Schnittstelle in host-Bytereihenfolge. Die [**GetAdaptersAddresses-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) kann verwendet werden, um die Schnittstellenindexinformationen abzurufen. Wenn *optval* 0 (null) ist, wird die Standardschnittstelle zum Senden von IPv6-Datenverkehr auf nicht angegeben festgelegt.  Beim Abrufen dieser Option gibt *optval* den aktuellen Standardschnittstellenindex zum Senden von IPv6-Datenverkehr in host-Bytereihenfolge zurück. |
| IPV6_USER_MTU | Ja | Ja | DWORD | Ruft eine Obergrenze für die IP-Schicht-MTU (in Bytes) für den angegebenen Socket ab oder legt diese fest. Wenn der Wert höher als die Schätzung des Pfads mtu des Systems ist (den Sie für einen verbundenen Socket abrufen können, indem Sie die **option IPV6_MTU** Socket abfragen), hat die Option keine Auswirkungen. Wenn der Wert niedriger ist, werden ausgehende Pakete, die größer als dieser sind, fragmentiert oder können nicht gesendet werden, abhängig vom Wert **von IPV6_DONTFRAG**. Der Standardwert ist **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Zur Typsicherheit sollten Sie die Funktionen [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) und [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) verwenden, anstatt die Socketoption direkt zu verwenden. |
| IPV6 \_ V6ONLY | Ja | Ja | DWORD (boolesch) | Gibt an, ob ein für die AF \_ INET6-Adressfamilie erstellter Socket auf die IPv6-Kommunikation beschränkt ist. Sockets, die für die AF \_ INET6-Adressfamilie erstellt wurden, können sowohl für die IPv6- als auch für die IPv4-Kommunikation verwendet werden. Einige Anwendungen möchten ihre Verwendung eines Sockets, der für die AF \_ INET6-Adressfamilie erstellt wurde, möglicherweise auf die IPv6-Kommunikation beschränken. Wenn dieser Wert ungleich 0 (standard für Windows) ist, kann ein Socket, der für die AF \_ INET6-Adressfamilie erstellt wurde, nur zum Senden und Empfangen von IPv6-Paketen verwendet werden. Wenn dieser Wert 0 (null) ist, kann ein Socket, der für die AF \_ INET6-Adressfamilie erstellt wurde, zum Senden und Empfangen von Paketen an eine und von einer IPv6-Adresse oder einer IPv4-Adresse verwendet werden. Die Möglichkeit der Interaktion mit einer IPv4-Adresse setzt die Verwendung von IPv4-zugeordneten Adressen voraus. Diese Socketoption wird unter Windows Vista oder höher unterstützt. |

## <a name="windows-support-for-ipproto_ipv6-socket-options"></a>Windows Unterstützung für IPPROTO \_ IPV6-Socketoptionen

| Option | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | x | x | x | | |
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

| Option | Windows Server 2003 | Windows XP |
|-|-|-|
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | | |
| IPV6_ADD_IFLIST | | |
| IPV6 \_ MITGLIEDSCHAFT HINZUFÜGEN \_ | x | x |
| IPV6_DEL_IFLIST | | |
| IPV6 \_ DROP \_ MEMBERSHIP | x | x |
| IPV6_GET_IFLIST | | |
| IPV6 \_ HDRINCL x | x |
| IPV6 \_ HOPLIMIT x | x |
| IPV6_IFLIST | | |
| IPV6 \_ JOIN \_ GROUP | x | x |
| IPV6 \_ LEAVE \_ GROUP | x | x |
| IPV6 \_ \_ MULTICAST-HOPS | x | x |
| IPV6 \_ MULTICAST \_ IF | x | x |
| IPV6 \_ \_ MULTICAST-SCHLEIFE | x | x |
| IPV6 \_ PKTINFO | x | x |
| [\_IPV6-SCHUTZEBENE \_](ipv6-protection-level.md) | x | x |
| IPV6 \_ RECVIF | | |
| IPV6 \_ \_ UNICAST-HOPS | x | x |
| IPV6 \_ UNICAST \_ IF | | |
| IPV6 \_ V6ONLY | | |

## <a name="remarks"></a>Hinweise

Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Headerdateien geändert, und die **IPPROTO \_ IPV6-Ebene** wird in der *Headerdatei Ws2def.h* definiert, die automatisch in der *Winsock2.h-Headerdatei* enthalten ist. Die **IPPROTO \_ IPV6-Socketoptionen** werden in der *Headerdatei Ws2ipdef.h* definiert, die automatisch in der *Headerdatei Ws2tcpip.h* enthalten ist. Die *Headerdateien "Ws2def.h"* und *"Ws2ipdef.h"* sollten nie direkt verwendet werden.

Die \_ IP ORIGINAL \_ ARRIVAL \_ IF-Socketoption wird auf Windows Server 2008 R2 sowie auf Windows 7 unterstützt.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | <dl> <dt>Ws2def.h (einschließlich Winsock2.h);</dt> <dt>Winsock2.h auf Windows Server 2003 und Windows XP</dt> </dl> |
