---
description: Die wsaaccept-Funktion ermöglicht einer Anwendung das Abrufen von Aufruferinformationen wie Aufrufer-ID und Quality of Service, bevor Sie entscheiden, ob eine eingehende Verbindungsanforderung akzeptiert
ms.assetid: 65883556-6890-4d0a-8c7f-c4ff68642caf
title: Einrichten und Löschen der Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c4ac1f32524d097e11825f8104eb41fee3c528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357335"
---
# <a name="connection-setup-and-teardown"></a>Einrichten und Löschen der Verbindung

Die [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Funktion ermöglicht einer Anwendung das Abrufen von Aufruferinformationen wie Aufrufer-ID und Quality of Service, bevor Sie entscheiden, ob eine eingehende Verbindungsanforderung akzeptiert Dies erfolgt mit einem Rückruf einer von der Anwendung bereitgestellten Bedingungs Funktion.

Benutzer-zu-Benutzer-Daten, die durch Parameter in der [**wsaconnetct**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) -Funktion und die Condition-Funktion von [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) angegeben werden, können während der Verbindungs Herstellung an den Peer übertragen werden, sofern diese Funktion vom Dienstanbieter unterstützt wird.

Es ist auch möglich (bei Protokollen, die dies unterstützen), Benutzerdaten zwischen den Endpunkten zum Zeitpunkt der Verbindungs Löschung auszutauschen. Das Ende, das "Beendigungs" initiiert, kann die [**wsasenddisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) -Funktion aufzurufen, um anzugeben, dass keine weiteren Daten gesendet werden, und um die Verbindungs-Beendigungs-Sequenz zu initiieren. Bei bestimmten Protokollen ist ein Teil von "Beendigungs" die Übermittlung von Disconnect-Daten vom Beendigungs-Initiator. Nachdem Sie festgestellt haben, dass das Remote Ende "Beendigungs" initiiert hat (in der Regel durch die Bestätigung der FD- \_ Schließung), kann die [**wsarecvdisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) -Funktion aufgerufen werden, um die Trennungs Daten zu empfangen, sofern vorhanden

Beachten Sie das folgende Szenario, um zu veranschaulichen, wie die Trennung von Daten verwendet werden kann. Die Client Hälfte einer Client/Server-Anwendung ist für das Beenden einer Socketverbindung verantwortlich. Koincident mit der Beendigung stellt die Gesamtzahl der Transaktionen, die Sie mit dem Server verarbeitet hat (unter Verwendung von Disconnect-Daten) bereit. Der Server antwortet wiederum mit der kumulativen Gesamtsumme der Transaktionen, die er mit allen Clients verarbeitet hat. Die Abfolge der Aufrufe und Anzeichen können wie folgt auftreten:

| Clientseitig                                                                                                              | Serverseitig                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (1) [**wsasenddisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) aufrufen, um die Sitzung zu beenden und die Transaktions Summe zu liefern.            |                                                                                                                                                                                                                               |
|                                                                                                                          | (2) Get FD \_ Close, [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) mit einem Rückgabewert von 0 (null) oder [wsaediscon](windows-sockets-error-codes-2.md) -Fehlerrückgabe von [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) , was auf das ordnungsgemäße Herunterfahren hinweist. |
|                                                                                                                          | (3) [**wsarecvdisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) aufrufen, um die Transaktions Summe des Clients zu erhalten.                                                                                                                                |
|                                                                                                                          | (4) berechnen des kumulativen Gesamtergebnisses aller Transaktionen.                                                                                                                                                                       |
|                                                                                                                          | (5) [**wsasenddisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) aufrufen, um das Gesamtergebnis zu übertragen.                                                                                                                                          |
| (6) empfangen Sie die Bestätigung von FD \_ .                                                                                        | (5a) rufen Sie [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)auf.                                                                                                                                                                             |
| (7) rufen Sie [**wsarecvdisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) auf, um eine kumulative Gesamtsumme von Transaktionen zu empfangen und zu speichern. |                                                                                                                                                                                                                               |
| (8) [ **closesocket** aufrufen](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                          |                                                                                                                                                                                                                               |



 

Beachten Sie, dass Step (5a) (Schritt (5)) befolgt werden muss, aber keine zeitliche Beziehungs Beziehung mit Schritt (6), (7) oder (8) aufweist.

 

 



