---
description: Jedes Ereignisprotokoll enthält einen Header (dargestellt durch die elf- \_ logfile- \_ Header Struktur) mit fester Größe, gefolgt von einer Variablen Anzahl von Ereignisdaten Sätzen (dargestellt durch EventLogRecord-Strukturen) und einem dateiendedatensatz (dargestellt durch die elf \_ EOF- \_ Daten Satzstruktur).
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: Format der Ereignisprotokoll Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4ba5c8bc0114e319107272e706801544e3effa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528751"
---
# <a name="event-log-file-format"></a><span data-ttu-id="2d3dc-103">Format der Ereignisprotokoll Datei</span><span class="sxs-lookup"><span data-stu-id="2d3dc-103">Event Log File Format</span></span>

<span data-ttu-id="2d3dc-104">Jedes Ereignisprotokoll enthält einen Header (dargestellt durch die [**elf- \_ logfile- \_ Header**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) Struktur) mit fester Größe, gefolgt von einer Variablen Anzahl von Ereignisdaten Sätzen (dargestellt durch [**EventLogRecord**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) -Strukturen) und einem dateiendedatensatz (dargestellt durch die [**elf \_ EOF- \_ Daten Satz**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) Struktur).</span><span class="sxs-lookup"><span data-stu-id="2d3dc-104">Each event log contains a header (represented by the [**ELF\_LOGFILE\_HEADER**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) structure) that has a fixed size, followed by a variable number of event records (represented by [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) structures), and an end-of-file record (represented by the [**ELF\_EOF\_RECORD**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) structure).</span></span>

<span data-ttu-id="2d3dc-105">Die **elf \_ logfile- \_ Header** Struktur und die **elf \_ EOF- \_ Daten Satz** Struktur werden im Ereignisprotokoll geschrieben, wenn das Ereignisprotokoll erstellt wird, und werden jedes Mal aktualisiert, wenn ein Ereignis in das Protokoll geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-105">The **ELF\_LOGFILE\_HEADER** structure and the **ELF\_EOF\_RECORD** structure are written in the event log when the event log is created and are updated each time an event is written to the log.</span></span>

<span data-ttu-id="2d3dc-106">Wenn eine Anwendung die [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) -Funktion aufruft, um einen Eintrag in das Ereignisprotokoll zu schreiben, übergibt das System die Parameter an den Ereignis Protokollierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-106">When an application calls the [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) function to write an entry to the event log, the system passes the parameters to the event-logging service.</span></span> <span data-ttu-id="2d3dc-107">Der Ereignis Protokollierungs Dienst verwendet die Informationen, um eine **EventLogRecord** -Struktur in das Ereignisprotokoll zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-107">The event-logging service uses the information to write an **EVENTLOGRECORD** structure to the event log.</span></span> <span data-ttu-id="2d3dc-108">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-108">The following diagram illustrates this process.</span></span>

![Schreiben einer Protokolldatei](images/evreport.png)

<span data-ttu-id="2d3dc-110">Die Ereignisdaten Sätze sind auf eine der folgenden Arten organisiert:</span><span class="sxs-lookup"><span data-stu-id="2d3dc-110">The event records are organized in one of the following ways:</span></span>

-   <span data-ttu-id="2d3dc-111">Nicht Umbrüchen.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-111">Non-wrapping.</span></span> <span data-ttu-id="2d3dc-112">Der älteste Datensatz liegt unmittelbar nach dem Ereignisprotokoll Header und neuen Datensätzen nach dem letzten hinzugefügten Datensatz (vor dem **elf- \_ EOF- \_ Datensatz**).</span><span class="sxs-lookup"><span data-stu-id="2d3dc-112">The oldest record is immediately after the event log header and new records are added after the last record that was added (before the **ELF\_EOF\_RECORD**).</span></span> <span data-ttu-id="2d3dc-113">Das folgende Beispiel zeigt die nicht Wrapping Methode:</span><span class="sxs-lookup"><span data-stu-id="2d3dc-113">The following example shows the non-wrapping method:</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    <span data-ttu-id="2d3dc-114">Eine nicht-Wrapping kann auftreten, wenn das Ereignisprotokoll erstellt wird oder wenn das Ereignisprotokoll gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-114">Non-wrapping can occur when the event log is created or when the event log is cleared.</span></span> <span data-ttu-id="2d3dc-115">Das Ereignisprotokoll wird weiterhin nicht umwickelt, bis die Größenbeschränkung für das Ereignisprotokoll erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-115">The event log continues to be non-wrapping until the event log size limit is reached.</span></span> <span data-ttu-id="2d3dc-116">Die Größe des Ereignis Protokolls wird entweder durch den **MaxSize** -Konfigurations Wert oder durch die Menge der Systemressourcen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-116">The event log size is limited by either the **MaxSize** configuration value or the amount of system resources.</span></span>

    <span data-ttu-id="2d3dc-117">Wenn das Größenlimit für das Ereignisprotokoll erreicht wird, beginnt es möglicherweise mit der Umbrüchen.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-117">When the event log size limit is reached, it might start wrapping.</span></span> <span data-ttu-id="2d3dc-118">Das umwickeln wird durch den Wert für die **Beibehaltungs** Konfiguration gesteuert.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-118">Wrapping is controlled by the **Retention** configuration value.</span></span> <span data-ttu-id="2d3dc-119">Weitere Informationen zu den Konfigurations Werten für das Ereignisprotokoll finden Sie unter [EventLog Key](eventlog-key.md).</span><span class="sxs-lookup"><span data-stu-id="2d3dc-119">For more information about the event log configuration values, see [Eventlog Key](eventlog-key.md).</span></span>

-   <span data-ttu-id="2d3dc-120">Wrapping.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-120">Wrapping.</span></span> <span data-ttu-id="2d3dc-121">Die Datensätze werden als Zirkel Puffer organisiert.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-121">The records are organized as a circular buffer.</span></span> <span data-ttu-id="2d3dc-122">Wenn neue Datensätze hinzugefügt werden, werden die ältesten Datensätze ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-122">As new records are added, the oldest records are replaced.</span></span> <span data-ttu-id="2d3dc-123">Der Speicherort der ältesten und neuesten Datensätze variiert.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-123">The location of the oldest and newest records will vary.</span></span> <span data-ttu-id="2d3dc-124">Das folgende Beispiel zeigt die Wrapping Methode.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-124">The following example shows the wrapping method.</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    EVENT RECORD 301         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 400         (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    Wasted space
    EVENT RECORD 102         (EVENTLOGRECORD)
    EVENT RECORD 103         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 299         (EVENTLOGRECORD)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    ```

    <span data-ttu-id="2d3dc-125">Im Beispiel ist der älteste Datensatz nicht mehr 1, sondern 102, da der Speicherplatz für die Datensätze 1 bis 101 überschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-125">In the example the oldest record is no longer 1, but is 102 because the space for records 1 to 101 was overwritten.</span></span>

    <span data-ttu-id="2d3dc-126">Zwischen dem **elf \_ EOF- \_ Datensatz** und dem ältesten Datensatz liegt ein Speicherplatz vor, da das System eine ganzzahlige Anzahl von Datensätzen löscht, um Speicherplatz für den neuesten Datensatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-126">There is some space between the **ELF\_EOF\_RECORD** and the oldest record because the system will erase an integral number of records to free space for the newest record.</span></span> <span data-ttu-id="2d3dc-127">Wenn der neueste Datensatz z. b. 100 Byte lang ist und die zwei ältesten Datensätze 75 Bytes lang sind, entfernt das System die beiden ältesten Datensätze.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-127">For example, if the newest record is 100 bytes long and the two oldest records are 75 bytes long, then the system will remove the two oldest records.</span></span> <span data-ttu-id="2d3dc-128">Die zusätzlichen 50 Bytes werden später verwendet, wenn neue Datensätze geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-128">The extra 50 bytes will be used later when new records are written.</span></span>

    <span data-ttu-id="2d3dc-129">Eine Ereignisprotokoll Datei hat eine festgelegte Größe, und wenn die Datensätze in der Datei wrappen, wird der Datensatz am Ende der Datei in der Regel in zwei Datensätze aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-129">An event log file has a fixed size and when the records in the file wrap, the record at the end of the file will typically be split into two records.</span></span> <span data-ttu-id="2d3dc-130">Wenn die Position für den nächsten Schreibvorgang z. b. 100 Bytes vom Dateiende und die Größe des Datensatzes 300 Bytes beträgt, werden die ersten 100 Bytes am Ende der Datei geschrieben, und die nächsten 200 Bytes werden am Anfang der Datei unmittelbar nach dem **elf- \_ logfile- \_ Header** geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-130">For example, if the position for the next write is 100 bytes from the end of the file and the size of the record is 300 bytes, the first 100 bytes will be written at the end of the file and the next 200 bytes will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="2d3dc-131">Wenn der verfügbare Speicherplatz am Ende der Datei kleiner ist als der festgelegte Teil von **EventLogRecord** (0x38 Bytes), werden alle neuen Datensätze am Anfang der Datei unmittelbar nach dem **elf- \_ logfile- \_ Header** geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-131">If the available space at the end of the file is less than the fixed portion of the **EVENTLOGRECORD** (0x38 bytes), all of the new record will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="2d3dc-132">Die nicht verwendeten Bytes am Ende der Datei werden mit dem Muster 0x00000027 aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="2d3dc-132">The unused bytes at the end of the file will be filled with the pattern 0x00000027.</span></span>

<span data-ttu-id="2d3dc-133">Weitere Informationen und ein Codebeispiel finden Sie unter [Berichterstellung für ein Ereignis](reporting-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="2d3dc-133">For more information and a code example, see [Reporting an Event](reporting-an-event.md).</span></span>

 

 
