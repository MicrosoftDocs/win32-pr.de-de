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
# <a name="deleting-an-event-collector-subscription"></a><span data-ttu-id="3170a-103">Löschen eines Ereignis Sammler Abonnements</span><span class="sxs-lookup"><span data-stu-id="3170a-103">Deleting an Event Collector Subscription</span></span>

<span data-ttu-id="3170a-104">Sie können ein Ereignis Sammler Abonnement von einem lokalen Computer löschen.</span><span class="sxs-lookup"><span data-stu-id="3170a-104">You can delete an Event Collector subscription from a local computer.</span></span> <span data-ttu-id="3170a-105">Sie müssen den Namen des Abonnements kennen, bevor Sie es löschen können.</span><span class="sxs-lookup"><span data-stu-id="3170a-105">You must know the name of the subscription before you can delete it.</span></span> <span data-ttu-id="3170a-106">Weitere Informationen zum Auflisten der aktuellen Abonnements auf einem lokalen Computer finden Sie unter Auflisten von [Event Collector-Abonnements](listing-event-collector-subscriptions.md), oder geben Sie den folgenden Befehl an der Eingabeaufforderung ein:</span><span class="sxs-lookup"><span data-stu-id="3170a-106">For more information about how to list the current subscriptions on a local computer, see [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or type the following command at the command prompt:</span></span>

<span data-ttu-id="3170a-107">**wecutil**</span><span class="sxs-lookup"><span data-stu-id="3170a-107">**wecutil es**</span></span>

> [!Note]
>
> <span data-ttu-id="3170a-108">Sie können dieses Beispiel verwenden, um ein Ereignis Sammler Abonnement zu löschen, oder Sie können den folgenden Befehl an der Eingabeaufforderung eingeben:</span><span class="sxs-lookup"><span data-stu-id="3170a-108">You can use this example to delete an Event Collector subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="3170a-109">*Abonnement Name* für **wecutil DS**</span><span class="sxs-lookup"><span data-stu-id="3170a-109">**wecutil ds** *SubscriptionName*</span></span>

 

<span data-ttu-id="3170a-110">Nachdem Sie den Namen des zu löschenden Event Collector-Abonnements abgerufen haben, können Sie den Namen des Abonnements als Parameter für [**ecdelta etesubdesigniangeben**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).</span><span class="sxs-lookup"><span data-stu-id="3170a-110">After you retrieve the name of the Event Collector subscription to delete, you can provide the name of the subscription as a parameter to [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).</span></span>

<span data-ttu-id="3170a-111">Im folgenden C++-Codebeispiel wird veranschaulicht, wie ein Ereignis Sammler Abonnement gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="3170a-111">The following C++ code example shows how to delete an Event Collector subscription.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3170a-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3170a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3170a-113">Auflisten von Event Collector-Abonnements</span><span class="sxs-lookup"><span data-stu-id="3170a-113">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="3170a-114">Referenz zur Windows-Ereignis Sammlung</span><span class="sxs-lookup"><span data-stu-id="3170a-114">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




