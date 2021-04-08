---
title: Problembehandlung bei Internet Verbindungen
description: In diesem Szenario versucht ein Benutzer, www.MSN.com über das HTTPS-Protokoll zu suchen, kann jedoch keine Verbindung herstellen. Mithilfe von Netsh und Netzwerkmonitor können Sie Ablauf Verfolgungen erfassen und anzeigen, um zu ermitteln, warum die Verbindung nicht hergestellt werden konnte.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753636c1186243a96e3cef5a4ab73244556daec4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855912"
---
# <a name="troubleshooting-internet-connections"></a>Problembehandlung bei Internet Verbindungen

In diesem Szenario versucht ein Benutzer, www.MSN.com über das HTTPS-Protokoll zu suchen, kann jedoch keine Verbindung herstellen. Mithilfe von Netsh und Netzwerkmonitor können Sie Ablauf Verfolgungen erfassen und anzeigen, um zu ermitteln, warum die Verbindung nicht hergestellt werden konnte.

Zuerst können Sie mit Netsh eine Ablauf Verfolgung starten. Wenn Sie **Netsh Trace Start Scenario = Internetclient Tracefile = MSN. ETL** eingeben, wird die Ablauf Verfolgung für alle unter dem Internet Client-Szenario aktivierten Anbieter gestartet, wobei die Ergebnisse in einer Datei namens MSN. ETL gespeichert werden. Nachdem Sie mithilfe eines Webbrowsers versucht haben, www.MSN.com zu erreichen, wird die Eingabe von **Netsh Trace beenden** beendet und die Ablauf Verfolgungs Datei korreliert.

Sie können dann die Datei msn. ETL in Netzwerkmonitor öffnen. Die Ereignisse werden im linken Bereich nach der Aktivitäts-ID gruppiert. Mithilfe der Filter **Beschreibung. enthält ("MSN")** zeigt nur die Ereignisse an, die die Zeichenfolge "MSN" in ihrer Protokoll Beschreibung enthalten.

![Problembehandlung bei Internetverbindungen mithilfe des Netzwerk Monitors (1)](images/internetclient1.png)

Als nächstes können Sie die Ereignisse in der Frame Zusammenfassung überprüfen, um ein Ereignis zu identifizieren, das relevant aussieht. Nachdem Sie das Ereignis ausgewählt haben, klicken Sie mit der rechten Maustaste, und zeigen Sie auf Konversationen suchen, und klicken Sie dann auf utevent, um die Konversation auf der utevent

![Problembehandlung bei Internetverbindungen mithilfe des Netzwerk Monitors (2)](images/internetclient2.png)

Die zugeordnete normalisierte Aktivität im linken Bereich wird dann hervorgehoben, in diesem Fall utevent ActivityId 397.

![Problembehandlung bei Internetverbindungen mithilfe des Netzwerk Monitors (3)](images/internetclient3.png)

Wenn Sie Netzwerkmonitor verwenden, um die Ablauf Verfolgungs Informationen anzuzeigen und zu filtern, wurde die Anzahl der zu überprüfenden Ereignisse von 1989 auf 96 reduziert.

 

 




