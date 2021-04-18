---
description: Damit ein Client in einem Netzwerk kommunizieren kann, muss eine Verbindung mit einem Server hergestellt werden.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Herstellen einer Verbindung mit einem Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa4461e1b00ba073320529d03e3b0fe32cdae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347171"
---
# <a name="connecting-to-a-socket"></a><span data-ttu-id="5cadc-103">Herstellen einer Verbindung mit einem Socket</span><span class="sxs-lookup"><span data-stu-id="5cadc-103">Connecting to a Socket</span></span>

<span data-ttu-id="5cadc-104">Damit ein Client in einem Netzwerk kommunizieren kann, muss eine Verbindung mit einem Server hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5cadc-104">For a client to communicate on a network, it must connect to a server.</span></span>

## <a name="to-connect-to-a-socket"></a><span data-ttu-id="5cadc-105">So verbinden Sie eine Verbindung mit einem Socket</span><span class="sxs-lookup"><span data-stu-id="5cadc-105">To connect to a socket</span></span>

<span data-ttu-id="5cadc-106">Ruft die [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) -Funktion auf und übergibt den erstellten Socket und die [**sockaddr**](sockaddr-2.md) -Struktur als Parameter.</span><span class="sxs-lookup"><span data-stu-id="5cadc-106">Call the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, passing the created socket and the [**sockaddr**](sockaddr-2.md) structure as parameters.</span></span> <span data-ttu-id="5cadc-107">Suchen Sie nach allgemeinen Fehlern.</span><span class="sxs-lookup"><span data-stu-id="5cadc-107">Check for general errors.</span></span>


```C++
// Connect to server.
iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    closesocket(ConnectSocket);
    ConnectSocket = INVALID_SOCKET;
}

// Should really try the next address returned by getaddrinfo
// if the connect call failed
// But for this simple example we just free the resources
// returned by getaddrinfo and print an error message

freeaddrinfo(result);

if (ConnectSocket == INVALID_SOCKET) {
    printf("Unable to connect to server!\n");
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="5cadc-108">Die [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion wird verwendet, um die Werte in der [**sockaddr**](sockaddr-2.md) -Struktur zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="5cadc-108">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure.</span></span> <span data-ttu-id="5cadc-109">In diesem Beispiel wird die erste IP-Adresse, die von der **getaddrinfo** -Funktion zurückgegeben wird, verwendet, um die **sockaddr** -Struktur anzugeben, die an die [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)-Klasse</span><span class="sxs-lookup"><span data-stu-id="5cadc-109">In this example, the first IP address returned by the **getaddrinfo** function is used to specify the **sockaddr** structure passed to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span></span> <span data-ttu-id="5cadc-110">Wenn der **Connect** -Befehl die erste IP-Adresse nicht erfüllt, versuchen Sie die nächste [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) -Struktur in der verknüpften Liste, die von der **getaddrinfo** -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5cadc-110">If the **connect** call fails to the first IP address, then try the next [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure in the linked list returned from the **getaddrinfo** function.</span></span>

<span data-ttu-id="5cadc-111">Die in der [**sockaddr**](sockaddr-2.md) -Struktur angegebenen Informationen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5cadc-111">The information specified in the [**sockaddr**](sockaddr-2.md) structure includes:</span></span>

-   <span data-ttu-id="5cadc-112">die IP-Adresse des Servers, mit dem der Client eine Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="5cadc-112">the IP address of the server that the client will try to connect to.</span></span>
-   <span data-ttu-id="5cadc-113">die Portnummer auf dem Server, mit der der Client eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="5cadc-113">the port number on the server that the client will connect to.</span></span> <span data-ttu-id="5cadc-114">Dieser Port wurde als Port 27015 angegeben, als der Client die [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="5cadc-114">This port was specified as port 27015 when the client called the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

<span data-ttu-id="5cadc-115">Nächster Schritt: [senden und empfangen von Daten auf dem Client](sending-and-receiving-data-on-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="5cadc-115">Next Step: [Sending and Receiving Data on the Client](sending-and-receiving-data-on-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cadc-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5cadc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cadc-117">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="5cadc-117">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="5cadc-118">WinSock-Client Anwendung</span><span class="sxs-lookup"><span data-stu-id="5cadc-118">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="5cadc-119">Erstellen eines Sockets für den Client</span><span class="sxs-lookup"><span data-stu-id="5cadc-119">Creating a Socket for the Client</span></span>](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
