---
description: 'Windows stellt Funktionen bereit, die die folgenden Aufgaben ausführen:'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Objektschnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc85eafdcfe4bb573d3e156b20f9b74dbf0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485246"
---
# <a name="object-interface"></a>Objektschnittstelle

Windows stellt Funktionen bereit, die die folgenden Aufgaben ausführen:

-   Erstellen eines Objekts
-   Objekt Handle erhalten
-   Informationen zum Objekt erhalten
-   Legen Sie Informationen zum Objekt fest.
-   Objekt Handle schließen
-   Objekt zerstören

Einige dieser Aufgaben sind für jedes Objekt nicht erforderlich. Einige dieser Aufgaben werden für bestimmte Objekte kombiniert. Beispielsweise kann eine Anwendung ein Ereignis Objekt erstellen. Andere Anwendungen können das Ereignis öffnen, um ein eindeutiges Handle für dieses Ereignis Objekt zu erhalten. Wenn jede Anwendung mit dem-Ereignis abgeschlossen wird, schließt Sie das Handle für das-Objekt. Wenn keine verbleibenden geöffneten Handles für das Ereignis Objekt vorhanden sind, zerstört das System das Ereignis Objekt. Im Gegensatz dazu kann eine Anwendung ein Handle für ein vorhandenes Fenster Objekt abrufen. Wenn das Window-Objekt nicht mehr benötigt wird, muss die Anwendung das-Objekt zerstören, wodurch das Fenster Handle ungültig wird.

Gelegentlich bleibt ein Objekt im Speicher, nachdem alle Objekt Handles geschlossen wurden. Ein Thread könnte z. b. ein Ereignis Objekt erstellen und auf das Ereignis Handle warten. Während der Thread wartet, könnte ein anderer Thread denselben Ereignis Objekt Handle schließen. Das Ereignis Objekt verbleibt im Arbeitsspeicher, ohne dass Ereignis Objekt Handles vorhanden sind, bis das Ereignis Objekt auf den signalisierten Zustand festgelegt ist und der Warte Vorgang abgeschlossen ist. Zu diesem Zeitpunkt entfernt das System das Objekt aus dem Arbeitsspeicher.

Handles und Objekte belegen Arbeitsspeicher. Um die Systemleistung zu erhalten, sollten Sie daher Handles schließen und Objekte löschen, sobald Sie nicht mehr benötigt werden. Wenn Sie dies nicht tun, kann die Systemleistung aufgrund einer übermäßigen Verwendung der Auslagerungs Datei durch die Anwendung beeinträchtigt werden.

Wenn ein Prozess beendet wird, schließt das System die Handles automatisch und löscht die vom Prozess erstellten Objekte. Wenn jedoch ein Thread beendet wird, schließt das System in der Regel keine Handles oder löscht Objekte. Die einzigen Ausnahmen sind Fenster, Hook, Fensterposition und DDE-Konversations Objekte (Dynamic Data Exchange). Diese Objekte werden zerstört, wenn der Erstellungsthread beendet wird.

 

 



