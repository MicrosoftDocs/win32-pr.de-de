---
description: Sobald der Socket eine Verbindung abhört, muss das Programm Verbindungsanforderungen für diesen Socket verarbeiten.
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: Akzeptieren einer Verbindung (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e066b53c22dd9964ad44dc8d67c15969641362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359835"
---
# <a name="accepting-a-connection-windows-sockets-2"></a>Akzeptieren einer Verbindung (Windows Sockets 2)

Sobald der Socket eine Verbindung abhört, muss das Programm Verbindungsanforderungen für diesen Socket verarbeiten.

**So akzeptieren Sie eine Verbindung für einen Socket**

1.  Erstellen Sie ein temporäres **Socketobjekt** namens Clientsocket für die Annahme von Verbindungen von Clients.
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  Normalerweise ist eine Serveranwendung so konzipiert, dass Sie auf Verbindungen von mehreren Clients lauscht. Bei Hochleistungsservern werden häufig mehrere Threads verwendet, um mehrere Clientverbindungen zu verarbeiten.

    Es gibt mehrere unterschiedliche Programmiertechniken, die Winsock verwenden, die zum lauschen auf mehrere Clientverbindungen verwendet werden können. Ein Programmierverfahren besteht darin, eine kontinuierliche Schleife zu erstellen, die mithilfe der Funktion " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) " die Verbindungsanforderungen überprüft (siehe [lauschen auf einem Socket](listening-on-a-socket.md)). Wenn eine Verbindungsanforderung auftritt, ruft die Anwendung die [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)-, [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex)-oder [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Funktion auf und übergibt die Arbeit an einen anderen Thread, um die Anforderung zu verarbeiten. Es sind mehrere andere Programmiertechniken möglich.

    Beachten Sie, dass dieses grundlegende Beispiel sehr einfach ist und nicht mehrere Threads verwendet. Das Beispiel lauscht auch nur auf eine einzelne Verbindung.

    ```C++
    
    ClientSocket = INVALID_SOCKET;

    // Accept a client socket
    ClientSocket = accept(ListenSocket, NULL, NULL);
    if (ClientSocket == INVALID_SOCKET) {
        printf("accept failed: %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
     
    
    ```

    

3.  Wenn die Client Verbindung akzeptiert wurde, übergibt eine Serveranwendung normalerweise den akzeptierten Client Socket (die Clientsocket-Variable im obigen Beispielcode) an einen Arbeits Thread oder einen e/a-Abschlussport und nimmt weiterhin weitere Verbindungen an. In diesem einfachen Beispiel wird der Server mit dem nächsten Schritt fortgesetzt.

    Es gibt eine Reihe von anderen Programmiertechniken, die verwendet werden können, um auf mehrere Verbindungen zu lauschen und diese zu akzeptieren. Dazu gehört die Verwendung der [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Funktionen. Beispiele für einige dieser verschiedenen Programmierverfahren werden in den [erweiterten Winsock-Beispielen](getting-started-with-winsock.md) veranschaulicht, die im Microsoft Windows Software Development Kit (SDK) enthalten sind.

    > [!Note]  
    > Auf UNIX-Systemen bestand eine gängige Programmiermethode für Server darin, dass eine Anwendung auf Verbindungen lauschen konnte. Wenn eine Verbindung akzeptiert wurde, ruft der übergeordnete Prozess die **Verzweigungs** Funktion auf, um einen neuen untergeordneten Prozess zum Verarbeiten der Client Verbindung zu erstellen, der den Socket vom übergeordneten Element erbt. Diese Programmiertechnik wird unter Windows nicht unterstützt, da die **Fork** -Funktion nicht unterstützt wird. Dieses Verfahren eignet sich in der Regel nicht für Hochleistungsserver, da die für die Erstellung eines neuen Prozesses benötigten Ressourcen wesentlich größer sind als die für einen Thread benötigten Ressourcen.

     

Nächster Schritt: [empfangen und Senden von Daten auf dem Server](receiving-and-sending-data-on-the-server.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock-Server Anwendung](winsock-server-application.md)
</dt> <dt>

[Lauschen an einem Socket](listening-on-a-socket.md)
</dt> </dl>

 

 
