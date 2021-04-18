---
description: 'Erstellen von Postfächern. Postslots werden von drei spezialisierten Funktionen unterstützt: "kreatemailslot", "getmailslotinfo" und "setmailslotinfo". Diese Funktionen werden vom Mailslot-Server verwendet.'
ms.assetid: 7f5a3b36-9583-43fc-a977-321c00a48edb
title: Erstellen eines postslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4cfbcf990162347d1e45da01c815002f39299e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351530"
---
# <a name="creating-a-mailslot"></a><span data-ttu-id="8a3e6-105">Erstellen eines postslots</span><span class="sxs-lookup"><span data-stu-id="8a3e6-105">Creating a Mailslot</span></span>

<span data-ttu-id="8a3e6-106">Postslots werden von drei spezialisierten Funktionen unterstützt: " [**kreatemailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)", " [**getmailslotinfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)" und " [**setmailslotinfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo)".</span><span class="sxs-lookup"><span data-stu-id="8a3e6-106">Mailslots are supported by three specialized functions: [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo), and [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo).</span></span> <span data-ttu-id="8a3e6-107">Diese Funktionen werden vom Mailslot-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a3e6-107">These functions are used by the mailslot server.</span></span>

<span data-ttu-id="8a3e6-108">Im folgenden Codebeispiel wird die [**Funktion "die Funktion**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) " in einem postslot mit dem Namen "Sample \_ Mailslot" verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a3e6-108">The following code sample uses the [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) function to retrieve the handle to a mailslot named "sample\_mailslot".</span></span> <span data-ttu-id="8a3e6-109">Das Codebeispiel beim [Schreiben in einen Mailslot](writing-to-a-mailslot.md) zeigt, wie die Client Anwendung in diesen Mailslot schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="8a3e6-109">The code sample in [Writing to a Mailslot](writing-to-a-mailslot.md) shows how client application can write to this mailslot.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

HANDLE hSlot;
LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL WINAPI MakeSlot(LPCTSTR lpszSlotName) 
{ 
    hSlot = CreateMailslot(lpszSlotName, 
        0,                             // no maximum message size 
        MAILSLOT_WAIT_FOREVER,         // no time-out for operations 
        (LPSECURITY_ATTRIBUTES) NULL); // default security
 
    if (hSlot == INVALID_HANDLE_VALUE) 
    { 
        printf("CreateMailslot failed with %d\n", GetLastError());
        return FALSE; 
    } 
    else printf("Mailslot created successfully.\n"); 
    return TRUE; 
}

void main()
{ 
   MakeSlot(SlotName);
}
```



<span data-ttu-id="8a3e6-110">Um einen Mailslot zu erstellen, der von untergeordneten Prozessen geerbt werden kann, sollte eine Anwendung die Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ändern, die als letzter Parameter von " [**kreatemailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)" übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8a3e6-110">To create a mailslot that can be inherited by child processes, an application should change the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure passed as the last parameter of [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota).</span></span> <span data-ttu-id="8a3e6-111">Zu diesem Zweck legt die Anwendung den **binherithandle** -Member dieser Struktur auf " **true** " fest (die Standardeinstellung ist " **false**").</span><span class="sxs-lookup"><span data-stu-id="8a3e6-111">To do this, the application sets the **bInheritHandle** member of this structure to **TRUE** (the default setting is **FALSE**).</span></span>

 

 
