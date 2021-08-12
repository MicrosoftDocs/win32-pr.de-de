---
title: Abfragen von Ereignissen
description: Sie können Ereignisse aus einem Kanal oder einer Protokolldatei abfragen.
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 981e4a8c39daebbce641c79e7d26331b9b36845d3c71fd1902ea667ca85c5dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587801"
---
# <a name="querying-for-events"></a>Abfragen von Ereignissen

Sie können Ereignisse aus einem Kanal oder einer Protokolldatei abfragen. Der Kanal oder die Protokolldatei kann auf dem lokalen Computer oder einem Remotecomputer vorhanden sein. Um die Ereignisse anzugeben, die Sie aus dem Kanal oder der Protokolldatei erhalten möchten, verwenden Sie eine XPath-Abfrage oder eine Struktur-XML-Abfrage. Weitere Informationen zum Schreiben der Abfrage finden Sie unter [Verwenden von Ereignissen.](consuming-events.md)

Rufen Sie zum Abfragen von Ereignissen die [**EvtQuery-Funktion**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) auf. Sie können die Reihenfolge angeben, in der die Ereignisse zurückgegeben werden (älteste bis neueste (Standard) oder neueste bis älteste), und angeben, ob falsch formatierte XPath-Ausdrücke in der Abfrage toleriert werden sollen (Details dazu, wie die Funktion die falsch formatierten Ausdrücke ignoriert, finden Sie unter [**EvtQueryTolerateQueryErrors-Flag).**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)

Das folgende Beispiel zeigt, wie Ereignisse aus einem Kanal mithilfe eines XPath-Ausdrucks abfragen.


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



Das folgende Beispiel zeigt, wie Ereignisse aus einem Kanal mithilfe einer strukturierten XML-Abfrage abfragen. Die Ereignisse werden in der Reihenfolge von der neuesten zur ältesten zurückgegeben.


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



Wenn Sie eine strukturierte XML-Abfrage verwenden und das EvtQueryTolerateQueryErrors-Flag an [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery)übergeben, ist die Funktion erfolgreich, obwohl eine oder mehrere Abfragen in der strukturierten Abfrage tatsächlich fehlgeschlagen sind. Um zu bestimmen, welche Abfragen in der strukturierten Abfrage erfolgreich waren oder fehlgeschlagen sind, rufen Sie die [**EvtGetQueryInfo-Funktion**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) auf. Wenn Sie das EvtQueryTolerateQueryErrors-Flag nicht übergeben, tritt bei der **EvtQuery-Funktion** der erste Fehler auf, den sie in der Abfrage findet. Wenn die Abfrage mit ERROR EVT INVALID QUERY fehlschlägt, rufen Sie die \_ \_ \_ [**EvtGetExtendedStatus-Funktion**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) auf, um eine Meldungszeichenfolge zu erhalten, die den XPath-Fehler beschreibt.

Das folgende Beispiel zeigt, wie Sie den Erfolg oder Fehler jeder Abfrage in einer strukturierten Abfrage ermitteln, wenn Sie das EvtQueryTolerateQueryErrors-Flag an [**EvtQuery übergeben.**](/windows/desktop/api/WinEvt/nf-winevt-evtquery)


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

Um die Ereignisse im ResultSet aufzählen zu können, rufen Sie die [**EvtNext-Funktion**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) in einer Schleife auf, bis die Funktion **FALSE** zurückgibt und die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) ERROR \_ NO MORE ITEMS \_ \_ zurückgibt. Die Ereignisse im ResultSet sind nicht statisch. Neue Ereignisse, die in den Kanal geschrieben werden, werden in das Ergebnisset aufgenommen, bis ERROR \_ NO MORE ITEMS festgelegt \_ \_ ist. Um die Leistung zu verbessern, rufen Sie Ereignisse aus dem Ergebnisset in Batches ab (unter Berücksichtigung der Größe jedes Ereignisses bei der Bestimmung der Anzahl der zu abrufenden Ereignisse).

Das folgende Beispiel zeigt, wie die Ereignisse in einem Resultset aufzählt werden.


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



Weitere Informationen zum Rendern der Ereignisse, die Sie aus dem Resultset erhalten, finden Sie unter [Renderingereignisse](rendering-events.md).

Wenn Sie Ereignisse abfragen möchten, von denen aus Sie aufgelassen haben, erstellen Sie ein Lesezeichen des letzten Ereignisses, das Sie gelesen haben, und verwenden Sie es beim nächsten Ausführen der Abfrage. Weitere Informationen finden Sie unter [Bookmarking Events](bookmarking-events.md).

 

 