---
description: Damit ein Server Clientverbindungen akzeptiert, muss er an eine Netzwerkadresse im System gebunden werden.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Binden eines Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc71ad25837a070074fefa2e3693c5546839ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348779"
---
# <a name="binding-a-socket"></a>Binden eines Sockets

Damit ein Server Clientverbindungen akzeptiert, muss er an eine Netzwerkadresse im System gebunden werden. Der folgende Code veranschaulicht, wie ein bereits erstelltes Socket an eine IP-Adresse und einen Port gebunden wird. Client Anwendungen verwenden die IP-Adresse und den Port, um eine Verbindung mit dem Host Netzwerk herzustellen.

## <a name="to-bind-a-socket"></a>So binden Sie einen Socket

Die [**sockaddr**](sockaddr-2.md) -Struktur enthält Informationen bezüglich der Adressfamilie, der IP-Adresse und der Portnummer.

Aufrufen der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion und übergeben der erstellten **Socket** -und [**sockaddr**](sockaddr-2.md) -Struktur, die von der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion als Parameter zurückgegeben wird. Suchen Sie nach allgemeinen Fehlern.


```C++
    // Setup the TCP listening socket
    iResult = bind( ListenSocket, result->ai_addr, (int)result->ai_addrlen);
    if (iResult == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
```



Nachdem die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion aufgerufen wurde, werden die von der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion zurückgegebenen Adressinformationen nicht mehr benötigt. Die [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) -Funktion wird aufgerufen, um den von der **getaddrinfo** -Funktion zugeordneten Arbeitsspeicher für diese Adressinformationen freizugeben.


```C++
    freeaddrinfo(result);

```



Nächster Schritt: [lauschen an einem Socket](listening-on-a-socket.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock-Server Anwendung](winsock-server-application.md)
</dt> <dt>

[Erstellen eines Sockets für den Server](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



