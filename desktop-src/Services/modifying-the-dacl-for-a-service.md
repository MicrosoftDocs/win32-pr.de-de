---
description: Ein Dienststeuerungsprogramm kann die einem Dienst zugeordnete DACL erstellen oder ändern, um den Zugriff zu steuern.
ms.assetid: 24bfb2b5-34be-4d38-a690-90d29f5d4f9c
title: Ändern der DACL für einen Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089c97a014682082436511cd9dfe11a384cc1ff8f67bd993b8ea02b601356ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967873"
---
# <a name="modifying-the-dacl-for-a-service"></a>Ändern der DACL für einen Dienst

Ein [Dienststeuerungsprogramm](service-control-programs.md) kann die einem Dienst zugeordnete DACL erstellen oder ändern, um den Zugriff zu steuern. Verwenden Sie die [**QueryServiceObjectSecurity-Funktion,**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) um die einem Dienstobjekt zugeordnete DACL abzurufen. Verwenden Sie die [**SetServiceObjectSecurity-Funktion,**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) um die DACL festzulegen. Alle Änderungen am [**SECURITY \_ DESCRIPTOR,**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) die dem Dienstobjekt zugeordnet sind, sind persistent, bis der Dienst aus dem System entfernt wird.

Im folgenden Beispiel wird eine neue DACL für den Dienst erstellt und festgelegt. Der Code führt einen Zugriffssteuerungseintrag (ACE) mit der vorhandenen DACL für den Dienst zusammen. Der neue ACE gewährt dem Gastkonto Start-, Beendigungs-, Lösch- und \_ LESEZUGRIFF auf den angegebenen Dienst. Der Zugriff auf den Dienst kann durch den *AccessPermissions-Parameter* geändert werden, der an die [**BuildExplicitAccessWithName-Funktion**](/windows/desktop/api/aclapi/nf-aclapi-buildexplicitaccesswithnamea) übergeben wird.

Die variable szSvcName ist eine globale Variable, die den Namen des Diensts enthält. Das vollständige Beispiel, in dem diese Variable festgelegt wird, finden Sie unter [SvcControl.cpp.](svccontrol-cpp.md)


```C++
//
// Purpose: 
//   Updates the service DACL to grant start, stop, delete, and read
//   control access to the Guest account.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoUpdateSvcDacl()
{
    EXPLICIT_ACCESS      ea;
    SECURITY_DESCRIPTOR  sd;
    PSECURITY_DESCRIPTOR psd            = NULL;
    PACL                 pacl           = NULL;
    PACL                 pNewAcl        = NULL;
    BOOL                 bDaclPresent   = FALSE;
    BOOL                 bDaclDefaulted = FALSE;
    DWORD                dwError        = 0;
    DWORD                dwSize         = 0;
    DWORD                dwBytesNeeded  = 0;

    // Get a handle to the SCM database. 
 
    schSCManager = OpenSCManager( 
        NULL,                    // local computer
        NULL,                    // ServicesActive database 
        SC_MANAGER_ALL_ACCESS);  // full access rights 
 
    if (NULL == schSCManager) 
    {
        printf("OpenSCManager failed (%d)\n", GetLastError());
        return;
    }

    // Get a handle to the service

    schService = OpenService( 
        schSCManager,              // SCManager database 
        szSvcName,                 // name of service 
        READ_CONTROL | WRITE_DAC); // access
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Get the current security descriptor.

    if (!QueryServiceObjectSecurity(schService,
        DACL_SECURITY_INFORMATION, 
        &psd,           // using NULL does not work on all versions
        0, 
        &dwBytesNeeded))
    {
        if (GetLastError() == ERROR_INSUFFICIENT_BUFFER)
        {
            dwSize = dwBytesNeeded;
            psd = (PSECURITY_DESCRIPTOR)HeapAlloc(GetProcessHeap(),
                    HEAP_ZERO_MEMORY, dwSize);
            if (psd == NULL)
            {
                // Note: HeapAlloc does not support GetLastError.
                printf("HeapAlloc failed\n");
                goto dacl_cleanup;
            }
  
            if (!QueryServiceObjectSecurity(schService,
                DACL_SECURITY_INFORMATION, psd, dwSize, &dwBytesNeeded))
            {
                printf("QueryServiceObjectSecurity failed (%d)\n", GetLastError());
                goto dacl_cleanup;
            }
        }
        else 
        {
            printf("QueryServiceObjectSecurity failed (%d)\n", GetLastError());
            goto dacl_cleanup;
        }
    }

    // Get the DACL.

    if (!GetSecurityDescriptorDacl(psd, &bDaclPresent, &pacl,
                                   &bDaclDefaulted))
    {
        printf("GetSecurityDescriptorDacl failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Build the ACE.

    BuildExplicitAccessWithName(&ea, TEXT("GUEST"),
        SERVICE_START | SERVICE_STOP | READ_CONTROL | DELETE,
        SET_ACCESS, NO_INHERITANCE);

    dwError = SetEntriesInAcl(1, &ea, pacl, &pNewAcl);
    if (dwError != ERROR_SUCCESS)
    {
        printf("SetEntriesInAcl failed(%d)\n", dwError);
        goto dacl_cleanup;
    }

    // Initialize a new security descriptor.

    if (!InitializeSecurityDescriptor(&sd, 
        SECURITY_DESCRIPTOR_REVISION))
    {
        printf("InitializeSecurityDescriptor failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Set the new DACL in the security descriptor.

    if (!SetSecurityDescriptorDacl(&sd, TRUE, pNewAcl, FALSE))
    {
        printf("SetSecurityDescriptorDacl failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Set the new DACL for the service object.

    if (!SetServiceObjectSecurity(schService, 
        DACL_SECURITY_INFORMATION, &sd))
    {
        printf("SetServiceObjectSecurity failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }
    else printf("Service DACL updated successfully\n");

dacl_cleanup:
    CloseServiceHandle(schSCManager);
    CloseServiceHandle(schService);

    if(NULL != pNewAcl)
        LocalFree((HLOCAL)pNewAcl);
    if(NULL != psd)
        HeapFree(GetProcessHeap(), 0, (LPVOID)psd);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel für den vollständigen Dienst](the-complete-service-sample.md)
</dt> </dl>

 

 
