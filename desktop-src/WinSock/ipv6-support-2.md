---
description: IPv6-Unterstützung, TCP/IP-Anhang und Windows-Sockets.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: IPv6-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ffc720a41c896653c74df2cb76f944cbbb310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129168"
---
# <a name="ipv6-support"></a>IPv6-Unterstützung

Um sowohl IPv4 als auch IPv6 unter Windows XP mit Service Pack 1 (SP1) und Windows Server 2003 zu unterstützen, muss eine Anwendung zwei Sockets erstellen, einen Socket für die Verwendung mit IPv4 und einen Socket für die Verwendung mit IPv6. Diese beiden Sockets müssen separat von der Anwendung behandelt werden.

Wenn ein TCP/IP-Dienstanbieter unter Windows XP mit SP1 und Windows Server 2003 die IPv4-und IPv6-Adressierung unterstützt, muss er zwei separate Sockets erstellen und separat auf diesen Sockets lauschen:

-   Einmal für IPv4.
-   Einmal für die IPv6-Adressfamilie.

Windows Vista und höher bieten die Möglichkeit, einen einzelnen IPv6-Socket zu erstellen, der sowohl IPv6-als auch IPv4-Datenverkehr verarbeiten kann. Beispielsweise wird ein TCP-lausch-Socket für IPv6 erstellt, in den Dual Stack-Modus versetzt und an Port 5001 gebunden. Dieser Dual-Stack-Socket kann Verbindungen von IPv6-TCP-Clients akzeptieren, die Verbindungen mit Port 5001 herstellen, sowie IPv4-TCP-Clients, die eine Verbindung mit 5001 Port Diese Funktion ermöglicht einen stark vereinfachten Anwendungs Entwurf und reduziert den Ressourcen Aufwand, der für die Bereitstellung von Vorgängen auf zwei separaten Sockets erforderlich ist. Es gibt jedoch einige Einschränkungen, die erfüllt sein müssen, damit ein Dual-Stack-Socket verwendet werden kann. Weitere Informationen finden Sie unter [Dual-Stack-Sockets](dual-stack-sockets.md).

[**Wsaenumprotokolle**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) gibt zwei [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Strukturen für jeden der unterstützten Socketypen zurück (Sock- \_ Stream, sock- \_ dgram, sock- \_ RAW). Die **iaddressfamily** muss von auf AF \_ inet für IPv4-Adressierung und auf AF \_ inet6 for IPv6-Adressierung festgelegt werden.

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

Wenn eine Anwendung Windows Sockets 1,1-Funktionen verwendet und IPv6-Adressen verwenden möchten, verwendet Sie möglicherweise weiterhin alle alten Funktionen, die die [**sockaddr**](sockaddr-2.md) -Struktur als einen der Parameter annehmen ([**Bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)usw.). Die einzige Änderung, die erforderlich ist, ist die Verwendung von **sockaddr \_ IN6** anstelle von **sockaddr \_ in**.

Die namens Auflösungs Funktionen ("[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)", " [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)" usw.) und die Adress Konvertierungs Funktionen ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ ntoia**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) können jedoch nicht wieder verwendet werden, da Sie davon ausgehen, dass eine IP-Adresse eine Länge von 4 Bytes hat. Eine Anwendung, die Namensauflösung und Adress Konvertierung für IPv6-Adressen durchführen möchte, muss Windows Sockets 2-spezifische Funktionen verwenden. Viele neue Funktionen wurden eingeführt, damit Windows Sockets 2-Anwendungen IPv6 nutzen können, einschließlich der Funktionen [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

Weitere Informationen zum Aktivieren von IPv6-Funktionen in einer Anwendung finden Sie im [IPv6-Handbuch für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md).

 

 
