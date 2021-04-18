---
description: In den folgenden Tabellen werden ipproto \_ IPv6-Socketoptionen beschrieben, die für Sockets gelten, die für die IPv6-Adressfamilie (AF \_ inet6) erstellt wurden. Weitere Informationen zum Ermitteln und Festlegen von Socketoptionen finden Sie auf den Referenzseiten zu den Funktionen getsockopt und setsockopt.
ms.assetid: 65f8f7a4-757b-43a3-9d47-b115754c89d6
title: IPPROTO_IPV6-Socketoptionen
ms.topic: article
ms.date: 10/07/2019
ms.openlocfilehash: 1ceaf08c2a59a24b9ff694ac9ff42b28fbf18480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372340"
---
# <a name="ipproto_ipv6-socket-options"></a>Ipproto \_ IPv6-Socketoptionen

In den folgenden Tabellen werden **ipproto \_ IPv6** -Socketoptionen beschrieben, die für Sockets gelten, die für die IPv6-Adressfamilie (AF \_ inet6) erstellt wurden. Weitere Informationen zum Ermitteln und Festlegen von Socketoptionen finden Sie auf den Referenzseiten zu den Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .

Verwenden Sie die [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)-, [**wscenumprotokolle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)-oder [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) -Funktion, um Protokolle aufzulisten und die unterstützten Eigenschaften für jedes installierte Protokoll zu ermitteln.

Einige Socketoptionen erfordern eine ausführlichere Erläuterung, als diese Tabellen vermitteln können. Diese Optionen enthalten Links zu weiteren Informationen.

## <a name="options"></a>Optionen

| Option | get | set | Optval-Typ | BESCHREIBUNG |
|-|-|-|-|-|
| IP- \_ ursprüngliche \_ Ankunft, \_ Wenn | ja | ja | DWORD (Boolean) | Gibt an, ob die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion optionale Steuerungsdaten zurückgeben soll, die die ursprüngliche Ankunfts Schnittstelle enthalten, an der das Paket für Datagramm-Sockets empfangen wurde. Diese Option wird mit IPv6-Übergangs Technologien (z. b. IPv6-zu-IPv4-, ISATAP-und Teredo-Tunnel) verwendet, die Adresszuweisung und automatisches Host-zu-Host-Tunnelung für IPv6-Unicastverkehr bereitstellen, wenn IPv6-Hosts IP4-Netzwerke durchlaufen müssen, um andere IPv6-Netzwerke IPv6-Pakete werden als IPv4-Pakete getunnelt gesendet. Mit dieser Option kann die ursprüngliche IPv4-Schnittstelle, an der das Paket empfangen wurde, in der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur zurückgegeben werden.  |
| IPV6_ADD_IFLIST | | ja | DWORD (IF_INDEX) | Fügt der iflist, die der **IP_IFLIST** Option zugeordnet ist, einen Schnittstellen Index hinzu. |
| IPv6 \_ - \_ Mitgliedschaft hinzufügen | | ja | [**IPv6- \_ MREQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Verknüpfen Sie den Socket mit der angegebenen Multicast Gruppe in der angegebenen Schnittstelle.  Diese Option ist nur für Datagramm-und RAW-Sockets gültig (der Sockettyp muss ein Sock- \_ dgram oder ein \_ socketrohdaten sein). |
| IPV6_DEL_IFLIST | | ja | DWORD (IF_INDEX) | Entfernt einen Schnittstellen Index aus der iflist-, die der **IP_IFLIST** Option zugeordnet ist. Einträge können nur von der Anwendung entfernt werden. Beachten Sie daher, dass Einträge möglicherweise veraltet sind, sobald eine Schnittstelle entfernt wurde. |
| IPv6- \_ Drop- \_ Mitgliedschaft | | ja | [**IPv6- \_ MREQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Belassen Sie die angegebene Multicast Gruppe von der angegebenen Schnittstelle.  Diese Option ist nur für Datagramm-und RAW-Sockets gültig (der Sockettyp muss ein Sock- \_ dgram oder ein \_ socketrohdaten sein). |
| IPV6_GET_IFLIST | ja | | DWORD [] (IF_INDEX []) | Ruft den aktuellen iflist ab, der der **IP_IFLIST** Option zugeordnet ist. Gibt einen Fehler zurück, wenn **IP_IFLIST** nicht aktiviert ist. |
| IPv6- \_ hdrincl | ja | ja | DWORD (Boolean) | Gibt an, dass die Anwendung den IPv6-Header für alle ausgehenden Daten bereitstellt. Wenn der *optval* -Parameter beim Aufrufen von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **1** festgelegt ist, ist die Option aktiviert. Wenn *optval* auf **0** festgelegt ist, ist die Option deaktiviert. Der Standardwert ist „deaktiviert“. Diese Option ist nur für Datagramm-und RAW-Sockets gültig (der Sockettyp muss ein Sock- \_ dgram oder eine \_ socketrohdaten sein). Ein TCP/IP-Dienstanbieter, der Sock RAW unterstützt, \_ sollte auch IPv6 \_ hdrincl unterstützen. |
| IPv6- \_ hoplimit | ja | ja | DWORD (Boolean) | Gibt an, dass Hop (TTL)-Informationen in der [**LPFN_WSARECVMSG-Funktion (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) zurückgegeben werden sollen. Wenn *optval* beim Aufrufen von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **1** festgelegt ist, ist die Option aktiviert. Wenn der Wert auf **0** festgelegt ist, ist die Option deaktiviert.  Diese Option ist nur für Datagramm-und RAW-Sockets gültig (der Sockettyp muss ein Sock- \_ dgram oder eine \_ socketrohdaten sein). |
| IPV6_IFLIST | ja | ja | DWORD (Boolean) | Ruft den **IP_IFLIST** Zustand des Sockets ab oder legt ihn fest. Wenn diese Option auf true festgelegt ist, ist der Datagramm-Empfang auf Schnittstellen beschränkt, die sich in iflist befinden. An allen anderen Schnittstellen Empfangene Datagramme werden ignoriert. Iflist beginnt leer. Verwenden Sie **IP_ADD_IFLIST** und **IP_DEL_IFLIST** , um den iflist zu bearbeiten. |
| IPv6 \_ - \_ joingruppe | | ja | [**IPv6- \_ MREQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Identisch mit IPv6 \_ - \_ Mitgliedschaft hinzufügen |
| IPv6 \_ - \_ Gruppe verlassen | | ja | [**IPv6- \_ MREQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Identisch mit IPv6- \_ Drop- \_ Mitgliedschaft |
| IPv6- \_ MTU | ja | | DWORD | Ruft die Schätzung des Systems für den Pfad der MTU ab. Der Socket muss verbunden sein. |
| Ermitteln der IPv6- \_ MTU \_ | ja | ja | DWORD (**pmtud- \_ Status**) | Ruft den Pfad der MTU-Ermittlung für den Socket ab oder legt ihn fest. Der Standardwert ist **IP \_ pmtudisk ist \_ nicht \_ festgelegt**. Bei Stream Sockets wird **IP \_ pmtudisc \_ nicht \_ festgelegt** , und **IP \_ pmtudisc \_** führt den Pfad der MTU Discovery aus. **IP \_ Bei der Ermittlung von pmtudisc \_ 't** und **IP \_ pmtudisc \_** wird der Pfad MTU Discovery deaktiviert. Bei Datagramm-Sockets, die auf **IP \_ pmtudisc \_** festgelegt sind, führt der Versuch, Pakete zu senden, die größer als der Pfad MTU sind, zu einem Fehler. Wenn die Einstellung auf **IP \_ pmtudisc \_** nicht festgelegt ist, werden die Pakete gemäß der MTU-Oberfläche fragmentiert. Wenn der Wert auf **IP \_ pmtudisc \_ Probe** festgelegt ist, führt die Übermittlung von Paketen, die größer als die der Schnittstelle sind, zu einem Fehler.  |
| IPv6- \_ Multicast \_ Hops | ja | ja | DWORD | Ruft den TTL-Wert ab, der dem IPv6-Multicast Verkehr im Socket zugeordnet ist, oder legt ihn fest Es ist unzulässig, die Gültigkeitsdauer auf einen Wert größer als 255 festzulegen.  Diese Option ist nur für Datagramm-und RAW-Sockets gültig (der Sockettyp muss ein Sock- \_ dgram oder eine \_ socketrohdaten sein). |
| IPv6- \_ Multicast, \_ Wenn | ja | ja | DWORD | Ruft die ausgehende Schnittstelle zum Senden von IPv6-Multicast Verkehr ab oder legt Sie fest Mit dieser Option wird die Standardschnittstelle für den Empfang von IPv6-Multicast Datenverkehr nicht geändert. Diese Option ist für mehrfach vernetzte Computer wichtig.  Der Eingabe Wert für das Festlegen dieser Option ist ein 4-Byte-Schnittstellen Index der gewünschten ausgehenden Schnittstelle in der Host-Byte Reihenfolge. Die [**getadaptersadressen**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) -Funktion kann zum Abrufen der Schnittstellen Indexinformationen verwendet werden. Wenn *optval* beim Aufrufen von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **null** festgelegt ist, wird die standardmäßige IPv6-Schnittstelle verwendet. Wenn *optval* NULL ist, wird die Standardschnittstelle zum Empfangen von Multicast zum Senden von Multicast Datenverkehr angegeben.  Beim Aktivieren dieser Option gibt das *optval* den aktuellen Standardschnittstellen Index zum Senden von Multicast-IPv6-Datenverkehr in der Host-Byte Reihenfolge zurück. |
| IPv6- \_ Multicast \_ Schleife | ja | ja | DWORD (Boolean) | Gibt an, dass Multicast Daten, die auf dem Socket gesendet werden, an den Sockets-Empfangs Puffer gesendet werden, wenn dieser auch in der Ziel-Multicast Gruppe verknüpft ist. Wenn *optval* beim Aufrufen von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)auf **1** festgelegt ist, ist die Option aktiviert. Wenn der Wert auf **0** festgelegt ist, ist die Option deaktiviert.  Diese Option ist nur für Datagramm-und RAW-Sockets gültig (der Sockettyp muss ein Sock- \_ dgram oder eine \_ socketrohdaten sein). |
| [IPv6- \_ pktinfo](ipv6-pktinfo.md) | ja | ja | DWORD (Boolean) | Gibt an, dass die Paketinformationen von der [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion zurückgegeben werden sollen. |
| [IPv6- \_ Schutz \_ Ebene](ipv6-protection-level.md) | ja | ja | INT | Aktiviert die Einschränkung eines Sockets auf einen angegebenen Bereich, z. b. Adressen mit demselben Link lokalen oder Standort lokalen Präfix. Bietet verschiedene Einschränkungs Stufen und Standardeinstellungen. Weitere Informationen finden Sie unter [IPv6- \_ Schutz \_ Ebene](ipv6-protection-level.md) . |
| IPv6- \_ recvif | ja | ja | DWORD (Boolean) | Gibt an, ob der IP-Stapel den Steuerelement Puffer mit Details auffüllen soll, welche Schnittstelle ein Paket mit einem Datagramm-Socket empfangen hat. Wenn dieser Wert true ist, gibt die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion optionale Steuerungsdaten zurück, die die Schnittstelle enthalten, an der das Paket für Datagramm-Sockets empfangen wurde. Mit dieser Option kann die IPv6-Schnittstelle, an der das Paket empfangen wurde, in der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur zurückgegeben werden.  Diese Option ist nur für Datagramm-und RAW-Sockets gültig (der Sockettyp muss ein Sock- \_ dgram oder eine \_ socketrohdaten sein). |
| IPv6- \_ recvtclass | ja | ja | DWORD (Boolean) | Gibt an, ob der IP-Stapel den Steuerelement Puffer mit einer Nachricht auffüllen soll, die das IPv6-Header Feld "Traffic Class" eines empfangenen Datagramms enthält. Wenn dieser Wert true ist, gibt die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion optionale Steuerungsdaten zurück, die den IPv6-Header Feldwert der Datenverkehrs Klasse des empfangenen Datagramms enthalten.  Mit dieser Option kann das IPv6-Header Feld "Traffic Class" des empfangenen Datagramms in der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur zurückgegeben werden. Der zurückgegebene Nachrichtentyp ist IPv6- \_ tclass. Alle DSCP-und ECN-Bits des Felds "Traffic Class" werden zurückgegeben.  Diese Option ist nur für Datagrammsockets gültig (der Sockettyp muss ein Sock- \_ dgram sein).  |
| IPv6- \_ \_ unicasthops | ja | ja | DWORD | Ruft den aktuellen TTL-Wert ab, der dem IPv6-Socket für Unicast-Datenverkehr zugeordnet ist Es ist unzulässig, die Gültigkeitsdauer auf einen Wert größer als 255 festzulegen. |
| IPv6- \_ Unicast, \_ Wenn | ja | ja | DWORD (bei \_ Index) | Ruft die ausgehende Schnittstelle zum Senden von IPv6-Datenverkehr ab oder legt Mit dieser Option wird die Standardschnittstelle für den Empfang von IPv6-Datenverkehr nicht geändert. Diese Option ist für mehrfach vernetzte Computer wichtig.  Der Eingabe Wert für das Festlegen dieser Option ist ein 4-Byte-Schnittstellen Index der gewünschten ausgehenden Schnittstelle in der Host-Byte Reihenfolge. Die [**getadaptersadressen**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) -Funktion kann zum Abrufen der Schnittstellen Indexinformationen verwendet werden. Wenn *optval* NULL ist, wird die Standardschnittstelle für das Senden von IPv6-Datenverkehr auf nicht angegeben festgelegt.  Beim Aktivieren dieser Option gibt das *optval* den aktuellen Standardschnittstellen Index zum Senden von IPv6-Datenverkehr in der Host-Byte Reihenfolge zurück. |
| IPV6_USER_MTU | ja | ja | DWORD | Ruft eine obere Grenze auf der IP-Ebenen-MTU (in Bytes) für den angegebenen Socket ab oder legt diese fest. Wenn der Wert höher ist als die Schätzung des Pfads des Pfads, den Sie auf einem verbundenen Socket abrufen können, indem Sie die Option **IPV6_MTU** Socket Abfragen), hat die Option keine Auswirkungen. Wenn der Wert niedriger ist, werden ausgehende Pakete, die größer als dieser ist, fragmentiert, oder es kann nicht gesendet werden, abhängig vom Wert **IPV6_DONTFRAG**. Der Standardwert ist **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Für die Typsicherheit sollten Sie die Funktionen [**wsagetipusermtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) und [**wsasetipusermtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) anstelle der direkten Verwendung der Socket-Option verwenden. |
| IPv6- \_ V6ONLY | ja | ja | DWORD (Boolean) | Gibt an, ob ein für die AF \_ inet6 Address-Familie erstellter Socket auf IPv6-Kommunikation beschränkt ist. Sockets, die für die Gruppe "AF inet6 Address" erstellt wurden, \_ können für die IPv6-und IPv4-Kommunikation verwendet werden Einige Anwendungen möchten möglicherweise die Verwendung eines für die AF- \_ inet6-Adressfamilie erstellten Sockets auf die IPv6-Kommunikation einschränken. Wenn dieser Wert ungleich 0 (standardmäßig unter Windows) ist, kann ein für die AF \_ inet6 Address-Familie erstellter Socket verwendet werden, um nur IPv6-Pakete zu senden und zu empfangen. Wenn dieser Wert 0 (null) ist, kann ein für die AF-inet6-Adressfamilie erstellter Socket \_ zum Senden und empfangen von Paketen an eine oder von einer IPv6-Adresse oder einer IPv4-Adresse verwendet werden. Die Möglichkeit der Interaktion mit einer IPv4-Adresse setzt die Verwendung von IPv4-zugeordneten Adressen voraus. Diese Socketoption wird unter Windows Vista oder höher unterstützt. |

## <a name="windows-support-for-ipproto_ipv6-socket-options"></a>Windows-Unterstützung für ipproto \_ IPv6-Socketoptionen

| Option | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|
| IP- \_ ursprüngliche \_ Ankunft, \_ Wenn | x | x | x | | |
| IPV6_ADD_IFLIST | Ab Windows 10, Version 1803 | | | | | |
| IPv6 \_ - \_ Mitgliedschaft hinzufügen | x | x | x | x | x |
| IPV6_DEL_IFLIST | Ab Windows 10, Version 1803 | | | | | |
| IPv6- \_ Drop- \_ Mitgliedschaft | x | x | x | x | x |
| IPV6_GET_IFLIST | Ab Windows 10, Version 1803 | | | | | |
| IPv6- \_ hdrincl | x | x | x | x | x |
| IPv6- \_ hoplimit | x | x | x | x | x |
| IPV6_IFLIST | Ab Windows 10, Version 1803 | | | | | |
| IPv6 \_ - \_ joingruppe | x | x | x | x | x |
| IPv6 \_ - \_ Gruppe verlassen | x | x | x | x | x |
| IPv6- \_ Multicast \_ Hops | x | x | x | x | x |
| IPv6- \_ Multicast, \_ Wenn | x | x | x | x | x |
| IPv6- \_ Multicast \_ Schleife | x | x | x | x | x |
| IPv6- \_ pktinfo | x | x | x | x | x |
| [IPv6- \_ Schutz \_ Ebene](ipv6-protection-level.md) | x | x | x | x | x |
| IPv6- \_ recvif | x | x | x | x | x |
| IPv6- \_ \_ unicasthops | x | x | x | x | x |
| IPv6- \_ Unicast, \_ Wenn | x | x | x | x | x |
| IPv6- \_ V6ONLY | x | x | x | x | x |

<br/>

| Option | Windows Server 2003 | Windows XP |
|-|-|-|
| IP- \_ ursprüngliche \_ Ankunft, \_ Wenn | | |
| IPV6_ADD_IFLIST | | |
| IPv6 \_ - \_ Mitgliedschaft hinzufügen | x | x |
| IPV6_DEL_IFLIST | | |
| IPv6- \_ Drop- \_ Mitgliedschaft | x | x |
| IPV6_GET_IFLIST | | |
| IPv6 \_ hdrincl x | x |
| IPv6- \_ hoplimit x | x |
| IPV6_IFLIST | | |
| IPv6 \_ - \_ joingruppe | x | x |
| IPv6 \_ - \_ Gruppe verlassen | x | x |
| IPv6- \_ Multicast \_ Hops | x | x |
| IPv6- \_ Multicast, \_ Wenn | x | x |
| IPv6- \_ Multicast \_ Schleife | x | x |
| IPv6- \_ pktinfo | x | x |
| [IPv6- \_ Schutz \_ Ebene](ipv6-protection-level.md) | x | x |
| IPv6- \_ recvif | | |
| IPv6- \_ \_ unicasthops | x | x |
| IPv6- \_ Unicast, \_ Wenn | | |
| IPv6- \_ V6ONLY | | |

## <a name="remarks"></a>Bemerkungen

Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Header Dateien geändert, und die **ipproto \_ IPv6** -Ebene wird in der Header Datei " *Ws2def. h* " definiert, die automatisch in der Header Datei " *Winsock2. h* " enthalten ist. Die **ipproto \_ IPv6** -Socketoptionen sind in der Header Datei " *Ws2ipdef. h* " definiert, die automatisch in der Header Datei " *Ws2tcpip. h* " enthalten ist. Die Header Dateien *Ws2def. h* und *Ws2ipdef. h* sollten niemals direkt verwendet werden.

Die IP- \_ ursprüngliche \_ Ankunft, wenn die \_ Socketoption unter Windows Server 2008 R2 sowie unter Windows 7 unterstützt wird.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | <dl> <dt>Ws2def. h (Include Winsock2. h); </dt> <dt>Winsock2. h unter Windows Server 2003 und Windows XP</dt> </dl> |
