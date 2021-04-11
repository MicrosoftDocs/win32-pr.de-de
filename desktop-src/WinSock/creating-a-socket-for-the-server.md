---
description: Nach der Initialisierung muss ein Socket-Objekt für die Verwendung durch den Server instanziiert werden.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Erstellen eines Sockets für den Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3fb00cb8b1155f4d26d94c9a88328256effe23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129205"
---
# <a name="creating-a-socket-for-the-server"></a>Erstellen eines Sockets für den Server

Nach der Initialisierung muss ein **Socket** -Objekt für die Verwendung durch den Server instanziiert werden.

**So erstellen Sie einen Socket für den Server**

1.  Die [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion wird verwendet, um die Werte in der [**sockaddr**](sockaddr-2.md) -Struktur zu ermitteln:

    -   **AF \_ INET** wird verwendet, um die IPv4-Adressfamilie anzugeben.
    -   **Sock \_ Stream** wird zum Angeben eines Stream-Sockets verwendet.
    -   **Ipproto \_ TCP** wird zum Angeben des TCP-Protokolls verwendet.
    -   **AI \_ Passives** Flag gibt an, dass der Aufrufer die zurückgegebene socketadressstruktur in einem Aufruf der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion verwenden soll. Wenn das Flag für das **\_ passive AI** -Flag festgelegt ist und der *NodeName* -Parameter der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion ein **null** -Zeiger ist, wird der IP-Adress Teil der **socketadressstruktur auf inaddr \_ any** für IPv4-Adressen oder **IN6ADDR \_ Any \_ Init** für IPv6-Adressen festgelegt.
    -   27015 ist die Portnummer, die dem Server zugeordnet ist, mit dem der Client eine Verbindung herstellt.

    Die [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) -Struktur wird von der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion verwendet.

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

    

2.  Erstellen Sie ein **Socketobjekt** mit dem Namen Listensocket, damit der Server auf Clientverbindungen lauschen muss.
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  Ruft die [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -Funktion auf und gibt ihren Wert an die Listensocket-Variable zurück. Verwenden Sie für diese Serveranwendung die erste IP-Adresse, die vom [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Befehl zurückgegeben wird, der mit der Adressfamilie, dem socketyp und dem Protokoll übereinstimmt, die im *Hints* -Parameter angegeben sind In diesem Beispiel wurde ein TCP-Datenstrom Socket für IPv4 mit der Adressfamilie IPv4 angefordert, einem Sockettyp von Sock \_ Stream und einem Protokoll von ipproto \_ TCP. Daher wird eine IPv4-Adresse für den Listensocket angefordert.

    Wenn die Serveranwendung IPv6 überwachen möchte, muss die Adressfamilie im hints-Parameter auf AF inet6 festgelegt werden \_ .  Wenn ein Server sowohl IPv6 als auch IPv4 lauschen möchte, müssen zwei lausch Sockets erstellt werden: eine für IPv6 und eine für IPv4. Diese beiden Sockets müssen separat von der Anwendung behandelt werden.

    Windows Vista und höher bieten die Möglichkeit, einen einzelnen IPv6-Socket zu erstellen, der in den Dual Stack-Modus versetzt wird, um sowohl IPv6 als auch IPv4 zu überwachen. Weitere Informationen zu diesem Feature finden Sie unter [Dual-Stack-Sockets](dual-stack-sockets.md).

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

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Initialisieren von Winsock](initializing-winsock.md)
</dt> <dt>

[Winsock-Server Anwendung](winsock-server-application.md)
</dt> </dl>

 

 
