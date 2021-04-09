---
description: Im folgenden wird beschrieben, wie ein Incident eine etablierte Socketverbindung herunterfährt.
ms.assetid: 052e04a4-5290-4dca-af7a-cd590ebfbe15
title: Herunterfahren der Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbde0cfe4c3a97435c2412d28970107f830308fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862580"
---
# <a name="connection-shutdown"></a>Herunterfahren der Verbindung

Im folgenden wird beschrieben, wie ein Incident eine etablierte Socketverbindung herunterfährt.

## <a name="initiating-shutdown-sequence"></a>Initiierungs Sequenz wird initiiert

Eine Socketverbindung kann auf verschiedene Arten heruntergefahren werden. [**Wspshutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (mit der gleichwertigen *Verwendung* von SD \_ Send oder SD \_ ) und [**wspsenddisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) können verwendet werden, um eine ordnungsgemäße Verbindung mit dem Herunterfahren zu initiieren. [**Wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) kann verwendet werden, um ein ordnungsgemäßes oder abgerufenes Herunterfahren zu initiieren, je nach den vom schließenden Socket aufgerufenen Linger-Optionen. Weitere Informationen zu ordnungsgemäßen und Abbruch Optionen finden Sie unten.

## <a name="indicating-remote-shutdown"></a>Angeben des Remote herunter Fahrens

Dienstanbieter geben an, dass die Verbindung von der Remote Partei über das FD- \_ Netzwerk Ereignis initiiert wurde. Ordnungsgemäßes Herunterfahren wird auch durch [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) angegeben, wenn die Anzahl der gelesenen Bytes 0 für bytestreamprotokolle ist, oder durch einen Rückgabe Fehlercode von wsaediscon für Nachrichten orientierte Protokolle. In jedem Fall gibt der **wsprecv** -Rückgabe Fehlercode von WSAECONNRESET an, dass ein Abbruch abgebrochen wurde.

## <a name="exchanging-user-data-at-shutdown-time"></a>Austauschen von Benutzerdaten beim Herunterfahren

Zum Austauschen von Benutzerdaten zwischen den Endpunkten ist es auch möglich, die Verbindung zwischen den Endpunkten zu unterstützen Das Ende, das "Beendigungs" initiiert, kann [**wspsenddisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) anrufen, um anzugeben, dass keine weiteren Daten gesendet werden sollen, und die Initiierung der verbindungsendesequenz auslösen soll. Bei bestimmten Protokollen ist ein Teil dieser Beendigungs-Sequenz die Übermittlung von Trennungs Daten vom Beendigungs-Initiator. Nachdem Sie festgestellt haben, dass das Remote Ende die Beendigungs-Sequenz initiiert hat (in der Regel über die \_ Bestätigung der Bestätigung von FD), kann die [**wsprecvdisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) -Funktion aufgerufen werden, um die Trennungs Daten zu empfangen (sofern vorhanden).

Beachten Sie das folgende Szenario, um zu veranschaulichen, wie die Trennung von Daten möglicherweise verwendet wird. Die Client Hälfte einer Client/Server-Anwendung ist für das Beenden einer Socketverbindung verantwortlich. Koincident mit der von ihm bereitgestellten Beendigung (Durchtrennen von Daten) der Gesamtzahl der Transaktionen, die mit dem Server verarbeitet wurden. Der Server antwortet wiederum mit der kumulativen Gesamtsumme von Transaktionen, die er mit allen Clients verarbeitet hat. Die Reihenfolge der Aufrufe und Anzeichen können wie in der folgenden Tabelle gezeigt auftreten.

| Clientseitig                                                                                                               | Serverseitig                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| (1) ruft [**wspsenddisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) auf, um die Sitzung zu beenden und die Transaktions Summe zu liefern.            |                                                                                                                                         |
|                                                                                                                           | (2) ruft "FD \_ Close" oder " [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) " mit dem Rückgabewert "Null" oder "wsaediscon" ab, was das ordnungsgemäße Herunterfahren anzeigt. |
|                                                                                                                           | (3) ruft [**wsprecvdisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) auf, um die Transaktions Summe des Clients zu erhalten.                                         |
|                                                                                                                           | (4) berechnet das kumulative Gesamtergebnis aller Transaktionen.                                                                                |
|                                                                                                                           | (5) ruft [**wspsenddisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) auf, um das Gesamtergebnis zu übertragen.                                                   |
| (6) empfängt die \_ Bestätigung von FD.                                                                                        | (5 ') ruft [ **wspclosesocket** auf](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                 |
| (7) ruft [**wsprecvdisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) auf, um eine kumulative Gesamtsumme von Transaktionen zu empfangen und zu speichern. |                                                                                                                                         |
|                                                                                                                           | (8) ruft [ **wspclosesocket** auf.](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                  |



 

Der Schritt (5) muss Schritt (5) entsprechen, hat jedoch keine zeitliche Beziehungs Beziehung mit Schritten (6), (7) oder (8).

 

 
