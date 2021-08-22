---
description: Windows Sockets 1.1 definierten eine Reihe von Routinen, die für die IPv4-Namensauflösung mit TCP/IP-Netzwerken verwendet wurden. Diese werden üblicherweise als GetXbyY-Funktionen bezeichnet und enthalten Folgendes.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Kompatible Namensauflösung für TCP/IP im Windows Sockets 1.1 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea355eb85d41a507e4970bf0c8d925a41ed81ca51c08b9c77955ad702a62d27c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051678"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a>Kompatible Namensauflösung für TCP/IP im Windows Sockets 1.1 SPI

Windows Sockets 1.1 definierten eine Reihe von Routinen, die für die IPv4-Namensauflösung mit TCP/IP-Netzwerken verwendet wurden. Diese werden üblicherweise als **GetXbyY-Funktionen** bezeichnet und enthalten Folgendes.

[**Gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname)

[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[**Gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)

Asynchrone Versionen dieser Funktionen wurden ebenfalls definiert.

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

Diese Funktionen sind spezifisch für TCP/IP-Netzwerke. Entwickler von protokollunabhängigen Anwendungen werden davon abgeraten, diese transportspezifischen Funktionen weiterhin zu nutzen. Um jedoch die strikte Abwärtskompatibilität mit Windows Sockets 1.1 beizubehalten, werden die vorherigen Funktionen weiterhin unterstützt, solange mindestens ein Namespaceanbieter vorhanden ist, der die AF \_ INET-Adressfamilie unterstützt.

Der *\_ Ws2-32.dll* implementiert diese Kompatibilitätsfunktionen in Bezug auf die neuen, protokollunabhängigen Namensauflösungsfunktionen mithilfe einer entsprechenden Sequenz von [**WSALookupServiceBegin-,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) [**WSALookupServiceNext-,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) [**WSALookupServiceEnd-Funktionsaufrufen.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) Die Details zur Zuordnung der **GetXbyY-Funktionen** zu Funktionen zur Namensauflösung sind unten angegeben. Die \_ Ws2-32.dll behandelt die Unterschiede zwischen den asynchronen und synchronen Versionen der **GetXbyY-Funktionen,** sodass nur die Implementierung der synchronen **GetXbyY-Funktionen** erläutert wird.

 

 
