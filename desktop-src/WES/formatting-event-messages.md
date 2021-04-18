---
title: Formatieren von Ereignismeldungen
description: Ein Ereignis kann lokalisierte Nachrichten Zeichenfolgen enthalten, die Sie für die Anzeige formatieren können.
ms.assetid: 31dd8276-1925-4a0e-9e2a-6966e8086238
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314742838e5a756787385930e5122117b3a012c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337152"
---
# <a name="formatting-event-messages"></a>Formatieren von Ereignismeldungen

Ein Ereignis kann lokalisierte Nachrichten Zeichenfolgen enthalten, die Sie für die Anzeige formatieren können. Um eine Meldungs Zeichenfolge aus dem Ereignis abzurufen, rufen Sie die [**evtformatmessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) -Funktion auf. Ein Ereignis kann die folgenden Meldungs Zeichenfolgen enthalten:

-   Eine Meldungs Zeichenfolge für das Ereignis selbst.
-   Eine Meldungs Zeichenfolge, die den dem Ereignis zugewiesenen levelwert beschreibt.
-   Eine Meldungs Zeichenfolge, die den dem Ereignis zugewiesenen Aufgaben Wert beschreibt.
-   Eine Meldungs Zeichenfolge, die den dem Ereignis zugewiesenen opcodewert beschreibt.
-   Eine Meldungs Zeichenfolge, die die dem Ereignis zugewiesenen Schlüsselwort Werte beschreibt.
-   Eine Meldungs Zeichenfolge, die den dem Ereignis zugewiesenen channelwert beschreibt.

Sie können auch [**evtformatmessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) verwenden, um die Meldungs Zeichenfolge für den Anbieter oder eine XML-Zeichenfolge mit dem Ereignis und allen Meldungs Zeichenfolgen zu erhalten.

Zusätzlich zum Absenden der Meldungs Zeichenfolgen aus den Ereignissen, die Sie Abfragen, können Sie auch die Meldungs Zeichenfolgen aus den Metadaten des Anbieters erhalten. Ausführliche Informationen zum Formatieren einer Nachricht auf der Grundlage einer Nachrichten-ID, die Sie aus den Metadaten des Anbieters erhalten, finden Sie unter Get [a Provider the Metadata](getting-a-provider-s-metadata-.md).

Im folgenden Beispiel wird gezeigt, wie die Meldungs Zeichenfolgen von einem Ereignis ausgegeben werden.


```C++
#include <windows.h>
#include <stdio.h>
#include <sddl.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

LPWSTR GetMessageString(EVT_HANDLE hMetadata, EVT_HANDLE hEvent, EVT_FORMAT_MESSAGE_FLAGS FormatId);

void main(void)
{
    EVT_HANDLE hProviderMetadata = NULL;
    EVT_HANDLE hResults = NULL;
    EVT_HANDLE hEvent = NULL;
    DWORD status = ERROR_SUCCESS;
    DWORD dwReturned = 0;
    LPWSTR pwsMessage = NULL;
    LPWSTR pwsPath = L"<name of the channel goes here>";
    LPWSTR pwsQuery = L"<xpath query goes here>";
    LPWSTR pwszPublisherName = L"<name of the publisher goes here>";

    // Get the handle to the provider's metadata that contains the message strings.
    hProviderMetadata = EvtOpenPublisherMetadata(NULL, pwszPublisherName, NULL, 0, 0);
    if (NULL == hProviderMetadata)
    {
        wprintf(L"EvtOpenPublisherMetadata failed with %d\n", GetLastError());
        goto cleanup;
    }

    // Query for an event.
    hResults = EvtQuery(NULL, pwsPath, pwsQuery, EvtQueryChannelPath);
    if (NULL == hResults)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"Channel %s was not found.\n", pwsPath);
        else
            wprintf(L"EvtQuery failed with %lu.\n", status);

        goto cleanup;
    }

    // Get a single event from the result set.
    if (!EvtNext(hResults, 1, &hEvent, INFINITE, 0, &dwReturned))
    {
        wprintf(L"EvtNext failed with %lu\n", status);
        goto cleanup;
    }

    // Get the various message strings from the event.
    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageEvent);
    if (pwsMessage)
    {
        wprintf(L"Event message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageLevel);
    if (pwsMessage)
    {
        wprintf(L"Level message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageTask);
    if (pwsMessage)
    {
        wprintf(L"Task message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageOpcode);
    if (pwsMessage)
    {
        wprintf(L"Opcode message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageKeyword);
    if (pwsMessage)
    {
        LPWSTR ptemp = pwsMessage;

        wprintf(L"Keyword message string: %s", ptemp);

        while (*(ptemp += wcslen(ptemp)+1))
            wprintf(L", %s", ptemp);

        wprintf(L"\n\n");
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageChannel);
    if (pwsMessage)
    {
        wprintf(L"Channel message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageProvider);
    if (pwsMessage)
    {
        wprintf(L"Provider message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageXml);
    if (pwsMessage)
    {
        wprintf(L"XML message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

cleanup:

    if (hEvent)
        EvtClose(hEvent);

    if (hResults)
        EvtClose(hResults);
    
    if (hProviderMetadata)
        EvtClose(hProviderMetadata);
}


// Gets the specified message string from the event. If the event does not
// contain the specified message, the function returns NULL.
LPWSTR GetMessageString(EVT_HANDLE hMetadata, EVT_HANDLE hEvent, EVT_FORMAT_MESSAGE_FLAGS FormatId)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD status = 0;

    if (!EvtFormatMessage(hMetadata, hEvent, 0, 0, NULL, FormatId, dwBufferSize, pBuffer, &dwBufferUsed))
    {
        status = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == status)
        {
            // An event can contain one or more keywords. The function returns keywords
            // as a list of keyword strings. To process the list, you need to know the
            // size of the buffer, so you know when you have read the last string, or you
            // can terminate the list of strings with a second null terminator character 
            // as this example does.
            if ((EvtFormatMessageKeyword == FormatId))
                pBuffer[dwBufferSize-1] = L'\0';
            else
                dwBufferSize = dwBufferUsed;

            pBuffer = (LPWSTR)malloc(dwBufferSize * sizeof(WCHAR));

            if (pBuffer)
            {
                EvtFormatMessage(hMetadata, hEvent, 0, 0, NULL, FormatId, dwBufferSize, pBuffer, &dwBufferUsed);

                // Add the second null terminator character.
                if ((EvtFormatMessageKeyword == FormatId))
                    pBuffer[dwBufferUsed-1] = L'\0';
            }
            else
            {
                wprintf(L"malloc failed\n");
            }
        }
        else if (ERROR_EVT_MESSAGE_NOT_FOUND == status || ERROR_EVT_MESSAGE_ID_NOT_FOUND == status)
            ;
        else
        {
            wprintf(L"EvtFormatMessage failed with %u\n", status);
        }
    }

    return pBuffer;
}
```



 

 




