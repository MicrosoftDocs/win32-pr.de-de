---
title: Abfragen von Ereignissen
description: Sie können Ereignisse von einem Kanal oder einer Protokolldatei Abfragen.
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6fa69f9b1308cd7ebbc4e4510692bb25ab031ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337463"
---
# <a name="querying-for-events"></a>Abfragen von Ereignissen

Sie können Ereignisse von einem Kanal oder einer Protokolldatei Abfragen. Der Kanal oder die Protokolldatei kann auf dem lokalen Computer oder einem Remote Computer vorhanden sein. Um die Ereignisse anzugeben, die Sie aus der Kanal-oder Protokolldatei erhalten möchten, verwenden Sie eine XPath-Abfrage oder eine XML-Struktur Abfrage. Ausführliche Informationen zum Schreiben der Abfrage finden Sie unter Verwenden von [Ereignissen](consuming-events.md).

Um Ereignisse abzufragen, müssen Sie die [**evtquery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) -Funktion aufzurufen. Sie können die Reihenfolge angeben, in der die Ereignisse zurückgegeben werden (die älteste zu den neuesten (Standard) oder die neueste zum ältesten) und ob falsch formatierte XPath-Ausdrücke in der Abfrage toleriert werden sollen (Ausführliche Informationen dazu, wie die Funktion die falsch formatierten Ausdrücke ignoriert, finden Sie im [**evtquerytoleratequeryerrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) -Flag).

Im folgenden Beispiel wird gezeigt, wie Sie mithilfe eines XPath-Ausdrucks Ereignisse aus einem Kanal Abfragen.


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent); // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;
    LPWSTR pwsPath = L"<Name of the channel goes here>";
    LPWSTR pwsQuery = L"Event/System[EventID=4]";

    hResults = EvtQuery(NULL, pwsPath, pwsQuery, EvtQueryChannelPath | EvtQueryReverseDirection);
    if (NULL == hResults)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"The channel was not found.\n");
        else if (ERROR_EVT_INVALID_QUERY == status)
            // You can call the EvtGetExtendedStatus function to try to get 
            // additional information as to what is wrong with the query.
            wprintf(L"The query is not valid.\n");
        else
            wprintf(L"EvtQuery failed with %lu.\n", status);

        goto cleanup;
    }

    PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



Im folgenden Beispiel wird gezeigt, wie Sie mithilfe einer strukturierten XML-Abfrage Ereignisse aus einem Kanal Abfragen. Die Ereignisse werden in der Reihenfolge von der aktuellen zum ältesten zurückgegeben.


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

// The structured XML query.
#define QUERY \
    L"<QueryList>" \
    L"  <Query Path='Name of the channel goes here'>" \
    L"    <Select>Event/System[EventID=4]</Select>" \
    L"  </Query>" \
    L"</QueryList>"

DWORD PrintQueryStatuses(EVT_HANDLE hResults);
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty);
DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);  // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;

    hResults = EvtQuery(NULL, NULL, QUERY, EvtQueryChannelPath | EvtQueryTolerateQueryErrors);
    if (NULL == hResults)
    {
        // Handle error.
        goto cleanup;
    }

    // Print the status of each query. If all the queries succeeded,
    // print the events in the result set. The status can be
    // ERROR_EVT_CHANNEL_NOT_FOUND or ERROR_EVT_INVALID_QUERY among others.
    if (ERROR_SUCCESS == PrintQueryStatuses(hResults))
        PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



Wenn Sie eine strukturierte XML-Abfrage verwenden und das evtquerytoleratequeryerrors-Flag an [**evtquery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery)übergeben, ist die Funktion erfolgreich, auch wenn mindestens eine der Abfragen in der strukturierten Abfrage tatsächlich fehlgeschlagen ist. Um zu ermitteln, welche Abfragen in der strukturierten Abfrage erfolgreich waren oder fehlgeschlagen sind, müssen Sie die [**evtgetqueryinfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) -Funktion aufrufen. Wenn Sie das evtquerytoleratequeryerrors-Flag nicht übergeben, schlägt die **evtquery** -Funktion mit dem ersten Fehler fehl, der in der Abfrage gefunden wird. Wenn die Abfrage mit \_ \_ einer ungültigen fehlerhaften Abfrage fehlschlägt \_ , können Sie die [**evtgetextendedstatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) -Funktion aufrufen, um eine Nachrichten Zeichenfolge abzurufen, die den XPath-Fehler beschreibt.

Das folgende Beispiel zeigt, wie Sie den Erfolg oder Misserfolg der einzelnen Abfragen in einer strukturierten Abfrage ermitteln können, wenn Sie das evtquerytoleratequeryerrors-Flag an [**evtquery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery)übergeben.


```C++
// Get the list of paths in the query and the status for each path. Return
// the sum of the statuses, so the caller can decide whether to enumerate 
// the results.
DWORD PrintQueryStatuses(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    PEVT_VARIANT pPaths = NULL;
    PEVT_VARIANT pStatuses = NULL;

    wprintf(L"List of channels/logs that were queried and their status\n\n");

    if (status = GetQueryStatusProperty(EvtQueryNames, hResults, pPaths))
        goto cleanup;

    if (status = GetQueryStatusProperty(EvtQueryStatuses, hResults, pStatuses))
        goto cleanup;

    for (DWORD i = 0; i < pPaths->Count; i++)
    {
        wprintf(L"%s (%lu)\n", pPaths->StringArr[i], pStatuses->UInt32Arr[i]);
        status += pStatuses->UInt32Arr[i];
    }

cleanup:

    if (pPaths)
        free(pPaths);

    if (pStatuses)
        free(pStatuses);

    return status;
}


// Get the list of paths specified in the query or the list of status values 
// for each path.
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;

    if  (!EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed))
    {
        status = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == status)
        {
            dwBufferSize = dwBufferUsed;
            pProperty = (PEVT_VARIANT)malloc(dwBufferSize);
            if (pProperty)
            {
                EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed);
            }
            else
            {
                wprintf(L"realloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtGetQueryInfo failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

cleanup:

    return status;
}
```



## <a name="reading-events-from-the-result-set"></a>Lesen von Ereignissen aus dem Resultset

Um die Ereignisse im Resultset aufzulisten, müssen Sie die [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) -Funktion in einer Schleife aufrufen, bis die Funktion " **false** " zurückgibt und die Funktion " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " einen Fehler \_ ohne \_ Weitere Elemente zurückgibt \_ . Die Ereignisse im Resultset sind nicht statisch. neue Ereignisse, die in den Kanal geschrieben werden, werden in das Resultset eingeschlossen, bis der Fehler \_ keine \_ weiteren \_ Elemente festgelegt ist. Um die Leistung zu verbessern, rufen Sie Ereignisse aus dem Resultset in Batches ab (berücksichtigen Sie dabei die Größe jedes Ereignisses, wenn Sie die Anzahl der abzurufenden Ereignisse bestimmen).

Im folgenden Beispiel wird gezeigt, wie die-Ereignisse in einem Resultset aufgelistet werden.


```C++
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

    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}
```



Ausführliche Informationen zum Rendern der Ereignisse, die Sie aus dem Resultset erhalten, finden Sie unter [Rendern von Ereignissen](rendering-events.md).

Wenn Sie Ereignisse abfragen möchten, von denen Sie aufgehört haben, erstellen Sie ein Lesezeichen für das letzte gelesene Ereignis, und verwenden Sie es, wenn Sie die Abfrage das nächste Mal ausführen. Weitere Informationen finden Sie unter [Lesezeichen Ereignisse](bookmarking-events.md).

 

 