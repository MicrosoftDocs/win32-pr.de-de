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
# <a name="receiving-and-sending-data-on-the-server"></a>Empfangen und Senden von Daten auf dem Server

Der folgende Code veranschaulicht die vom Server verwendeten [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -und [**Sende**](/windows/desktop/api/Winsock2/nf-winsock2-send) Funktionen.

### <a name="to-receive-and-send-data-on-a-socket"></a>So empfangen und senden Sie Daten für einen Socket


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



Die Funktionen [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) und [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) geben jeweils einen ganzzahligen Wert für die Anzahl der gesendeten oder empfangenen Bytes oder einen Fehler zurück. Jede Funktion verwendet auch die gleichen Parameter: den aktiven Socket, einen **char** -Puffer, die Anzahl der zu sendenden Bytes, die Anzahl der zu sendenden Bytes und alle Flags, die verwendet werden sollen.

Nächster Schritt: [Trennen der Verbindung mit dem Server](disconnecting-the-server.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock-Server Anwendung](winsock-server-application.md)
</dt> <dt>

[Akzeptieren einer Verbindung](accepting-a-connection.md)
</dt> </dl>

 

 



