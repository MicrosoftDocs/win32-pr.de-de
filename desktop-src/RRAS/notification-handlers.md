---
title: Benachrichtigungs Handler
description: Bei einem asynchronen rasdial-Befehl muss ein Benachrichtigungs Handler angegeben werden.
ms.assetid: 6d23d6ac-08ad-4fe2-a4af-021e4d384079
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe735a17de4386bc48648cd20decd218ab102d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948030"
---
# <a name="notification-handlers"></a>Benachrichtigungs Handler

Bei einem asynchronen [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Befehl muss ein Benachrichtigungs Handler angegeben werden. Bei einem asynchronen Verbindungsvorgang verwendet der RAS-Verbindungs-Manager den Benachrichtigungs Handler, um den RAS-Client zu benachrichtigen, wenn sich der [Verbindungsstatus](connection-states.md) ändert oder ein Fehler auftritt.

Die von einem Benachrichtigungs Handler ausgeführten Aktionen können in die folgenden Kategorien unterteilt werden:

-   [Behandeln von Fehlern](handling-ras-errors.md).
-   Das Senden von Feedback an den Benutzer, während der Verbindungsvorgang die verschiedenen Verbindungszustände durchläuft. Siehe [Informations Benachrichtigungen](informational-notifications.md).
-   Behandlung von [angehaltenen Zuständen](paused-states.md).
-   Signalisierung der RAS-Client Anwendung, wenn der Verbindungsvorgang abgeschlossen wurde. Siehe [Abschluss Benachrichtigungen](completion-notifications.md).

Es gibt drei Typen von Benachrichtigungs Handlern, von denen jede die gleichen grundlegenden Informationen erhält: den aktuellen Verbindungsstatus und einen nicht-NULL-Wert, wenn ein Fehler aufgetreten ist.



| Wert                                | Definition                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Rasdialfunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)   | Ein Rückruf Funktionsprototyp, der nur den aktuellen Verbindungsstatus und Fehlercode Informationen empfängt.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) | Ein Rückruf Funktionsprototyp, der zusätzlich zu den grundlegenden Informationen das **hrasconn** -Verbindungs Handle und erweiterte Fehlerinformationen empfängt. Der Parameter für den Verbindungs Handle macht [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) nützlich für Client Anwendungen, die mehrere gleichzeitige Verbindungs Vorgänge unterstützen. Dies ermöglicht es dem Client, dieselbe Rückruffunktion für alle Vorgänge anzugeben, und ermöglicht der Rückruffunktion, zu bestimmen, welche Verbindung sich ändert. |
| [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) | Eine Rückruffunktion, die mit [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)vergleichbar ist. [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) wird jedoch verbessert, um Multilinkverbindungen zu unterstützen.                                                                                                                                                                                                                                                                                                                             |
| Fenster handle                        | Ein Fenster Handle, an das RAS [**WM- \_ rasdialevent**](wm-rasdialevent.md) -Nachrichten sendet, die den aktuellen Verbindungsstatus und Fehlercode Informationen enthalten. Verwenden Sie diese Methode, wenn der Quellcode mit 16-Bit-Fenstern kompatibel sein muss, da 16-Bit-Windows keine der Rückruf Funktionen unterstützt.                                                                                                                                                                            |



 

Der RAS-Verbindungs-Manager hält den Verbindungsvorgang an, bis der Benachrichtigungs Handler zurückgibt. Aus diesem Grund sollte der Handler so schnell wie möglich zurückgeben, es sei denn, es ist ein Fehler aufgetreten.

Die Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " sollte nicht innerhalb eines Benachrichtigungs Handlers aufgerufen werden. Die anderen Remote Zugriffs Funktionen (" [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa)", " [**rasenreentries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa)", " [**rasenumschlag**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa)", " [**rasgeterrorstring**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)" und " [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa)") können innerhalb eines Handlers aufgerufen werden.

 

 




