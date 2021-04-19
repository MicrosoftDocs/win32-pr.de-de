---
description: Die Winsock-Transport-SPI ähnelt der Winsock-API, da alle grundlegenden Socketfunktionen angezeigt werden.
ms.assetid: 37ef8a69-2aa0-4824-8ca9-4b84158086db
title: Transport Zuordnung zwischen API-und SPI-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f11b950c48d0887f1e593c65f9d77e27c33917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350007"
---
# <a name="transport-mapping-between-api-and-spi-functions"></a>Transport Zuordnung zwischen API-und SPI-Funktionen

Die Winsock-Transport-SPI ähnelt der Winsock-API, da alle grundlegenden Socketfunktionen angezeigt werden. Wenn eine neue Version einer Winsock-Funktion und die ursprüngliche Version in der API vorhanden sind, wird nur die neue Version in der SPI angezeigt. Dies wird in der folgenden Liste veranschaulicht.

-   " [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) " und " [**wsaconnetct**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) " sind jeweils [**wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) zugeordnet.
-   [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) -und [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Zuordnung zu [**wspaccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)
-   [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) und [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) Map to [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)

Weitere API-Funktionen, die in den erweiterten Versionen in SPI reduziert werden, umfassen Folgendes:

-   [**Senden**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto)
-   [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

Support Funktionen wie [**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl), [**htons**](/windows/desktop/api/winsock/nf-winsock-htons), [**numhl**](/windows/desktop/api/winsock/nf-winsock-ntohl)und [**NUM**](/windows/desktop/api/winsock/nf-winsock-ntohs) werden im Ws2 \_ -32.dll implementiert und nicht an Dienstanbieter übermittelt. Das gleiche gilt für die WSA-Versionen dieser Funktionen.

Die Enumeration des Windows Sockets Service-Anbieters und die blockierenden Hook-bezogenen Funktionen werden im Ws2- \_32.dll erkannt, sodass [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking), [wsasetblockinghook](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)und [wsaunhookblockinghook](/windows/desktop/api/winsock2/nf-winsock2-wsaunhookblockinghook) nicht als SPI-Funktionen angezeigt werden.

Da Fehlercodes zusammen mit SPI-Funktionen zurückgegeben werden, sind die Entsprechungen von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) und [**wsasetlasterror**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) in der SPI nicht erforderlich.

Die Bearbeitungs-und Wait-Funktionen von Ereignis Objekten, einschließlich [**wsacreateevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**wsacloseevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**wsasetevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**wsaresetevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)und [**wsawaitformultipleevents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) , werden direkt den systemeigenen Windows-Diensten zugeordnet und sind daher nicht in der SPI vorhanden.

Alle TCP/IP-spezifischen Funktionen zum Konvertieren und Auflösen von Namen in Windows Sockets 1,1, wie z. b. **getxbyy**, **WSAAsyncGetXbyY** und [**wsacancelasynkrequest**](/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest)sowie [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) , werden innerhalb der Ws2- \_32.dll in Bezug auf die neuen Funktionen zur Namensauflösung implementiert. Weitere Informationen finden Sie unter [kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md). Konvertierungs Funktionen wie [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) und [**inet \_ ntoia**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) werden innerhalb der Ws2- \_32.dll implementiert.

 

 
