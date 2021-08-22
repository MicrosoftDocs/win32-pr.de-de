---
description: Damit ein Client in einem Netzwerk kommunizieren kann, muss er eine Verbindung mit einem Server herstellen.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Herstellen einer Verbindung mit einem Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a5a81c18089bdf5f35e96aa55a8ede87dc88598a98acd3bc5ab8338afb1208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132673"
---
# <a name="connecting-to-a-socket"></a>Herstellen einer Verbindung mit einem Socket

Damit ein Client in einem Netzwerk kommunizieren kann, muss er eine Verbindung mit einem Server herstellen.

## <a name="to-connect-to-a-socket"></a>So stellen Sie eine Verbindung mit einem Socket her

Rufen Sie die [**connect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-connect) auf, und übergeben Sie den erstellten Socket und die [**Sockaddr-Struktur**](sockaddr-2.md) als Parameter. Suchen Sie nach allgemeinen Fehlern.


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



Die [**getaddrinfo-Funktion**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) wird verwendet, um die Werte in der [**sockaddr-Struktur**](sockaddr-2.md) zu bestimmen. In diesem Beispiel wird die erste IP-Adresse, die von der **getaddrinfo-Funktion** zurückgegeben wird, verwendet, um die **sockaddr-Struktur** anzugeben, die an die [**Verbindung**](/windows/desktop/api/Winsock2/nf-winsock2-connect)übergeben wird. Wenn beim **Verbindungsaufruf** ein Fehler bei der ersten IP-Adresse auftritt, versuchen Sie es mit der nächsten [**addrinfo-Struktur**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) in der verknüpften Liste, die von der **getaddrinfo-Funktion** zurückgegeben wird.

Die in der [**Sockaddr-Struktur angegebenen**](sockaddr-2.md) Informationen umfassen Folgendes:

-   die IP-Adresse des Servers, mit dem der Client versucht, eine Verbindung herzustellen.
-   Die Portnummer auf dem Server, mit dem der Client eine Verbindung herstellt. Dieser Port wurde als Port 27015 angegeben, als der Client die [**getaddrinfo-Funktion**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) aufgerufen hat.

Nächster Schritt: [Senden und Empfangen von Daten auf dem Client](sending-and-receiving-data-on-the-client.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock-Clientanwendung](winsock-client-application.md)
</dt> <dt>

[Erstellen eines Sockets für den Client](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
