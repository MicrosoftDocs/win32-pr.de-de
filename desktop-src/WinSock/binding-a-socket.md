---
description: Damit ein Server Clientverbindungen akzeptiert, muss er an eine Netzwerkadresse im System gebunden werden.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Binden eines Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc71ad25837a070074fefa2e3693c5546839ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348779"
---
# <a name="binding-a-socket"></a><span data-ttu-id="538c1-103">Binden eines Sockets</span><span class="sxs-lookup"><span data-stu-id="538c1-103">Binding a Socket</span></span>

<span data-ttu-id="538c1-104">Damit ein Server Clientverbindungen akzeptiert, muss er an eine Netzwerkadresse im System gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="538c1-104">For a server to accept client connections, it must be bound to a network address within the system.</span></span> <span data-ttu-id="538c1-105">Der folgende Code veranschaulicht, wie ein bereits erstelltes Socket an eine IP-Adresse und einen Port gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="538c1-105">The following code demonstrates how to bind a socket that has already been created to an IP address and port.</span></span> <span data-ttu-id="538c1-106">Client Anwendungen verwenden die IP-Adresse und den Port, um eine Verbindung mit dem Host Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="538c1-106">Client applications use the IP address and port to connect to the host network.</span></span>

## <a name="to-bind-a-socket"></a><span data-ttu-id="538c1-107">So binden Sie einen Socket</span><span class="sxs-lookup"><span data-stu-id="538c1-107">To bind a socket</span></span>

<span data-ttu-id="538c1-108">Die [**sockaddr**](sockaddr-2.md) -Struktur enthält Informationen bezüglich der Adressfamilie, der IP-Adresse und der Portnummer.</span><span class="sxs-lookup"><span data-stu-id="538c1-108">The [**sockaddr**](sockaddr-2.md) structure holds information regarding the address family, IP address, and port number.</span></span>

<span data-ttu-id="538c1-109">Aufrufen der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion und übergeben der erstellten **Socket** -und [**sockaddr**](sockaddr-2.md) -Struktur, die von der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion als Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="538c1-109">Call the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, passing the created **socket** and [**sockaddr**](sockaddr-2.md) structure returned from the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function as parameters.</span></span> <span data-ttu-id="538c1-110">Suchen Sie nach allgemeinen Fehlern.</span><span class="sxs-lookup"><span data-stu-id="538c1-110">Check for general errors.</span></span>


```C++
    // Setup the TCP listening socket
    iResult = bind( ListenSocket, result->ai_addr, (int)result->ai_addrlen);
    if (iResult == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
```



<span data-ttu-id="538c1-111">Nachdem die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion aufgerufen wurde, werden die von der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion zurückgegebenen Adressinformationen nicht mehr benötigt.</span><span class="sxs-lookup"><span data-stu-id="538c1-111">Once the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called, the address information returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is no longer needed.</span></span> <span data-ttu-id="538c1-112">Die [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) -Funktion wird aufgerufen, um den von der **getaddrinfo** -Funktion zugeordneten Arbeitsspeicher für diese Adressinformationen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="538c1-112">The [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) function is called to free the memory allocated by the **getaddrinfo** function for this address information.</span></span>


```C++
    freeaddrinfo(result);

```



<span data-ttu-id="538c1-113">Nächster Schritt: [lauschen an einem Socket](listening-on-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="538c1-113">Next Step: [Listening on a Socket](listening-on-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="538c1-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="538c1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="538c1-115">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="538c1-115">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="538c1-116">Winsock-Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="538c1-116">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="538c1-117">Erstellen eines Sockets für den Server</span><span class="sxs-lookup"><span data-stu-id="538c1-117">Creating a Socket for the Server</span></span>](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



