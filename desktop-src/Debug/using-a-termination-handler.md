---
description: Das folgende Beispiel zeigt, wie ein Beendigungshandler verwendet wird, um sicherzustellen, dass Ressourcen freigegeben werden, wenn die Ausführung eines geschützten Codetexts beendet wird.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Verwenden eines Beendigungshandlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6fe2d2ba8a7b8443eb164571a42347ce6cfb7e99c44f90da25c6fd57863e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655080"
---
# <a name="using-a-termination-handler"></a>Verwenden eines Beendigungshandlers

Das folgende Beispiel zeigt, wie ein Beendigungshandler verwendet wird, um sicherzustellen, dass Ressourcen freigegeben werden, wenn die Ausführung eines geschützten Codetexts beendet wird. In diesem Fall verwendet ein Thread die [**EnterCriticalSection-Funktion,**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) um auf den Besitz eines kritischen Abschnittsobjekts zu warten. Wenn der Thread die Ausführung des Codes abgeschlossen hat, der durch den kritischen Abschnitt geschützt ist, muss er die [**LeaveCriticalSection-Funktion**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) aufrufen, um das kritische Abschnittsobjekt für andere Threads verfügbar zu machen. Die Verwendung eines Beendigungshandlers garantiert, dass dies geschieht. Weitere Informationen finden Sie unter [Wichtige Abschnittsobjekte.](../sync/critical-section-objects.md)


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



 

 
