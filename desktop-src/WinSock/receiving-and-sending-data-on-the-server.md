---
description: Der folgende Code veranschaulicht die vom Server verwendeten empfangener-und sende Funktionen.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Empfangen und Senden von Daten auf dem Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ab20f074db750bef6459c6b9fcb5fd5636a522
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358823"
---
# <a name="receiving-and-sending-data-on-the-server"></a><span data-ttu-id="9d9fc-103">Empfangen und Senden von Daten auf dem Server</span><span class="sxs-lookup"><span data-stu-id="9d9fc-103">Receiving and Sending Data on the Server</span></span>

<span data-ttu-id="9d9fc-104">Der folgende Code veranschaulicht die vom Server verwendeten [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -und [**Sende**](/windows/desktop/api/Winsock2/nf-winsock2-send) Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9d9fc-104">The following code demonstrates the [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) and [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) functions used by the server.</span></span>

### <a name="to-receive-and-send-data-on-a-socket"></a><span data-ttu-id="9d9fc-105">So empfangen und senden Sie Daten für einen Socket</span><span class="sxs-lookup"><span data-stu-id="9d9fc-105">To receive and send data on a socket</span></span>


```C++
#define DEFAULT_BUFLEN 512

char recvbuf[DEFAULT_BUFLEN];
int iResult, iSendResult;
int recvbuflen = DEFAULT_BUFLEN;

// Receive until the peer shuts down the connection
do {

    iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0) {
        printf("Bytes received: %d\n", iResult);

        // Echo the buffer back to the sender
        iSendResult = send(ClientSocket, recvbuf, iResult, 0);
        if (iSendResult == SOCKET_ERROR) {
            printf("send failed: %d\n", WSAGetLastError());
            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }
        printf("Bytes sent: %d\n", iSendResult);
    } else if (iResult == 0)
        printf("Connection closing...\n");
    else {
        printf("recv failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }

} while (iResult > 0);
```



<span data-ttu-id="9d9fc-106">Die Funktionen [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) und [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) geben jeweils einen ganzzahligen Wert für die Anzahl der gesendeten oder empfangenen Bytes oder einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9d9fc-106">The [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions both return an integer value of the number of bytes sent or received, respectively, or an error.</span></span> <span data-ttu-id="9d9fc-107">Jede Funktion verwendet auch die gleichen Parameter: den aktiven Socket, einen **char** -Puffer, die Anzahl der zu sendenden Bytes, die Anzahl der zu sendenden Bytes und alle Flags, die verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9d9fc-107">Each function also takes the same parameters: the active socket, a **char** buffer, the number of bytes to send or receive, and any flags to use.</span></span>

<span data-ttu-id="9d9fc-108">Nächster Schritt: [Trennen der Verbindung mit dem Server](disconnecting-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="9d9fc-108">Next Step: [Disconnecting the Server](disconnecting-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d9fc-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d9fc-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d9fc-110">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="9d9fc-110">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="9d9fc-111">Winsock-Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="9d9fc-111">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="9d9fc-112">Akzeptieren einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="9d9fc-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> </dl>

 

 



