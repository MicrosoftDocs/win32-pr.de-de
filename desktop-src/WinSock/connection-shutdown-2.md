---
description: Im Folgenden wird der Vorgangsvorfall zum Herunterfahren einer eingerichteten Socketverbindung beschrieben.
ms.assetid: 052e04a4-5290-4dca-af7a-cd590ebfbe15
title: Herunterfahren der Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babbd26716c255c83a8ecc17305d9e59676645739a6f90d18ac72b5bcda49241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898420"
---
# <a name="connection-shutdown"></a>Herunterfahren der Verbindung

Im Folgenden wird der Vorgangsvorfall zum Herunterfahren einer eingerichteten Socketverbindung beschrieben.

## <a name="initiating-shutdown-sequence"></a>Initiieren der Sequenz zum Herunterfahren

Eine Socketverbindung kann auf verschiedene Weise heruntergenommen werden. [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) *(entspricht* SD \_ SEND oder SD \_ BOTH) und [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) können verwendet werden, um ein ordnungsgemäßes Herunterfahren der Verbindung zu initiieren. [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) kann verwendet werden, um ein ordnungsgemäßes oder abgebrochenes Herunterfahren zu initiieren. Dies hängt von den vom schließenden Socket aufgerufenen Optionen ab. Im Folgenden finden Sie weitere Informationen zu ordnungsgemäßen und abgebrochenen Herunterfahren sowie zu weiteren Optionen.

## <a name="indicating-remote-shutdown"></a>Angeben des Remoteabfahrens

Dienstanbieter geben die Verbindungsentbindung an, die von der Remotepartei über das FD \_ CLOSE-Netzwerkereignis initiiert wird. Das ordnungsgemäße Herunterfahren wird auch über [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) angegeben, wenn die Anzahl der gelesenen Bytes für Bytestreamprotokolle 0 beträgt, oder durch einen Rückgabefehlercode von WSAEDISCON für nachrichtenorientierte Protokolle. In jedem Fall gibt ein **WSPRecv-Rückgabefehlercode** von WSAECONNRESET ein abgebrochenes Herunterfahren an.

## <a name="exchanging-user-data-at-shutdown-time"></a>Austauschen von Benutzerdaten beim Herunterfahren

Zum Zeitpunkt der Verbindungsentsperrung ist es auch möglich (für Protokolle, die dies unterstützen), Benutzerdaten zwischen den Endpunkten auszutauschen. Das Ende, das die Beendigung initiiert, kann [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) aufrufen, um anzugeben, dass keine weiteren Daten gesendet werden sollen und dass die Sequenz zum Beenden der Verbindung initiiert wird. Bei bestimmten Protokollen ist ein Teil dieser Abtrennungssequenz die Übermittlung der Trennung von Daten vom Initiator für das Beenden. Nachdem Sie Benachrichtigung erhalten haben, dass das Remoteend die Beendigungssequenz initiiert hat (in der Regel über die FD \_ CLOSE-Angabe), kann die [**WSPRecvDisconnect-Funktion**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) aufgerufen werden, um die Trennungsdaten (falls vorhanden) zu empfangen.

Sehen Sie sich das folgende Szenario an, um zu veranschaulichen, wie Daten getrennt werden können. Die Clienthälfte einer Client-/Serveranwendung ist für das Beenden einer Socketverbindung verantwortlich. Zufällig mit der Beendigung, die (durch Trennen von Daten) die Gesamtzahl der Transaktionen, die er mit dem Server verarbeitet hat, bereitstellt. Der Server antwortet wiederum mit der kumulativen Gesamtsumme der Transaktionen, die er mit allen Clients verarbeitet hat. Die Reihenfolge der Aufrufe und Hinweise kann wie in der folgenden Tabelle dargestellt auftreten.

| Clientseitig                                                                                                               | Serverseitig                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| (1) Ruft [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) auf, um die Sitzung abzuschließen und die Transaktionssumme zu liefern.            |                                                                                                                                         |
|                                                                                                                           | (2) Ruft FD \_ CLOSE oder [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) mit einem Rückgabewert von 0 (null) oder WSAEDISCON ab, der angibt, dass das ordnungsgemäße Herunterfahren ausgeführt wird. |
|                                                                                                                           | (3) Ruft [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) auf, um die Transaktionssumme des Clients abzurufen.                                         |
|                                                                                                                           | (4) Berechnet die kumulative Gesamtsumme aller Transaktionen.                                                                                |
|                                                                                                                           | (5) Ruft [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) auf, um die Gesamtsumme zu übertragen.                                                   |
| (6) Empfängt die \_ FD CLOSE-Angabe.                                                                                        | (5') Ruft [ **WSPCloseSocket** auf](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                 |
| (7) Ruft [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) auf, um die kumulative Gesamtsumme der Transaktionen zu empfangen und zu speichern. |                                                                                                                                         |
|                                                                                                                           | (8) Ruft [ **WSPCloseSocket** auf](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                  |



 

Schritt (5) muss Schritt (5) folgen, weist jedoch keine zeitliche Beziehung mit den Schritten (6), (7) oder (8) auf.

 

 
