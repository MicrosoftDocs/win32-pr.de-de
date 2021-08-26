---
description: Das folgende Beispiel zeigt, wie ein Thread einen kritischen Abschnitt initialisiert, einlässt und frei gibt. Sie verwendet die Funktionen InitializeCriticalSectionAndSpinCount, EnterCriticalSection, LeaveCriticalSection und DeleteCriticalSection.
ms.assetid: 3c96414b-97e7-4ebb-a629-bfdb7a77c576
title: Verwenden kritischer Abschnittsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe2634987b49ebd6fb0109597fe7429ac9467e4e5178f0e65242f1c7cf402be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073060"
---
# <a name="using-critical-section-objects"></a>Verwenden kritischer Abschnittsobjekte

Das folgende Beispiel zeigt, wie ein Thread einen kritischen Abschnitt initialisiert, [einlässt und frei gibt.](critical-section-objects.md) Sie verwendet die [**Funktionen InitializeCriticalSectionAndSpinCount,**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) [**EnterCriticalSection,**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection)und [**DeleteCriticalSection.**](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection)

``` syntax
// Global variable
CRITICAL_SECTION CriticalSection; 

int main( void )
{
    ...

    // Initialize the critical section one time only.
    if (!InitializeCriticalSectionAndSpinCount(&CriticalSection, 
        0x00000400) ) 
        return;
    ...

    // Release resources used by the critical section object.
    DeleteCriticalSection(&CriticalSection);
}

DWORD WINAPI ThreadProc( LPVOID lpParameter )
{
    ...

    // Request ownership of the critical section.
    EnterCriticalSection(&CriticalSection); 

    // Access the shared resource.

    // Release ownership of the critical section.
    LeaveCriticalSection(&CriticalSection);

    ...
return 1;
}
```

 

 
