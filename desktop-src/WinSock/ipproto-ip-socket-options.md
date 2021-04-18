---
description: In den folgenden Tabellen werden ipproto \_ IP-Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4-Adressfamilie (AF \_ inet) erstellt wurden. Weitere Informationen zum Ermitteln und Festlegen von Socketoptionen finden Sie auf den Referenzseiten zu den Funktionen getsockopt und setsockopt.
ms.assetid: 6b06a29e-59cd-4446-bd2f-131dc25bf571
title: IPPROTO_IP-Socketoptionen
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: b4c8daa18e7bd60e61473bdda1c885bbd163f0b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372311"
---
# <a name="ipproto_ip-socket-options"></a>Ipproto \_ IP-Socketoptionen

In den folgenden Tabellen werden **IPPROTO_IP** Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4-Adressfamilie (AF \_ inet) erstellt wurden. Weitere Informationen zum Ermitteln und Festlegen von Socketoptionen finden Sie auf den Referenzseiten zu den Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .

Verwenden Sie die [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)-, [**wscenumprotokolle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)-oder [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) -Funktion, um Protokolle aufzulisten und die unterstützten Eigenschaften für jedes installierte Protokoll zu ermitteln.

Einige Socketoptionen erfordern eine ausführlichere Erläuterung, als diese Tabellen vermitteln können. Diese Optionen enthalten Links zu weiteren Seiten.

## <a name="options"></a>Optionen

| Option | Herunterladen | Set | Optval-Typ | BESCHREIBUNG |
|-|-|-|-|-|
| IP_ADD_IFLIST | | ja | DWORD (IF_INDEX) | Fügt der iflist, die der **IP_IFLIST** Option zugeordnet ist, einen Schnittstellen Index hinzu. |
| IP_ADD_MEMBERSHIP | | ja | [**ip_mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Verknüpfen Sie den Socket mit der angegebenen Multicast Gruppe in der angegebenen Schnittstelle. |
| IP_ADD_SOURCE_MEMBERSHIP | | ja | [**IP- \_ MREQ- \_ Quelle**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Verknüpfen Sie die angegebene Multicast Gruppe für die angegebene Schnittstelle, und akzeptieren Sie Daten, die von der angegebenen Quelladresse stammen. |
| IP- \_ Block \_ Quelle | | ja | [**IP- \_ MREQ- \_ Quelle**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Entfernt die angegebene Quelle als Absender für die angegebene Multicast Gruppe und Schnittstelle. |
| IP_DEL_IFLIST | | ja | DWORD (IF_INDEX) | Entfernt einen Schnittstellen Index aus der iflist-, die der **IP_IFLIST** Option zugeordnet ist. Einträge können nur von der Anwendung entfernt werden. Beachten Sie daher, dass Einträge möglicherweise veraltet sind, sobald eine Schnittstelle entfernt wurde. |
| IP- \_ DontFragment | ja | ja | DWORD (Boolean) | Gibt an, dass Daten unabhängig von der lokalen MTU nicht fragmentiert werden sollen. Nur für Nachrichten orientierte Protokolle gültig. Microsoft TCP/IP-Anbieter berücksichtigen diese Option für UDP und ICMP. |
| IP- \_ Drop- \_ Mitgliedschaft | | ja | [**IP- \_ MREQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Verlässt die angegebene Multicast Gruppe von der angegebenen-Schnittstelle. Dienstanbieter müssen diese Option unterstützen, wenn Multicast unterstützt wird. Die Unterstützung wird in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur angegeben, die von einem [**wsaenumprotokolle**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) -Funktionsbefehl mit folgendem Befehl zurückgegeben wird: XPI- \_ Unterstützung für \_ Multipoint = 1, XP1 \_ Multipoint \_ Control \_ Plane = 0, XP1 \_ Multipoint \_ Data \_ Plane = 0. |
| IP- \_ Drop- \_ Quell \_ Mitgliedschaft | | ja | [**IP- \_ MREQ- \_ Quelle**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Löscht die Mitgliedschaft in der angegebenen Multicast Gruppe, Schnittstelle und Quelladresse. |
| IP_GET_IFLIST | ja | | DWORD [] (IF_INDEX []) | Ruft den aktuellen iflist ab, der der **IP_IFLIST** Option zugeordnet ist. Gibt einen Fehler zurück, wenn **IP_IFLIST** nicht aktiviert ist. |
| IP \_ hdrincl | ja | ja | DWORD (Boolean) | Wenn diese Einstellung auf **true** festgelegt ist, gibt die Anwendung den IP-Header an. Gilt nur für \_ socketrohsockets. Der TCP/IP-Dienstanbieter kann das ID-Feld festlegen, wenn der von der Anwendung bereitgestellte Wert 0 (null) ist.  Die Option "IP \_ hdrincl" wird nur auf den \_ kopierohtyp des Protokolls angewendet. Ein TCP/IP-Dienstanbieter, der Sock RAW unterstützt, \_ sollte auch IP \_ hdrincl unterstützen.  |
| IP_IFLIST | ja | ja | DWORD (Boolean) | Ruft den **IP_IFLIST** Zustand des Sockets ab oder legt ihn fest. Wenn diese Option auf true festgelegt ist, ist der Datagramm-Empfang auf Schnittstellen beschränkt, die sich in iflist befinden. An allen anderen Schnittstellen Empfangene Datagramme werden ignoriert. Iflist beginnt leer. Verwenden Sie **IP_ADD_IFLIST** und **IP_DEL_IFLIST** , um den iflist zu bearbeiten. |
| IP- \_ MTU | ja | | DWORD | Ruft die Schätzung des Systems für den Pfad der MTU ab. Der Socket muss verbunden sein. |
| IP- \_ MTU \_ ermitteln | ja | ja | DWORD (**pmtud- \_ Status**) | Ruft den Pfad der MTU-Ermittlung für den Socket ab oder legt ihn fest. Der Standardwert ist **IP \_ pmtudisk ist \_ nicht \_ festgelegt**. Bei Stream Sockets wird **IP \_ pmtudisc \_ nicht \_ festgelegt** , und **IP \_ pmtudisc \_** führt den Pfad der MTU Discovery aus. **IP \_ Bei der Ermittlung von pmtudisc \_ 't** und **IP \_ pmtudisc \_** wird der Pfad MTU Discovery deaktiviert. Für Datagrammsockets zwingt **IP \_ pmtudisk \_** , dass für alle ausgehenden Pakete das DF-Bit festgelegt wird, und der Versuch, Pakete zu senden, die größer als der Pfad MTU sind, führt zu einem Fehler. **IP \_ Pmtudisc \_** zwingt nicht, dass alle ausgehenden Pakete das DF-Bit nicht festgelegt haben, und die Pakete werden entsprechend der-Schnittstelle der MTU fragmentiert. **IP \_ Der pmtudisc \_** -Test zwingt, dass für alle ausgehenden Pakete das DF-Bit festgelegt ist, und ein Versuch, Pakete zu senden, die größer als die-Schnittstelle ist, führt zu einem Fehler |
| IP- \_ Multicast \_ if | ja | ja | DWORD | Ruft die ausgehende Schnittstelle zum Senden von IPv4-Multicast Verkehr ab oder legt Sie fest Mit dieser Option wird die Standardschnittstelle für den Empfang von IPv4-Multicast Datenverkehr nicht geändert.  Der Eingabe Wert für das Festlegen dieser Option ist eine 4-Byte-IPv4-Adresse in der Netzwerk-Byte Reihenfolge. Dieser DWORD-Parameter kann auch ein Schnittstellen Index in der Netzwerk-Byte Reihenfolge sein. Jede IP-Adresse im 0. x. x. x-Block (erstes Oktett von 0) außer der IPv4-Adresse 0.0.0.0 wird als Schnittstellen Index behandelt. Ein Schnittstellen Index ist eine 24-Bit-Zahl, und der 0.0.0.0/8-IPv4-Adressblock wird nicht verwendet (dieser Bereich ist reserviert). Der Schnittstellen Index kann verwendet werden, um die Standardschnittstelle für Multicast Datenverkehr für IPv4 anzugeben. Wenn *optval* NULL ist, wird die Standardschnittstelle zum Empfangen von Multicast zum Senden von Multicast Datenverkehr angegeben.  Beim Aktivieren dieser Option gibt das *optval* den aktuellen Standardschnittstellen Index zum Senden von Multicast-IPv4-Datenverkehr in der Host-Byte Reihenfolge zurück. |
| IP- \_ Multicast \_ Schleife | ja | ja | DWORD (Boolean) | Steuert, ob von einer Anwendung auf dem lokalen Computer (nicht notwendigerweise durch denselben Socket) gesendete Daten in einer Multicast Sitzung von einem Socket empfangen werden, der der Multicast Zielgruppe in der Loopback Schnittstelle angehört. Der Wert **true** bewirkt, dass von einer Anwendung auf dem lokalen Computer gesendete Multicast Daten an einen Abhör Socket an der Loopback Schnittstelle übermittelt werden. Mit dem Wert " **false** " wird verhindert, dass von einer Anwendung auf dem lokalen Computer gesendete Multicast Daten an einen Abhör Socket an der Loopback Schnittstelle übermittelt werden. Standardmäßig ist das **IP- \_ Multicast- \_ Loopback** aktiviert. |
| IP- \_ Multicast- \_ TTL | ja | ja | DWORD | Legt den TTL-Wert fest, der dem IP-Multicast Datenverkehr auf dem Socket zugeordnet ist |
| IP- \_ Optionen | ja | ja | Char \[\] | Gibt IP-Optionen an, die in ausgehende Pakete eingefügt werden sollen. Wenn Sie neue Optionen festlegen, werden alle zuvor angegebenen Optionen überschrieben. Wenn optval auf NULL festgelegt wird, werden alle zuvor angegebenen Optionen entfernt. Die \_ Unterstützung von IP-Optionen ist nicht erforderlich. um zu überprüfen, ob IP- \_ Optionen unterstützt werden, verwenden Sie [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) , um aktuelle Optionen Wenn **getsockopt** fehlschlägt, wird die IP- \_ Option nicht unterstützt. |
| IP- \_ ursprüngliche \_ Ankunft, \_ Wenn | ja | ja | DWORD (Boolean) | Gibt an, ob die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion optionale Steuerungsdaten zurückgeben soll, die die Ankunfts Schnittstelle enthalten, an der das Paket für Datagramm-Sockets empfangen wurde. Mit dieser Option kann die IPv4-Schnittstelle, an der das Paket empfangen wurde, in der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur zurückgegeben werden.  Diese Option ist nur für Datagramm-und RAW-Sockets gültig (der Sockettyp muss ein Sock- \_ dgram oder ein \_ socketrohdaten sein). |
| [IP- \_ pktinfo](ip-pktinfo.md) | ja | ja | DWORD | Gibt an, dass die Paketinformationen von der **wsarecvmsg** -Funktion zurückgegeben werden sollen. |
| IP- \_ Empfangs \_ Übertragung | ja | ja | DWORD (Boolean) | Ermöglicht oder blockiert Broadcast Empfang. |
| IP- \_ recvif | ja | ja | DWORD (Boolean) | Gibt an, ob der IP-Stapel den Steuerelement Puffer mit Details auffüllen soll, welche Schnittstelle ein Paket mit einem Datagramm-Socket empfangen hat. Wenn dieser Wert true ist, gibt die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion optionale Steuerungsdaten zurück, die die Schnittstelle enthalten, an der das Paket für Datagramm-Sockets empfangen wurde. Mit dieser Option kann die IPv4-Schnittstelle, an der das Paket empfangen wurde, in der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur zurückgegeben werden.  Diese Option ist nur für Datagramm-und RAW-Sockets gültig (der Sockettyp muss ein Sock- \_ dgram oder ein \_ socketrohdaten sein). |
| IP- \_ recvtos | ja | ja | DWORD (Boolean) | Gibt an, ob der IP-Stapel den Steuerelement Puffer mit einer Nachricht auffüllen soll, die den Typ des IPv4-Header Felds (Type of Service, TOS) eines empfangenen Datagramms enthält. Wenn dieser Wert "true" ist, gibt die Funktion " [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) " optionale Steuerungsdaten zurück, die den IPv4-Header Feldwert des empfangenen Datagramms enthalten.  Mit dieser Option kann das IPv4-Header Feld "TOS" des empfangenen Datagramms in der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur zurückgegeben werden. Der zurückgegebene Nachrichtentyp lautet IP-Adressen \_ . Alle DSCP-und ECN-Bits des Felds "TOS" werden zurückgegeben.  Diese Option ist nur für Datagrammsockets gültig (der Sockettyp muss ein Sock- \_ dgram sein).  |
| IP- \_ recvttl | ja | ja | DWORD (Boolean) | Gibt an, dass Hop (TTL)-Informationen in der [**LPFN_WSARECVMSG-Funktion (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) zurückgegeben werden sollen. Wenn *optval* beim Aufrufen von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **1** festgelegt ist, ist die Option aktiviert. Wenn der Wert auf **0** festgelegt ist, ist die Option deaktiviert.  Diese Option ist nur für Datagramm-und RAW-Sockets gültig (der Sockettyp muss ein Sock- \_ dgram oder eine \_ socketrohdaten sein). |
| IP \_ -Adressen | ja | ja | DWORD (Boolean) | Darf nicht verwendet werden. Der Typ der Dienst Einstellungen (TOS) sollte nur mit der Quality of Service-API festgelegt werden. Weitere Informationen finden Sie unter [differenzierte Dienste](/previous-versions/windows/desktop/qos/differentiated-services) im Abschnitt "Quality of Service" des Platform SDK. |
| IP- \_ TTL | ja | ja | DWORD (Boolean) | Ändert den Standardwert, der vom TCP/IP-Dienstanbieter im TTL-Feld des IP-Headers in ausgehenden Datagramme festgelegt wird. Die \_ Unterstützung von IP TTL ist nicht erforderlich. um zu überprüfen, ob IP \_ TTL unterstützt wird, verwenden Sie [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) zum Aufrufen der aktuellen Optionen. Wenn **getsockopt** fehlschlägt, \_ wird IP TTL nicht unterstützt. |
| IP- \_ Block \_ Quelle | | ja | [**IP- \_ MREQ- \_ Quelle**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Fügt die angegebene Quelle als Absender der angegebenen Multicast Gruppe und-Schnittstelle hinzu. |
| IP- \_ Unicast \_ if | ja | ja | DWORD (bei \_ Index) | Ruft die ausgehende Schnittstelle zum Senden von IPv4-Datenverkehr ab oder legt Mit dieser Option wird die Standardschnittstelle für das Empfangen von IPv4-Datenverkehr nicht geändert. Diese Option ist für mehrfach vernetzte Computer wichtig.  Der Eingabe Wert für das Festlegen dieser Option ist eine 4-Byte-IPv4-Adresse in der Netzwerk-Byte Reihenfolge. Dieser DWORD-Parameter muss ein Schnittstellen Index in der Netzwerk-Byte Reihenfolge sein. Jede IP-Adresse im 0. x. x. x-Block (erstes Oktett von 0) außer der IPv4-Adresse 0.0.0.0 wird als Schnittstellen Index behandelt. Ein Schnittstellen Index ist eine 24-Bit-Zahl, und der 0.0.0.0/8-IPv4-Adressblock wird nicht verwendet (dieser Bereich ist reserviert). Der Schnittstellen Index kann verwendet werden, um die Standardschnittstelle für das Senden von Datenverkehr für IPv4 anzugeben. Die [**getadaptersadressen**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) -Funktion kann zum Abrufen der Schnittstellen Indexinformationen verwendet werden. Wenn *optval* NULL ist, wird die Standardschnittstelle für das Senden von Datenverkehr auf nicht angegeben festgelegt.  Beim Aktivieren dieser Option gibt das *optval* den aktuellen Standardschnittstellen Index zum Senden von IPv4-Datenverkehr in der Host-Byte Reihenfolge zurück. |
| IP_USER_MTU | ja | ja | DWORD | Ruft eine obere Grenze auf der IP-Ebenen-MTU (in Bytes) für den angegebenen Socket ab oder legt diese fest. Wenn der Wert höher ist als die Schätzung des Pfads des Pfads, den Sie auf einem verbundenen Socket abrufen können, indem Sie die Option **IP_MTU** Socket Abfragen), hat die Option keine Auswirkungen. Wenn der Wert niedriger ist, werden ausgehende Pakete, die größer als dieser ist, fragmentiert, oder es kann nicht gesendet werden, abhängig vom Wert **IP_DONTFRAGMENT**. Der Standardwert ist **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Für die Typsicherheit sollten Sie die Funktionen [**wsagetipusermtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) und [**wsasetipusermtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) anstelle der direkten Verwendung der Socket-Option verwenden. |
| IP- \_ WFP- \_ Umleitungs \_ Kontext | ja | ja | Wsacmsghdr mit Steuerungsdaten | Ein Datagrammsocket-Hilfstyp (CMSG- \_ Typ), der den Umleitungs Kontext für einen UDP-Socket angibt, der von einem Windows-Filter Plattform-Umleitungs Dienst (WFP) im Benutzermodus verwendet wird |
| IP- \_ WFP- \_ Umleitungs \_ Einträge | ja | ja | Wsacmsghdr mit Steuerungsdaten | Ein Datagrammsocket-hilfsdatentyp (CMSG- \_ Typ), der den Umleitungs Daten Satz für einen UDP-Socket angibt, der von einem Windows-Filter Plattform-Umleitungs Dienst (WFP) im Benutzermodus |

## <a name="windows-support-for-ip_proto-options"></a>Windows-Unterstützung für IP- \_ Proto-Optionen

| Option | Windows 10 | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|-|
| IP_ADD_IFLIST | Ab Windows 10, Version 1803 | | | | | |
| IP \_ - \_ Mitgliedschaft hinzufügen | x | x | x | x | x | x |
| IP \_ - \_ Quell \_ Mitgliedschaft hinzufügen | x | x | x | x | x | x |
| IP- \_ Block \_ Quelle | x | x | x | x | x | x |
| IP_DEL_IFLIST | Ab Windows 10, Version 1803 | | | | | |
| IP- \_ DontFragment | x | x | x | x | x | x |
| IP- \_ Drop- \_ Mitgliedschaft | x | x | x | x | x | x |
| IP- \_ Drop- \_ Quell \_ Mitgliedschaft | x | x | x | x | x | x |
| IP_GET_IFLIST | Ab Windows 10, Version 1803 | | | | | |
| IP \_ hdrincl | x | x | x | x | x | x |
| IP_IFLIST | Ab Windows 10, Version 1803 | | | | | |
| IP- \_ Multicast \_ if | x | x | x | x | x | x |
| IP- \_ Multicast \_ Schleife | x | x | x | x | x | x |
| IP- \_ Multicast- \_ TTL | x | x | x | x | x | x |
| IP- \_ Optionen | x | x | x | x | x | x |
| IP- \_ ursprüngliche \_ Ankunft, \_ Wenn | x | x | x | x | | |
| IP- \_ pktinfo | x | x | x | x | x | x |
| IP- \_ Empfangs \_ Übertragung | x | x | x | x | x | x |
| IP- \_ recvif | Ab Windows 10, Version 1703 | x | x | x | x | x |
| IP- \_ recvttl | x | | | | | |
| IP \_ -Adressen | x | x | x | | | |
| IP- \_ TTL | x | x | x | x | x | x |
| IP- \_ Block \_ Quelle | x | x | x | x | x | x |
| IP- \_ Unicast \_ if | x | x | x | x | x | x |
| IP- \_ WFP- \_ Umleitungs \_ Kontext | x | x | x | | | |
| IP- \_ WFP- \_ Umleitungs \_ Einträge | x | x | x | | | |

<br/>

| Option | Windows Server 2003 | Windows XP |
|-|-|-|
| IP_ADD_IFLIST | | |
| IP \_ - \_ Mitgliedschaft hinzufügen | x | x |
| IP \_ - \_ Quell \_ Mitgliedschaft hinzufügen | x | x |
| IP- \_ Block \_ Quelle | x | x |
| IP_DEL_IFLIST | | |
| IP- \_ DontFragment | x | x |
| IP- \_ Drop- \_ Mitgliedschaft | x | x |
| IP- \_ Drop- \_ Quell \_ Mitgliedschaft | x | x |
| IP_GET_IFLIST | | |
| IP \_ hdrincl | x | x |
| IP_IFLIST | | |
| IP- \_ Multicast \_ if | x | x |
| IP- \_ Multicast \_ Schleife | x | x |
| IP- \_ Multicast- \_ TTL | x | x |
| IP- \_ Optionen | x | x |
| IP- \_ ursprüngliche \_ Ankunft, \_ Wenn | | |
| IP- \_ pktinfo | x | x |
| IP- \_ Empfangs \_ Übertragung | x | x |
| IP- \_ recvif | | |
| IP- \_ recvttl | | |
| IP \_ -Adressen | | |
| IP- \_ TTL | x | x |
| IP- \_ Block \_ Quelle | x | x |
| IP- \_ Unicast \_ if | | |
| IP- \_ WFP- \_ Umleitungs \_ Kontext | | |
| IP- \_ WFP- \_ Umleitungs \_ Einträge | | |

## <a name="remarks"></a>Bemerkungen

Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Header Dateien geändert, und die **ipproto \_ -IP-** Ebene wird in der Header Datei " *Ws2def. h* " definiert, die automatisch in der Header Datei " *Winsock2. h* " enthalten ist. Einige der **ipproto \_ -IP-** Socketoptionen sind in der Header Datei " *Ws2ipdef. h* " definiert, die automatisch in der Header Datei " *Ws2tcpip. h* " enthalten ist. Die verbleibenden **ipproto \_ IP-** Socketoptionen werden in der Header Datei " *Wsipv6ok. h* " definiert, die automatisch in der Header Datei " *Winsock2. h* " enthalten ist. Die Header Dateien *Ws2def. h*, *Ws2ipdef. h* und *Wsipv6ok. h* sollten niemals direkt verwendet werden.

Im Platform SDK, das für Windows Server 2003 und Windows XP veröffentlicht wurde, wird die **ipproto \_ -IP-** Ebene in der Header Datei " *Winsock2. h* " definiert. Einige der **ipproto \_ IP-** Socketoptionen sind in der Header Datei " *Ws2tcpip. h* " definiert. Die verbleibenden **ipproto \_ IP-** Socketoptionen werden in der Header Datei " *Wsipv6ok. h* " definiert, die automatisch in der Header Datei " *Winsock2. h* " enthalten ist. Die Header Datei " *Wsipv6ok. h* " sollte niemals direkt verwendet werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | <dl> <dt>Ws2def. h (Include Winsock2. h); </dt> <dt>Ws2ipdef. h (Include Ws2tcpip. h); </dt> <dt>Wsipv6ok. h (Include Winsock2. h)</dt> </dl> |
