---
title: Auflisten von Event Collector-Abonnements
description: Sie können eine Liste mit Namen von Event Collector-Abonnements abrufen, die auf einem lokalen Computer aktiviert sind.
ms.assetid: b44fc694-b94a-4fc5-95d1-72afb016ad72
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab030e3f85b1abc0e763c30dfa4208023b2e654
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712203"
---
# <a name="listing-event-collector-subscriptions"></a>Auflisten von Event Collector-Abonnements

Sie können eine Liste mit Namen von Event Collector-Abonnements abrufen, die auf einem lokalen Computer aktiviert sind. Mithilfe der [**ecopenabonptionenum**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum) -Funktion können Sie ein Handle für einen Abonnement Enumerator abrufen. Nachdem das Handle erstellt wurde, wird die Funktion [**ecenumnextabonnement**](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription) verwendet, um die Abonnements auf dem lokalen Computer aufzulisten.

> [!Note]
>
> Sie können das folgende Codebeispiel verwenden, um eine Liste von Abonnements abzurufen, oder Sie können den folgenden Befehl an der Eingabeaufforderung eingeben:
>
> **wecutil**

 

Im folgenden C++-Codebeispiel wird gezeigt, wie die Event Collector-Abonnements aufgelistet werden.


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

void __cdecl wmain()
{
    // Lists the Event Collector subscriptions that are available 
    // on the local computer.
    DWORD dwBufferSizeUsed, dwError = ERROR_SUCCESS;
    BOOL bRetVal = true;
    std::vector<WCHAR> buffer(MAX_PATH);
    EC_HANDLE hEnumerator;
    DWORD dwRetVal;

    // Create a handle to access the subscriptions.
    hEnumerator = EcOpenSubscriptionEnum(NULL);

    if (hEnumerator)
    {
        while (bRetVal)
        {
            // Get the next subscription.
            bRetVal = EcEnumNextSubscription(hEnumerator, 
                (DWORD) buffer.size(),
                (LPWSTR) &buffer[0],
                &dwBufferSizeUsed);
            dwError = GetLastError();

            // If the buffer is not large enough, resize it to accommodate the
            // subscription information.
            if (!bRetVal && ERROR_INSUFFICIENT_BUFFER == dwError)
            {
                dwError = ERROR_SUCCESS;
                buffer.resize(dwBufferSizeUsed);

                bRetVal = EcEnumNextSubscription(hEnumerator,
                    (DWORD) buffer.size(),
                    (LPWSTR) &buffer[0],
                    &dwBufferSizeUsed);
                dwError = GetLastError();
            }

            if (!bRetVal && ERROR_NO_MORE_ITEMS == dwError)
            {
                dwError = ERROR_SUCCESS;
                break;
            }

            if (bRetVal && ERROR_SUCCESS != dwError)
            {
                break;
            }
            
            // Output the subscription name.
            wprintf(L"%s\n", (LPCWSTR) &buffer[0]);    
        }
    }
    else
    {
        dwRetVal = GetLastError();
        LPVOID lpwszBuffer;

        FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
            NULL,
            dwRetVal,
            0,
            (LPWSTR) &lpwszBuffer,
            0,
            NULL);

        if (!lpwszBuffer)
        {
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u. Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\nError Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }

    EcClose(hEnumerator);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zur Windows-Ereignis Sammlung](windows-event-collector-reference.md)
</dt> </dl>

 

 




