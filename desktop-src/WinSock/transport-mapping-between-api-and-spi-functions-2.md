---
description: Die Winsock-Transport-SPI ähnelt der Winsock-API, da alle grundlegenden Socketfunktionen angezeigt werden.
ms.assetid: 37ef8a69-2aa0-4824-8ca9-4b84158086db
title: Transportzuordnung zwischen API- und SPI-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf4167353fa05c5656c588a9dff99c96564a5202ffdc4d21edf358c340634e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739940"
---
# <a name="transport-mapping-between-api-and-spi-functions"></a>Transportzuordnung zwischen API- und SPI-Funktionen

Die Winsock-Transport-SPI ähnelt der Winsock-API, da alle grundlegenden Socketfunktionen angezeigt werden. Wenn sowohl eine neue Version einer Winsock-Funktion als auch die ursprüngliche Version in der API vorhanden sind, wird nur die neue Version in der SPI angezeigt. Dies wird in der folgenden Liste veranschaulicht.

-   [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) und [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) sind beide [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) zugeordnet.
-   [**Accept-**](/windows/desktop/api/Winsock2/nf-winsock2-accept) und [**WSAAccept-Zuordnung**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) zu [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)
-   [**Socket-**](/windows/desktop/api/Winsock2/nf-winsock2-socket) und [**WSASocket-Zuordnung**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) zu [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)

Andere API-Funktionen, die in die erweiterten Versionen in SPI reduziert werden, umfassen Folgendes:

-   [**Senden**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**Sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)
-   [**Recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

Unterstützungsfunktionen wie [**htonl,**](/windows/desktop/api/winsock/nf-winsock-htonl) [**htons,**](/windows/desktop/api/winsock/nf-winsock-htons) [**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)und [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) werden im Ws2-32.dll implementiert \_ und nicht an Dienstanbieter übergeben. Dasselbe gilt für die WSA-Versionen dieser Funktionen.

Windows Sockets-Dienstanbieterenumeration und die blockierenden hookbezogenen Funktionen werden im Ws2-32.dll realisiert. Daher \_ werden [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [WSAIsBlocking,](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) [WSASetBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)und [WSAUnhookBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsaunhookblockinghook) nicht als SPI-Funktionen angezeigt.

Da Fehlercodes zusammen mit SPI-Funktionen zurückgegeben werden, sind Äquivalente von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) und [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) in der SPI nicht erforderlich.

Die Funktionen zum Bearbeiten und Warten von Ereignisobjekten, einschließlich [**WSACreateEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) [**WSACloseEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) [**WSASetEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent) [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)und [**WSAWaitForMultipleEvents,**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) werden nativen Windows Diensten direkt zugeordnet und sind daher im SPI nicht vorhanden.

Alle TCP/IP-spezifischen Namenskonvertierungs- und Auflösungsfunktionen in Windows Sockets 1.1 wie **GetXbyY,** **WSAAsyncGetXByY** und [**WSACancelAsyncRequest**](/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest)sowie [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) werden im Ws2-32.dll in Bezug auf die neuen Funktionen zur \_ Namensauflösung implementiert. Weitere Informationen finden Sie unter [Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI (Kompatible Namensauflösung für TCP/IP im Windows Sockets 1.1 SPI).](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md) Konvertierungsfunktionen wie [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) und [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) werden innerhalb der Ws2-32.dll \_ implementiert.

 

 
