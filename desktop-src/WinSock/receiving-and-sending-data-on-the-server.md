---
description: Der folgende Code veranschaulicht die recv- und send-Funktionen, die vom Server verwendet werden.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Empfangen und Senden von Daten auf dem Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f943fe9f1c4045c087b31861bc6db5f1eb394ad800ee0133e0ec8fb668fcbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857850"
---
# <a name="receiving-and-sending-data-on-the-server"></a>Empfangen und Senden von Daten auf dem Server

Der folgende Code veranschaulicht die [**recv-**](/windows/desktop/api/winsock/nf-winsock-recv) und [**send-Funktionen,**](/windows/desktop/api/Winsock2/nf-winsock2-send) die vom Server verwendet werden.

### <a name="to-receive-and-send-data-on-a-socket"></a>So empfangen und senden Sie Daten auf einem Socket


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



Die [**Funktionen send**](/windows/desktop/api/Winsock2/nf-winsock2-send) und [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) geben jeweils einen ganzzahligen Wert der Anzahl gesendeter bzw. empfangener Bytes bzw. einen Fehler zurück. Jede Funktion verwendet auch die gleichen Parameter: den aktiven Socket, einen **char-Puffer,** die Anzahl der zu sendenden oder zu empfangenden Bytes und alle zu verwendenden Flags.

Nächster Schritt: [Trennen des Servers](disconnecting-the-server.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock Server-Anwendung](winsock-server-application.md)
</dt> <dt>

[Akzeptieren einer Verbindung](accepting-a-connection.md)
</dt> </dl>

 

 



