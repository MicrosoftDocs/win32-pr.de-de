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
# <a name="event-log-records"></a><span data-ttu-id="87d81-105">Ereignisprotokoll Datensätze</span><span class="sxs-lookup"><span data-stu-id="87d81-105">Event Log Records</span></span>

<span data-ttu-id="87d81-106">Informationen zu den einzelnen Ereignissen werden im Ereignisprotokoll in einem *Ereignisprotokoll Daten Satz* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="87d81-106">Information about each event is stored in the event log in an *event log record*.</span></span> <span data-ttu-id="87d81-107">Der Ereignisprotokoll Daten Satz enthält Informationen zu Zeit, Typ und Kategorie.</span><span class="sxs-lookup"><span data-stu-id="87d81-107">The event log record includes time, type, and category information.</span></span> <span data-ttu-id="87d81-108">Weitere Informationen finden Sie in der [**EventLogRecord**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="87d81-108">For more information, see the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure.</span></span>

<span data-ttu-id="87d81-109">Der **RecordNumber** -Member von [**EventLogRecord**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) enthält die Datensatznummer für den Ereignisprotokoll Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="87d81-109">The **RecordNumber** member of [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contains the record number for the event log record.</span></span> <span data-ttu-id="87d81-110">Der erste Datensatz, der in ein Ereignisprotokoll geschrieben wird, ist die Datensatznummer 1, und andere Datensätze werden sequenziell nummeriert.</span><span class="sxs-lookup"><span data-stu-id="87d81-110">The very first record written to an event log is record number 1, and other records are numbered sequentially.</span></span> <span data-ttu-id="87d81-111">Wenn die Datensatznummer ULONG \_ Max erreicht, ist die Nummer des nächsten Datensatzes 0, nicht 1. Sie verwenden jedoch 0 (null), um nach dem Datensatz zu suchen.</span><span class="sxs-lookup"><span data-stu-id="87d81-111">If the record number reaches ULONG\_MAX, the next record number will be 0, not 1; however, you use zero to seek to the record.</span></span>

<span data-ttu-id="87d81-112">Wenn der [Aufbewahrungs](eventlog-key.md) Registrierungs Wert auf 0 (null) festgelegt ist, werden die Ereignisdaten Sätze überschrieben, wenn die maximale Protokoll Größe erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="87d81-112">If the [Retention](eventlog-key.md) registry value is set to zero, the event records are overwritten when the maximum log size is reached.</span></span> <span data-ttu-id="87d81-113">Daher ist der älteste Datensatz in einem Ereignisprotokoll möglicherweise nicht die Datensatznummer 1.</span><span class="sxs-lookup"><span data-stu-id="87d81-113">Therefore, the oldest record in an event log may not be record number 1.</span></span> <span data-ttu-id="87d81-114">Um den ältesten Datensatz im Protokoll zu identifizieren, müssen Sie die [**getoldesteventlogrecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="87d81-114">To identify the oldest record in the log, call the [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) function.</span></span> <span data-ttu-id="87d81-115">Sie können dann die [**getnumofeventlogrecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) -Funktion aufrufen und den zurückgegebenen Wert der ältesten Datensatznummer hinzufügen, um den neuesten Datensatz zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="87d81-115">You can then call the [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) function and add the returned value to the oldest record number to determine the newest record.</span></span>

<span data-ttu-id="87d81-116">Mithilfe der [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) -Funktion können Sie einzelne Datensätze aus dem Ereignisprotokoll lesen.</span><span class="sxs-lookup"><span data-stu-id="87d81-116">You can read individual records from the event log using the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function.</span></span> <span data-ttu-id="87d81-117">Weitere Informationen finden Sie unter [Abfragen von Ereignis Informationen](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="87d81-117">For more information, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



