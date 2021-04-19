---
description: In der folgenden Tabelle werden die ipproto \_ UDP-Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4-und IPv6-Adressfamilien (AF \_ inet und AF inet6) erstellt wurden, \_ mit dem Protokoll Parameter für die als UDP (ipproto UDP) angegebene Socketfunktion \_ .
ms.assetid: 579448a1-22af-488f-a1f5-97ba69a15524
title: IPPROTO_UDP-Socketoptionen
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 6f1f25ebae34d7db4290ab23bbf799fc0e0b68df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368386"
---
# <a name="ipproto_udp-socket-options"></a>Ipproto \_ UDP-Socketoptionen

In der folgenden Tabelle werden die **ipproto \_ UDP** -Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4-und IPv6-Adressfamilien (AF \_ inet und AF inet6) erstellt wurden, \_ mit dem *Protokoll* Parameter für die als UDP (ipproto UDP) angegebene [**Socketfunktion**](/windows/win32/api/Winsock2/nf-winsock2-socket) \_ . Weitere Informationen zum Ermitteln und Festlegen von Socketoptionen finden Sie auf den Referenzseiten zu den Funktionen [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) und [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) .

Verwenden Sie die [**wsaenumprotokolls**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa)-, [**wscenumprotokolle**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols)-oder [**WSCEnumProtocols32**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols32) -Funktion, um Protokolle aufzulisten und die unterstützten Eigenschaften für jedes installierte Protokoll zu ermitteln.

## <a name="options"></a>Optionen

| Option | Herunterladen | Set | Optval-Typ | BESCHREIBUNG |
|-|-|-|-|-|
| UDP- \_ Prüfsummen \_ Abdeckung (Ws2tcpip. h) | ja | ja | DWORD (Boolean) | **True** gibt an, dass UDP-Datagramme mit einer Prüfsumme gesendet werden. |
| UDP \_ nochecksum (Ws2tcpip. h) | ja | ja | DWORD (Boolean) | **True** gibt an, dass UDP-Datagramme mit der Prüfsumme 0 (null) gesendet werden. Für Dienstanbieter erforderlich. Wenn ein Dienstanbieter keinen Mechanismus zum Deaktivieren der UDP-Prüfsummenberechnung hat, wird diese Option möglicherweise einfach gespeichert, ohne dass eine Aktion ausgeführt wird. Diese Option wird für IPv6 nicht unterstützt. |
| UDP_RECV_MAX_COALESCED_SIZE (ws2ipdef. h; include Ws2tcpip. h) | ja | ja | DWORD | Wenn ein Wert ungleich 0 (null) festgelegt ist, können mehrere Empfangene Datagramme in einen einzelnen Nachrichten Puffer zusammengebracht werden, bevor Sie für die Anwendung angegeben werden. Der Optionswert stellt die maximale Nachrichtengröße in Bytes für zusammengeführte Nachrichten dar, die für die Anwendung angezeigt werden können. Nicht zusammengestellte Nachrichten, die größer sind als der Optionswert, können weiterhin angegeben werden. Der Standardwert ist 0 (keine zusammen Fügung). Datagramme werden nur zusammengebracht, wenn Sie von derselben Quelladresse und demselben Port stammen. Alle zusammengefügten Datagramme haben dieselbe Größe &mdash; , außer dem letzten Datagramm, das möglicherweise kleiner ist. Wenn die Anwendung die Datagramm-Größen abrufen möchte (mit Ausnahme des letzten Datagramms, das sich unterscheiden kann), das zusammengefügt wurde, müssen Sie eine Receive-API verwenden, die Steuerungsinformationen unterstützt (z. b. [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)). Die Größe aller außer der letzten Nachricht ist in der **UDP_COALESCED_INFO** -Steuerungs Meldung, die vom Typ DWORD ist, zu finden. Bei der Typsicherheit sollte Ihre Anwendung die Funktionen [wsagetudprecvmaxcoalescedsize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) und [wsasetudprecvmaxcoalescedsize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) anstelle der Socket-Option direkt verwenden. |
| UDP_SEND_MSG_SIZE (ws2ipdef. h; include Ws2tcpip. h) | ja | ja | DWORD | Wenn der Wert ungleich 0 (null) festgelegt ist, werden die von der Anwendung gesendeten Puffer vom Netzwerk Stapel in mehrere Nachrichten aufgeteilt. Der Optionswert stellt die Größe jeder aufgeschlenen Nachricht dar. Der Optionswert wird in Bytes dargestellt. Die Größe des letzten Segments kann kleiner sein als der Wert der Option. Der Standardwert ist 0 (keine Segmentierung). Die Anwendung sollte einen Wert festlegen, der niedriger ist als die MTU des Pfads zu den Zielen, um die IP-Fragmentierung zu vermeiden. Bei der Typsicherheit sollte Ihre Anwendung die Funktionen [wsagetudpsendmessagesize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) und [wsasetudpsendmessagesize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) anstelle der Socket-Option direkt verwenden. |

## <a name="legacy-windows-support-for-ipproto_udp-options"></a>Ältere Windows-Unterstützung für ipproto \_ UDP-Optionen

**UDP \_ Die Prüfsummen \_ Abdeckung** ist unter Windows 2000 und Windows NT4 nicht verfügbar. **UDP \_ Prüfsummen \_ Abdeckung** und **UDP \_ nochecksum** sind unter Windows 9X/ME nicht verfügbar. 

## <a name="remarks"></a>Bemerkungen

Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Header Dateien geändert, und die **ipproto- \_ UDP** -Ebene wird in der Header Datei " *Ws2def. h* " definiert, die automatisch in der Header Datei " *Winsock2. h* " enthalten ist. Die **ipproto- \_ UDP** -Socketoptionen sind in der Header Datei " *Ws2tcpip. h* " definiert. Die Header Datei " *Ws2def. h* " sollte niemals direkt verwendet werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header<br/> | <dl> <dt>ws2ipdef. h (Include Ws2tcpip. h) und Ws2tcpip. h</dt> <dt>Winsock2. h unter Windows Server 2003, Windows XP und Windows 2000</dt> </dl> |
