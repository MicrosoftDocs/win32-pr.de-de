---
description: In den folgenden Tabellen werden \_ IPPROTO-IP-Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4-Adressfamilie (AF \_ INET) erstellt wurden. Weitere Informationen zum Abrufen und Festlegen von Socketoptionen finden Sie auf den Referenzseiten der Funktionen getsockopt und setsockopt.
ms.assetid: 6b06a29e-59cd-4446-bd2f-131dc25bf571
title: IPPROTO_IP-Socketoptionen
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 4ce469ab9989bc1cd3ec261e3d3a1b3b819c30443225fee24ae06c92efb6bace
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927710"
---
# <a name="ipproto_ip-socket-options"></a>\_IPPROTO-IP-Socketoptionen

In den folgenden Tabellen werden **IPPROTO_IP** Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4-Adressfamilie (AF \_ INET) erstellt wurden. Weitere Informationen zum Abrufen und Festlegen von Socketoptionen finden Sie auf den Referenzseiten der Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Um Protokolle aufzulisten und unterstützte Eigenschaften für jedes installierte Protokoll zu ermitteln, verwenden Sie die Funktion [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)oder [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

Einige Socketoptionen erfordern mehr Erklärung, als diese Tabellen vermitteln können. diese Optionen enthalten Links zu zusätzlichen Seiten.

## <a name="options"></a>Optionen

| Option | Herunterladen | Set | Optval-Typ | Beschreibung |
|-|-|-|-|-|
| IP_ADD_IFLIST | | Ja | DWORD (IF_INDEX) | Fügt der IFLIST, die der **option IP_IFLIST** zugeordnet ist, einen Schnittstellenindex hinzu. |
| IP_ADD_MEMBERSHIP | | Ja | [**ip_mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Verbinden Sie den Socket mit der angegebenen Multicastgruppe auf der angegebenen Schnittstelle. |
| IP_ADD_SOURCE_MEMBERSHIP | | Ja | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Join the supplied multicast group on the given interface and accept data sourced from the supplied source address. |
| \_ \_ IP-BLOCKQUELLE | | Ja | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Entfernt die angegebene Quelle als Absender für die angegebene Multicastgruppe und Schnittstelle. |
| IP_DEL_IFLIST | | Ja | DWORD (IF_INDEX) | Entfernt einen Schnittstellenindex aus der IFLIST, die der **option IP_IFLIST** zugeordnet ist. Einträge können nur von der Anwendung entfernt werden. Beachten Sie daher, dass Einträge möglicherweise veraltet sind, sobald eine Schnittstelle entfernt wird. |
| \_IP-DONTFRAGMENT | Ja | Ja | DWORD (boolesch) | Gibt an, dass Daten unabhängig von der lokalen MTU nicht fragmentiert werden sollen. Nur für nachrichtenorientierte Protokolle gültig. Microsoft-TCP/IP-Anbieter berücksichtigen diese Option für UDP und ICMP. |
| IP \_ DROP \_ MEMBERSHIP | | Ja | [**ip \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Verlässt die angegebene Multicastgruppe von der angegebenen Schnittstelle. Dienstanbieter müssen diese Option unterstützen, wenn Multicast unterstützt wird. Die Unterstützung wird in der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) angegeben, die von einem [**WSAEnumProtocols-Funktionsaufruf**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) mit folgendem Inhalt zurückgegeben wird: XPI \_ SUPPORT \_ MULTIPOINT=1, XP1 \_ MULTIPOINT \_ CONTROL \_ PLANE=0, XP1 \_ MULTIPOINT DATA \_ \_ PLANE=0. |
| IP \_ DROP \_ SOURCE \_ MEMBERSHIP | | Ja | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Löscht die Mitgliedschaft in der angegebenen Multicastgruppe, Schnittstelle und Quelladresse. |
| IP_GET_IFLIST | Ja | | DWORD[] (IF_INDEX[]) | Ruft die aktuelle IFLIST ab, die der **option IP_IFLIST** zugeordnet ist. Gibt einen Fehler zurück, wenn **IP_IFLIST** nicht aktiviert ist. |
| IP \_ HDRINCL | Ja | Ja | DWORD (boolesch) | Wenn auf **TRUE** festgelegt ist, gibt an, dass die Anwendung den IP-Header bereitstellt. Gilt nur für SOCK \_ RAW-Sockets. Der TCP/IP-Dienstanbieter kann das FELD ID festlegen, wenn der von der Anwendung bereitgestellte Wert 0 (null) ist.  Die \_ IP-HDRINCL-Option wird nur auf den SOCK \_ RAW-Protokolltyp angewendet. Ein TCP/IP-Dienstanbieter, der SOCK RAW unterstützt, \_ sollte auch \_ IP-HDRINCL unterstützen.  |
| IP_IFLIST | Ja | Ja | DWORD (boolesch) | Ruft den **IP_IFLIST** Zustand des Sockets ab oder legt diese fest. Wenn diese Option auf TRUE festgelegt ist, ist der Empfang von Datagrammen auf Schnittstellen beschränkt, die sich in der IFLIST befinden. Für andere Schnittstellen empfangene Datagramme werden ignoriert. IFLIST wird leer gestartet. Verwenden Sie **IP_ADD_IFLIST** und **IP_DEL_IFLIST,** um die IFLIST zu bearbeiten. |
| \_IP-MTU | Ja | | DWORD | Ruft die Schätzung des Pfads mtu des Systems ab. Socket muss verbunden sein. |
| \_IP-MTU-ERMITTLUNG \_ | Ja | Ja | DWORD (**PMTUD \_ STATE**) | Ruft den MTU-Ermittlungsstatus des Pfads für den Socket ab oder legt den Pfad fest. Der Standardwert ist **IP \_ PMTUDISC \_ NOT \_ SET.** Für Streamsockets führen **IP \_ PMTUDISC \_ NOT \_ SET** und **IP \_ PMTUDISC \_ DO** die Pfad-MTU-Ermittlung durch. **IP-Adresse \_ PMTUDISC \_ DONT** und **IP \_ PMTUDISC \_ PROBE** deaktivieren die PFAD-MTU-Ermittlung. Für Datagrammsockets **zwingt IP \_ PMTUDISC \_ DO** alle ausgehenden Pakete, das DF-Bit festzulegen, und ein Versuch, Pakete zu senden, die größer als die PFAD-MTU sind, führt zu einem Fehler. **IP-Adresse \_ PMTUDISC \_ DONT zwingt** alle ausgehenden Pakete, das DF-Bit nicht festzulegen, und Pakete werden gemäß der MTU der Schnittstelle fragmentiert. **IP-Adresse \_ PMTUDISC \_ PROBE zwingt** alle ausgehenden Pakete, das DF-Bit festzulegen, und ein Versuch, Pakete zu senden, die größer als die MTU der Schnittstelle sind, führt zu einem Fehler. |
| IP \_ MULTICAST \_ IF | Ja | Ja | DWORD | Ruft die ausgehende Schnittstelle zum Senden von IPv4-Multicastdatenverkehr ab oder legt sie fest. Diese Option ändert nicht die Standardschnittstelle für den Empfang von IPv4-Multicastdatenverkehr.  Der Eingabewert zum Festlegen dieser Option ist eine 4-Byte-IPv4-Adresse in Netzwerk-Bytereihenfolge. Dieser DWORD-Parameter kann auch ein Schnittstellenindex in Netzwerk-Bytereihenfolge sein. Jede IP-Adresse im Block 0.x.x.x (erstes Oktett von 0) mit Ausnahme der IPv4-Adresse 0.0.0.0 wird als Schnittstellenindex behandelt. Ein Schnittstellenindex ist eine 24-Bit-Zahl, und der IPv4-Adressblock 0.0.0.0/8 wird nicht verwendet (dieser Bereich ist reserviert). Der Schnittstellenindex kann verwendet werden, um die Standardschnittstelle für Multicastdatenverkehr für IPv4 anzugeben. Wenn *optval* 0 (null) ist, wird die Standardschnittstelle für den Empfang von Multicast zum Senden von Multicastdatenverkehr angegeben.  Beim Abrufen dieser Option gibt *optval* den aktuellen Standardschnittstellenindex zum Senden von Multicast-IPv4-Datenverkehr in host-Bytereihenfolge zurück. |
| IP \_ \_ MULTICAST-SCHLEIFE | Ja | Ja | DWORD (boolesch) | Steuert, ob daten, die von einer Anwendung auf dem lokalen Computer (nicht unbedingt vom gleichen Socket) in einer Multicastsitzung gesendet werden, von einem Socket empfangen werden, der mit der Multicastzielgruppe auf der Loopbackschnittstelle verknüpft ist. Der Wert **TRUE** bewirkt, dass Multicastdaten, die von einer Anwendung auf dem lokalen Computer gesendet werden, an einen Lauschsocket auf der Loopbackschnittstelle übermittelt werden. Der Wert **FALSE** verhindert, dass Multicastdaten, die von einer Anwendung auf dem lokalen Computer gesendet werden, an einen Lauschsocket auf der Loopbackschnittstelle übermittelt werden. Standardmäßig ist **IP \_ MULTICAST \_ LOOPBACK** aktiviert. |
| IP \_ MULTICAST \_ TTL | Ja | Ja | DWORD | Legt den TTL-Wert fest, der dem IP-Multicastdatenverkehr auf dem Socket zugeordnet ist,/ruft den Wert ab. |
| \_IP-OPTIONEN | Ja | Ja | Char \[\] | Gibt IP-Optionen an, die in ausgehende Pakete eingefügt werden sollen. Durch das Festlegen neuer Optionen werden alle zuvor angegebenen Optionen überschrieben. Wenn Optval auf 0 festgelegt wird, werden alle zuvor angegebenen Optionen entfernt. Unterstützung \_ für IP-OPTIONEN ist nicht erforderlich. Um zu überprüfen, ob IP-Optionen unterstützt \_ werden, verwenden Sie [**getsockopt,**](/windows/desktop/api/winsock/nf-winsock-getsockopt) um aktuelle Optionen abzurufen. Wenn **getsockopt** fehlschlägt, \_ werden IP-Optionen nicht unterstützt. |
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | Ja | Ja | DWORD (boolesch) | Gibt an, ob die [**LPFN_WSARECVMSG -Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) optionale Steuerdaten zurückgeben soll, die die Eingangsschnittstelle enthalten, an der das Paket für Datagrammsockets empfangen wurde. Mit dieser Option kann die IPv4-Schnittstelle, an der das Paket empfangen wurde, in der [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) zurückgegeben werden.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| [IP \_ PKTINFO](ip-pktinfo.md) | Ja | Ja | DWORD | Gibt an, dass Paketinformationen von der **WSARecvMsg-Funktion** zurückgegeben werden sollen. |
| \_IP-EMPFANGSÜBERTRAGUNG \_ | Ja | Ja | DWORD (boolesch) | Ermöglicht oder blockiert den Empfang von Übertragungen. |
| IP \_ RECVIF | Ja | Ja | DWORD (boolesch) | Gibt an, ob der IP-Stapel den Steuerungspuffer mit Details darüber auffüllen soll, welche Schnittstelle ein Paket mit einem Datagrammsocket empfangen hat. Wenn dieser Wert true ist, gibt die [**WSARecvMsg-Funktion (LPFN_WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) optionale Steuerdaten zurück, die die Schnittstelle enthalten, an die das Paket für Datagrammsockets empfangen wurde. Mit dieser Option kann die IPv4-Schnittstelle, an der das Paket empfangen wurde, in der [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) zurückgegeben werden.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| IP \_ RECVTOS | Ja | Ja | DWORD (boolesch) | Gibt an, ob der IP-Stapel den Steuerungspuffer mit einer Nachricht auffüllen soll, die das IPv4-Headerfeld "Typ des Diensts" (TOS) für ein empfangenes Datagramm enthält. Wenn dieser Wert true ist, gibt die [**LPFN_WSARECVMSG -Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) optionale Steuerdaten zurück, die den TOS IPv4-Headerfeldwert des empfangenen Datagramms enthalten.  Mit dieser Option kann das TOS IPv4-Headerfeld des empfangenen Datagramms in der [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) zurückgegeben werden. Der zurückgegebene Nachrichtentyp lautet \_ IP-TOS. Alle DSCP- und ECN-Bits des TOS-Felds werden zurückgegeben.  Diese Option ist nur für Datagrammsockets gültig (der Sockettyp muss SOCK \_ DGRAM sein).  |
| IP \_ RECVTTL | Ja | Ja | DWORD (boolesch) | Gibt an, dass Hopinformationen (TTL) in der [**funktion LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) zurückgegeben werden sollen. Wenn *optval* beim Aufruf von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **1** festgelegt ist, ist die Option aktiviert. Wenn auf **0** festgelegt ist, ist die Option deaktiviert.  Diese Option ist nur für Datagramm- und Rohsockets gültig (der Sockettyp muss SOCK \_ DGRAM oder SOCK \_ RAW sein). |
| \_IP-TOS | Ja | Ja | DWORD (boolesch) | Darf nicht verwendet werden. Der Typ der Diensteinstellungen (TOS) sollte nur mithilfe der Quality of Service-API festgelegt werden. Weitere Informationen finden Sie unter [Differentiated Services](/previous-versions/windows/desktop/qos/differentiated-services) im Abschnitt Quality of Service des Plattform-SDK. |
| \_IP-Gültigkeitsdauer | Ja | Ja | DWORD (boolesch) | Ändert den Standardwert, der vom TCP/IP-Dienstanbieter im TTL-Feld des IP-Headers in ausgehenden Datagrammen festgelegt wird. \_Ip-TTL-Unterstützung ist nicht erforderlich. Um zu überprüfen, ob die \_ IP-Gültigkeitsdauer unterstützt wird, verwenden Sie [**getsockopt,**](/windows/desktop/api/winsock/nf-winsock-getsockopt) um aktuelle Optionen abzurufen. Wenn **getsockopt** fehlschlägt, wird die \_ IP-Gültigkeitsdauer nicht unterstützt. |
| IP \_ UNBLOCK \_ SOURCE | | Ja | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Fügt der angegebenen Multicastgruppe und -schnittstelle die angegebene Quelle als Absender hinzu. |
| IP \_ UNICAST \_ IF | Ja | Ja | DWORD (IF \_ INDEX) | Ruft die ausgehende Schnittstelle zum Senden von IPv4-Datenverkehr ab oder legt sie fest. Diese Option ändert nicht die Standardschnittstelle für den Empfang von IPv4-Datenverkehr. Diese Option ist für mehrfach vernetzten Computer wichtig.  Der Eingabewert zum Festlegen dieser Option ist eine 4-Byte-IPv4-Adresse in Netzwerk-Bytereihenfolge. Dieser DWORD-Parameter muss ein Schnittstellenindex in Netzwerk-Bytereihenfolge sein. Jede IP-Adresse im Block 0.x.x.x (erstes Oktett von 0) mit Ausnahme der IPv4-Adresse 0.0.0.0 wird als Schnittstellenindex behandelt. Ein Schnittstellenindex ist eine 24-Bit-Zahl, und der IPv4-Adressblock 0.0.0.0/8 wird nicht verwendet (dieser Bereich ist reserviert). Der Schnittstellenindex kann verwendet werden, um die Standardschnittstelle zum Senden von Datenverkehr für IPv4 anzugeben. Die [**GetAdaptersAddresses-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) kann verwendet werden, um die Schnittstellenindexinformationen abzurufen. Wenn *optval* 0 (null) ist, wird die Standardschnittstelle zum Senden von Datenverkehr auf nicht angegeben festgelegt.  Beim Abrufen dieser Option gibt *optval* den aktuellen Standardschnittstellenindex zum Senden von IPv4-Datenverkehr in Host-Byte-Reihenfolge zurück. |
| IP_USER_MTU | Ja | Ja | DWORD | Ruft eine Obergrenze für die IP-Schicht-MTU (in Bytes) für den angegebenen Socket ab oder legt diese fest. Wenn der Wert höher als die Schätzung des Pfads der MTU ist (die Sie auf einem verbundenen Socket abrufen können, indem Sie die Option **IP_MTU** Socket abfragen), hat die Option keine Auswirkungen. Wenn der Wert niedriger ist, werden ausgehende Pakete, die größer als dieser sind, fragmentiert oder können je nach Wert von nicht **gesendet IP_DONTFRAGMENT.** Der Standardwert ist **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Zur Typsicherheit sollten Sie die [**Funktionen WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) und [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) verwenden, anstatt die Socketoption direkt zu verwenden. |
| \_ \_ IP-WFP-UMLEITUNGSKONTEXT \_ | Ja | Ja | WSACMSGHDR mit Steuerungsdaten | Ein Datagrammsocket-Hilfsdatentyp (cmsg-Typ), um den Umleitungskontext für einen UDP-Socket anzugeben, der von einem Benutzermodus \_ Windows Filtering Platform (WFP)-Umleitungsdienst verwendet wird. |
| \_ \_ IP-WFP-UMLEITUNGSDATENSÄTZE \_ | Ja | Ja | WSACMSGHDR mit Steuerungsdaten | Ein Datagrammsocket-Hilfsdatentyp (cmsg-Typ), um den Umleitungsdatensatz für einen UDP-Socket anzugeben, der von einem Benutzermodus \_ Windows Filtering Platform (WFP)-Umleitungsdienst verwendet wird. |

## <a name="windows-support-for-ip_proto-options"></a>Windows für IP \_ PROTO-Optionen

| Option | Windows 10 | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|-|
| IP_ADD_IFLIST | Ab Windows 10 Version 1803 | | | | | |
| \_IP-MITGLIEDSCHAFT \_ HINZUFÜGEN | x | x | x | x | x | x |
| \_IP-ADRESSE: \_ \_ QUELLMITGLIEDSCHAFT HINZUFÜGEN | x | x | x | x | x | x |
| \_ \_ IP-BLOCKQUELLE | x | x | x | x | x | x |
| IP_DEL_IFLIST | Ab Windows 10 Version 1803 | | | | | |
| IP \_ DONTFRAGMENT | x | x | x | x | x | x |
| IP \_ DROP \_ MEMBERSHIP | x | x | x | x | x | x |
| IP \_ DROP \_ SOURCE \_ MEMBERSHIP | x | x | x | x | x | x |
| IP_GET_IFLIST | Ab Windows 10 Version 1803 | | | | | |
| IP \_ HDRINCL | x | x | x | x | x | x |
| IP_IFLIST | Ab Windows 10 Version 1803 | | | | | |
| IP \_ MULTICAST \_ IF | x | x | x | x | x | x |
| IP \_ \_ MULTICAST-SCHLEIFE | x | x | x | x | x | x |
| \_ \_ IP-MULTICAST-TTL | x | x | x | x | x | x |
| \_IP-OPTIONEN | x | x | x | x | x | x |
| URSPRÜNGLICHE \_ \_ IP-ANKUNFT, \_ WENN | x | x | x | x | | |
| \_IP-PKTINFO | x | x | x | x | x | x |
| \_ \_ IP-EMPFANGSÜBERTRAGUNG | x | x | x | x | x | x |
| IP \_ RECVIF | Ab Windows 10 Version 1703 | x | x | x | x | x |
| IP \_ RECVTTL | x | | | | | |
| \_IP-TOS | x | x | x | | | |
| \_IP-Tl | x | x | x | x | x | x |
| \_ \_ IP-ENTSPERRUNGSQUELLE | x | x | x | x | x | x |
| IP \_ UNICAST \_ IF | x | x | x | x | x | x |
| \_ \_ IP-WFP-UMLEITUNGSKONTEXT \_ | x | x | x | | | |
| \_ \_ IP-WFP-UMLEITUNGSDATENSÄTZE \_ | x | x | x | | | |

<br/>

| Option | Windows Server 2003 | Windows XP |
|-|-|-|
| IP_ADD_IFLIST | | |
| \_IP-MITGLIEDSCHAFT \_ HINZUFÜGEN | x | x |
| \_IP-ADRESSE: \_ \_ QUELLMITGLIEDSCHAFT HINZUFÜGEN | x | x |
| \_ \_ IP-BLOCKQUELLE | x | x |
| IP_DEL_IFLIST | | |
| IP \_ DONTFRAGMENT | x | x |
| IP \_ DROP \_ MEMBERSHIP | x | x |
| IP \_ DROP \_ SOURCE \_ MEMBERSHIP | x | x |
| IP_GET_IFLIST | | |
| IP \_ HDRINCL | x | x |
| IP_IFLIST | | |
| IP \_ MULTICAST \_ IF | x | x |
| IP \_ \_ MULTICAST-SCHLEIFE | x | x |
| \_ \_ IP-MULTICAST-TTL | x | x |
| \_IP-OPTIONEN | x | x |
| URSPRÜNGLICHE \_ \_ IP-ANKUNFT, \_ WENN | | |
| \_IP-PKTINFO | x | x |
| \_ \_ IP-EMPFANGSÜBERTRAGUNG | x | x |
| IP \_ RECVIF | | |
| IP \_ RECVTTL | | |
| \_IP-TOS | | |
| \_IP-Tl | x | x |
| \_ \_ IP-ENTSPERRUNGSQUELLE | x | x |
| IP \_ UNICAST \_ IF | | |
| \_ \_ IP-WFP-UMLEITUNGSKONTEXT \_ | | |
| \_ \_ IP-WFP-UMLEITUNGSDATENSÄTZE \_ | | |

## <a name="remarks"></a>Hinweise

Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Headerdateien geändert, und die **\_ IPPROTO-IP-Ebene** wird in der *Headerdatei Ws2def.h* definiert, die automatisch in der *Winsock2.h-Headerdatei* enthalten ist. Einige der **\_ IPPROTO-IP-Socketoptionen** werden in der *Headerdatei Ws2ipdef.h* definiert, die automatisch in der *Headerdatei Ws2tcpip.h* enthalten ist. Die **verbleibenden \_ IPPROTO-IP-Socketoptionen** werden in der *Headerdatei Wsipv6ok.h* definiert, die automatisch in der *Winsock2.h-Headerdatei* enthalten ist. Die *Headerdateien Ws2def.h,* *Ws2ipdef.h* und *Wsipv6ok.h* sollten nie direkt verwendet werden.

Im Plattform-SDK, das für Windows Server 2003 und Windows XP veröffentlicht wurde, wird die **\_ IPPROTO-IP-Ebene** in der *Headerdatei Winsock2.h* definiert. Einige der **\_ IPPROTO-IP-Socketoptionen** sind in der *Headerdatei Ws2tcpip.h* definiert. Die **verbleibenden \_ IPPROTO-IP-Socketoptionen** werden in der *Headerdatei Wsipv6ok.h* definiert, die automatisch in der *Winsock2.h-Headerdatei* enthalten ist. Die *Wsipv6ok.h-Headerdatei* sollte nie direkt verwendet werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | <dl> <dt>Ws2def.h (einschließlich Winsock2.h); </dt> <dt>Ws2ipdef.h (einschließlich Ws2tcpip.h); </dt> <dt>Wsipv6ok.h (einschließlich Winsock2.h)</dt> </dl> |
