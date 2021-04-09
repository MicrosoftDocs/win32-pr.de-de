---
description: Informationen zu den einzelnen Ereignissen werden im Ereignisprotokoll in einem Ereignisprotokoll Daten Satz gespeichert. Der Ereignisprotokoll Daten Satz enthält Informationen zu Zeit, Typ und Kategorie. Weitere Informationen finden Sie in der EventLogRecord-Struktur.
ms.assetid: 73731505-97f5-4985-8d00-c6ce8604902d
title: Ereignisprotokoll Datensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cc6caf1011c06eda0dca240bb7a3478c549827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864248"
---
# <a name="event-log-records"></a>Ereignisprotokoll Datensätze

Informationen zu den einzelnen Ereignissen werden im Ereignisprotokoll in einem *Ereignisprotokoll Daten Satz* gespeichert. Der Ereignisprotokoll Daten Satz enthält Informationen zu Zeit, Typ und Kategorie. Weitere Informationen finden Sie in der [**EventLogRecord**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) -Struktur.

Der **RecordNumber** -Member von [**EventLogRecord**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) enthält die Datensatznummer für den Ereignisprotokoll Daten Satz. Der erste Datensatz, der in ein Ereignisprotokoll geschrieben wird, ist die Datensatznummer 1, und andere Datensätze werden sequenziell nummeriert. Wenn die Datensatznummer ULONG \_ Max erreicht, ist die Nummer des nächsten Datensatzes 0, nicht 1. Sie verwenden jedoch 0 (null), um nach dem Datensatz zu suchen.

Wenn der [Aufbewahrungs](eventlog-key.md) Registrierungs Wert auf 0 (null) festgelegt ist, werden die Ereignisdaten Sätze überschrieben, wenn die maximale Protokoll Größe erreicht wird. Daher ist der älteste Datensatz in einem Ereignisprotokoll möglicherweise nicht die Datensatznummer 1. Um den ältesten Datensatz im Protokoll zu identifizieren, müssen Sie die [**getoldesteventlogrecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) -Funktion aufrufen. Sie können dann die [**getnumofeventlogrecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) -Funktion aufrufen und den zurückgegebenen Wert der ältesten Datensatznummer hinzufügen, um den neuesten Datensatz zu ermitteln.

Mithilfe der [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) -Funktion können Sie einzelne Datensätze aus dem Ereignisprotokoll lesen. Weitere Informationen finden Sie unter [Abfragen von Ereignis Informationen](querying-for-event-source-messages.md).

 

 



