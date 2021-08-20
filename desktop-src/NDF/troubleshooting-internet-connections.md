---
title: Problembehandlung bei Internetverbindungen
description: In diesem Szenario versucht ein Benutzer, mithilfe des HTTPS-Protokolls zu www.msn.com zu navigieren, kann aber keine Verbindung herstellen. Sie können Netsh und Netzwerkmonitor verwenden, um Ablaufverfolgungen zu erfassen und anzuzeigen, um zu ermitteln, warum die Verbindung fehlgeschlagen ist.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fadeefe0413a5a6be5d3ec7f5676ef346e21bc1f4b9e4c3cca026b54d761784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133397"
---
# <a name="troubleshooting-internet-connections"></a>Problembehandlung bei Internetverbindungen

In diesem Szenario versucht ein Benutzer, mithilfe des HTTPS-Protokolls zu www.msn.com zu navigieren, kann aber keine Verbindung herstellen. Sie können Netsh und Netzwerkmonitor verwenden, um Ablaufverfolgungen zu erfassen und anzuzeigen, um zu ermitteln, warum die Verbindung fehlgeschlagen ist.

Zunächst können Sie netsh verwenden, um eine Ablaufverfolgung zu starten. Eingabe von **netsh trace start scenario = InternetClient tracefile=msn.etl** startet die Ablaufverfolgung für alle Anbieter, die im InternetClient-Szenario aktiviert sind, und speichert die Ergebnisse in einer Datei namens msn.etl. Nachdem Sie mithilfe eines Webbrowsers versucht haben, www.msn.com zu erreichen, wird die Eingabe von **netsh trace stop** beendet und korreliert die Ablaufverfolgungsdatei.

Sie können dann die Datei msn.etl in Netzwerkmonitor öffnen. Die Ereignisse werden im linken Bereich nach Aktivitäts-ID gruppiert. Wenn Sie den Filter **description.contains("msn")** verwenden, werden nur die Ereignisse angezeigt, die die Zeichenfolge "msn" in ihrer Protokollbeschreibung enthalten.

![Problembehandlung bei Internetverbindungen mithilfe des Netzwerkmonitors (1)](images/internetclient1.png)

Als Nächstes können Sie die Ereignisse in der Rahmenzusammenfassung überprüfen, um ein Ereignis zu identifizieren, das relevant aussieht. Nachdem Sie das Ereignis ausgewählt haben, klicken Sie mit der rechten Maustaste, zeigen Sie auf Konversationen suchen, und klicken Sie dann auf UTEvent, um die Konversation auf UTEvent-Ebene auszuwählen.

![Problembehandlung bei Internetverbindungen mithilfe des Netzwerkmonitors (2)](images/internetclient2.png)

Die zugeordnete normalisierte Aktivität im linken Bereich wird dann hervorgehoben, in diesem Fall UTEvent ActivityID 397.

![Problembehandlung bei Internetverbindungen mithilfe des Netzwerkmonitors (3)](images/internetclient3.png)

Durch die Verwendung Netzwerkmonitor zum Anzeigen und Filtern der Ablaufverfolgungsinformationen wurde die Anzahl der zu untersuchende Ereignisse von 1989 auf 96 reduziert.

 

 




