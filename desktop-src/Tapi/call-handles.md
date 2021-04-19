---
description: Wie in der Übersicht über Sitzungs Bezeichner erwähnt, ist ein Rückruf handle das Mittel, mit dem eine TAPI 2,2-Anwendung eine bestimmte Kommunikationssitzung identifiziert.
ms.assetid: 5f6a7adf-c074-4bf6-9828-76604eb7609c
title: Rückruf Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacad5b73d9d22caa006b734acaf8b992203d7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348812"
---
# <a name="call-handles"></a>Rückruf Handles

Wie in der Übersicht über [Sitzungs Bezeichner](./session-identifier-ovr.md) erwähnt, ist ein Rückruf handle das Mittel, mit dem eine TAPI 2,2-Anwendung eine bestimmte Kommunikationssitzung identifiziert. Wenn eine Anwendung eine Sitzung initiiert, gibt TAPI ein Rückruf Handle zur Verwendung in weiteren Vorgängen oder Abfragen zurück. Wenn eine Anwendung über eine eingehende Sitzung benachrichtigt wird, übergibt TAPI auch ein "callhandle".

Nachdem eine Sitzung beendet wurde und sich der Sitzungszustand im Leerlauf befindet, bleibt das Telefon Handle gültig, bis die Anwendung das Handle zuweist oder die Zeile geschlossen wird. Die Zeile wird möglicherweise von der Anwendung geschlossen, oder es wird eine Meldung zum [**\_ Schließen**](line-close.md) der Nachricht empfangen. Wenn eine Zeile geschlossen wird, werden alle Aufruf Handles für Aufrufe in der Zeile sofort ungültig.

Nachdem ein-Rückruf in den *Leerlauf* Zustand wechselt, kann die Anwendung die Informationsstruktur und den Status des Aufrufes weiterhin lesen. Dies ermöglicht es Anwendungen, Vorgänge wie [**linegetcallinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) zum Abrufen von Aufruf Informationen zu Protokollierungs Zwecken zu verwenden.

Wenn die Anwendung nicht mehr für das Handle eines im Leerlauf befindlichen Aufrufes verwendet wird, muss Sie [**linedebelegungecall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) aufrufen, um den vom-Anruf im Zusammenhang mit dem-Befehl zugeordneten Speicher freizugeben. TAPI ordnet für jede Anwendung, die über ein Handle für den-Befehl verfügt, Arbeitsspeicher zu. Es ist wahrscheinlich, dass Dienstanbieter auch Speicher zum Speichern von Telefon Informationen zuweisen. Durch die Aufhebung der Zuordnung des-aufrufhandles einer Anwendung können die Bibliothek und der Dienstanbieter diese Speicherressourcen freigeben. Das Handle einer Anwendung für einen-Aufrufvorgang wird nach einer erfolgreichen Aufhebung der Zuordnung ungültig.

Die Anwendung muss selbst Speicher freigeben, der sich auf den-Rückruf bezieht, den Sie für Ihre eigenen Zwecke zugeordnet hat.

 

 
