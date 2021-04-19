---
description: Beachten Sie, dass alle Windows Sockets 1,1-Funktionen für die Namensauflösung für IPv4-TCP/IP-Netzwerke spezifisch sind.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2447590b25861abc80bd0a89be173272fb809814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350437"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a>Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API

> [!Note]  
> Alle Windows Sockets 1,1-Funktionen für die Namensauflösung sind spezifisch für IPv4-TCP/IP-Netzwerke. Anwendungsentwickler werden dringend davon abgeraten, diese Transport spezifischen Funktionen, die nur IPv4 unterstützen, weiterhin zu verwenden.

 

Anwendungsentwickler sollten die folgenden Funktionen verwenden, die Protokoll unabhängig sind und sowohl die IPv6-als auch die IPv4-Namensauflösung unterstützen.

-   [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [**Getaddrinfow**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [**getnameingefo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [**Getnameingefow**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

Windows Sockets 1,1 hat eine Reihe von Routinen definiert, die für die Namensauflösung mit TCP/IP-Netzwerken (IP-Version 4) verwendet werden. Diese werden mitunter als **getxbyy** -Funktionen bezeichnet und umfassen Folgendes:

<dl>

[**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

Asynchrone Versionen dieser Funktionen wurden ebenfalls definiert.

<dl>

[**Wsaasyncgethostbyaddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[**Wsaasyncgethostbyname**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[**Wsaasyncgetprotobyname**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[**Wsaasyncgetprotobynumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[**Wsaasyncgetservbyname**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[**Wsaasyncgetservbyport**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

Es gibt auch zwei Funktionen, die jetzt in der Winsock2.dll implementiert sind und zum Konvertieren von gepunkteten IPv4-Adress Notation in bzw. aus Zeichen folgen-und Binär Darstellungen verwendet werden.

<dl>

[**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[**inet \_ NUM**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

Um die strikte Abwärtskompatibilität mit Windows Sockets 1,1 beizubehalten, werden alle älteren reinen IPv4-Funktionen weiterhin unterstützt, solange mindestens ein Namespace Anbieter vorhanden ist, der die AF \_ inet-Adressfamilie unterstützt (diese Funktionen sind für die IP-Version 6, die durch AF inet6 gekennzeichnet ist, nicht relevant \_ ).

Die Ws2- \_32.dll implementiert diese Kompatibilitätsfunktionen in Bezug auf die neuen, Protokoll unabhängigen namens Auflösungs Funktionen mit einer entsprechenden Sequenz von [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) / **Next** / **End** -Funktionsaufrufen. Die Details zur Zuordnung der **getxbyy** -Funktionen zu namens Auflösungs Funktionen finden Sie unten. Der WSs2 \_ -32.dll behandelt die Unterschiede zwischen den asynchronen und synchronen Versionen der **getxbyy** -Funktionen, sodass nur die Implementierung der synchronen **getxbyy** -Funktionen erläutert wird.

In diesem Abschnitt wird die kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API beschrieben. In der folgenden Liste werden die Themen in diesem Abschnitt beschrieben:

-   [Grundlegender Ansatz für getxbyy in der API](basic-approach-for-getxbyy-in-the-api-2.md)
-   [Funktionen "getprotobyname" und "getprotobynumber" in der API](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [Funktionen "getservbyname" und "getservbyport" in der API](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [Funktion "gethostbyname" in der API](gethostbyname-function-in-the-api-2.md)
-   [Funktion "gethostbyaddr" in der API](gethostbyaddr-function-in-the-api-2.md)
-   [Funktion "GetHostName" in der API](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokoll unabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
