---
description: Durch das Aktivieren einer Berechtigung in einem Zugriffs Token kann der Prozess Aktionen auf Systemebene durchführen, die zuvor nicht möglich waren.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Aktivieren und Deaktivieren von Berechtigungen in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354f3ac2b27a7c027bd7c48e753263c43b676dd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050279"
---
# <a name="enabling-and-disabling-privileges-in-c"></a>Aktivieren und Deaktivieren von Berechtigungen in C++

Durch das Aktivieren einer Berechtigung in einem Zugriffs Token kann der Prozess Aktionen auf Systemebene durchführen, die zuvor nicht möglich waren. Die Anwendung sollte gründlich überprüfen, ob die Berechtigung für den Kontotyp geeignet ist, insbesondere für die folgenden leistungsstarken Berechtigungen.



| Berechtigungs Konstante           | Zeichenfolgenwert                  | `Display name`                        |
|------------------------------|-------------------------------|-------------------------------------|
| Name des zugriffsdiensts "SE" \_ \_ | SeAssignPrimaryTokenPrivilege | Ersetzen eines Tokens auf Prozessebene       |
| Name der SE- \_ Sicherung \_             | SeBackupPrivilege             | Sichern von Dateien und Verzeichnissen       |
| SE \_ - \_ debugname              | SeDebugPrivilege              | Debuggen von Programmen                      |
| \_ansteigende \_ Kontingent \_ Name für SE    | SeIncreaseQuotaPrivilege      | Anpassen von Speicherkontingenten für einen Prozess  |
| SE \_ TCB- \_ Name                | SeTcbPrivilege                | Einsetzen als Teil des Betriebssystems |



 

Bevor Sie diese potenziell gefährlichen Berechtigungen aktivieren, stellen Sie fest, dass Funktionen oder Vorgänge in Ihrem Code tatsächlich die Berechtigungen erfordern. So erfordern beispielsweise nur wenige Funktionen im Betriebssystem " **SeTcbPrivilege**". Eine Liste aller verfügbaren Berechtigungen finden Sie unter [Berechtigungs Konstanten](authorization-constants.md).

Im folgenden Beispiel wird gezeigt, wie Sie eine Berechtigung in einem [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)aktivieren oder deaktivieren. Im Beispiel wird die [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) -Funktion aufgerufen, um den [*lokal eindeutigen Bezeichner*](/windows/desktop/SecGloss/l-gly) (LUID) zu erhalten, den das lokale System zur Identifizierung der Berechtigung verwendet. Im Beispiel wird die Funktion "- [**tokenprivilegien**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) " aufgerufen, die entweder die Berechtigung aktiviert oder deaktiviert, die vom Wert des Parameters " *benableprivilege* " abhängt.


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "cmcfg32.lib")

BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) 
{
    TOKEN_PRIVILEGES tp;
    LUID luid;

    if ( !LookupPrivilegeValue( 
            NULL,            // lookup privilege on local system
            lpszPrivilege,   // privilege to lookup 
            &luid ) )        // receives LUID of privilege
    {
        printf("LookupPrivilegeValue error: %u\n", GetLastError() ); 
        return FALSE; 
    }

    tp.PrivilegeCount = 1;
    tp.Privileges[0].Luid = luid;
    if (bEnablePrivilege)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // Enable the privilege or disable all privileges.

    if ( !AdjustTokenPrivileges(
           hToken, 
           FALSE, 
           &tp, 
           sizeof(TOKEN_PRIVILEGES), 
           (PTOKEN_PRIVILEGES) NULL, 
           (PDWORD) NULL) )
    { 
          printf("AdjustTokenPrivileges error: %u\n", GetLastError() ); 
          return FALSE; 
    } 

    if (GetLastError() == ERROR_NOT_ALL_ASSIGNED)

    {
          printf("The token does not have the specified privilege. \n");
          return FALSE;
    } 

    return TRUE;
}

```



 

