---
description: IPv6-Unterstützung, TCP/IP-Anhang und Windows Sockets.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: IPv6-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f48e5b46ef1fcf1a2257db4a04b5435443552bb49f6c3c2b2dc4784077dcbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794800"
---
# <a name="ipv6-support"></a>IPv6-Unterstützung

Um sowohl IPv4 als auch IPv6 unter Windows XP mit Service Pack 1 (SP1) und auf Windows Server 2003 zu unterstützen, muss eine Anwendung zwei Sockets erstellen, einen Socket für die Verwendung mit IPv4 und einen Socket für die Verwendung mit IPv6. Diese beiden Sockets müssen separat von der Anwendung verarbeitet werden.

Wenn ein TCP/IP-Dienstanbieter unter Windows XP mit SP1 und auf Windows Server 2003 die IPv4- und IPv6-Adressierung unterstützt, muss er zwei separate Sockets erstellen und separat an diesen Sockets lauschen:

-   Einmal für IPv4.
-   Einmal für die IPv6-Adressfamilie.

Windows Vista und höher bieten die Möglichkeit, einen einzelnen IPv6-Socket zu erstellen, der sowohl IPv6- als auch IPv4-Datenverkehr verarbeiten kann. Beispielsweise wird ein TCP-Lauschensocket für IPv6 erstellt, in den Dual Stack-Modus übertragen und an Port 5001 gebunden. Dieser Doppelstapelsocket kann Verbindungen von IPv6-TCP-Clients akzeptieren, die eine Verbindung mit Port 5001 herstellen, und von IPv4-TCP-Clients, die eine Verbindung mit Port 5001 herstellen. Dieses Feature ermöglicht einen erheblich vereinfachten Anwendungsentwurf und reduziert den Ressourcenaufwand, der für die Veröffentlichung von Vorgängen auf zwei separaten Sockets erforderlich ist. Es gibt jedoch einige Einschränkungen, die erfüllt sein müssen, um einen Doppelstapelsocket zu verwenden. Weitere Informationen finden Sie unter [Dual-Stack Sockets](dual-stack-sockets.md).

[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) gibt zwei [**WSAPROTOCOL \_ INFO-Strukturen**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für jeden unterstützten Sockettyp zurück (SOCK \_ STREAM, SOCK \_ DGRAM, SOCK \_ RAW). **iAddressFamily** muss für die IPv4-Adressierung auf AF INET und für die \_ IPv6-Adressierung auf AF \_ INET6 festgelegt werden.

Die IPv6-Adressen werden in den folgenden Strukturen beschrieben.

``` syntax
struct in_addr6 {
    u_char    s6_addr[16];             /* IPv6 address */
};

struct sockaddr_in6 {
    short             sin6_family;     /* AF_INET6 */
    u_short           sin6_port;       /* Transport level port number */
    u_long            sin6_flowinfo;   /* IPv6 flow information */
    struct in_addr6   sin6_addr;       /* IPv6 address */
    u_long            sin6_scope_id;   /* set of interfaces for a scope */
   };
```

Wenn eine Anwendung Windows Sockets 1.1-Funktionen verwendet und IPv6-Adressen verwenden möchte, kann sie weiterhin alle alten Funktionen verwenden, die die [**Sockaddr-Struktur**](sockaddr-2.md) als einen der Parameter akzeptieren [**(**](/windows/desktop/api/winsock/nf-winsock-bind)binden [**,**](/windows/desktop/api/Winsock2/nf-winsock2-connect)verbinden, [**senden**](/windows/desktop/api/winsock/nf-winsock-sendto)zu und von [**ableiten,**](/windows/desktop/api/winsock/nf-winsock-recvfrom) [**akzeptieren**](/windows/desktop/api/Winsock2/nf-winsock2-accept)usw.). Die einzige erforderliche Änderung ist die Verwendung von **sockaddr \_ in6** anstelle von **sockaddr \_ in**.

Die Namensauflösungsfunktionen ([**gethostbyname,**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)usw.) und die Adresskonvertierungsfunktionen ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) können jedoch nicht wiederverwendet werden, da sie davon ausgehen, dass eine IP-Adresse 4 Byte lang ist. Eine Anwendung, die namensauflösung und Adresskonvertierung für IPv6-Adressen durchführen möchte, muss Windows Sockets 2-spezifische Funktionen verwenden. Es wurden viele neue Funktionen eingeführt, um Windows Sockets 2-Anwendungen die Nutzung von IPv6 zu ermöglichen, einschließlich der [**Getaddrinfo-**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und [**getnameinfo-Funktionen.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)

Weitere Informationen zum Aktivieren von IPv6-Funktionen in einer Anwendung finden Sie im [IPv6-Handbuch für Windows Sockets-Anwendungen.](ipv6-guide-for-windows-sockets-applications-2.md)

 

 
