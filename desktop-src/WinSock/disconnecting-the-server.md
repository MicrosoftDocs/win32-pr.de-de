---
description: Nachdem der Server den Empfang von Daten vom Client abgeschlossen und die Daten an den Client zurückgesendet hat, trennt der Server die Verbindung mit dem Client und beendet den Socket.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Trennen der Verbindung mit dem Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6abf7754da39a891b3d29c69f6c835706debd36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862572"
---
# <a name="disconnecting-the-server"></a>Trennen der Verbindung mit dem Server

Nachdem der Server den Empfang von Daten vom Client abgeschlossen und die Daten an den Client zurückgesendet hat, trennt der Server die Verbindung mit dem Client und beendet den Socket.

**So trennen Sie einen Socket und fahren ihn herunter**

1.  Wenn der Server das Senden von Daten an den Client abgeschlossen hat, kann die Funktion zum [**herunter**](/windows/desktop/api/winsock/nf-winsock-shutdown) fahren aufgerufen werden, wobei SD \_ Send zum Herunterfahren der Sendeseite des Sockets aufgerufen wird. Dadurch kann der Client einige der Ressourcen für diesen Socket freigeben. Die Serveranwendung kann weiterhin Daten auf dem Socket empfangen.
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ClientSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Wenn die Client Anwendung mit dem empfangen von Daten abgeschlossen ist, wird die [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion aufgerufen, um den Socket zu schließen.

    Wenn die Client Anwendung mit der Windows Sockets-DLL abgeschlossen ist, wird die [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) -Funktion aufgerufen, um Ressourcen freizugeben.

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a>Vervollständigen des Server Quellcodes

-   [Vervollständigen des Server Codes](complete-server-code.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock-Server Anwendung](winsock-server-application.md)
</dt> <dt>

[Empfangen und Senden von Daten auf dem Server](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[Ausführen des WinSock-Client-und Server Code Beispiels](finished-server-and-client-code.md)
</dt> </dl>

 

 



