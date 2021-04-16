---
title: Ändern des Kennworts für das Benutzerkonto eines Dienstanbieter
description: Bei einer Dienst Instanz, die sich mit einem Benutzerkonto anstatt mit dem LocalSystem-Konto anmeldet, speichert der Dienststeuerungs-Manager auf dem Host Computer das Konto Kennwort, das für die Anmeldung beim Dienst beim Start des Diensts verwendet wird.
ms.assetid: d9cef772-bd85-4103-901e-3cf786b29163
ms.tgt_platform: multiple
keywords:
- Ändern des Kennworts für das Benutzerkonto-AD eines Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf16b018796979d3710825472a5f9abab72cd24
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472676"
---
# <a name="changing-the-password-on-a-services-user-account"></a>Ändern des Kennworts für das Benutzerkonto eines Dienstanbieter

Bei einer Dienst Instanz, die sich mit einem Benutzerkonto anstatt mit dem LocalSystem-Konto anmeldet, speichert der Dienststeuerungs-Manager auf dem Host Computer das Konto Kennwort, das für die Anmeldung beim Dienst beim Start des Diensts verwendet wird. Wie bei jedem Benutzerkonto müssen Sie das Kennwort in regelmäßigen Abständen ändern, um die Sicherheit zu gewährleisten. Wenn Sie das Kennwort für ein Dienst Konto ändern, aktualisieren Sie das Kennwort, das vom SCM gespeichert wird. Im folgenden Codebeispiel wird gezeigt, wie beides durchzuführen ist.

In den Codebeispielen wird [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) verwendet, um das Konto Kennwort festzulegen. Diese Methode verwendet den Distinguished Name des Kontos. Anschließend wird im Beispiel ein Handle für den installierten Dienst auf dem angegebenen Host Computer geöffnet und die [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) -Funktion verwendet, um das vom SCM zwischengespeicherte Kennwort zu aktualisieren. Diese Funktion verwendet den SAM-Namen (" <domain> \\ <username> ") des Kontos.

> [!Note]  
> Dieser Code muss von einem Domänen Administrator ausgeführt werden.

 

Bei einem replizierbaren Dienst, bei dem jedes Replikat ein anderes Anmelde Konto verwendet, können Sie die Kenn Wörter für alle Replikate aktualisieren, indem Sie die Dienst Instanzen auflisten. Weitere Informationen und ein Codebeispiel finden Sie unter Auflisten [der Replikate eines Dienstanbieter](enumerating-the-replicas-of-a-service.md).


```C++
DWORD UpdateAccountPassword(
    LPTSTR szServerDNS,   // DNS name of host computer
    LPTSTR szAccountDN,   // Distinguished name of service 
                          // logon account
    LPTSTR szServiceName, // Name of the service
    LPTSTR szOldPassword, // Old password
    LPTSTR szNewPassword  // New password
    )
{
SC_HANDLE schService = NULL;
SC_HANDLE schSCManager = NULL;
 
DWORD dwLen = MAX_PATH;
TCHAR szAccountPath[MAX_PATH];
IADsUser *pUser = NULL;
HRESULT hr;
 
DWORD dwStatus = 0;
SC_LOCK sclLock = NULL; 

if( !szServerDNS || 
    !szAccountDN || 
    !szServiceName || 
    !szOldPassword || 
    !szNewPassword)
{
    _tprintf(TEXT("Invalid parameter"));
    goto cleanup;
}
 
// Set the password on the account.
// Use the distinguished name to bind to the account object.
_tcsncpy_s(szAccountPath, TEXT("LDAP://"), MAX_PATH);
_tcscat_s(szAccountPath, 
    szAccountDN, 
    MAX_PATH - _tcslen(szAccountPath));
hr = ADsGetObject(szAccountPath, IID_IADsUser, (void**)&pUser);
if (FAILED(hr)) 
{
    _tprintf(TEXT("Get IADsUser failed - 0x%x\n"), dwStatus = hr);
       goto cleanup;
}
 
// Set the password on the account. 
hr = pUser->ChangePassword(CComBSTR(szOldPassword), 
    CComBSTR(szNewPassword));
if (FAILED(hr)) 
{
    _tprintf(TEXT("ChangePassword failed - 0x%x\n"), 
             dwStatus = hr);
    goto cleanup;
}
 
// Update the account and password in the SCM database.
// Open the Service Control Manager on the specified computer.
schSCManager = OpenSCManager(
                szServerDNS,          // DNS name of host computer
                NULL,                 // database (NULL == default)
                SC_MANAGER_ALL_ACCESS // access required
                        );
if (! schSCManager) 
{
    _tprintf(TEXT("OpenSCManager failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Open a handle to the service instance.
schService = OpenService(schSCManager, 
    szServiceName, 
    SERVICE_ALL_ACCESS);
if (! schService) 
{
    _tprintf(TEXT("OpenService failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Get the SCM database lock before changing the password. 
sclLock = LockServiceDatabase(schSCManager); 
if (sclLock == NULL) {
    _tprintf(TEXT("LockServiceDatabase failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Set the account and password that the service uses at startup.
if (! ChangeServiceConfig( 
        schService,        // Handle of service 
        SERVICE_NO_CHANGE, // Service type: no change 
        SERVICE_NO_CHANGE, // Change service start type 
        SERVICE_NO_CHANGE, // Error control: no change 
        NULL,              // Binary path: no change 
        NULL,              // Load order group: no change 
        NULL,              // Tag ID: no change 
        NULL,              // Dependencies: no change 
        NULL,              // Account name: no change 
        szNewPassword,     // New password 
        NULL) )            // Display name: no change
{
    _tprintf(TEXT("ChangeServiceConfig failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
_tprintf(TEXT("Password changed for service instance on: %s\n"), 
    szServerDNS);

cleanup:
 
if (sclLock)
    UnlockServiceDatabase(sclLock); 
if (schService)
    CloseServiceHandle(schService);
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (pUser)
    pUser->Release();
 
return dwStatus;
}
```



 

 