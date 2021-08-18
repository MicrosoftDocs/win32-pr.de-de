---
description: Das Token des Aufrufers muss die Sicherungs- und Wiederherstellungsberechtigungen enthalten, damit die Api für die Sicherung und Wiederherstellung der Zertifikatdienste erfolgreich aufgerufen werden kann.
ms.assetid: 409a9fad-7141-4ba8-ab3d-fb590366001e
title: Festlegen der Sicherungs- und Wiederherstellungsberechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990f1009ec5b57d6dcc9f11ef505e705fb483362518d6e54f5d0c9a0167cc211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900310"
---
# <a name="setting-the-backup-and-restore-privileges"></a>Festlegen der Sicherungs- und Wiederherstellungsberechtigungen

Zum erfolgreichen Aufrufen der Sicherungs- und Wiederherstellungs-API der Zertifikatdienste muss das Token des Aufrufers die Sicherungs- und [*Wiederherstellungsberechtigungen*](../secgloss/p-gly.md)enthalten. Diese Berechtigungen können programmgesteuert festgelegt werden, und im folgenden Beispiel können diese Berechtigungen festgelegt oder entfernt werden. Die Sicherungs- und Wiederherstellungsberechtigungen sind für alle Sicherungs- und Wiederherstellungsanwendungen erforderlich, nicht nur für die Sicherung und Wiederherstellung von Zertifikatdiensten. Informationen zu den Sicherheitsauswirkungen beim Ändern von Berechtigungen finden Sie unter [Ausführen mit speziellen Berechtigungen.](../secbp/running-with-special-privileges.md)


```C++
// The following example can be used to enable or disable the
// backup privilege. By making the indicated substitutions, you can
// also use this example to enable or disable the restore privilege 
// Use the following statement to enable the privilege:
//   hr = ModifyPrivilege(SE_BACKUP_NAME, TRUE);
// Use the following statement to disable the privilege:
//   hr = ModifyPrivilege(SE_BACKUP_NAME, FALSE);
// Use SE_RESTORE_NAME for the restore privilege.
// The main function in this example enables the backup privilege.
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <stdio.h>


HRESULT ModifyPrivilege(
    IN LPCTSTR szPrivilege,
    IN BOOL fEnable)
{
    HRESULT hr = S_OK;
    TOKEN_PRIVILEGES NewState;
    LUID             luid;
    HANDLE hToken    = NULL;

    // Open the process token for this process.
    if (!OpenProcessToken(GetCurrentProcess(),
                          TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY,
                          &hToken ))
    {
        printf("Failed OpenProcessToken\n");
        return ERROR_FUNCTION_FAILED;
    }

    // Get the local unique ID for the privilege.
    if ( !LookupPrivilegeValue( NULL,
                                szPrivilege,
                                &luid ))
    {
        CloseHandle( hToken );
        printf("Failed LookupPrivilegeValue\n");
        return ERROR_FUNCTION_FAILED;
    }

    // Assign values to the TOKEN_PRIVILEGE structure.
    NewState.PrivilegeCount = 1;
    NewState.Privileges[0].Luid = luid;
    NewState.Privileges[0].Attributes = 
              (fEnable ? SE_PRIVILEGE_ENABLED : 0);

    // Adjust the token privilege.
    if (!AdjustTokenPrivileges(hToken,
                               FALSE,
                               &NewState,
                               0,
                               NULL,
                               NULL))
    {
        printf("Failed AdjustTokenPrivileges\n");
        hr = ERROR_FUNCTION_FAILED;
    }

    // Close the handle.
    CloseHandle(hToken);

    return hr;
}

void main(void)
{
    HRESULT hr;

    hr = ModifyPrivilege(SE_BACKUP_NAME, TRUE);

    if (!SUCCEEDED(hr))
        printf("\nFailed to modify privilege.\n");
    else
        printf("\nSuccessfully modified privilege.\n");
}

```



 

 
