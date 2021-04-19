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
# <a name="accepting-a-connection-windows-sockets-2"></a><span data-ttu-id="88bbc-103">Akzeptieren einer Verbindung (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="88bbc-103">Accepting a Connection (Windows Sockets 2)</span></span>

<span data-ttu-id="88bbc-104">Sobald der Socket eine Verbindung abhört, muss das Programm Verbindungsanforderungen für diesen Socket verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="88bbc-104">Once the socket is listening for a connection, the program must handle connection requests on that socket.</span></span>

<span data-ttu-id="88bbc-105">**So akzeptieren Sie eine Verbindung für einen Socket**</span><span class="sxs-lookup"><span data-stu-id="88bbc-105">**To accept a connection on a socket**</span></span>

1.  <span data-ttu-id="88bbc-106">Erstellen Sie ein temporäres **Socketobjekt** namens Clientsocket für die Annahme von Verbindungen von Clients.</span><span class="sxs-lookup"><span data-stu-id="88bbc-106">Create a temporary **SOCKET** object called ClientSocket for accepting connections from clients.</span></span>
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  <span data-ttu-id="88bbc-107">Normalerweise ist eine Serveranwendung so konzipiert, dass Sie auf Verbindungen von mehreren Clients lauscht.</span><span class="sxs-lookup"><span data-stu-id="88bbc-107">Normally a server application would be designed to listen for connections from multiple clients.</span></span> <span data-ttu-id="88bbc-108">Bei Hochleistungsservern werden häufig mehrere Threads verwendet, um mehrere Clientverbindungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="88bbc-108">For high-performance servers, multiple threads are commonly used to handle the multiple client connections.</span></span>

    <span data-ttu-id="88bbc-109">Es gibt mehrere unterschiedliche Programmiertechniken, die Winsock verwenden, die zum lauschen auf mehrere Clientverbindungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="88bbc-109">There are several different programming techniques using Winsock that can be used to listen for multiple client connections.</span></span> <span data-ttu-id="88bbc-110">Ein Programmierverfahren besteht darin, eine kontinuierliche Schleife zu erstellen, die mithilfe der Funktion " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) " die Verbindungsanforderungen überprüft (siehe [lauschen auf einem Socket](listening-on-a-socket.md)).</span><span class="sxs-lookup"><span data-stu-id="88bbc-110">One programming technique is to create a continuous loop that checks for connection requests using the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function (see [Listening on a Socket](listening-on-a-socket.md)).</span></span> <span data-ttu-id="88bbc-111">Wenn eine Verbindungsanforderung auftritt, ruft die Anwendung die [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)-, [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex)-oder [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Funktion auf und übergibt die Arbeit an einen anderen Thread, um die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="88bbc-111">If a connection request occurs, the application calls the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function and passes the work to another thread to handle the request.</span></span> <span data-ttu-id="88bbc-112">Es sind mehrere andere Programmiertechniken möglich.</span><span class="sxs-lookup"><span data-stu-id="88bbc-112">Several other programming techniques are possible.</span></span>

    <span data-ttu-id="88bbc-113">Beachten Sie, dass dieses grundlegende Beispiel sehr einfach ist und nicht mehrere Threads verwendet.</span><span class="sxs-lookup"><span data-stu-id="88bbc-113">Note that this basic example is very simple and does not use multiple threads.</span></span> <span data-ttu-id="88bbc-114">Das Beispiel lauscht auch nur auf eine einzelne Verbindung.</span><span class="sxs-lookup"><span data-stu-id="88bbc-114">The example also just listens for and accepts only a single connection.</span></span>

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

    

3.  <span data-ttu-id="88bbc-115">Wenn die Client Verbindung akzeptiert wurde, übergibt eine Serveranwendung normalerweise den akzeptierten Client Socket (die Clientsocket-Variable im obigen Beispielcode) an einen Arbeits Thread oder einen e/a-Abschlussport und nimmt weiterhin weitere Verbindungen an.</span><span class="sxs-lookup"><span data-stu-id="88bbc-115">When the client connection has been accepted, a server application would normally pass the accepted client socket (the ClientSocket variable in the above sample code) to a worker thread or an I/O completion port and continue accepting additional connections.</span></span> <span data-ttu-id="88bbc-116">In diesem einfachen Beispiel wird der Server mit dem nächsten Schritt fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="88bbc-116">In this basic example, the server continues to the next step.</span></span>

    <span data-ttu-id="88bbc-117">Es gibt eine Reihe von anderen Programmiertechniken, die verwendet werden können, um auf mehrere Verbindungen zu lauschen und diese zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="88bbc-117">There are a number of other programming techniques that can be used to listen for and accept multiple connections.</span></span> <span data-ttu-id="88bbc-118">Dazu gehört die Verwendung der [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="88bbc-118">These include using the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions.</span></span> <span data-ttu-id="88bbc-119">Beispiele für einige dieser verschiedenen Programmierverfahren werden in den [erweiterten Winsock-Beispielen](getting-started-with-winsock.md) veranschaulicht, die im Microsoft Windows Software Development Kit (SDK) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="88bbc-119">Examples of some of these various programming techniques are illustrated in the [Advanced Winsock Samples](getting-started-with-winsock.md) included with the Microsoft Windows Software Development Kit (SDK).</span></span>

    > [!Note]  
    > <span data-ttu-id="88bbc-120">Auf UNIX-Systemen bestand eine gängige Programmiermethode für Server darin, dass eine Anwendung auf Verbindungen lauschen konnte.</span><span class="sxs-lookup"><span data-stu-id="88bbc-120">On Unix systems, a common programming technique for servers was for an application to listen for connections.</span></span> <span data-ttu-id="88bbc-121">Wenn eine Verbindung akzeptiert wurde, ruft der übergeordnete Prozess die **Verzweigungs** Funktion auf, um einen neuen untergeordneten Prozess zum Verarbeiten der Client Verbindung zu erstellen, der den Socket vom übergeordneten Element erbt.</span><span class="sxs-lookup"><span data-stu-id="88bbc-121">When a connection was accepted, the parent process would call the **fork** function to create a new child process to handle the client connection, inheriting the socket from the parent.</span></span> <span data-ttu-id="88bbc-122">Diese Programmiertechnik wird unter Windows nicht unterstützt, da die **Fork** -Funktion nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="88bbc-122">This programming technique is not supported on Windows, since the **fork** function is not supported.</span></span> <span data-ttu-id="88bbc-123">Dieses Verfahren eignet sich in der Regel nicht für Hochleistungsserver, da die für die Erstellung eines neuen Prozesses benötigten Ressourcen wesentlich größer sind als die für einen Thread benötigten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="88bbc-123">This technique is also not usually suitable for high-performance servers, since the resources needed to create a new process are much greater than those needed for a thread.</span></span>

     

<span data-ttu-id="88bbc-124">Nächster Schritt: [empfangen und Senden von Daten auf dem Server](receiving-and-sending-data-on-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="88bbc-124">Next Step: [Receiving and Sending Data on the Server](receiving-and-sending-data-on-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="88bbc-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88bbc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88bbc-126">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="88bbc-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="88bbc-127">Winsock-Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="88bbc-127">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="88bbc-128">Lauschen an einem Socket</span><span class="sxs-lookup"><span data-stu-id="88bbc-128">Listening on a Socket</span></span>](listening-on-a-socket.md)
</dt> </dl>

 

 
