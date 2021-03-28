---
title: Workingsetinformationen
description: Das Workingset eines Prozesses ist die Menge an Arbeitsspeicher, die physisch dem Prozess Kontext zugeordnet ist. PSAPI ermöglicht das Erstellen von Momentaufnahmen des Workingsets oder das Überwachen des Workingsets.
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3942796ec1150dee411d6074b13f9ee2be4a22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102159"
---
# <a name="working-set-information"></a>Workingsetinformationen

Das Workingset eines Prozesses ist die Menge an Arbeitsspeicher, die physisch dem Prozess Kontext zugeordnet ist. PSAPI ermöglicht das Erstellen von Momentaufnahmen des Workingsets oder das Überwachen des Workingsets.

Die [**queryworkingset**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) -oder [**queryworkingsetex**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) -Funktion füllt einen Puffer mit einer Momentaufnahme der Informationen für jede Seite im aktuellen Workingset des angegebenen Prozesses aus. Die-Funktion meldet nur die Seiten, die physisch vorhanden sind, wenn Sie aufgerufen werden.

Mithilfe der workingsetüberwachung können Sie feststellen, wie viel zusätzlicher RAM ein bestimmter Vorgang benötigt (z. b. das Speichern einer Datei). Um mit der Überwachung des Workingsets zu beginnen, müssen Sie die [**initializeprocessforwswatch**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) -Funktion aufrufen. Nicht alle Prozesse ermöglichen es Ihnen, ihre Workingsetinformationen zu lesen. Achten Sie daher darauf, dass die Funktion einen Wert ungleich 0 zurückgibt, bevor Sie fortfahren Als nächstes wird die [**getwschanges**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) -Funktion aufgerufen. Diese Funktion meldet nur die Seiten, die seit der Überwachung des Workingsets in den Arbeitsspeicher geladen wurden. Die-Funktion gibt Daten in einem Array von [**PSAPI \_ WS- \_ Überwachungs \_ Informations**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) Strukturen zurück, eine Struktur für jede neue Seite, die dem Workingset des Prozesses hinzugefügt wird. Die-Struktur gibt Aufschluss darüber, welche Seiten im Arbeitsspeicher vorhanden sind und was bewirkt hat, dass das System Sie ausstellt.

Die [**EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) -Funktion nimmt ein Prozess handle an. Es entfernt so viele Seiten wie möglich aus dem Arbeits Satz des Prozesses. Dieser Vorgang ist hauptsächlich zum Testen und optimieren nützlich. Beachten Sie, dass die Funktion " [**SetProcessWorkingSetSize**](/windows/desktop/api/winbase/nf-winbase-setprocessworkingsetsize) " das gleiche bewirkt, wenn Sie "-1" für die Mindest-und Höchstgröße übergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeitssatz](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 