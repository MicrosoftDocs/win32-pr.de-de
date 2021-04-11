---
description: Das folgende Beispiel zeigt, wie ein Thread einen kritischen Abschnitt initialisiert, eingibt und freigibt. Er verwendet die Funktionen InitializeCriticalSectionAndSpinCount, EnterCriticalSection, LeaveCriticalSection und DeleteCriticalSection.
ms.assetid: 3c96414b-97e7-4ebb-a629-bfdb7a77c576
title: Verwenden von kritischen Abschnitts Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e280319e3eb3078ea67a1f96065598d4517766
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216188"
---
# <a name="using-critical-section-objects"></a>Verwenden von kritischen Abschnitts Objekten

Das folgende Beispiel zeigt, wie ein Thread einen [kritischen Abschnitt](critical-section-objects.md)initialisiert, eingibt und freigibt. Er verwendet die Funktionen [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount), [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection), [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection)und [**DeleteCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection) .

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

 

 
