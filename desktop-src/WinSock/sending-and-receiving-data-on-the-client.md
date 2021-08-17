---
description: Der folgende Code veranschaulicht die Sende- und Recv-Funktionen, die vom Client verwendet werden, sobald eine Verbindung hergestellt wurde.
ms.assetid: 9c6d366d-2bc6-4c92-8d0b-21c51e08ed4f
title: Senden und Empfangen von Daten auf dem Client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3150c853f50e8626451cc344179645289058df928600d71bf437dc95d9738986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740561"
---
# <a name="sending-and-receiving-data-on-the-client"></a>Senden und Empfangen von Daten auf dem Client

Der folgende Code veranschaulicht die [**Sende-**](/windows/desktop/api/Winsock2/nf-winsock2-send) und [**Recv-Funktionen,**](/windows/desktop/api/winsock/nf-winsock-recv) die vom Client verwendet werden, sobald eine Verbindung hergestellt wurde.

## <a name="client"></a>Client


```C++
#define DEFAULT_BUFLEN 512

int recvbuflen = DEFAULT_BUFLEN;

const char *sendbuf = "this is a test";
char recvbuf[DEFAULT_BUFLEN];

int iResult;

// Send an initial buffer
iResult = send(ConnectSocket, sendbuf, (int) strlen(sendbuf), 0);
if (iResult == SOCKET_ERROR) {
    printf("send failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

printf("Bytes Sent: %ld\n", iResult);

// shutdown the connection for sending since no more data will be sent
// the client can still use the ConnectSocket for receiving data
iResult = shutdown(ConnectSocket, SD_SEND);
if (iResult == SOCKET_ERROR) {
    printf("shutdown failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

// Receive data until the server closes the connection
do {
    iResult = recv(ConnectSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0)
        printf("Bytes received: %d\n", iResult);
    else if (iResult == 0)
        printf("Connection closed\n");
    else
        printf("recv failed: %d\n", WSAGetLastError());
} while (iResult > 0);
```



Die [**Funktionen send**](/windows/desktop/api/Winsock2/nf-winsock2-send) und [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) geben jeweils einen ganzzahligen Wert der Anzahl gesendeter bzw. empfangener Bytes bzw. einen Fehler zurück. Jede Funktion verwendet auch die gleichen Parameter: den aktiven Socket, einen **char-Puffer,** die Anzahl der zu sendenden oder zu empfangenden Bytes und alle zu verwendenden Flags.

Nächster Schritt: [Trennen des Clients](disconnecting-the-client.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock-Clientanwendung](winsock-client-application.md)
</dt> <dt>

[Herstellen einer Verbindung mit einem Socket](connecting-to-a-socket.md)
</dt> </dl>

 

 



