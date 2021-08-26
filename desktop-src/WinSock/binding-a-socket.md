---
description: Damit ein Server Clientverbindungen akzeptiert, muss er an eine Netzwerkadresse im System gebunden werden.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Binden eines Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9e745395209228584ea5535864cca57e30494b2e30bfff02fe2abc527ed5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996919"
---
# <a name="binding-a-socket"></a>Binden eines Sockets

Damit ein Server Clientverbindungen akzeptiert, muss er an eine Netzwerkadresse im System gebunden werden. Der folgende Code veranschaulicht, wie sie einen Socket, der bereits erstellt wurde, an eine IP-Adresse und einen Port binden. Clientanwendungen verwenden die IP-Adresse und den Port, um eine Verbindung mit dem Hostnetzwerk herzustellen.

## <a name="to-bind-a-socket"></a>So binden Sie einen Socket

Die [**Sockaddr-Struktur**](sockaddr-2.md) enthält Informationen zur Adressfamilie, ip-Adresse und Portnummer.

Rufen Sie die [**Bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) auf, und übergeben Sie den erstellten **Socket** und die [**sockaddr-Struktur,**](sockaddr-2.md) die von der [**getaddrinfo-Funktion**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) zurückgegeben werden, als Parameter. Überprüfen Sie, ob allgemeine Fehler vorliegen.


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



Nachdem die [**Bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) aufgerufen wurde, werden die von der [**getaddrinfo-Funktion zurückgegebenen**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Adressinformationen nicht mehr benötigt. Die [**freeaddrinfo-Funktion**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) wird aufgerufen, um den von der **getaddrinfo-Funktion belegten** Arbeitsspeicher für diese Adressinformationen freizugeben.


```C++
    freeaddrinfo(result);

```



Nächster Schritt: [Lauschen an einem Socket](listening-on-a-socket.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock-Serveranwendung](winsock-server-application.md)
</dt> <dt>

[Erstellen eines Sockets für den Server](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



