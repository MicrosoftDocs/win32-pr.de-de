---
description: Ein Dienst Steuerungsprogramm kann die mit einem Dienst verknüpfte DACL erstellen oder ändern, um den Zugriff zu steuern.
ms.assetid: 24bfb2b5-34be-4d38-a690-90d29f5d4f9c
title: Ändern der DACL für einen Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d814f6bc81b6d6a207bebf0e9b88c0bb672cdfbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867608"
---
# <a name="modifying-the-dacl-for-a-service"></a><span data-ttu-id="4de02-103">Ändern der DACL für einen Dienst</span><span class="sxs-lookup"><span data-stu-id="4de02-103">Modifying the DACL for a Service</span></span>

<span data-ttu-id="4de02-104">Ein [Dienst Steuerungsprogramm](service-control-programs.md) kann die mit einem Dienst verknüpfte DACL erstellen oder ändern, um den Zugriff zu steuern.</span><span class="sxs-lookup"><span data-stu-id="4de02-104">A [service control program](service-control-programs.md) can create or modify the DACL associated with a service to control access.</span></span> <span data-ttu-id="4de02-105">Verwenden Sie zum Abrufen der DACL, die einem Dienst Objekt zugeordnet ist, die [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4de02-105">To retrieve the DACL associated with a service object, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function.</span></span> <span data-ttu-id="4de02-106">Verwenden Sie die Funktion [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) , um die DACL festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4de02-106">To set the DACL, use the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function.</span></span> <span data-ttu-id="4de02-107">Alle Änderungen an der [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die dem Dienst Objekt zugeordnet ist, bleiben persistent, bis der Dienst aus dem System entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4de02-107">Any changes made to the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associated with the service object are persistent until the service is removed from the system.</span></span>

<span data-ttu-id="4de02-108">Im folgenden Beispiel wird eine neue DACL für den Dienst erstellt und festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4de02-108">The following example creates and sets a new DACL for the service.</span></span> <span data-ttu-id="4de02-109">Der Code verbindet einen Zugriffs Steuerungs Eintrag (ACE) mit der vorhandenen DACL für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="4de02-109">The code merges one access control entry (ACE) to the existing DACL for the service.</span></span> <span data-ttu-id="4de02-110">Der neue ACE gewährt dem Gast Konto den \_ Zugriff auf den angegebenen Dienst und den Vorgang zum Starten, Abbrechen, löschen und lesen.</span><span class="sxs-lookup"><span data-stu-id="4de02-110">The new ACE grants the Guest account start, stop, delete, and READ\_CONTROL access to the specified service.</span></span> <span data-ttu-id="4de02-111">Der Zugriff auf den Dienst kann durch den Parameter " *accesspermissions* " geändert werden, der an die Funktion " [**buildexplicitaccesswithname**](/windows/desktop/api/aclapi/nf-aclapi-buildexplicitaccesswithnamea) " übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4de02-111">Access to the service can be modified by the *AccessPermissions* parameter passed to the [**BuildExplicitAccessWithName**](/windows/desktop/api/aclapi/nf-aclapi-buildexplicitaccesswithnamea) function.</span></span>

<span data-ttu-id="4de02-112">Die szsvcname-Variable ist eine globale Variable, die den Namen des Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="4de02-112">The szSvcName variable is a global variable that contains the name of the service.</span></span> <span data-ttu-id="4de02-113">Das komplette Beispiel, in dem diese Variable festgelegt wird, finden Sie unter [svccontrol. cpp](svccontrol-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="4de02-113">For the complete example that sets this variable, see [SvcControl.cpp](svccontrol-cpp.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4de02-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4de02-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4de02-115">Das Complete Service-Beispiel</span><span class="sxs-lookup"><span data-stu-id="4de02-115">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
