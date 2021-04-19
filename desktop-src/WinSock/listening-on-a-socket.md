---
description: Nachdem der Socket an eine IP-Adresse und einen Port auf dem System gebunden ist, muss der Server diese IP-Adresse und den Port für eingehende Verbindungsanforderungen überwachen.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Lauschen an einem Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348998"
---
# <a name="listening-on-a-socket"></a><span data-ttu-id="fa464-103">Lauschen an einem Socket</span><span class="sxs-lookup"><span data-stu-id="fa464-103">Listening on a Socket</span></span>

<span data-ttu-id="fa464-104">Nachdem der Socket an eine IP-Adresse und einen Port auf dem System gebunden ist, muss der Server diese IP-Adresse und den Port für eingehende Verbindungsanforderungen überwachen.</span><span class="sxs-lookup"><span data-stu-id="fa464-104">After the socket is bound to an IP address and port on the system, the server must then listen on that IP address and port for incoming connection requests.</span></span>

## <a name="to-listen-on-a-socket"></a><span data-ttu-id="fa464-105">So lauschen Sie an einem Socket</span><span class="sxs-lookup"><span data-stu-id="fa464-105">To listen on a socket</span></span>

<span data-ttu-id="fa464-106">Nennen Sie die Funktion " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) ", und übergeben Sie als Parameter den erstellten Socket und einen Wert für den *Rückstand*, die maximale Länge der Warteschlange für ausstehende Verbindungen, die akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fa464-106">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, passing as parameters the created socket and a value for the *backlog*, maximum length of the queue of pending connections to accept.</span></span> <span data-ttu-id="fa464-107">In diesem Beispiel *wurde der* backbackparameter auf **somaxconn** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fa464-107">In this example, the *backlog* parameter was set to **SOMAXCONN**.</span></span> <span data-ttu-id="fa464-108">Dieser Wert ist eine spezielle Konstante, die den Winsock-Anbieter für diesen Socket anweist, eine maximale zulässige Anzahl von ausstehenden Verbindungen in der Warteschlange zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="fa464-108">This value is a special constant that instructs the Winsock provider for this socket to allow a maximum reasonable number of pending connections in the queue.</span></span> <span data-ttu-id="fa464-109">Überprüfen Sie den Rückgabewert auf allgemeine Fehler.</span><span class="sxs-lookup"><span data-stu-id="fa464-109">Check the return value for general errors.</span></span>


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="fa464-110">Nächster Schritt: [akzeptieren einer Verbindung](accepting-a-connection.md)</span><span class="sxs-lookup"><span data-stu-id="fa464-110">Next Step: [Accepting a Connection](accepting-a-connection.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa464-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa464-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa464-112">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="fa464-112">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="fa464-113">Winsock-Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="fa464-113">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="fa464-114">Binden eines Sockets</span><span class="sxs-lookup"><span data-stu-id="fa464-114">Binding a Socket</span></span>](binding-a-socket.md)
</dt> </dl>

 

 



