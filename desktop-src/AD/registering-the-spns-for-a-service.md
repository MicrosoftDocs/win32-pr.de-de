---
title: Registrieren der SPNs für einen Dienst
description: Im folgenden Codebeispiel wird die Registrierung eines oder mehrere Dienstprinzipalnamen (SERVICE Principal Names, SPNs) für eine Dienstinstanz registriert oder aufgehoben.
ms.assetid: 60c252c7-76d2-4683-bf90-0f3483e6e8e0
ms.tgt_platform: multiple
keywords:
- Registrieren der SPNs für ein Dienst-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ff5d339ac9c2e51bceb15f29b7ad9cfd94e992ce826d596e2d81fcb25178ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184445"
---
# <a name="registering-the-spns-for-a-service"></a>Registrieren der SPNs für einen Dienst

Im folgenden Codebeispiel wird die Registrierung eines oder mehrere Dienstprinzipalnamen (SERVICE Principal Names, SPNs) für eine Dienstinstanz registriert oder aufgehoben.

Das Beispiel ruft die [**DsWriteAccountSpn-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) auf, die die SPNs in Active Directory Domain Services unter dem [**servicePrincipalName-Attribut**](/windows/desktop/ADSchema/a-serviceprincipalname) des Kontoobjekts speichert, das durch den *pszServiceAcctDN-Parameter* angegeben wird. Das Kontoobjekt entspricht dem Anmeldekonto, das im [**CreateService-Aufruf**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) für diese Dienstinstanz angegeben ist. Wenn das Anmeldekonto ein Domänenbenutzerkonto ist, muss *pszServiceAcctDN* der Distinguished Name des Kontoobjekts in Active Directory-Domäne Server für dieses Benutzerkonto sein. Wenn das Anmeldekonto des Diensts das LocalSystem-Konto ist, muss *pszServiceAcctDN* der Distinguished Name des Computerkontoobjekts für den Hostcomputer sein, auf dem der Dienst installiert ist.


```C++
/***************************************************************************

    SpnRegister()

    Register or unregister the SPNs under the service's account.

    If the service runs in LocalSystem account, pszServiceAcctDN is the 
    distinguished name of the local computer account.

    Parameters:

    pszServiceAcctDN - Contains the distinguished name of the logon 
    account for this instance of the service.

    pspn - Contains an array of SPNs to register.

    ulSpn - Contains the number of SPNs in the array.

    Operation - Contains one of the DS_SPN_WRITE_OP values that determines 
    the type of operation to perform on the SPNs.

***************************************************************************/

DWORD SpnRegister(TCHAR *pszServiceAcctDN,
                  TCHAR **pspn,
                  unsigned long ulSpn,
                  DS_SPN_WRITE_OP Operation)
{
    DWORD dwStatus;
    HANDLE hDs;
    TCHAR szSamName[512];
    DWORD dwSize = sizeof(szSamName) / sizeof(szSamName[0]);
    PDOMAIN_CONTROLLER_INFO pDcInfo;

    // Bind to a domain controller. 
    // Get the domain for the current user.
    if(GetUserNameEx(NameSamCompatible, szSamName, &dwSize))
    {
        TCHAR *pWhack = _tcschr(szSamName, '\\');
        if(pWhack)
        {
            *pWhack = '\0';
        }
    } 
    else 
    {
        return GetLastError();
    }
     
    // Get the name of a domain controller in that domain.
    dwStatus = DsGetDcName(NULL,
        szSamName,
        NULL,
        NULL,
        DS_IS_FLAT_NAME |
            DS_RETURN_DNS_NAME |
            DS_DIRECTORY_SERVICE_REQUIRED,
        &pDcInfo);
    if(dwStatus != 0) 
    {
        return dwStatus;
    }
     
    // Bind to the domain controller.
    dwStatus = DsBind(pDcInfo->DomainControllerName, NULL, &hDs);
     
    // Free the DOMAIN_CONTROLLER_INFO buffer.
    NetApiBufferFree(pDcInfo);
    if(dwStatus != 0) 
    {
        return dwStatus;
    }
     
    // Write the SPNs to the service account or computer account.
    dwStatus = DsWriteAccountSpn(
            hDs,                    // Handle to the directory.
            Operation,              // Add or remove SPN from account's existing SPNs.
            pszServiceAcctDN,       // DN of service account or computer account.
            ulSpn,                  // Number of SPNs to add.
            (const TCHAR **)pspn);  // Array of SPNs.

    // Unbind the DS in any case.
    DsUnBind(&hDs);
     
    return dwStatus;
}
```



 

 