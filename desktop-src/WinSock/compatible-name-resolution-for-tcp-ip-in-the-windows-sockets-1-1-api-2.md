---
description: Beachten Sie, dass alle Windows Sockets 1.1-Funktionen für die Namensauflösung spezifisch für IPv4-TCP/IP-Netzwerke sind.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1.1-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13dfb1a403f782d0349e20729117fe1f4aed01479b01a6c2b5968f1d9bf15f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322300"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a>Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1.1-API

> [!Note]  
> Alle Windows Sockets 1.1-Funktionen für die Namensauflösung sind spezifisch für IPv4-TCP/IP-Netzwerke. Anwendungsentwicklern wird dringend davon abgeraten, diese transportspezifischen Funktionen, die nur IPv4 unterstützen, weiterhin zu verwenden.

 

Anwendungsentwickler sollten die folgenden Funktionen verwenden, die protokollunabhängig sind und sowohl die IPv6- als auch die IPv4-Namensauflösung unterstützen.

-   [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

Windows Sockets 1.1 definiert eine Reihe von Routinen, die für die Namensauflösung mit TCP/IP-Netzwerken (IP-Version 4) verwendet werden. Diese werden manchmal als **getXbyY-Funktionen** bezeichnet und enthalten Folgendes:

<dl>

[**Gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[**Gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

Asynchrone Versionen dieser Funktionen wurden ebenfalls definiert.

<dl>

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

Es gibt auch zwei Funktionen, die jetzt im Winsock2.dll implementiert sind und verwendet werden, um gepunktete Ipv4-Adress notationen in bzw. aus Zeichenfolgen- bzw. binären Darstellungen zu konvertieren.

<dl>

[**\_Inet-Add-Inr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

Um die strikte Abwärtskompatibilität mit Windows Sockets 1.1 beizubehalten, werden alle älteren reinen IPv4-Funktionen weiterhin unterstützt, solange mindestens ein Namespaceanbieter vorhanden ist, der die AF \_ INET-Adressfamilie unterstützt (diese Funktionen sind für IP-Version 6, angegeben durch AF \_ INET6, nicht relevant).

Die \_ Ws2-32.dll implementiert diese Kompatibilitätsfunktionen im Hinblick auf die neuen, protokollunabhängigen Namensauflösungsfunktionen mithilfe einer entsprechenden Sequenz von [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) / **Next** / **End-Funktionsaufrufen.** Die Details dazu, wie die **getXbyY-Funktionen** Namensauflösungsfunktionen zugeordnet werden, finden Sie unten. Die WSs2-32.dll \_ behandelt die Unterschiede zwischen den asynchronen und synchronen Versionen der **getXbyY-Funktionen,** sodass nur die Implementierung der synchronen **getXbyY-Funktionen** erläutert wird.

In diesem Abschnitt wird die kompatible Namensauflösung für TCP/IP in der Windows Sockets 1.1-API beschrieben. In der folgenden Liste werden die Themen in diesem Abschnitt beschrieben:

-   [Grundlegende Vorgehensweise für GetXbyY in der API](basic-approach-for-getxbyy-in-the-api-2.md)
-   [getprotobyname- und getprotobynumber-Funktionen in der API](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [getservbyname- und getservbyport-Funktionen in der API](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [gethostbyname-Funktion in der API](gethostbyname-function-in-the-api-2.md)
-   [gethostbyaddr-Funktion in der API](gethostbyaddr-function-in-the-api-2.md)
-   [gethostname-Funktion in der API](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokollunabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierungs- und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
