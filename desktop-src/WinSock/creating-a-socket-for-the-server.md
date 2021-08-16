---
description: Nach der Initialisierung muss ein SOCKET-Objekt für die Verwendung durch den Server instanziiert werden.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Erstellen eines Sockets für den Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e71d6ee0117153b00a9ab77c53bd7555aa031b3fa9d1f7a425ea9aaf0e358f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322200"
---
# <a name="creating-a-socket-for-the-server"></a>Erstellen eines Sockets für den Server

Nach der Initialisierung muss ein **SOCKET-Objekt** für die Verwendung durch den Server instanziiert werden.

**So erstellen Sie einen Socket für den Server**

1.  Die [**getaddrinfo-Funktion**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) wird verwendet, um die Werte in der [**sockaddr-Struktur**](sockaddr-2.md) zu bestimmen:

    -   **AF \_ INET** wird verwendet, um die IPv4-Adressfamilie anzugeben.
    -   **SOCK \_ STREAM** wird verwendet, um einen Streamsocket anzugeben.
    -   **IPPROTO \_ TCP** wird verwendet, um das TCP-Protokoll anzugeben.
    -   **KI \_ Das PASSIVE-Flag** gibt an, dass der Aufrufer die zurückgegebene Socketadressstruktur in einem Aufruf der [**Bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) verwenden möchte. Wenn das **AI \_ PASSIVE-Flag** festgelegt ist und der *Nodename-Parameter* für die [**getaddrinfo-Funktion**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) ein **NULL-Zeiger** ist, wird der IP-Adressteil der Socketadressstruktur für IPv4-Adressen auf **INADDR \_ ANY** oder für IPv6-Adressen auf **IN6ADDR \_ ANY \_ INIT** festgelegt.
    -   27015 ist die Portnummer, die dem Server zugeordnet ist, mit dem der Client eine Verbindung herstellt.

    Die [**addrinfo-Struktur**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) wird von der [**getaddrinfo-Funktion**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) verwendet.

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Erstellen Sie ein **SOCKET-Objekt** namens ListenSocket, damit der Server auf Clientverbindungen lauscht.
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  Rufen Sie die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) auf, und geben Sie ihren Wert an die ListenSocket-Variable zurück. Verwenden Sie für diese Serveranwendung die erste IP-Adresse, die durch den Aufruf von [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) zurückgegeben wird, die mit der Adressfamilie, dem Sockettyp und dem Protokoll übereinstimmt, die im *Hints-Parameter* angegeben sind. In diesem Beispiel wurde ein TCP-Streamsocket für IPv4 mit einer Adressfamilie von IPv4, einem Sockettyp von SOCK \_ STREAM und einem Protokoll von IPPROTO TCP \_ angefordert. Daher wird eine IPv4-Adresse für listenSocket angefordert.

    Wenn die Serveranwendung IPv6 abhören möchte, muss die Adressfamilie \_ im *Hints-Parameter* auf AF INET6 festgelegt werden. Wenn ein Server sowohl auf IPv6 als auch auf IPv4 lauschen möchte, müssen zwei Listensockets erstellt werden, einer für IPv6 und einer für IPv4. Diese beiden Sockets müssen von der Anwendung separat behandelt werden.

    Windows Vista und höher bieten die Möglichkeit, einen einzelnen IPv6-Socket zu erstellen, der in den Dual Stack-Modus versetzt wird, um sowohl auf IPv6 als auch auf IPv4 zu lauschen. Weitere Informationen zu diesem Feature finden Sie unter [Dual-Stack-Sockets.](dual-stack-sockets.md)

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  Überprüfen Sie auf Fehler, um sicherzustellen, dass der Socket ein gültiger Socket ist.
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

Nächster Schritt: [Binden eines Sockets](binding-a-socket.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Initialisieren von Winsock](initializing-winsock.md)
</dt> <dt>

[Winsock-Serveranwendung](winsock-server-application.md)
</dt> </dl>

 

 
