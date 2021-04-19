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
# <a name="listening-on-a-socket"></a>Lauschen an einem Socket

Nachdem der Socket an eine IP-Adresse und einen Port auf dem System gebunden ist, muss der Server diese IP-Adresse und den Port für eingehende Verbindungsanforderungen überwachen.

## <a name="to-listen-on-a-socket"></a>So lauschen Sie an einem Socket

Nennen Sie die Funktion " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) ", und übergeben Sie als Parameter den erstellten Socket und einen Wert für den *Rückstand*, die maximale Länge der Warteschlange für ausstehende Verbindungen, die akzeptiert werden sollen. In diesem Beispiel *wurde der* backbackparameter auf **somaxconn** festgelegt. Dieser Wert ist eine spezielle Konstante, die den Winsock-Anbieter für diesen Socket anweist, eine maximale zulässige Anzahl von ausstehenden Verbindungen in der Warteschlange zuzulassen. Überprüfen Sie den Rückgabewert auf allgemeine Fehler.


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



Nächster Schritt: [akzeptieren einer Verbindung](accepting-a-connection.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock-Server Anwendung](winsock-server-application.md)
</dt> <dt>

[Binden eines Sockets](binding-a-socket.md)
</dt> </dl>

 

 



