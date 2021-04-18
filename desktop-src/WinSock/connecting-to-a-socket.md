---
description: Damit ein Client in einem Netzwerk kommunizieren kann, muss eine Verbindung mit einem Server hergestellt werden.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Herstellen einer Verbindung mit einem Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa4461e1b00ba073320529d03e3b0fe32cdae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347171"
---
# <a name="connecting-to-a-socket"></a>Herstellen einer Verbindung mit einem Socket

Damit ein Client in einem Netzwerk kommunizieren kann, muss eine Verbindung mit einem Server hergestellt werden.

## <a name="to-connect-to-a-socket"></a>So verbinden Sie eine Verbindung mit einem Socket

Ruft die [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) -Funktion auf und übergibt den erstellten Socket und die [**sockaddr**](sockaddr-2.md) -Struktur als Parameter. Suchen Sie nach allgemeinen Fehlern.


```C++
// Connect to server.
iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    closesocket(ConnectSocket);
    ConnectSocket = INVALID_SOCKET;
}

// Should really try the next address returned by getaddrinfo
// if the connect call failed
// But for this simple example we just free the resources
// returned by getaddrinfo and print an error message

freeaddrinfo(result);

if (ConnectSocket == INVALID_SOCKET) {
    printf("Unable to connect to server!\n");
    WSACleanup();
    return 1;
}
```



Die [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion wird verwendet, um die Werte in der [**sockaddr**](sockaddr-2.md) -Struktur zu bestimmen. In diesem Beispiel wird die erste IP-Adresse, die von der **getaddrinfo** -Funktion zurückgegeben wird, verwendet, um die **sockaddr** -Struktur anzugeben, die an die [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)-Klasse Wenn der **Connect** -Befehl die erste IP-Adresse nicht erfüllt, versuchen Sie die nächste [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) -Struktur in der verknüpften Liste, die von der **getaddrinfo** -Funktion zurückgegeben wird.

Die in der [**sockaddr**](sockaddr-2.md) -Struktur angegebenen Informationen umfassen Folgendes:

-   die IP-Adresse des Servers, mit dem der Client eine Verbindung herstellen soll.
-   die Portnummer auf dem Server, mit der der Client eine Verbindung herstellt. Dieser Port wurde als Port 27015 angegeben, als der Client die [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion aufgerufen hat.

Nächster Schritt: [senden und empfangen von Daten auf dem Client](sending-and-receiving-data-on-the-client.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[WinSock-Client Anwendung](winsock-client-application.md)
</dt> <dt>

[Erstellen eines Sockets für den Client](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
