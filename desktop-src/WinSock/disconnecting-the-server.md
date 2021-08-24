---
description: Sobald der Server den Empfang von Daten vom Client und das Zurücksenden von Daten an den Client abgeschlossen hat, trennt der Server die Verbindung mit dem Client und beendet den Socket.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Trennen des Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f644b8727898a9d77ab5aa5fb10b0a0ae5b58cdf88a3beb1b9642215d142b6b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898360"
---
# <a name="disconnecting-the-server"></a>Trennen des Servers

Sobald der Server den Empfang von Daten vom Client und das Zurücksenden von Daten an den Client abgeschlossen hat, trennt der Server die Verbindung mit dem Client und beendet den Socket.

**So trennen Sie einen Socket und fahren es herunter**

1.  Wenn der Server mit dem Senden von Daten an den Client fertig ist, kann die Funktion zum [**Herunterfahren**](/windows/desktop/api/winsock/nf-winsock-shutdown) aufgerufen werden, die SD SEND \_ angibt, um die sendende Seite des Sockets herunterzufahren. Dadurch kann der Client einige der Ressourcen für diesen Socket freigeben. Die Serveranwendung kann weiterhin Daten auf dem Socket empfangen.
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

    

2.  Wenn die Clientanwendung mit dem Empfangen von Daten fertig ist, wird die [**Closesocket-Funktion**](/windows/desktop/api/winsock/nf-winsock-closesocket) aufgerufen, um den Socket zu schließen.

    Wenn die Clientanwendung mithilfe der Windows Sockets-DLL abgeschlossen ist, wird die [**WSACleanup-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) aufgerufen, um Ressourcen freizugeben.

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a>Vollständiger Serverquellcode

-   [Servercode vervollständigen](complete-server-code.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock-Serveranwendung](winsock-server-application.md)
</dt> <dt>

[Empfangen und Senden von Daten auf dem Server](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[Ausführen des Winsock-Client- und Servercodebeispiels](finished-server-and-client-code.md)
</dt> </dl>

 

 



