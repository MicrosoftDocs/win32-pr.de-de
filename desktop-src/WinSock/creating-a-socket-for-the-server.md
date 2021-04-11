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
# <a name="creating-a-socket-for-the-server"></a><span data-ttu-id="e0c3e-103">Erstellen eines Sockets für den Server</span><span class="sxs-lookup"><span data-stu-id="e0c3e-103">Creating a Socket for the Server</span></span>

<span data-ttu-id="e0c3e-104">Nach der Initialisierung muss ein **Socket** -Objekt für die Verwendung durch den Server instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-104">After initialization, a **SOCKET** object must be instantiated for use by the server.</span></span>

<span data-ttu-id="e0c3e-105">**So erstellen Sie einen Socket für den Server**</span><span class="sxs-lookup"><span data-stu-id="e0c3e-105">**To create a socket for the server**</span></span>

1.  <span data-ttu-id="e0c3e-106">Die [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion wird verwendet, um die Werte in der [**sockaddr**](sockaddr-2.md) -Struktur zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="e0c3e-106">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure:</span></span>

    -   <span data-ttu-id="e0c3e-107">**AF \_ INET** wird verwendet, um die IPv4-Adressfamilie anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-107">**AF\_INET** is used to specify the IPv4 address family.</span></span>
    -   <span data-ttu-id="e0c3e-108">**Sock \_ Stream** wird zum Angeben eines Stream-Sockets verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-108">**SOCK\_STREAM** is used to specify a stream socket.</span></span>
    -   <span data-ttu-id="e0c3e-109">**Ipproto \_ TCP** wird zum Angeben des TCP-Protokolls verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-109">**IPPROTO\_TCP** is used to specify the TCP protocol .</span></span>
    -   <span data-ttu-id="e0c3e-110">**AI \_ Passives** Flag gibt an, dass der Aufrufer die zurückgegebene socketadressstruktur in einem Aufruf der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-110">**AI\_PASSIVE** flag indicates the caller intends to use the returned socket address structure in a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function.</span></span> <span data-ttu-id="e0c3e-111">Wenn das Flag für das **\_ passive AI** -Flag festgelegt ist und der *NodeName* -Parameter der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion ein **null** -Zeiger ist, wird der IP-Adress Teil der **socketadressstruktur auf inaddr \_ any** für IPv4-Adressen oder **IN6ADDR \_ Any \_ Init** für IPv6-Adressen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-111">When the **AI\_PASSIVE** flag is set and *nodename* parameter to the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is a **NULL** pointer, the IP address portion of the socket address structure is set to **INADDR\_ANY** for IPv4 addresses or **IN6ADDR\_ANY\_INIT** for IPv6 addresses.</span></span>
    -   <span data-ttu-id="e0c3e-112">27015 ist die Portnummer, die dem Server zugeordnet ist, mit dem der Client eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-112">27015 is the port number associated with the server that the client will connect to.</span></span>

    <span data-ttu-id="e0c3e-113">Die [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) -Struktur wird von der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-113">The [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure is used by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

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

    

2.  <span data-ttu-id="e0c3e-114">Erstellen Sie ein **Socketobjekt** mit dem Namen Listensocket, damit der Server auf Clientverbindungen lauschen muss.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-114">Create a **SOCKET** object called ListenSocket for the server to listen for client connections.</span></span>
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  <span data-ttu-id="e0c3e-115">Ruft die [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -Funktion auf und gibt ihren Wert an die Listensocket-Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-115">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ListenSocket variable.</span></span> <span data-ttu-id="e0c3e-116">Verwenden Sie für diese Serveranwendung die erste IP-Adresse, die vom [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Befehl zurückgegeben wird, der mit der Adressfamilie, dem socketyp und dem Protokoll übereinstimmt, die im *Hints* -Parameter angegeben sind</span><span class="sxs-lookup"><span data-stu-id="e0c3e-116">For this server application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="e0c3e-117">In diesem Beispiel wurde ein TCP-Datenstrom Socket für IPv4 mit der Adressfamilie IPv4 angefordert, einem Sockettyp von Sock \_ Stream und einem Protokoll von ipproto \_ TCP.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-117">In this example, a TCP stream socket for IPv4 was requested with an address family of IPv4, a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="e0c3e-118">Daher wird eine IPv4-Adresse für den Listensocket angefordert.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-118">So an IPv4 address is requested for the ListenSocket.</span></span>

    <span data-ttu-id="e0c3e-119">Wenn die Serveranwendung IPv6 überwachen möchte, muss die Adressfamilie im hints-Parameter auf AF inet6 festgelegt werden \_ . </span><span class="sxs-lookup"><span data-stu-id="e0c3e-119">If the server application wants to listen on IPv6, then the address family needs to be set to AF\_INET6 in the *hints* parameter.</span></span> <span data-ttu-id="e0c3e-120">Wenn ein Server sowohl IPv6 als auch IPv4 lauschen möchte, müssen zwei lausch Sockets erstellt werden: eine für IPv6 und eine für IPv4.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-120">If a server wants to listen on both IPv6 and IPv4, two listen sockets must be created, one for IPv6 and one for IPv4.</span></span> <span data-ttu-id="e0c3e-121">Diese beiden Sockets müssen separat von der Anwendung behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-121">These two sockets must be handled separately by the application.</span></span>

    <span data-ttu-id="e0c3e-122">Windows Vista und höher bieten die Möglichkeit, einen einzelnen IPv6-Socket zu erstellen, der in den Dual Stack-Modus versetzt wird, um sowohl IPv6 als auch IPv4 zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-122">Windows Vista and later offer the ability to create a single IPv6 socket that is put in dual stack mode to listen on both IPv6 and IPv4.</span></span> <span data-ttu-id="e0c3e-123">Weitere Informationen zu diesem Feature finden Sie unter [Dual-Stack-Sockets](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="e0c3e-123">For more information on this feature, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  <span data-ttu-id="e0c3e-124">Überprüfen Sie auf Fehler, um sicherzustellen, dass der Socket ein gültiger Socket ist.</span><span class="sxs-lookup"><span data-stu-id="e0c3e-124">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="e0c3e-125">Nächster Schritt: [Binden eines Sockets](binding-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="e0c3e-125">Next Step: [Binding a Socket](binding-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0c3e-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0c3e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0c3e-127">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="e0c3e-127">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="e0c3e-128">Initialisieren von Winsock</span><span class="sxs-lookup"><span data-stu-id="e0c3e-128">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="e0c3e-129">Winsock-Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="e0c3e-129">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> </dl>

 

 
