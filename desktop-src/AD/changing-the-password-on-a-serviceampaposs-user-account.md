---
title: Ändern des Kennworts für das Benutzerkonto eines Diensts
description: Bei einer Dienstinstanz, die sich nicht mit dem LocalSystem-Konto, sondern mit einem Benutzerkonto anmeldet, speichert der Dienststeuerungs-Manager (Service Control Manager, SCM) auf dem Hostcomputer das Kontokennwort, das zum Anmelden beim Dienst beim Starten des Diensts verwendet wird.
ms.assetid: d9cef772-bd85-4103-901e-3cf786b29163
ms.tgt_platform: multiple
keywords:
- Ändern des Kennworts für das Ad-Benutzerkonto eines Diensts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66f0d7b4dc668697b7a0a8d5b120735f3a445cf
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881629"
---
# <a name="changing-the-password-on-a-services-user-account"></a>Ändern des Kennworts für das Benutzerkonto eines Diensts

Bei einer Dienstinstanz, die sich nicht mit dem LocalSystem-Konto, sondern mit einem Benutzerkonto anmeldet, speichert der Dienststeuerungs-Manager (Service Control Manager, SCM) auf dem Hostcomputer das Kontokennwort, das zum Anmelden beim Dienst beim Starten des Diensts verwendet wird. Wie bei jedem Benutzerkonto müssen Sie das Kennwort in regelmäßigen Abständen ändern, um die Sicherheit zu gewährleisten. Wenn Sie das Kennwort für ein Dienstkonto ändern, aktualisieren Sie das vom SCM gespeicherte Kennwort. Im folgenden Codebeispiel wird gezeigt, wie beides funktioniert.

In den Codebeispielen wird [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) verwendet, um das Kontokennwort festzulegen. Diese Methode verwendet den Distinguished Name des Kontos. Anschließend öffnet das Beispiel ein Handle für den installierten Dienst auf dem angegebenen Hostcomputer und verwendet die [**ChangeServiceConfig-Funktion,**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) um das vom SCM zwischengespeicherte Kennwort zu aktualisieren. Diese Funktion verwendet den SAM-Namen &lt; &gt; \\ &lt; ("Domänenbenutzername") &gt; des Kontos.

> [!Note]  
> Dieser Code muss von einem Domänenadministrator ausgeführt werden.

 

Für einen replikatierbaren Dienst, bei dem jedes Replikat ein anderes Anmeldekonto verwendet, können Sie die Kennwörter für alle Replikate aktualisieren, indem Sie die Dienstinstanzen aufzählen. Weitere Informationen und ein Codebeispiel finden Sie unter [Aufzählen der Replikate eines Diensts.](enumerating-the-replicas-of-a-service.md)


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



 

 
