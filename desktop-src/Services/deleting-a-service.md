---
description: Ein Dienst Konfigurationsprogramm verwendet die OpenService-Funktion, um ein Handle für ein installiertes Dienst Objekt zu erhalten. Das Programm kann dann das Dienst Objekt Handle in der Delta Service-Funktion verwenden, um den Dienst aus der SCM-Datenbank zu löschen.
ms.assetid: 3bfe4d42-a8a0-4613-9b0f-a80eef54b622
title: Löschen eines Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b1e0e95e0ea943487a0d3fa513afa2c0563d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960442"
---
# <a name="deleting-a-service"></a><span data-ttu-id="6e064-104">Löschen eines Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="6e064-104">Deleting a Service</span></span>

<span data-ttu-id="6e064-105">Ein [Dienst Konfigurationsprogramm](service-configuration-programs.md) verwendet die [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) -Funktion, um ein Handle für ein installiertes Dienst Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e064-105">A [service configuration program](service-configuration-programs.md) uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function to get a handle to an installed service object.</span></span> <span data-ttu-id="6e064-106">Das Programm kann dann das Dienst Objekt Handle in der [**Delta**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) Service-Funktion verwenden, um den Dienst aus der SCM-Datenbank zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6e064-106">The program can then use the service object handle in the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service from the SCM database.</span></span>

<span data-ttu-id="6e064-107">Die Funktion dodelta etesvc im folgenden Beispiel zeigt, wie ein Dienst aus der SCM-Datenbank gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6e064-107">The DoDeleteSvc function in the following example shows how to delete a service from the SCM database.</span></span> <span data-ttu-id="6e064-108">Die szsvcname-Variable ist eine globale Variable, die den Namen des zu löschenden dienstanens enthält.</span><span class="sxs-lookup"><span data-stu-id="6e064-108">The szSvcName variable is a global variable that contains the name of the service to be deleted.</span></span> <span data-ttu-id="6e064-109">Das komplette Beispiel, in dem diese Variable festgelegt wird, finden Sie unter [svcconfig. cpp](svcconfig-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="6e064-109">For the complete example that sets this variable, see [SvcConfig.cpp](svcconfig-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Deletes a service from the SCM database
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoDeleteSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    SERVICE_STATUS ssStatus; 

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

    // Get a handle to the service.

    schService = OpenService( 
        schSCManager,       // SCM database 
        szSvcName,          // name of service 
        DELETE);            // need delete access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }

    // Delete the service.
 
    if (! DeleteService(schService) ) 
    {
        printf("DeleteService failed (%d)\n", GetLastError()); 
    }
    else printf("Service deleted successfully\n"); 
 
    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a><span data-ttu-id="6e064-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e064-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e064-111">Dienst Installation, Entfernung und Enumeration</span><span class="sxs-lookup"><span data-stu-id="6e064-111">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> <dt>

[<span data-ttu-id="6e064-112">Das Complete Service-Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e064-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



