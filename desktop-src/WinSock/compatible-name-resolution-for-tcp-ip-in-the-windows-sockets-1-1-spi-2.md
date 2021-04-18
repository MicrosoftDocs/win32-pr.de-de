---
description: 'Windows Sockets 1,1 hat eine Reihe von Routinen definiert, die für die IPv4-Namensauflösung mit TCP/IP-Netzwerken verwendet wurden. Diese werden in der Regel als getxbyy-Funktionen bezeichnet und umfassen Folgendes:'
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Kompatible Namensauflösung für TCP/IP in Windows Sockets 1,1 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347172"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a>Kompatible Namensauflösung für TCP/IP in Windows Sockets 1,1 SPI

Windows Sockets 1,1 hat eine Reihe von Routinen definiert, die für die IPv4-Namensauflösung mit TCP/IP-Netzwerken verwendet wurden. Diese werden in der Regel als **getxbyy** -Funktionen bezeichnet und umfassen Folgendes:

[**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname)

[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)

Asynchrone Versionen dieser Funktionen wurden ebenfalls definiert.

[**Wsaasyncgethostbyaddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[**Wsaasyncgethostbyname**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[**Wsaasyncgetprotobyname**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[**Wsaasyncgetprotobynumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[**Wsaasyncgetservbyname**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[**Wsaasyncgetservbyport**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

Diese Funktionen sind spezifisch für TCP/IP-Netzwerke. Entwickler von Protokoll unabhängigen Anwendungen werden davon abgeraten, diese Transport spezifischen Funktionen weiterhin zu verwenden. Um jedoch eine strikte Abwärtskompatibilität mit Windows Sockets 1,1 beizubehalten, werden die vorangehenden Funktionen weiterhin unterstützt, solange mindestens ein Namespace Anbieter vorhanden ist, der die AF \_ inet-Adressfamilie unterstützt.

Die *Ws2- \_32.dll* implementiert diese Kompatibilitätsfunktionen in Bezug auf die neuen, Protokoll unabhängigen namens Auflösungs Funktionen mit einer entsprechenden Sequenz von [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)und [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) -Funktionsaufrufen. Die Details zur Zuordnung der **getxbyy** -Funktionen zu namens Auflösungs Funktionen finden Sie unten. Der Ws2 \_ -32.dll behandelt die Unterschiede zwischen den asynchronen und synchronen Versionen der **getxbyy** -Funktionen, sodass nur die Implementierung der synchronen **getxbyy** -Funktionen erläutert wird.

 

 
