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
# <a name="ipv6-support"></a><span data-ttu-id="fc6ba-103">IPv6-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="fc6ba-103">IPv6 Support</span></span>

<span data-ttu-id="fc6ba-104">Um sowohl IPv4 als auch IPv6 unter Windows XP mit Service Pack 1 (SP1) und Windows Server 2003 zu unterstützen, muss eine Anwendung zwei Sockets erstellen, einen Socket für die Verwendung mit IPv4 und einen Socket für die Verwendung mit IPv6.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-104">In order to support both IPv4 and IPv6 on Windows XP with Service Pack 1 (SP1) and on Windows Server 2003, an application has to create two sockets, one socket for use with IPv4 and one socket for use with IPv6.</span></span> <span data-ttu-id="fc6ba-105">Diese beiden Sockets müssen separat von der Anwendung behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-105">These two sockets must be handled separately by the application.</span></span>

<span data-ttu-id="fc6ba-106">Wenn ein TCP/IP-Dienstanbieter unter Windows XP mit SP1 und Windows Server 2003 die IPv4-und IPv6-Adressierung unterstützt, muss er zwei separate Sockets erstellen und separat auf diesen Sockets lauschen:</span><span class="sxs-lookup"><span data-stu-id="fc6ba-106">If a TCP/IP service provider on Windows XP with SP1 and on Windows Server 2003 supports IPv4 and IPv6 addressing, it must create two separate sockets and listen separately on these sockets:</span></span>

-   <span data-ttu-id="fc6ba-107">Einmal für IPv4.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-107">Once for IPv4.</span></span>
-   <span data-ttu-id="fc6ba-108">Einmal für die IPv6-Adressfamilie.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-108">Once for the IPv6 address family.</span></span>

<span data-ttu-id="fc6ba-109">Windows Vista und höher bieten die Möglichkeit, einen einzelnen IPv6-Socket zu erstellen, der sowohl IPv6-als auch IPv4-Datenverkehr verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-109">Windows Vista and later offer the ability to create a single IPv6 socket which can handle both IPv6 and IPv4 traffic.</span></span> <span data-ttu-id="fc6ba-110">Beispielsweise wird ein TCP-lausch-Socket für IPv6 erstellt, in den Dual Stack-Modus versetzt und an Port 5001 gebunden.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-110">For example, a TCP listening socket for IPv6 is created, put into dual stack mode, and bound to port 5001.</span></span> <span data-ttu-id="fc6ba-111">Dieser Dual-Stack-Socket kann Verbindungen von IPv6-TCP-Clients akzeptieren, die Verbindungen mit Port 5001 herstellen, sowie IPv4-TCP-Clients, die eine Verbindung mit 5001 Port</span><span class="sxs-lookup"><span data-stu-id="fc6ba-111">This dual-stack socket can accept connections from IPv6 TCP clients connecting to port 5001 and from IPv4 TCP clients connecting to port 5001.</span></span> <span data-ttu-id="fc6ba-112">Diese Funktion ermöglicht einen stark vereinfachten Anwendungs Entwurf und reduziert den Ressourcen Aufwand, der für die Bereitstellung von Vorgängen auf zwei separaten Sockets erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-112">This feature allows for greatly simplified application design and reduces the resource overhead required of posting operations on two separate sockets.</span></span> <span data-ttu-id="fc6ba-113">Es gibt jedoch einige Einschränkungen, die erfüllt sein müssen, damit ein Dual-Stack-Socket verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-113">However, there are some restrictions that must be met in order to use a dual-stack socket.</span></span> <span data-ttu-id="fc6ba-114">Weitere Informationen finden Sie unter [Dual-Stack-Sockets](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="fc6ba-114">For more information, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="fc6ba-115">[**Wsaenumprotokolle**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) gibt zwei [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Strukturen für jeden der unterstützten Socketypen zurück (Sock- \_ Stream, sock- \_ dgram, sock- \_ RAW).</span><span class="sxs-lookup"><span data-stu-id="fc6ba-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) returns two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures for each of the supported socket types (SOCK\_STREAM, SOCK\_DGRAM, SOCK\_RAW).</span></span> <span data-ttu-id="fc6ba-116">Die **iaddressfamily** muss von auf AF \_ inet für IPv4-Adressierung und auf AF \_ inet6 for IPv6-Adressierung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-116">The **iAddressFamily** must by set to AF\_INET for IPv4 addressing, and to AF\_INET6 for IPv6 addressing.</span></span>

<span data-ttu-id="fc6ba-117">Die IPv6-Adressen werden in den folgenden Strukturen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-117">The IPv6 addresses are described in the following structures.</span></span>

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

<span data-ttu-id="fc6ba-118">Wenn eine Anwendung Windows Sockets 1,1-Funktionen verwendet und IPv6-Adressen verwenden möchten, verwendet Sie möglicherweise weiterhin alle alten Funktionen, die die [**sockaddr**](sockaddr-2.md) -Struktur als einen der Parameter annehmen ([**Bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)usw.).</span><span class="sxs-lookup"><span data-stu-id="fc6ba-118">If an application uses Windows Sockets 1.1 functions and wants to use IPv6 addresses, it may continue to use all the old functions that take the [**sockaddr**](sockaddr-2.md) structure as one of the parameters ([**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), and so forth).</span></span> <span data-ttu-id="fc6ba-119">Die einzige Änderung, die erforderlich ist, ist die Verwendung von **sockaddr \_ IN6** anstelle von **sockaddr \_ in**.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-119">The only change that is required is to use **sockaddr\_in6** instead of **sockaddr\_in**.</span></span>

<span data-ttu-id="fc6ba-120">Die namens Auflösungs Funktionen ("[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)", " [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)" usw.) und die Adress Konvertierungs Funktionen ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ ntoia**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) können jedoch nicht wieder verwendet werden, da Sie davon ausgehen, dass eine IP-Adresse eine Länge von 4 Bytes hat.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-120">However, the name resolution functions ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and so forth) and address conversion functions ([**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet\_ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) cannot be reused because they assume an IP address is 4 bytes in length.</span></span> <span data-ttu-id="fc6ba-121">Eine Anwendung, die Namensauflösung und Adress Konvertierung für IPv6-Adressen durchführen möchte, muss Windows Sockets 2-spezifische Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc6ba-121">An application that wants to perform name resolution and address conversion for IPv6 addresses must use Windows Sockets 2-specific functions.</span></span> <span data-ttu-id="fc6ba-122">Viele neue Funktionen wurden eingeführt, damit Windows Sockets 2-Anwendungen IPv6 nutzen können, einschließlich der Funktionen [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="fc6ba-122">Many new functions have been introduced to enable Windows Sockets 2 applications to take advantage of IPv6, including the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

<span data-ttu-id="fc6ba-123">Weitere Informationen zum Aktivieren von IPv6-Funktionen in einer Anwendung finden Sie im [IPv6-Handbuch für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md).</span><span class="sxs-lookup"><span data-stu-id="fc6ba-123">For more information on how to enable IPv6 capabilities in an application, see the [IPv6 Guide for Windows Sockets Applications](ipv6-guide-for-windows-sockets-applications-2.md).</span></span>

 

 
