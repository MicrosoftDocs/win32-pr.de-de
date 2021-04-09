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
# <a name="creating-a-socket-for-the-client"></a><span data-ttu-id="a162e-103">Erstellen eines Sockets für den Client</span><span class="sxs-lookup"><span data-stu-id="a162e-103">Creating a socket for the client</span></span>

<span data-ttu-id="a162e-104">Nach der Initialisierung muss ein **Socket** -Objekt für die Verwendung durch den Client instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="a162e-104">After initialization, a **SOCKET** object must be instantiated for use by the client.</span></span>

<span data-ttu-id="a162e-105">**So erstellen Sie einen Socket**</span><span class="sxs-lookup"><span data-stu-id="a162e-105">**To create a socket**</span></span>

1.  <span data-ttu-id="a162e-106">Deklarieren Sie ein [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) -Objekt, das eine [**sockaddr**](sockaddr-2.md) -Struktur enthält, und initialisieren Sie diese Werte.</span><span class="sxs-lookup"><span data-stu-id="a162e-106">Declare an [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) object that contains a [**sockaddr**](sockaddr-2.md) structure and initialize these values.</span></span> <span data-ttu-id="a162e-107">Für diese Anwendung ist die Internet Adressfamilie nicht angegeben, sodass entweder eine IPv6-oder eine IPv4-Adresse zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a162e-107">For this application, the Internet address family is unspecified so that either an IPv6 or IPv4 address can be returned.</span></span> <span data-ttu-id="a162e-108">Die Anwendung fordert den socketyp als Stream-Socket für das TCP-Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="a162e-108">The application requests the socket type to be a stream socket for the TCP protocol.</span></span>
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  <span data-ttu-id="a162e-109">Aufrufen der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion anfordern der IP-Adresse für den Servernamen, der in der Befehlszeile weitergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a162e-109">Call the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function requesting the IP address for the server name passed on the command line.</span></span> <span data-ttu-id="a162e-110">Der TCP-Port auf dem Server, mit dem der Client eine Verbindung herstellt, wird \_ in diesem Beispiel über den Standardport 27015 als definiert.</span><span class="sxs-lookup"><span data-stu-id="a162e-110">The TCP port on the server that the client will connect to is defined by DEFAULT\_PORT as 27015 in this sample.</span></span> <span data-ttu-id="a162e-111">Die **getaddrinfo** -Funktion gibt ihren Wert als Ganzzahl zurück, die auf Fehler geprüft wird.</span><span class="sxs-lookup"><span data-stu-id="a162e-111">The **getaddrinfo** function returns its value as an integer that is checked for errors.</span></span>
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

    

3.  <span data-ttu-id="a162e-112">Erstellen Sie ein **Socketobjekt** mit dem Namen connectsocket.</span><span class="sxs-lookup"><span data-stu-id="a162e-112">Create a **SOCKET** object called ConnectSocket.</span></span>
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  <span data-ttu-id="a162e-113">Ruft die [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -Funktion auf und gibt ihren Wert an die connectsocket-Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="a162e-113">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ConnectSocket variable.</span></span> <span data-ttu-id="a162e-114">Verwenden Sie für diese Anwendung die erste IP-Adresse, die vom [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Befehl zurückgegeben wird, der mit der Adressfamilie, dem Sockettyp und dem Protokoll übereinstimmt, die im *Hints* -Parameter angegeben sind</span><span class="sxs-lookup"><span data-stu-id="a162e-114">For this application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="a162e-115">In diesem Beispiel wurde ein TCP-streamingsocket mit einem Sockettyp von Sock \_ Stream und einem Protokoll von ipproto \_ TCP angegeben.</span><span class="sxs-lookup"><span data-stu-id="a162e-115">In this example, a TCP stream socket was specified with a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="a162e-116">Die Adressfamilie wurde nicht angegeben (AF \_ unspec), sodass die zurückgegebene IP-Adresse entweder eine IPv6-oder IPv4-Adresse für den Server sein könnte.</span><span class="sxs-lookup"><span data-stu-id="a162e-116">The address family was left unspecified (AF\_UNSPEC), so the returned IP address could be either an IPv6 or IPv4 address for the server.</span></span>

    <span data-ttu-id="a162e-117">Wenn die Client Anwendung nur über IPv6 oder IPv4 eine Verbindung herstellen möchte, muss die Adressfamilie auf AF \_ inet6 for IPv6 oder AF \_ inet for IPv4 im *Hints* -Parameter festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a162e-117">If the client application wants to connect using only IPv6 or IPv4, then the address family needs to be set to AF\_INET6 for IPv6 or AF\_INET for IPv4 in the *hints* parameter.</span></span>

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  <span data-ttu-id="a162e-118">Überprüfen Sie auf Fehler, um sicherzustellen, dass der Socket ein gültiger Socket ist.</span><span class="sxs-lookup"><span data-stu-id="a162e-118">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="a162e-119">Die an die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) über gebenden Parameter können für verschiedene Implementierungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a162e-119">The parameters passed to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be changed for different implementations.</span></span>

<span data-ttu-id="a162e-120">Die Fehlererkennung ist ein wichtiger Bestandteil des erfolgreichen Netzwerk Codes.</span><span class="sxs-lookup"><span data-stu-id="a162e-120">Error detection is a key part of successful networking code.</span></span> <span data-ttu-id="a162e-121">Wenn der [**socketbefehl**](/windows/desktop/api/Winsock2/nf-winsock2-socket) fehlschlägt, wird ein ungültiger Socket zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="a162e-121">If the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call fails, it returns INVALID\_SOCKET.</span></span> <span data-ttu-id="a162e-122">Die **if** -Anweisung im vorherigen Code wird verwendet, um Fehler abzufangen, die möglicherweise beim Erstellen des Sockets aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="a162e-122">The **if** statement in the previous code is used to catch any errors that may have occurred while creating the socket.</span></span> <span data-ttu-id="a162e-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt eine Fehlernummer zurück, die dem zuletzt aufgetretenen Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a162e-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns an error number associated with the last error that occurred.</span></span>

> [!Note]  
> <span data-ttu-id="a162e-124">Abhängig von der Anwendung ist möglicherweise eine umfangreichere Fehlerüberprüfung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a162e-124">More extensive error checking may be necessary depending on the application.</span></span>
>
> <span data-ttu-id="a162e-125">Wenn Sie z. b. *hints.ai_family* auf **AF_UNSPEC** festlegen, kann der Connect-Befehl fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="a162e-125">For example, setting *hints.ai_family* to **AF_UNSPEC** can cause the connect call to fail.</span></span> <span data-ttu-id="a162e-126">Wenn dies der Fall ist, verwenden Sie stattdessen einen bestimmten IPv4-(**AF_INET**) oder IPv6-Wert (**AF_INET6**).</span><span class="sxs-lookup"><span data-stu-id="a162e-126">If that happens, then use a specific IPv4 (**AF_INET**) or IPv6 (**AF_INET6**) value instead.</span></span>

<span data-ttu-id="a162e-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) wird verwendet, um die Verwendung der ws2 32-dll zu beenden \_ .</span><span class="sxs-lookup"><span data-stu-id="a162e-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) is used to terminate the use of the WS2\_32 DLL.</span></span>

<span data-ttu-id="a162e-128">Nächster Schritt: [Herstellen einer Verbindung mit einem Socket](connecting-to-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="a162e-128">Next Step: [Connecting to a Socket](connecting-to-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a162e-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a162e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a162e-130">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="a162e-130">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="a162e-131">Initialisieren von Winsock</span><span class="sxs-lookup"><span data-stu-id="a162e-131">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="a162e-132">WinSock-Client Anwendung</span><span class="sxs-lookup"><span data-stu-id="a162e-132">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> </dl>

 

 
