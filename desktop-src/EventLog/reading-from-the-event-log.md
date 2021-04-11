---
description: Eine Ereignisanzeige Anwendung verwendet die OpenEventLog-Funktion, um das Ereignisprotokoll für eine Ereignis Quelle zu öffnen.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Lesen aus dem Ereignisprotokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4642c003d31c986be55a819b513f1c28c784af2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042098"
---
# <a name="reading-from-the-event-log"></a><span data-ttu-id="0505f-103">Lesen aus dem Ereignisprotokoll</span><span class="sxs-lookup"><span data-stu-id="0505f-103">Reading from the Event Log</span></span>

<span data-ttu-id="0505f-104">Eine Ereignisanzeige Anwendung verwendet die [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) -Funktion, um das Ereignisprotokoll für eine Ereignis Quelle zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0505f-104">An event viewer application uses the [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to open the event log for an event source.</span></span> <span data-ttu-id="0505f-105">Die Ereignisanzeige kann dann mit der [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) -Funktion Ereignisdaten Sätze aus dem Protokoll lesen.</span><span class="sxs-lookup"><span data-stu-id="0505f-105">The event viewer can then use the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to read event records from the log.</span></span> <span data-ttu-id="0505f-106">**ReadEventLog** gibt einen Puffer zurück, der eine [**EventLogRecord**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) -Struktur und zusätzliche Informationen enthält, die ein protokolliertes Ereignis beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0505f-106">**ReadEventLog** returns a buffer containing an [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure and additional information that describes a logged event.</span></span> <span data-ttu-id="0505f-107">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="0505f-107">The following diagram illustrates this process.</span></span>

![Lesen aus dem Ereignisprotokoll](images/readlog.png)

<span data-ttu-id="0505f-109">Beispielcode finden Sie unter [Abfragen von Ereignis Informationen](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="0505f-109">For example code, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



