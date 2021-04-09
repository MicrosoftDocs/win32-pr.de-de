---
description: Nach der Initialisierung muss ein Socket-Objekt für die Verwendung durch den Client instanziiert werden.
ms.assetid: 088a79ef-b430-4860-8edc-902a1a03ed0d
title: Erstellen eines Sockets für den Client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64467406f13ed40bdbe134e7796dd2aa5ff7bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862576"
---
# <a name="creating-a-socket-for-the-client"></a>Erstellen eines Sockets für den Client

Nach der Initialisierung muss ein **Socket** -Objekt für die Verwendung durch den Client instanziiert werden.

**So erstellen Sie einen Socket**

1.  Deklarieren Sie ein [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) -Objekt, das eine [**sockaddr**](sockaddr-2.md) -Struktur enthält, und initialisieren Sie diese Werte. Für diese Anwendung ist die Internet Adressfamilie nicht angegeben, sodass entweder eine IPv6-oder eine IPv4-Adresse zurückgegeben werden kann. Die Anwendung fordert den socketyp als Stream-Socket für das TCP-Protokoll an.
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  Aufrufen der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion anfordern der IP-Adresse für den Servernamen, der in der Befehlszeile weitergegeben wurde. Der TCP-Port auf dem Server, mit dem der Client eine Verbindung herstellt, wird \_ in diesem Beispiel über den Standardport 27015 als definiert. Die **getaddrinfo** -Funktion gibt ihren Wert als Ganzzahl zurück, die auf Fehler geprüft wird.
    ```C++
    #define DEFAULT_PORT "27015"

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

3.  Erstellen Sie ein **Socketobjekt** mit dem Namen connectsocket.
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  Ruft die [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -Funktion auf und gibt ihren Wert an die connectsocket-Variable zurück. Verwenden Sie für diese Anwendung die erste IP-Adresse, die vom [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Befehl zurückgegeben wird, der mit der Adressfamilie, dem Sockettyp und dem Protokoll übereinstimmt, die im *Hints* -Parameter angegeben sind In diesem Beispiel wurde ein TCP-streamingsocket mit einem Sockettyp von Sock \_ Stream und einem Protokoll von ipproto \_ TCP angegeben. Die Adressfamilie wurde nicht angegeben (AF \_ unspec), sodass die zurückgegebene IP-Adresse entweder eine IPv6-oder IPv4-Adresse für den Server sein könnte.

    Wenn die Client Anwendung nur über IPv6 oder IPv4 eine Verbindung herstellen möchte, muss die Adressfamilie auf AF \_ inet6 for IPv6 oder AF \_ inet for IPv4 im *Hints* -Parameter festgelegt werden.

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  Überprüfen Sie auf Fehler, um sicherzustellen, dass der Socket ein gültiger Socket ist.
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

Die an die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) über gebenden Parameter können für verschiedene Implementierungen geändert werden.

Die Fehlererkennung ist ein wichtiger Bestandteil des erfolgreichen Netzwerk Codes. Wenn der [**socketbefehl**](/windows/desktop/api/Winsock2/nf-winsock2-socket) fehlschlägt, wird ein ungültiger Socket zurückgegeben \_ . Die **if** -Anweisung im vorherigen Code wird verwendet, um Fehler abzufangen, die möglicherweise beim Erstellen des Sockets aufgetreten sind. [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt eine Fehlernummer zurück, die dem zuletzt aufgetretenen Fehler zugeordnet ist.

> [!Note]  
> Abhängig von der Anwendung ist möglicherweise eine umfangreichere Fehlerüberprüfung erforderlich.
>
> Wenn Sie z. b. *hints.ai_family* auf **AF_UNSPEC** festlegen, kann der Connect-Befehl fehlschlagen. Wenn dies der Fall ist, verwenden Sie stattdessen einen bestimmten IPv4-(**AF_INET**) oder IPv6-Wert (**AF_INET6**).

[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) wird verwendet, um die Verwendung der ws2 32-dll zu beenden \_ .

Nächster Schritt: [Herstellen einer Verbindung mit einem Socket](connecting-to-a-socket.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Initialisieren von Winsock](initializing-winsock.md)
</dt> <dt>

[WinSock-Client Anwendung](winsock-client-application.md)
</dt> </dl>

 

 
