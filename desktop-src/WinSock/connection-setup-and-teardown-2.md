---
description: Mit der WSAAccept-Funktion kann eine Anwendung Aufruferinformationen wie aufrufer identifier und Quality of Service abrufen, bevor sie entscheidet, ob eine eingehende Verbindungsanforderung akzeptiert werden soll.
ms.assetid: 65883556-6890-4d0a-8c7f-c4ff68642caf
title: Verbindungseinrichtung und -abbruch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c5e8c8a95c9baa90e95bd7b7da2702f3522b2a575d3d0181271428837e27b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051718"
---
# <a name="connection-setup-and-teardown"></a>Verbindungseinrichtung und -abbruch

Mit [**der WSAAccept-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) kann eine Anwendung Aufruferinformationen wie aufrufer identifier und Quality of Service abrufen, bevor sie entscheidet, ob eine eingehende Verbindungsanforderung akzeptiert werden soll. Dies erfolgt mit einem Rückruf einer von der Anwendung bereitgestellten Bedingungsfunktion.

Benutzer-zu-Benutzer-Daten, die durch Parameter in der [**WSAConnect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) und die Bedingungsfunktion von [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) angegeben werden, können während der Verbindungseinrichtung an den Peer übertragen werden, sofern diese Funktion vom Dienstanbieter unterstützt wird.

Es ist auch möglich (für Protokolle, die dies unterstützen), Benutzerdaten zwischen den Endpunkten zum Zeitpunkt des Verbindungsentbruchs austauschen. Das Ende, das den Abbruch initiiert, kann die [**WSASendDisconnect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) aufrufen, um anzugeben, dass keine Daten mehr gesendet werden, und um die Sequenz zum Beenden der Verbindung zu initiieren. Bei bestimmten Protokollen ist ein Teil des Abbruchs die Übermittlung der Trennung von Daten vom Teardown-Initiator. Nachdem sie eine Benachrichtigung erhalten haben, dass das Remoteend die Trennung initiiert hat (in der Regel durch die \_ FD CLOSE-Angabe), kann die [**WSARecvDisconnect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) aufgerufen werden, um die Trennungsdaten zu empfangen( falls möglich).

Um zu veranschaulichen, wie Daten getrennt werden können, betrachten Sie das folgende Szenario. Die Clienthälfte einer Client-/Serveranwendung ist für das Beenden einer Socketverbindung verantwortlich. Zufällig mit der Beendigung wird (mithilfe von Datentrennung) die Gesamtzahl der Transaktionen, die mit dem Server verarbeitet wurden, angezeigt. Der Server antwortet wiederum mit dem kumulativen Gesamtwert der Transaktionen, die er mit allen Clients verarbeitet hat. Die Reihenfolge der Aufrufe und Hinweise kann wie folgt auftreten:

| Clientseitig                                                                                                              | Serverseitig                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (1) Rufen Sie [**WSASendDisconnect auf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) um die Sitzung abzuschließen und die Transaktionssumme zu liefern.            |                                                                                                                                                                                                                               |
|                                                                                                                          | (2) Get FD \_ CLOSE, recv with a return value of 0 (Null) oder WSAEDISCON error return from WSARecv (Rückgabe des [**Fehlers "FD**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) CLOSE", [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) mit dem Rückgabewert 0 (null) oder [WSAEDISCON-Fehler,](windows-sockets-error-codes-2.md) der angibt, dass das ordnungsgemäß heruntergefahrene Herunterfahren in Bearbeitung ist. |
|                                                                                                                          | (3) Rufen Sie [**WSARecvDisconnect auf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) um die Transaktionssumme des Clients zu erhalten.                                                                                                                                |
|                                                                                                                          | (4) Berechnen sie die kumulative Gesamtsumme aller Transaktionen.                                                                                                                                                                       |
|                                                                                                                          | (5) Rufen Sie [**WSASendDisconnect auf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) um die Gesamtsumme zu übertragen.                                                                                                                                          |
| (6) Empfangen der FD \_ CLOSE-Angabe.                                                                                        | (5a) Rufen Sie [**closesocket auf.**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                                                                                                                             |
| (7) Rufen Sie [**WSARecvDisconnect auf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) um die kumulative Gesamtsumme von Transaktionen zu empfangen und zu speichern. |                                                                                                                                                                                                                               |
| (8) Aufrufen [ **von closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                          |                                                                                                                                                                                                                               |



 

Beachten Sie, dass Schritt (5a) Schritt (5) folgen muss, aber keine zeitliche Beziehung zu Schritt (6), (7) oder (8) hat.

 

 



