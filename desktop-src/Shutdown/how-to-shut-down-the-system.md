---
description: Im folgenden Beispiel wird die ExitWindowsEx-Funktion verwendet, um das System herunterzufahren.
ms.assetid: bf8723aa-1c7f-4761-9034-d5a9447a4bc4
title: Herunterfahren des Systems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3880319e0ada6c82c6c6c12a7f3b5faf00415a93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373037"
---
# <a name="how-to-shut-down-the-system"></a>Herunterfahren des Systems

Im folgenden Beispiel wird die [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) -Funktion verwendet, um das System herunterzufahren. Beim Herunterfahren werden die Datei Puffer auf den Datenträger geleert, und das System wird zu einer Bedingung, in der der Computer sicher ausgeschaltet werden kann. Die Anwendung muss zuerst die Berechtigung für das Herunterfahren des Namens "SE" aktivieren \_ \_ Weitere Informationen finden Sie unter [Berechtigungen](../secauthz/privileges.md).


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



Der letzte Parameter im [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) -aufrufswert gibt an, dass das System für ein Planungs Update des Betriebssystems heruntergefahren wurde. Weitere Informationen finden Sie unter [Grund Codes](system-shutdown-reason-codes.md)für das Herunterfahren des Systems.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wird heruntergefahren](shutting-down.md)
</dt> </dl>

 

 
