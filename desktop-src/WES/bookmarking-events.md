---
title: Lesezeichen Ereignisse
description: Ein Lesezeichen identifiziert ein Ereignis in einer Kanal-oder Protokolldatei.
ms.assetid: e7eeafc3-deb9-4cdc-9763-f784db7333be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64d7fb4aef883a51084420c5a2d78e4f0ff25dac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339075"
---
# <a name="bookmarking-events"></a>Lesezeichen Ereignisse

Ein Lesezeichen identifiziert ein Ereignis in einer Kanal-oder Protokolldatei. Wenn Sie Ereignisse Abfragen oder Ereignisse abonnieren, können Sie ein Lesezeichen verwenden, um mit dem Lesen von Ereignissen aus diesem Lese markierten Ereignis zu beginnen. Normalerweise erstellen Sie ein Lesezeichen für das letzte Ereignis im Resultset (vorausgesetzt, Sie haben alle Ereignisse im Resultset aufgezählt).

Im folgenden Verfahren wird beschrieben, wie Sie ein Lesezeichen aus einem Ereignis erstellen.

**So erstellen Sie ein Lesezeichen aus einem Ereignis**

1.  Rufen Sie die [**evtkreatebookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) -Funktion auf, um ein Lesezeichen zu erstellen. Übergeben Sie **null** für das-Argument.
2.  Rufen Sie die [**evtupdatebookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtupdatebookmark) -Funktion auf, um das Lesezeichen mit dem Ereignis zu aktualisieren. Übergeben Sie das Handle als Argument an das-Ereignis.
3.  Rufen Sie die [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) -Funktion auf, um eine XML-Zeichenfolge für das Lesezeichen zu erstellen. Übergeben Sie evtrenderbookmark als Rendering-Flag.
4.  Speichern Sie die XML-Zeichenfolge für die spätere Verwendung (Sie können z. b. die XML-Zeichenfolge in einer Datei oder in der Registrierung beibehalten).

Im folgenden Verfahren wird beschrieben, wie Sie ein Lesezeichen erstellen, indem Sie eine XML-Lesezeichen Folge verwenden, die in der vorherigen Prozedur beibehalten wurde

**So erstellen Sie ein Lesezeichen mithilfe einer XML-Zeichenfolge**

1.  Die XML-Zeichenfolge, die das zuvor beibehaltene Lesezeichen darstellt, wird aufgerufen.
2.  Rufen Sie die [**evtkreatebookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) -Funktion auf, um ein Lesezeichen zu erstellen. Übergeben Sie die XML-Zeichenfolge für das-Argument.

Im folgenden Verfahren wird beschrieben, wie Sie ein Lesezeichen in einer Abfrage verwenden.

**So verwenden Sie ein Lesezeichen in einer Abfrage**

1.  Wenden Sie die [**evtquery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) -Funktion an, um Ereignisse abzurufen, die Ihrer Abfrage entsprechen.
2.  Wenden Sie die [**evtseek**](/windows/desktop/api/WinEvt/nf-winevt-evtseek) -Funktion an, um nach dem Lesezeichen-Ereignis zu suchen. Übergeben Sie das Handle an das Lesezeichen und das evtseekrelativetobookmark-Flag.
3.  Nennen Sie die [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) -Funktion in einer Schleife, um die Ereignisse aufzuzählen, die nach dem Ereignis mit Lesezeichen beginnen (abhängig vom Offset, den Sie in [**evtseek**](/windows/desktop/api/WinEvt/nf-winevt-evtseek)angegeben haben).

Ein Beispiel finden Sie unter [Verwenden eines Lesezeichens in einer Abfrage](#using-a-bookmark-in-a-query).

Im folgenden Verfahren wird die Verwendung eines Lesezeichens in einem Abonnement beschrieben.

**So verwenden Sie ein Lesezeichen in einem Abonnement**

1.  Wenden Sie die [**evtsubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) -Funktion an, um Ereignisse zu abonnieren, die Ihrer Abfrage entsprechen. Übergeben Sie das Handle an das Lesezeichen und das evtabonbestartafterbookmark-Flag.
2.  Wenn Sie die [**EVT- \_ Abonnement \_ Rückruf**](/windows/win32/api/winevt/nc-winevt-evt_subscribe_callback) Funktion implementiert haben, empfängt der Rückruf Ereignisse, die nach dem Ereignis mit Lesezeichen beginnen.
3.  Wenn Sie den Rückruf nicht implementiert haben, rufen Sie die [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) -Funktion in einer Schleife auf, um die Ereignisse aufzuzählen, die nach dem Ereignis mit Lesezeichen beginnen.

Ein Beispiel finden Sie unter [Verwenden eines Lesezeichens in einem Abonnement](#using-a-bookmark-in-a-subscription).

## <a name="using-a-bookmark-in-a-query"></a>Verwenden eines Lesezeichens in einer Abfrage

Im folgenden Beispiel wird gezeigt, wie Sie ein Lesezeichen in einer Abfrage verwenden. Im Beispiel wird das Beispiel für das [Abfragen von Ereignissen](querying-for-events.md)erweitert.


```C++
// Enumerate all the events in the result set beginning with the bookmarked event. 
DWORD PrintResults(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hEvents[ARRAY_SIZE];
    DWORD dwReturned = 0;
    LPWSTR pwsBookmarkXml = NULL;
    EVT_HANDLE hBookmark = NULL;

    // Get the persisted bookmark XML string.
    pwsBookmarkXml = GetBookmarkedString();

    // If the bookmark string was persisted, create a bookmark and
    // seek to the bookmarked event in the result set.
    if (pwsBookmarkXml)
    {
        hBookmark = EvtCreateBookmark(pwsBookmarkXml);
        if (NULL == hBookmark)
        {
            wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
            goto cleanup;
        }

        if (!EvtSeek(hResults, 1, hBookmark, 0, EvtSeekRelativeToBookmark))
        {
            wprintf(L"EvtSeek failed with %lu\n", GetLastError());
            goto cleanup;
        }
    }

    // Enumerate the events in the result set after the bookmarked event.
    while (true)
    {
        if (!EvtNext(hResults, ARRAY_SIZE, hEvents, INFINITE, 0, &dwReturned))
        {
            if (ERROR_NO_MORE_ITEMS != (status = GetLastError()))
            {
                wprintf(L"EvtNext failed with %lu\n", status);
            }

            goto cleanup;
        }

        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (status = PrintEvent(hEvents[i]))
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

    if (ERROR_NO_MORE_ITEMS == status)
    {
        // Get the last event in the result set, use it to create a
        // bookmark, render the bookmark as an XML string, and persist the string.
        if (ERROR_SUCCESS != (status = SaveBookmark(hResults)))
            wprintf(L"\nFailed to save bookmark\n");
    }
    else
    {
        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (NULL != hEvents[i])
                EvtClose(hEvents[i]);
        }
    }

    if (pwsBookmarkXml)
        free(pwsBookmarkXml);

    return status;
}

// Get the bookmark XML string from wherever you persisted it.
LPWSTR GetBookmarkedString(void)
{
    LPWSTR pwsBookmarkXML = NULL;

    // TODO: Add the code to get the bookmark XML string from storage.

    return pwsBookmarkXML;
}


// Persist the bookmark XML string. This example assumes that we've read through
// the result set and are persisting the last event as the bookmark.
DWORD SaveBookmark(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    DWORD dwReturned = 0;
    LPWSTR pBookmarkXml = NULL;
    EVT_HANDLE hBookmark = NULL;
    EVT_HANDLE hEvent = NULL;

    // Seek to the last event in the result set and get the event.
    if (!EvtSeek(hResults, 0, NULL, 0, EvtSeekRelativeToLast))
    {
        wprintf(L"EvtSeek failed with %lu\n", status = GetLastError());
        goto cleanup;
    }

    if (!EvtNext(hResults, 1, &hEvent, INFINITE, 0, &dwReturned))
    {
        wprintf(L"EvtNext failed with %lu\n", status = GetLastError());
        goto cleanup;
    }

    // Create a bookmark and update it with the last event in the result set.
    hBookmark = EvtCreateBookmark(NULL);
    if (NULL == hBookmark)
    {
        wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

    if (!EvtUpdateBookmark(hBookmark, hEvent))
    {
        wprintf(L"EvtUpdateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

    // Render the bookmark as an XML string that you can then persist.
    if (!EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pBookmarkXml = (LPWSTR)malloc(dwBufferSize);
            if (pBookmarkXml)
            {
                EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount);
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

    // TODO: Add code to persist bookmark XML string.

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

    if (hBookmark)
        EvtClose(hBookmark);

    if (hEvent)
        EvtClose(hEvent);

    return status;
}
```



## <a name="using-a-bookmark-in-a-subscription"></a>Verwenden eines Lesezeichens in einem Abonnement

Im folgenden Beispiel wird gezeigt, wie ein Lesezeichen in einem Pushabonnement verwendet wird.


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent);
DWORD PrintEvent(EVT_HANDLE hEvent);
EVT_HANDLE GetBookmark();
DWORD SaveBookmark(EVT_HANDLE hBookmark);


void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    EVT_HANDLE hBookmark = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"<xpath query goes here>";

    // Get the saved bookmark.
    hBookmark = GetBookmark();

    // Subscribe to existing and furture events beginning with the bookmarked event.
    // If the bookmark has not been persisted, pass an empty bookmark and the subscription
    // will begin with the second event that matches the query criteria.
    hSubscription = EvtSubscribe(NULL, NULL, pwsPath, pwsQuery, hBookmark, (PVOID)hBookmark, 
                                 (EVT_SUBSCRIBE_CALLBACK)SubscriptionCallback, EvtSubscribeStartAfterBookmark);
    if (NULL == hSubscription)
    {
        wprintf(L"EvtSubscribe failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    wprintf(L"Hit any key to quit\n\n");
    while (!_kbhit())
        Sleep(10);

    status = SaveBookmark(hBookmark);

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);

    if (hBookmark)
        EvtClose(hBookmark);
 }


// The callback that receives the events that match the query criteria. Use the 
// context parameter to pass the handle to the bookmark, so you can update the bookmark
// with each event that you receive.
DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hBookmark = (EVT_HANDLE)pContext;

    switch(action)
    {
        // You should only get the EvtSubscribeActionError action if your subscription flags 
        // includes EvtSubscribeStrict and the channel contains missing event records.
        case EvtSubscribeActionError:
            if (ERROR_EVT_QUERY_RESULT_STALE == (DWORD)hEvent)
            {
                wprintf(L"The subscription callback was notified that event records are missing.\n");
                // Handle if this is an issue for your application.
            }
            else
            {
                wprintf(L"The subscription callback received the following Win32 error: %lu\n", (DWORD)hEvent);
            }

            break;

        case EvtSubscribeActionDeliver:
            if (ERROR_SUCCESS != (status = PrintEvent(hEvent)))
            {
                goto cleanup;
            }

            if (!EvtUpdateBookmark(hBookmark, hEvent))
            {
                wprintf(L"EvtUpdateBookmark failed with %lu\n", status = GetLastError());
                goto cleanup;
            }

            break;

        default:
            wprintf(L"SubscriptionCallback: Unknown action.\n");
    }

cleanup:

    if (ERROR_SUCCESS != status)
    {
        // End subscription - Use some kind of IPC mechanism to signal
        // your application to close the subscription handle.
    }

    return status; // The service ignores the returned status.
}


EVT_HANDLE GetBookmark(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hBookmark = NULL;
    LPWSTR pBookmarkXml = NULL;

    // Set pBookmarkXml to the XML string that you persisted in SaveBookmark.

    hBookmark = EvtCreateBookmark(pBookmarkXml);
    if (NULL == hBookmark)
    {
        wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

    return hBookmark;
}


DWORD SaveBookmark(EVT_HANDLE hBookmark)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pBookmarkXml = NULL;

    if (!EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pBookmarkXml = (LPWSTR)malloc(dwBufferSize);
            if (pBookmarkXml)
            {
                EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount);
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
            wprintf(L"EvtRender failed with %d\n", status);
            goto cleanup;
        }
    }

    // Persist bookmark to a file or the registry.

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

    return status;
}


// Render the event as an XML string and print it.
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

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
            wprintf(L"EvtRender failed with %d\n", status);
            goto cleanup;
        }
    }

    wprintf(L"%s\n\n", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}
```



 

 