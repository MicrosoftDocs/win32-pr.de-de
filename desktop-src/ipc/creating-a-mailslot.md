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
# <a name="creating-a-mailslot"></a>Erstellen eines postslots

Postslots werden von drei spezialisierten Funktionen unterstützt: " [**kreatemailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)", " [**getmailslotinfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)" und " [**setmailslotinfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo)". Diese Funktionen werden vom Mailslot-Server verwendet.

Im folgenden Codebeispiel wird die [**Funktion "die Funktion**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) " in einem postslot mit dem Namen "Sample \_ Mailslot" verwendet. Das Codebeispiel beim [Schreiben in einen Mailslot](writing-to-a-mailslot.md) zeigt, wie die Client Anwendung in diesen Mailslot schreiben kann.


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



Um einen Mailslot zu erstellen, der von untergeordneten Prozessen geerbt werden kann, sollte eine Anwendung die Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ändern, die als letzter Parameter von " [**kreatemailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)" übergeben wurde. Zu diesem Zweck legt die Anwendung den **binherithandle** -Member dieser Struktur auf " **true** " fest (die Standardeinstellung ist " **false**").

 

 
