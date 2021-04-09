---
description: Das folgende Beispiel zeigt, wie ein Beendigungs Handler verwendet wird, um sicherzustellen, dass Ressourcen freigegeben werden, wenn die Ausführung eines überwachten Code Texts beendet wird.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Verwenden eines Beendigungs Handlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbe73eda8533ed5805159d5386b69daa4d03194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958373"
---
# <a name="using-a-termination-handler"></a>Verwenden eines Beendigungs Handlers

Das folgende Beispiel zeigt, wie ein Beendigungs Handler verwendet wird, um sicherzustellen, dass Ressourcen freigegeben werden, wenn die Ausführung eines überwachten Code Texts beendet wird. In diesem Fall verwendet ein Thread die [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) -Funktion, um auf den Besitz eines kritischen Abschnitts Objekts zu warten. Wenn die Ausführung des Codes, der durch den kritischen Abschnitt geschützt ist, abgeschlossen ist, muss die [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) -Funktion aufgerufen werden, damit das kritische Abschnitts Objekt anderen Threads zur Verfügung steht. Die Verwendung eines Beendigungs Handlers stellt sicher, dass dies geschieht. Weitere Informationen finden Sie unter [Critical Section Objects](../sync/critical-section-objects.md).


```C++
LPTSTR lpBuffer = NULL; 
CRITICAL_SECTION CriticalSection; 

// EnterCriticalSection synchronizes code with other threads. 
EnterCriticalSection(&CriticalSection); 
 
__try 
{ 
    // Perform a task that may cause an exception. 
    lpBuffer = (LPTSTR) LocalAlloc(LPTR, 10); 
    StringCchCopy(lpBuffer, 10, TEXT("Hello"));

    _tprintf(TEXT("%s\n"),lpBuffer); 
    LocalFree(lpBuffer); 
} 
__finally 
{ 
    // LeaveCriticalSection is called even if an exception occurred. 
    LeaveCriticalSection(&CriticalSection); 
}
```



 

 
