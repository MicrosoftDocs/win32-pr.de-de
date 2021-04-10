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
# <a name="disconnecting-the-client"></a><span data-ttu-id="47737-103">Trennen der Verbindung des Clients</span><span class="sxs-lookup"><span data-stu-id="47737-103">Disconnecting the Client</span></span>

<span data-ttu-id="47737-104">Sobald der Client das Senden und empfangen von Daten abgeschlossen hat, trennt der Client die Verbindung mit dem Server und beendet den Socket.</span><span class="sxs-lookup"><span data-stu-id="47737-104">Once the client is completed sending and receiving data, the client disconnects from the server and shutdowns the socket.</span></span>

<span data-ttu-id="47737-105">**So trennen Sie einen Socket und fahren ihn herunter**</span><span class="sxs-lookup"><span data-stu-id="47737-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="47737-106">Wenn der Client das Senden von Daten an den Server abgeschlossen hat, kann die Funktion zum [**herunter**](/windows/desktop/api/winsock/nf-winsock-shutdown) fahren aufgerufen werden, wobei SD \_ Send zum Herunterfahren der Sendeseite des Sockets aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="47737-106">When the client is done sending data to the server, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="47737-107">Dadurch kann der Server einige der Ressourcen für diesen Socket freigeben.</span><span class="sxs-lookup"><span data-stu-id="47737-107">This allows the server to release some of the resources for this socket.</span></span> <span data-ttu-id="47737-108">Die Client Anwendung kann weiterhin Daten auf dem Socket empfangen.</span><span class="sxs-lookup"><span data-stu-id="47737-108">The client application can still receive data on the socket.</span></span>
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

    

2.  <span data-ttu-id="47737-109">Wenn die Client Anwendung mit dem empfangen von Daten abgeschlossen ist, wird die [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion aufgerufen, um den Socket zu schließen.</span><span class="sxs-lookup"><span data-stu-id="47737-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="47737-110">Wenn die Client Anwendung mit der Windows Sockets-DLL abgeschlossen ist, wird die [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) -Funktion aufgerufen, um Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="47737-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a><span data-ttu-id="47737-111">Vervollständigen des Client Quellcodes</span><span class="sxs-lookup"><span data-stu-id="47737-111">Complete Client Source Code</span></span>

-   [<span data-ttu-id="47737-112">Vervollständigen von Client Code</span><span class="sxs-lookup"><span data-stu-id="47737-112">Complete Client Code</span></span>](complete-client-code.md)

## <a name="related-topics"></a><span data-ttu-id="47737-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47737-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47737-114">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="47737-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="47737-115">WinSock-Client Anwendung</span><span class="sxs-lookup"><span data-stu-id="47737-115">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="47737-116">Senden und empfangen von Daten auf dem Client</span><span class="sxs-lookup"><span data-stu-id="47737-116">Sending and Receiving Data on the Client</span></span>](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



