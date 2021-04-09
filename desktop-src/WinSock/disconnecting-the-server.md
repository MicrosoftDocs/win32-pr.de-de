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
# <a name="disconnecting-the-server"></a><span data-ttu-id="c1cbb-103">Trennen der Verbindung mit dem Server</span><span class="sxs-lookup"><span data-stu-id="c1cbb-103">Disconnecting the Server</span></span>

<span data-ttu-id="c1cbb-104">Nachdem der Server den Empfang von Daten vom Client abgeschlossen und die Daten an den Client zurückgesendet hat, trennt der Server die Verbindung mit dem Client und beendet den Socket.</span><span class="sxs-lookup"><span data-stu-id="c1cbb-104">Once the server is completed receiving data from the client and sending data back to the client, the server disconnects from the client and shutdowns the socket.</span></span>

<span data-ttu-id="c1cbb-105">**So trennen Sie einen Socket und fahren ihn herunter**</span><span class="sxs-lookup"><span data-stu-id="c1cbb-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="c1cbb-106">Wenn der Server das Senden von Daten an den Client abgeschlossen hat, kann die Funktion zum [**herunter**](/windows/desktop/api/winsock/nf-winsock-shutdown) fahren aufgerufen werden, wobei SD \_ Send zum Herunterfahren der Sendeseite des Sockets aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c1cbb-106">When the server is done sending data to the client, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="c1cbb-107">Dadurch kann der Client einige der Ressourcen für diesen Socket freigeben.</span><span class="sxs-lookup"><span data-stu-id="c1cbb-107">This allows the client to release some of the resources for this socket.</span></span> <span data-ttu-id="c1cbb-108">Die Serveranwendung kann weiterhin Daten auf dem Socket empfangen.</span><span class="sxs-lookup"><span data-stu-id="c1cbb-108">The server application can still receive data on the socket.</span></span>
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

    

2.  <span data-ttu-id="c1cbb-109">Wenn die Client Anwendung mit dem empfangen von Daten abgeschlossen ist, wird die [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion aufgerufen, um den Socket zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c1cbb-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="c1cbb-110">Wenn die Client Anwendung mit der Windows Sockets-DLL abgeschlossen ist, wird die [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) -Funktion aufgerufen, um Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c1cbb-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a><span data-ttu-id="c1cbb-111">Vervollständigen des Server Quellcodes</span><span class="sxs-lookup"><span data-stu-id="c1cbb-111">Complete Server Source Code</span></span>

-   [<span data-ttu-id="c1cbb-112">Vervollständigen des Server Codes</span><span class="sxs-lookup"><span data-stu-id="c1cbb-112">Complete Server Code</span></span>](complete-server-code.md)

## <a name="related-topics"></a><span data-ttu-id="c1cbb-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1cbb-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1cbb-114">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="c1cbb-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="c1cbb-115">Winsock-Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="c1cbb-115">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="c1cbb-116">Empfangen und Senden von Daten auf dem Server</span><span class="sxs-lookup"><span data-stu-id="c1cbb-116">Receiving and Sending Data on the Server</span></span>](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[<span data-ttu-id="c1cbb-117">Ausführen des WinSock-Client-und Server Code Beispiels</span><span class="sxs-lookup"><span data-stu-id="c1cbb-117">Running the Winsock Client and Server Code Sample</span></span>](finished-server-and-client-code.md)
</dt> </dl>

 

 



