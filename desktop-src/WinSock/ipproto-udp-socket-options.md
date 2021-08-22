---
description: In der folgenden Tabelle werden \_ IPPROTO-UDP-Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4- und IPv6-Adressfamilien (AF \_ INET und AF \_ INET6) mit dem Protokollparameter für die Socketfunktion erstellt wurden, die als UDP (IPPROTO \_ UDP) angegeben ist.
ms.assetid: 579448a1-22af-488f-a1f5-97ba69a15524
title: IPPROTO_UDP-Socketoptionen
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 763e45a78ffd8bfed15d09f4e77bc17be71ccc110499d8937b60b49294f499c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051478"
---
# <a name="ipproto_udp-socket-options"></a>\_IPPROTO-UDP-Socketoptionen

In der folgenden Tabelle werden **\_ IPPROTO-UDP-Socketoptionen** beschrieben, die für Sockets gelten, die für die IPv4- und IPv6-Adressfamilien (AF \_ INET und AF \_ INET6) mit dem *Protokollparameter* für die [**Socketfunktion**](/windows/win32/api/Winsock2/nf-winsock2-socket) erstellt wurden, die als UDP (IPPROTO \_ UDP) angegeben ist. Weitere Informationen zum Abrufen und Festlegen von Socketoptionen finden Sie auf den Referenzseiten der Funktionen [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) und [**setsockopt.**](/windows/win32/api/winsock/nf-winsock-setsockopt)

Um Protokolle aufzulisten und unterstützte Eigenschaften für jedes installierte Protokoll zu ermitteln, verwenden Sie die Funktion [**WSAEnumProtocols,**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols)oder [**WSCEnumProtocols32.**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

## <a name="options"></a>Optionen

| Option | Herunterladen | Set | Optval-Typ | Beschreibung |
|-|-|-|-|-|
| UDP \_ CHECKSUM \_ COVERAGE (ws2tcpip.h) | Ja | Ja | DWORD (boolesch) | Bei **TRUE** werden UDP-Datagramme mit einer Prüfsumme gesendet. |
| UDP \_ NOCHECKSUM (ws2tcpip.h) | Ja | Ja | DWORD (boolesch) | True gibt an, dass UDP-Datagramme mit der Prüfsumme 0 (null) gesendet werden. Erforderlich für Dienstanbieter. Wenn ein Dienstanbieter nicht über einen Mechanismus zum Deaktivieren der UDP-Prüfsummenberechnung verfügt, kann er diese Option einfach speichern, ohne eine Aktion durchzuführen. Diese Option wird für IPv6 nicht unterstützt. |
| UDP_RECV_MAX_COALESCED_SIZE (ws2ipdef.h; include ws2tcpip.h) | Ja | Ja | DWORD | Bei Festlegung auf einen Wert ungleich 0 (null) können mehrere empfangene Datagramme in einem einzelnen Nachrichtenpuffer zusammengefasst werden, bevor sie ihrer Anwendung angezeigt werden. Der Optionswert stellt die maximale Nachrichtengröße in Bytes für zusammengeknüpfte Nachrichten dar, die ihrer Anwendung angezeigt werden können. Nicht zusammengeknüpfte Nachrichten, die größer als der Optionswert sind, können weiterhin angezeigt werden. Der Standardwert ist 0 (keine Zusammenfühung). Datagramme werden nur zusammengeführt, wenn sie von der gleichen Quelladresse und demselben Port stammen. Alle zusammengeknüpften Datagramme haben die gleiche &mdash; Größe, mit Ausnahme des letzten Datagramms, das kleiner sein kann. Wenn Ihre Anwendung die zusammengeknüpften Datagrammgrößen abrufen möchte (mit Ausnahme des letzten Datagramms, das sich möglicherweise unterscheidet), müssen Sie eine Empfangs-API verwenden, die Steuerungsinformationen unterstützt (z. [**B. LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Die Größe aller bis auf die letzte Nachricht befindet sich in der **UDP_COALESCED_INFO** Steuernachricht vom Typ DWORD. Aus Gründen der Typsicherheit sollte Ihre Anwendung die Funktionen [WSAGetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) und [WSASetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) anstelle der Socketoption direkt verwenden. |
| UDP_SEND_MSG_SIZE (ws2ipdef.h; include ws2tcpip.h) | Ja | Ja | DWORD | Bei Festlegung auf einen Wert ungleich 0 (null) werden von Ihrer Anwendung gesendete Puffer vom Netzwerkstapel in mehrere Nachrichten unterteilt. Der Optionswert stellt die Größe jeder aufgeschlüsselten Nachricht dar. Der Optionswert wird in Bytes dargestellt. Die Größe des letzten Segments kann kleiner als der Wert der Option sein. Der Standardwert ist 0 (keine Segmentierung). Ihre Anwendung sollte einen Wert festlegen, der niedriger als die MTU des Pfads zu den Zielen ist, um eine IP-Fragmentierung zu vermeiden. Aus Gründen der Typsicherheit sollte Ihre Anwendung die Funktionen [WSAGetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) und [WSASetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) anstelle der Socketoption direkt verwenden. |

## <a name="legacy-windows-support-for-ipproto_udp-options"></a>Unterstützung von Legacy-Windows für \_ IPPROTO-UDP-Optionen

**UDP \_ CHECKSUM \_ COVERAGE** ist für Windows 2000 und für Windows NT4 nicht verfügbar. **UDP \_ CHECKSUM \_ COVERAGE** und **UDP \_ NOCHECKSUM** sind auf Windows 9x/Me nicht verfügbar. 

## <a name="remarks"></a>Hinweise

Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Headerdateien geändert, und die **\_ IPPROTO-UDP-Ebene** wird in der *Ws2def.h-Headerdatei* definiert, die automatisch in der *Winsock2.h-Headerdatei* enthalten ist. Die **\_ IPPROTO-UDP-Socketoptionen** werden in der *Headerdatei Ws2tcpip.h* definiert. Die *Headerdatei Ws2def.h* sollte nie direkt verwendet werden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header<br/> | <dl> <dt>ws2ipdef.h (einschließlich ws2tcpip.h) und ws2tcpip.h</dt> <dt>Winsock2.h auf Windows Server 2003, Windows XP und Windows 2000</dt> </dl> |
