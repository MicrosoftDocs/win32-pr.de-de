---
title: Problembehandlung für drahtlose LAN-Verbindungen
description: In diesem Szenario versucht ein Benutzer, eine Verbindung mit einem drahtlosen LAN herzustellen, kann jedoch keine Verbindung herstellen. Mithilfe von Netsh und Netzwerkmonitor können Sie Ablauf Verfolgungen erfassen und anzeigen, um zu ermitteln, warum die Verbindung nicht hergestellt werden konnte.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55878afcee0091634415d4dbc465d1b143f46057
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037435"
---
# <a name="troubleshooting-wireless-lan-connections"></a>Problembehandlung für drahtlose LAN-Verbindungen

In diesem Szenario versucht ein Benutzer, eine Verbindung mit einem drahtlosen LAN herzustellen, kann jedoch keine Verbindung herstellen. Mithilfe von Netsh und Netzwerkmonitor können Sie Ablauf Verfolgungen erfassen und anzeigen, um zu ermitteln, warum die Verbindung nicht hergestellt werden konnte.

Zuerst können Sie mit Netsh eine Ablauf Verfolgung starten. Wenn Sie **Netsh Trace Start Scenario = WLAN Tracefile = wlanwpp. ETL** eingeben, wird die Ablauf Verfolgung für alle Anbieter gestartet, die im WLAN-Szenario aktiviert sind, und die Ergebnisse werden in einer Datei namens wlanwpp. ETL gespeichert. Wenn Sie versuchen, eine Verbindung mit dem drahtlosen LAN herzustellen, wird die Eingabe von **Netsh Trace beenden** beendet und die Ablauf Verfolgungs Datei korreliert.

Anschließend können Sie die Datei wlanwpp. ETL in Netzwerkmonitor öffnen. Die Ereignisse werden im linken Bereich nach der Aktivitäts-ID gruppiert.

![Problembehandlung bei drahtlosen LAN-Verbindungen mithilfe des Netzwerk Monitors (1)](images/1wlan.png)

Die ETL enthält viele Ablauf Verfolgungen von anderen aktivierten Netzwerkanbietern. Sie können einen Filter anwenden, um nur die Ereignisse anzuzeigen, die für den **WLAN- \_ microsoftwindowtauautoconfig** -Anbieter relevant sind.

![Problembehandlung bei drahtlosen LAN-Verbindungen mithilfe des Netzwerk Monitors (2)](images/2wlan.png)

Nachdem der Filter angewendet wurde, können Sie die Ereignisse in der Frame Zusammenfassung überprüfen, um ein Ereignis zu identifizieren, das relevant ist. Nachdem Sie das Ereignis ausgewählt haben, klicken Sie mit der rechten Maustaste, zeigen Sie auf Konversationen suchen, und klicken Sie auf netevent

![Problembehandlung bei drahtlosen LAN-Verbindungen mithilfe des Netzwerk Monitors (3)](images/3wlan.png)

Wenn Sie die Elemente unter einer Aktivitäts-ID im linken Bereich erweitern, können Sie alle anderen relevanten Anbieter für den Verbindungsversuch anzeigen. Um die Ereignisse von anderen Anbietern anzuzeigen, werden alle Filter entfernt, indem Sie im **Anzeige Filter** Bereich auf **Entfernen** klicken. Die Ablauf Verfolgungen können analysiert werden, indem Sie durch die Frame Zusammenfassung scrollen und nach Bedarf weitere Ereignisse auswählen, um weitere Informationen zu erhalten. In diesem Fall enthält der Bereich "Frame Details" Informationen, dass der Fehler aufgrund eines Schlüsselaustausch Fehlers verursacht wird. Dies liegt wahrscheinlich daran, dass der Benutzer die falsche Pass-Taste eingegeben hat.

 

 




