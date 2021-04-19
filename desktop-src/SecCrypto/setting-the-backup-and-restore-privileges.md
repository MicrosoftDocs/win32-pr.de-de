---
description: Um die Backup-und Restore-API der Zertifikat Dienste erfolgreich aufzurufen, muss das Token des Aufrufers die Sicherungs-und Wiederherstellungs Berechtigungen enthalten.
ms.assetid: 409a9fad-7141-4ba8-ab3d-fb590366001e
title: Festlegen der Sicherungs-und Wiederherstellungs Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd70c3726c435efa1f000add101bbf50b725bb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344239"
---
# <a name="setting-the-backup-and-restore-privileges"></a><span data-ttu-id="5f73b-103">Festlegen der Sicherungs-und Wiederherstellungs Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="5f73b-103">Setting the Backup and Restore Privileges</span></span>

<span data-ttu-id="5f73b-104">Um die Backup-und Restore-API der Zertifikat Dienste erfolgreich aufzurufen, muss das Token des Aufrufers die Sicherungs-und Wiederherstellungs [*Berechtigungen*](../secgloss/p-gly.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="5f73b-104">To successfully call the Certificate Services backup and restore API, the caller's token must include the backup and restore [*privileges*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="5f73b-105">Diese Berechtigungen können Programm gesteuert festgelegt werden, und das folgende Beispiel kann verwendet werden, um diese Berechtigungen festzulegen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5f73b-105">These privileges can be programmatically set, and the following example can be used to set or remove these privileges.</span></span> <span data-ttu-id="5f73b-106">Die Sicherungs-und Wiederherstellungs Berechtigungen sind für alle Sicherungs-und Wiederherstellungs Anwendungen erforderlich, nicht nur für die Sicherung und Wiederherstellung von Zertifikat Diensten.</span><span class="sxs-lookup"><span data-stu-id="5f73b-106">The backup and restore privileges are required of all backup and restore applications, not merely Certificate Services backup and restore.</span></span> <span data-ttu-id="5f73b-107">Informationen zu den Sicherheitsauswirkungen der Änderung von Berechtigungen finden Sie unter [Ausführen mit besonderen Berechtigungen](../secbp/running-with-special-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="5f73b-107">For information about the security implications of modifying privileges, see [Running with Special Privileges](../secbp/running-with-special-privileges.md).</span></span>


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



 

 
