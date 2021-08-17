---
description: Wenn Sie eine Berechtigung in einem Zugriffstoken aktivieren, kann der Prozess Aktionen auf Systemebene ausführen, die zuvor nicht möglich waren.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Aktivieren und Deaktivieren von Berechtigungen in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc36e3db162b1a7a7f12f1849ab7708bda19d90991e58a65135d0eb4c0abd04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781726"
---
# <a name="enabling-and-disabling-privileges-in-c"></a>Aktivieren und Deaktivieren von Berechtigungen in C++

Wenn Sie eine Berechtigung in einem Zugriffstoken aktivieren, kann der Prozess Aktionen auf Systemebene ausführen, die zuvor nicht möglich waren. Ihre Anwendung sollte gründlich überprüfen, ob die Berechtigung für den Typ des Kontos geeignet ist, insbesondere für die folgenden leistungsstarken Berechtigungen.



| Berechtigungskonstante           | Zeichenfolgenwert                  | Anzeigename                        |
|------------------------------|-------------------------------|-------------------------------------|
| \_SE ASSIGNPRIMARYTOKEN-NAME \_ | SeAssignPrimaryTokenPrivilege | Ersetzen eines Tokens auf Prozessebene       |
| \_SE \_SICHERUNGSNAME             | SeBackupPrivilege             | Sichern von Dateien und Verzeichnissen       |
| \_SE \_DEBUGNAME              | SeDebugPrivilege              | Debuggen von Programmen                      |
| \_SE ERHÖHEN DES \_ \_ KONTINGENTNAMENS    | SeIncreaseQuotaPrivilege      | Anpassen von Speicherkontingenten für einen Prozess  |
| \_SE \_TCB-NAME                | SeTcbPrivilege                | Einsetzen als Teil des Betriebssystems |



 

Bevor Sie diese potenziell gefährlichen Berechtigungen aktivieren, bestimmen Sie, ob Funktionen oder Vorgänge in Ihrem Code die Berechtigungen tatsächlich benötigen. Beispielsweise erfordern nur sehr wenige Funktionen im Betriebssystem tatsächlich **seTcbPrivilege**. Eine Liste aller verfügbaren Berechtigungen finden Sie unter [Berechtigungskonstanten.](authorization-constants.md)

Das folgende Beispiel zeigt, wie Sie eine Berechtigung in einem [*Zugriffstoken*](/windows/desktop/SecGloss/a-gly)aktivieren oder deaktivieren. Das Beispiel ruft die [**LookupPrivilegeValue-Funktion**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) auf, um den [*lokal eindeutigen Bezeichner*](/windows/desktop/SecGloss/l-gly) (LUID) abzurufen, den das lokale System zum Identifizieren der Berechtigung verwendet. Anschließend ruft das Beispiel die [**AdjustTokenPrivileges-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) auf, die die Berechtigung aktiviert oder deaktiviert, die vom Wert des *bEnablePrivilege-Parameters* abhängt.


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



 

