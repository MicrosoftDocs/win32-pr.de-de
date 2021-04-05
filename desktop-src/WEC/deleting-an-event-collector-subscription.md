---
title: Löschen eines Ereignis Sammler Abonnements
description: Sie können ein Ereignis Sammler Abonnement von einem lokalen Computer löschen.
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cec036625bbb94e33e71af0f1d9808ad9252a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710133"
---
# <a name="deleting-an-event-collector-subscription"></a>Löschen eines Ereignis Sammler Abonnements

Sie können ein Ereignis Sammler Abonnement von einem lokalen Computer löschen. Sie müssen den Namen des Abonnements kennen, bevor Sie es löschen können. Weitere Informationen zum Auflisten der aktuellen Abonnements auf einem lokalen Computer finden Sie unter Auflisten von [Event Collector-Abonnements](listing-event-collector-subscriptions.md), oder geben Sie den folgenden Befehl an der Eingabeaufforderung ein:

**wecutil**

> [!Note]
>
> Sie können dieses Beispiel verwenden, um ein Ereignis Sammler Abonnement zu löschen, oder Sie können den folgenden Befehl an der Eingabeaufforderung eingeben:
>
> *Abonnement Name* für **wecutil DS**

 

Nachdem Sie den Namen des zu löschenden Event Collector-Abonnements abgerufen haben, können Sie den Namen des Abonnements als Parameter für [**ecdelta etesubdesigniangeben**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).

Im folgenden C++-Codebeispiel wird veranschaulicht, wie ein Ereignis Sammler Abonnement gelöscht wird.


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

[Auflisten von Event Collector-Abonnements](listing-event-collector-subscriptions.md)
</dt> <dt>

[Referenz zur Windows-Ereignis Sammlung](windows-event-collector-reference.md)
</dt> </dl>

 

 




