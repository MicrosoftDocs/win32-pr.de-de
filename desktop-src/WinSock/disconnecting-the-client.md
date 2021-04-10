---
description: Sobald der Client das Senden und empfangen von Daten abgeschlossen hat, trennt der Client die Verbindung mit dem Server und beendet den Socket.
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: Trennen der Verbindung des Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ac34036cc92386d7d68b3d5debda4d37a92ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343529"
---
# <a name="disconnecting-the-client"></a>Trennen der Verbindung des Clients

Sobald der Client das Senden und empfangen von Daten abgeschlossen hat, trennt der Client die Verbindung mit dem Server und beendet den Socket.

**So trennen Sie einen Socket und fahren ihn herunter**

1.  Wenn der Client das Senden von Daten an den Server abgeschlossen hat, kann die Funktion zum [**herunter**](/windows/desktop/api/winsock/nf-winsock-shutdown) fahren aufgerufen werden, wobei SD \_ Send zum Herunterfahren der Sendeseite des Sockets aufgerufen wird. Dadurch kann der Server einige der Ressourcen für diesen Socket freigeben. Die Client Anwendung kann weiterhin Daten auf dem Socket empfangen.
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ConnectSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Wenn die Client Anwendung mit dem empfangen von Daten abgeschlossen ist, wird die [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion aufgerufen, um den Socket zu schließen.

    Wenn die Client Anwendung mit der Windows Sockets-DLL abgeschlossen ist, wird die [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) -Funktion aufgerufen, um Ressourcen freizugeben.

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a>Vervollständigen des Client Quellcodes

-   [Vervollständigen von Client Code](complete-client-code.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[WinSock-Client Anwendung](winsock-client-application.md)
</dt> <dt>

[Senden und empfangen von Daten auf dem Client](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



