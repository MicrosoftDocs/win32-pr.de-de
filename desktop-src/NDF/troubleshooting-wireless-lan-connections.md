---
title: Problembehandlung bei WLAN-Verbindungen
description: In diesem Szenario versucht ein Benutzer, eine Verbindung mit einem WLAN herzustellen, kann aber keine Verbindung herstellen. Sie können Netsh und Netzwerkmonitor verwenden, um Ablaufverfolgungen zu sammeln und anzeigen, um zu ermitteln, warum die Verbindung fehlgeschlagen ist.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3749b3e3a45ef68cb33b7d3658ca346dd4c6e0a8ba8ea11626573f4da6edfbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801823"
---
# <a name="troubleshooting-wireless-lan-connections"></a>Problembehandlung bei WLAN-Verbindungen

In diesem Szenario versucht ein Benutzer, eine Verbindung mit einem WLAN herzustellen, kann aber keine Verbindung herstellen. Sie können Netsh und Netzwerkmonitor verwenden, um Ablaufverfolgungen zu sammeln und anzeigen, um zu ermitteln, warum die Verbindung fehlgeschlagen ist.

Zunächst können Sie netsh verwenden, um eine Ablaufverfolgung zu starten. Wenn Sie **netsh trace start scenario = wlan tracefile=wlanwpp.etl** eingeben, wird die Ablaufverfolgung für alle Anbieter gestartet, die im WLAN-Szenario aktiviert sind, und die Ergebnisse werden in einer Datei namens wlanwpp.etl gespeichert. Nach dem Versuch, eine Verbindung mit dem WLAN herzustellen, wird die Eingabe von **netsh trace stop** beendet und korreliert die Ablaufverfolgungsdatei.

Anschließend können Sie die Datei wlanwpp.etl im Netzwerkmonitor. Die Ereignisse werden im linken Bereich nach Aktivitäts-ID gruppiert.

![Problembehandlung bei WLAN-Verbindungen mithilfe des Netzwerkmonitors (1)](images/1wlan.png)

Die ETL enthält viele Ablaufverfolgungen von anderen Netzwerkanbietern, die aktiviert sind. Sie können einen Filter anwenden, um nur die Ereignisse anzuzeigen, die für den **\_ WLAN-Anbieter MicrosoftWindowsWlanAutoConfig relevant** sind.

![Problembehandlung bei WLAN-Verbindungen mithilfe des Netzwerkmonitors (2)](images/2wlan.png)

Nachdem der Filter angewendet wurde, können Sie die Ereignisse in der Framezusammenfassung überprüfen, um ein Ereignis zu identifizieren, das relevant aussieht. Nachdem Sie das Ereignis ausgewählt haben, klicken Sie mit der rechten Maustaste, zeigen Sie auf Konversationen suchen, und klicken Sie dann auf NetEvent.

![Problembehandlung bei WLAN-Verbindungen mithilfe des Netzwerkmonitors (3)](images/3wlan.png)

Wenn Sie die Elemente unter einer Aktivitäts-ID im linken Bereich erweitern, können Sie alle anderen relevanten Anbieter für den Verbindungsversuch anzeigen. Um die Ereignisse anderer Anbieter anzuzeigen, werden  alle Filter entfernt, indem Sie im Bereich **Filter anzeigen auf Entfernen** klicken. Die Ablaufverfolgungen können analysiert werden, indem Sie durch die Framezusammenfassung scrollen und bei Bedarf zusätzliche Ereignisse auswählen, um weitere Informationen zu sammeln. In diesem Fall enthält der Bereich Framedetails Informationen dazu, dass der Fehler auf einen Schlüsselaustauschfehler zurückgeht. Dies liegt wahrscheinlich daran, dass der Benutzer die falsche Passtaste eingeht.

 

 




