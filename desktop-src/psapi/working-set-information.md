---
title: Informationen zum Arbeitssatz
description: Der Arbeitssatz eines Prozesses ist die Menge an Arbeitsspeicher, die dem Prozesskontext physisch zugeordnet ist. Mit PSAPI können Sie Momentaufnahmen des Arbeitssets erstellen oder den Arbeitssatz überwachen.
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6003886d50cb47b128bfce92cba4c28950ee078dbe13499d8909676d938aad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032978"
---
# <a name="working-set-information"></a>Informationen zum Arbeitssatz

Der Arbeitssatz eines Prozesses ist die Menge an Arbeitsspeicher, die dem Prozesskontext physisch zugeordnet ist. Mit PSAPI können Sie Momentaufnahmen des Arbeitssets erstellen oder den Arbeitssatz überwachen.

Die [**QueryWorkingSet-**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) oder [**QueryWorkingSetEx-Funktion**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) füllt einen Puffer mit einer Momentaufnahme der Informationen für jede Seite im aktuellen Arbeitssatz des angegebenen Prozesses. Die Funktion meldet nur die Seiten, die zu dem Zeitpunkt physisch vorhanden sind, zu dem sie aufgerufen wird.

Sie können die Arbeitssatzüberwachung verwenden, um herauszufinden, wie viel zusätzlicher RAM ein bestimmter Vorgang benötigt (z. B. speichern einer Datei). Um mit der Überwachung des Arbeitssets zu beginnen, rufen Sie die [**InitializeProcessForWsWatch-Funktion**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) auf. Nicht bei allen Prozessen können Sie ihre Arbeitssatzinformationen lesen. Stellen Sie daher sicher, dass die Funktion einen Wert ungleich 0 (null) zurückgibt, bevor Sie fortfahren. Rufen Sie als Nächstes die [**GetWsChanges-Funktion**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) auf. Diese Funktion meldet nur die Seiten, die seit beginn der Überwachung des Arbeitssets in den Arbeitsspeicher geladen wurden. Die Funktion gibt Daten in einem Array von [**\_ PSAPI WS \_ WATCH \_ INFORMATION-Strukturen**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) zurück, eine Struktur für jede neue Seite, die dem Arbeitssatz des Prozesses hinzugefügt wird. Die -Struktur teilt Ihnen mit, welche Seiten sich im Arbeitsspeicher befinden und was das System dazu führte, dass sie ausblättern.

Die [**EmptyWorkingSet-Funktion**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) verwendet ein Prozesshandle. Es werden so viele Seiten wie möglich aus dem Prozessarbeitssatz entfernt. Dieser Vorgang ist in erster Linie für Tests und Optimierungen nützlich. Beachten [**Sie, dass die SetProcessWorkingSetSize-Funktion**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) dasselbe macht, wenn Sie -1 für die minimale und maximale Größe übergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeitssatz](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 