---
description: 'Windows stellt Funktionen zur Verfügung, die die folgenden Aufgaben ausführen:'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Objektschnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3db15a60d88b8258f5959d2bf4cf447496cbe97ae906bdf087fe316f449b276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763989"
---
# <a name="object-interface"></a>Objektschnittstelle

Windows stellt Funktionen zur Verfügung, die die folgenden Aufgaben ausführen:

-   Erstellen eines Objekts
-   Get an object handle (Objekthand handle)
-   Informationen zum Objekt
-   Festlegen von Informationen zum Objekt
-   Schließen des Objekthandpunkts
-   Zerstören des Objekts

Einige dieser Aufgaben sind nicht für jedes Objekt erforderlich. Einige dieser Aufgaben werden für bestimmte Objekte kombiniert. Beispielsweise kann eine Anwendung ein Ereignisobjekt erstellen. Andere Anwendungen können das Ereignis öffnen, um ein eindeutiges Handle für dieses Ereignisobjekt zu erhalten. Wenn jede Anwendung die Verwendung des -Ereignisses beendet, schließt sie ihr Handle für das -Objekt. Wenn es keine verbleibenden offenen Handles für das Ereignisobjekt gibt, zerstört das System das Ereignisobjekt. Im Gegensatz dazu kann eine Anwendung ein Handle für ein vorhandenes Fensterobjekt abrufen. Wenn das Fensterobjekt nicht mehr benötigt wird, muss die Anwendung das Objekt zerstören, wodurch das Fensterhandy ungültig wird.

Gelegentlich verbleibt ein Objekt im Arbeitsspeicher, nachdem alle Objekthandles geschlossen wurden. Beispielsweise könnte ein Thread ein Ereignisobjekt erstellen und auf das Ereignishand handle warten. Während der Thread wartet, könnte ein anderer Thread dasselbe Ereignisobjekthand handle schließen. Das Ereignisobjekt verbleibt im Arbeitsspeicher ohne Ereignisobjekthandles, bis das Ereignisobjekt auf den signalisierten Zustand festgelegt ist und der Wartevorgang abgeschlossen ist. Zu diesem Zeitpunkt entfernt das System das Objekt aus dem Arbeitsspeicher.

Handles und Objekte verbrauchen Arbeitsspeicher. Daher sollten Sie Handles schließen und Objekte löschen, sobald sie nicht mehr benötigt werden, um die Systemleistung zu erhalten. Wenn Sie dies nicht tun, kann Ihre Anwendung die Systemleistung beeinträchtigen, da die Auslagerungsdatei übermäßig verwendet wird.

Wenn ein Prozess beendet wird, schließt das System automatisch Handles und löscht vom Prozess erstellte Objekte. Wenn ein Thread beendet wird, schließt das System jedoch in der Regel keine Handles und löscht keine Objekte. Die einzigen Ausnahmen sind Fenster-, Hook-, Fensterpositions- und DDE-Konversationsobjekte (Dynamic Data Exchange). diese Objekte werden zerstört, wenn der erstellende Thread beendet wird.

 

 



