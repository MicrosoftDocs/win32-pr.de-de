---
description: Im folgenden Beispiel wird die ExitWindowsEx-Funktion verwendet, um das System herunterzufahren.
ms.assetid: bf8723aa-1c7f-4761-9034-d5a9447a4bc4
title: Herunterfahren des Systems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb366a3a6159cd43cf1f88f050d01ea75d365035c2f55598f69e91e89fc81de0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117963621"
---
# <a name="how-to-shut-down-the-system"></a>Herunterfahren des Systems

Im folgenden Beispiel wird die [**ExitWindowsEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) verwendet, um das System herunterzufahren. Beim Herunterfahren werden Dateipuffer auf den Datenträger geleert, und das System wird in eine Bedingung versetzt, in der es sicher ist, den Computer zu deaktivieren. Die Anwendung muss zuerst die berechtigung SE \_ SHUTDOWN \_ NAME aktivieren. Weitere Informationen finden Sie unter [Berechtigungen.](../secauthz/privileges.md)


```C++
#include <windows.h>

#pragma comment(lib, "user32.lib")
#pragma comment(lib, "advapi32.lib")

BOOL MySystemShutdown()
{
   HANDLE hToken; 
   TOKEN_PRIVILEGES tkp; 
 
   // Get a token for this process. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return( FALSE ); 
 
   // Get the LUID for the shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get the shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Shut down the system and force all applications to close. 
 
   if (!ExitWindowsEx(EWX_SHUTDOWN | EWX_FORCE, 
               SHTDN_REASON_MAJOR_OPERATINGSYSTEM |
               SHTDN_REASON_MINOR_UPGRADE |
               SHTDN_REASON_FLAG_PLANNED)) 
      return FALSE; 

   //shutdown was successful
   return TRUE;
}
```



Der letzte Parameter im Aufruf von [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) gibt an, dass das System für ein Planungsupdate des Betriebssystems heruntergefahren wurde. Weitere Informationen finden Sie unter [Ursachencodes für das Herunterfahren](system-shutdown-reason-codes.md)des Systems.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herunterfahren](shutting-down.md)
</dt> </dl>

 

 
