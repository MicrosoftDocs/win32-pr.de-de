---
description: Diese enthält Beispiele, in denen mithilfe der verifyversioninfo-Funktion bestimmt wird, ob die Anwendung unter einem bestimmten Betriebssystem ausgeführt wird.
ms.assetid: f39c35ae-9be5-4a03-9079-6fcc63387f6b
title: Überprüfen der System Version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ddb3562230d0708ddc55d0f8214286ea6c3008
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215550"
---
# <a name="verifying-the-system-version"></a>Überprüfen der System Version

\[ Verwendung der [**verifyversioninfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) -Funktion zum Überprüfen, ob das aktuell laufende Betriebssystem nicht empfohlen wird. Verwenden Sie stattdessen die Versions Hilfsobjekte. [ ](version-helper-apis.md)\]

Diese enthält Beispiele, in denen mithilfe der [**verifyversioninfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) -Funktion bestimmt wird, ob die Anwendung unter einem bestimmten Betriebssystem ausgeführt wird.

Die Hauptschritte in jedem Beispiel lauten wie folgt:

1.  Legen Sie die entsprechenden Werte in der [**OSVERSIONINFOEX**](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa) -Struktur fest.
2.  Legen Sie die entsprechende Bedingungs Maske mithilfe des "Ver"-Bedingungs Makros fest. [**\_ \_**](/windows/desktop/api/Winnt/nf-winnt-ver_set_condition)
3.  Ruft [**verifyversioninfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) auf, um den Test auszuführen.

## <a name="example-1"></a>Beispiel 1

Im folgenden Beispiel wird ermittelt, ob die Anwendung unter Windows XP mit Service Pack 2 (SP2) oder einer höheren Version von Windows ausgeführt wird, wie z. b. Windows Server 2003 oder Windows Vista.


```C++
#include <windows.h>
#include <stdio.h>

BOOL Is_WinXP_SP2_or_Later () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
   int op=VER_GREATER_EQUAL;

   // Initialize the OSVERSIONINFOEX structure.

   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.dwMinorVersion = 1;
   osvi.wServicePackMajor = 2;
   osvi.wServicePackMinor = 0;

   // Initialize the condition mask.

   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_MINORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMAJOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMINOR, op );

   // Perform the test.

   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_MINORVERSION | 
      VER_SERVICEPACKMAJOR | VER_SERVICEPACKMINOR,
      dwlConditionMask);
}

void main()
{
    if(Is_WinXP_SP2_or_Later())
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}
```



## <a name="example-2"></a>Beispiel 2

Der folgende Code überprüft, ob die Anwendung auf Windows 2000 Server oder einem späteren Server ausgeführt wird, z. b. Windows Server 2003 oder Windows Server 2008.


```C++
#include <windows.h>
#include <stdio.h>

BOOL Is_Win_Server() 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
   int op=VER_GREATER_EQUAL;

   // Initialize the OSVERSIONINFOEX structure.

   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.dwMinorVersion = 0;
   osvi.wServicePackMajor = 0;
   osvi.wServicePackMinor = 0;
   osvi.wProductType = VER_NT_SERVER;

   // Initialize the condition mask.

   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_MINORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMAJOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMINOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, VER_EQUAL );

   // Perform the test.

   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_MINORVERSION | 
      VER_SERVICEPACKMAJOR | VER_SERVICEPACKMINOR |
      VER_PRODUCT_TYPE,
      dwlConditionMask);
}

void main()
{
    if(Is_Win_Server())
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}
```



 

 



