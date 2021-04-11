---
title: Speichern von Ereignissen in einer Protokolldatei
description: Um Ereignisse von einem Kanal in einer Protokolldatei zu speichern, müssen Sie die evtclearlog-oder die evtexportlog-Funktion aufrufen.
ms.assetid: 6d71ed15-97e3-4888-b161-c7e31bf3fc6d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3295d8a7a235fbb5fd5857d1b7283e9ca1fbb773
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207207"
---
# <a name="saving-events-to-a-log-file"></a><span data-ttu-id="c540a-103">Speichern von Ereignissen in einer Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="c540a-103">Saving Events to a Log File</span></span>

<span data-ttu-id="c540a-104">Um Ereignisse von einem Kanal in einer Protokolldatei zu speichern, müssen Sie die [**evtclearlog**](/windows/desktop/api/WinEvt/nf-winevt-evtclearlog) -oder die [**evtexportlog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c540a-104">To save events from a channel to a log file, call the [**EvtClearLog**](/windows/desktop/api/WinEvt/nf-winevt-evtclearlog) or [**EvtExportLog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) function.</span></span> <span data-ttu-id="c540a-105">Die Funktion " [**evtclearlog**](/windows/desktop/api/WinEvt/nf-winevt-evtclearlog) " kopiert die Ereignisse in die Protokolldatei und löscht sie aus dem Kanal.</span><span class="sxs-lookup"><span data-stu-id="c540a-105">The [**EvtClearLog**](/windows/desktop/api/WinEvt/nf-winevt-evtclearlog) function copies the events to the log file and deletes them from the channel.</span></span> <span data-ttu-id="c540a-106">Die [**evtexportlog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) -Funktion kopiert die Ereignisse auch in die Protokolldatei, löscht sie aber nicht aus dem Kanal.</span><span class="sxs-lookup"><span data-stu-id="c540a-106">The [**EvtExportLog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) function also copies the events to the log file but does not delete them from the channel.</span></span> <span data-ttu-id="c540a-107">Zum Löschen eines Kanals muss der Benutzer über die Berechtigungen Lesen und Löschen verfügen.</span><span class="sxs-lookup"><span data-stu-id="c540a-107">To clear a channel, the user must have Read and Clear permissions.</span></span>

<span data-ttu-id="c540a-108">Sie können Ereignisse aus der von Ihnen erstellten Protokolldatei Abfragen. zum Rendering der Ereignisse muss der Anbieter jedoch auf dem Computer registriert werden.</span><span class="sxs-lookup"><span data-stu-id="c540a-108">You can query events from the log file that you created; however, to render the events, the provider must be registered on the computer.</span></span> <span data-ttu-id="c540a-109">Zum Rendering von Ereignissen aus einer Protokolldatei, wenn der Anbieter nicht auf dem Computer registriert ist, müssen Sie das [**evtarchiveexportedlog-Objekt**](/windows/desktop/api/WinEvt/nf-winevt-evtarchiveexportedlog), das die Ressourcen aus dem Anbieter kopiert und in die Protokolldatei einfügt, abrufen.</span><span class="sxs-lookup"><span data-stu-id="c540a-109">To render events from a log file when the provider is not registered on the computer, you must call the [**EvtArchiveExportedLog**](/windows/desktop/api/WinEvt/nf-winevt-evtarchiveexportedlog), which copies the resources from the provider and adds them to the log file.</span></span> <span data-ttu-id="c540a-110">Anschließend können Sie die Protokolldatei auf einen beliebigen Computer kopieren und deren Ereignisse erfolgreich Abfragen und Rendering.</span><span class="sxs-lookup"><span data-stu-id="c540a-110">You can then copy the log file to any computer and successfully query and render its events.</span></span>

<span data-ttu-id="c540a-111">Zusätzlich zur Verwendung von [**evtexportlog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) zum Kopieren von Ereignissen aus einem Kanal können Sie es auch zum erneuten Protokollieren von Ereignissen aus einer Protokolldatei in eine andere Protokolldatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="c540a-111">In addition to using [**EvtExportLog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) to copy events from a channel, you can also use it to relog events from one log file to another log file.</span></span> <span data-ttu-id="c540a-112">Sie können Sie auch verwenden, um Ereignisse aus mehreren Kanälen zusammenzuführen, wenn Sie eine strukturierte XML-Abfrage verwenden, aber Sie können Sie nicht verwenden, um Ereignisse aus mehreren Protokolldateien zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="c540a-112">You can also use it to merge events from multiple channels if you use a structured XML query but you cannot use it to merge events from multiple log files.</span></span>

<span data-ttu-id="c540a-113">Im folgenden Beispiel wird gezeigt, wie Ereignisse von einem Kanal in eine Protokolldatei kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="c540a-113">The following example shows how to copy events from a channel to a log file.</span></span> <span data-ttu-id="c540a-114">Im Beispiel werden dann bestimmte Ereignisse aus der neu erstellten Protokolldatei in einer neuen Protokolldatei neu protokolliert.</span><span class="sxs-lookup"><span data-stu-id="c540a-114">The example then relogs specific events from the newly created log file to a new log file.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10

DWORD DumpEvents(LPCWSTR pwsLogFile);
DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    LPWSTR pPath = L"<path to channel goes here>";
    LPWSTR pQuery = NULL;
    LPWSTR pTargetLogFile = L".\\log.evtx";

    // Export all the events in the specified channel to the target log file.
    if (!EvtExportLog(NULL, pPath, pQuery, pTargetLogFile, EvtExportLogChannelPath))
    {
        wprintf(L"EvtExportLog failed for initial export with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Dump the events from the log file.
    wprintf(L"Events from %s log file\n\n", pTargetLogFile);
    DumpEvents(pTargetLogFile);

    // Create a new log file that will contain all events from the specified 
    // log file where the event ID is 2.
    pPath =  L".\\log.evtx";
    pQuery = L"Event/System[EventID=2]";
    pTargetLogFile = L".\\log2.evtx";

    // Export all events from the specified log file that have an ID of 2 and
    // write them to a new log file.
    if (!EvtExportLog(NULL, pPath, pQuery, pTargetLogFile, EvtExportLogFilePath))
    {
        wprintf(L"EvtExportLog failed for relog with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Dump the events from the log file.
    wprintf(L"\n\n\nEvents from %s log file\n\n", pTargetLogFile);
    DumpEvents(pTargetLogFile);

cleanup:

    return;
}


// Dump all the events in the from the log file.
DWORD DumpEvents(LPCWSTR pwsPath)
{
    EVT_HANDLE hResults = NULL;
    DWORD status = ERROR_SUCCESS;

    hResults = EvtQuery(NULL, pwsPath, NULL, EvtQueryFilePath);
    if (NULL == hResults)
    {
        wprintf(L"EvtQuery failed with %lu.\n", status = GetLastError());
        goto cleanup;
    }

    status = PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

    return status;
}


// Enumerate all the events in the result set. 
DWORD PrintResults(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hEvents[ARRAY_SIZE];
    DWORD dwReturned = 0;

    while (true)
    {
        // Get a block of events from the result set.
        if (!EvtNext(hResults, ARRAY_SIZE, hEvents, INFINITE, 0, &dwReturned))
        {
            if (ERROR_NO_MORE_ITEMS != (status = GetLastError()))
            {
                wprintf(L"EvtNext failed with %lu\n", status);
            }

            goto cleanup;
        }

        // For each event, call the PrintEvent function which renders the
        // event for display. PrintEvent is shown in RenderingEvents.
        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (ERROR_SUCCESS == (status = PrintEvent(hEvents[i])))
            {
                EvtClose(hEvents[i]);
                hEvents[i] = NULL;
            }
            else
            {
                goto cleanup;
            }
        }
    }

cleanup:

    // Executed only if there was an error.
    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}


// Print the event as an XML string.
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

    // The EvtRenderEventXml flag tells EvtRender to render the event as an XML string.
    if (!EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedContent = (LPWSTR)malloc(dwBufferSize);
            if (pRenderedContent)
            {
                EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

    wprintf(L"\n\n%s", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}
```



<span data-ttu-id="c540a-115">Im folgenden Beispiel wird gezeigt, wie ein Ereignis aus mehreren Kanälen mithilfe einer strukturierten XML-Abfrage zusammengeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c540a-115">The following example shows how to merge event from multiple channels using a structured XML query.</span></span> <span data-ttu-id="c540a-116">Im Beispiel wird die Main-Prozedur aus dem vorherigen Beispiel ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c540a-116">The example replaces the main procedure from the previous example.</span></span>


```C++
void main(void)
{
    DWORD status = ERROR_SUCCESS;
    LPWSTR pTargetLogFile = L".\\log.evtx";
    LPWSTR pQuery = L"<QueryList>"
                    L"  <Query Id='0'>"
                    L"    <Select Path='<path to channel goes here>'>*</Select>"
                    L"  </Query>"
                    L"  <Query Id='1'>"
                    L"    <Select Path='<path to channel goes here>'>*</Select>"
                    L"  </Query>"
                    L"</QueryList>";

    if (!EvtExportLog(NULL, NULL, pQuery, pTargetLogFile, EvtExportLogChannelPath)) 
    {
        wprintf(L"EvtExportLog failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    wprintf(L"Events from %s log file\n\n", pTargetLogFile);
    DumpEvents(pTargetLogFile);

cleanup:

    return;
}
```



 

 




