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
# <a name="how-to-shut-down-the-system"></a><span data-ttu-id="00fc1-103">Herunterfahren des Systems</span><span class="sxs-lookup"><span data-stu-id="00fc1-103">How to Shut Down the System</span></span>

<span data-ttu-id="00fc1-104">Im folgenden Beispiel wird die [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) -Funktion verwendet, um das System herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="00fc1-104">The following example uses the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function to shut down the system.</span></span> <span data-ttu-id="00fc1-105">Beim Herunterfahren werden die Datei Puffer auf den Datenträger geleert, und das System wird zu einer Bedingung, in der der Computer sicher ausgeschaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="00fc1-105">Shutting down flushes file buffers to disk and brings the system to a condition in which it is safe to turn off the computer.</span></span> <span data-ttu-id="00fc1-106">Die Anwendung muss zuerst die Berechtigung für das Herunterfahren des Namens "SE" aktivieren \_ \_</span><span class="sxs-lookup"><span data-stu-id="00fc1-106">The application must first enable the SE\_SHUTDOWN\_NAME privilege.</span></span> <span data-ttu-id="00fc1-107">Weitere Informationen finden Sie unter [Berechtigungen](../secauthz/privileges.md).</span><span class="sxs-lookup"><span data-stu-id="00fc1-107">For more information, see [Privileges](../secauthz/privileges.md).</span></span>


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



<span data-ttu-id="00fc1-108">Der letzte Parameter im [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) -aufrufswert gibt an, dass das System für ein Planungs Update des Betriebssystems heruntergefahren wurde.</span><span class="sxs-lookup"><span data-stu-id="00fc1-108">The final parameter in the call to [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) indicates that the system was shut down for a planning update of the operating system.</span></span> <span data-ttu-id="00fc1-109">Weitere Informationen finden Sie unter [Grund Codes](system-shutdown-reason-codes.md)für das Herunterfahren des Systems.</span><span class="sxs-lookup"><span data-stu-id="00fc1-109">For more information, see [System Shutdown Reason Codes](system-shutdown-reason-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00fc1-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00fc1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00fc1-111">Wird heruntergefahren</span><span class="sxs-lookup"><span data-stu-id="00fc1-111">Shutting Down</span></span>](shutting-down.md)
</dt> </dl>

 

 
