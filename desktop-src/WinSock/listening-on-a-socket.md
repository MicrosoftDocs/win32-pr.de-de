---
description: Nachdem der Socket an eine IP-Adresse und einen Port auf dem System gebunden ist, muss der Server diese IP-Adresse und diesen Port auf eingehende Verbindungsanforderungen lauschen.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Lauschen an einem Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d6d98a13fc6e994fb5a264827b6b93047fd24e03d3e3f9953203b1fa15140f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569780"
---
# <a name="listening-on-a-socket"></a>Lauschen an einem Socket

Nachdem der Socket an eine IP-Adresse und einen Port auf dem System gebunden ist, muss der Server diese IP-Adresse und diesen Port auf eingehende Verbindungsanforderungen lauschen.

## <a name="to-listen-on-a-socket"></a>So lauschen Sie an einem Socket

Rufen Sie die [**Lauschfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-listen) auf, und übergeben Sie als Parameter den erstellten Socket und einen Wert für das Backlog *,* die maximale Länge der Warteschlange ausstehender Verbindungen, die akzeptiert werden müssen. In diesem Beispiel wurde der *Backlog-Parameter* auf **SOMAXCONN festgelegt.** Dieser Wert ist eine spezielle Konstante, die den Winsock-Anbieter für diesen Socket anweisen soll, eine maximale angemessene Anzahl ausstehender Verbindungen in der Warteschlange zu ermöglichen. Überprüfen Sie den Rückgabewert auf allgemeine Fehler.


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



Nächster Schritt: [Akzeptieren einer Verbindung](accepting-a-connection.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock Server-Anwendung](winsock-server-application.md)
</dt> <dt>

[Binden eines Sockets](binding-a-socket.md)
</dt> </dl>

 

 



