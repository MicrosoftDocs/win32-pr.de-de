---
title: Löschen eines Ereignissammlerabonnements
description: Sie können ein Ereignissammlerabonnement von einem lokalen Computer löschen.
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9edf2f9dda2b6393ab147d5f58ff8f889952eaeb7f31f82080558697f117f3c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006090"
---
# <a name="deleting-an-event-collector-subscription"></a>Löschen eines Ereignissammlerabonnements

Sie können ein Ereignissammlerabonnement von einem lokalen Computer löschen. Sie müssen den Namen des Abonnements kennen, bevor Sie es löschen können. Weitere Informationen zum Auflisten der aktuellen Abonnements auf einem lokalen Computer finden Sie unter Auflisten von [Ereignissammlerabonnements,](listing-event-collector-subscriptions.md)oder geben Sie den folgenden Befehl an der Eingabeaufforderung ein:

**wecutil es**

> [!Note]
>
> Sie können dieses Beispiel verwenden, um ein Ereignissammlerabonnement zu löschen, oder Sie können den folgenden Befehl an der Eingabeaufforderung eingeben:
>
> **wecutil ds** *SubscriptionName*

 

Nachdem Sie den Namen des zu löschenden Event Collector-Abonnements abgerufen haben, können Sie den Namen des Abonnements als Parameter für [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)angeben.

Das folgende C++-Codebeispiel zeigt, wie Sie ein Ereignissammlerabonnement löschen.


```C++
#include <windows.h>
#include <EvColl.h>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

void __cdecl wmain()
{
    DWORD dwRetVal;
    LPWSTR lpSubname = L"MyTestSubscription";

    // Delete the specified Event Collector subscription.
    if (!EcDeleteSubscription(lpSubname, 0))
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
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." 
                L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n"
            L"Error Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auflisten von Ereignissammlerabonnements](listing-event-collector-subscriptions.md)
</dt> <dt>

[Windows Ereignissammlerreferenz](windows-event-collector-reference.md)
</dt> </dl>

 

 




