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
# <a name="deleting-a-service"></a>Löschen eines Dienstanbieter

Ein [Dienst Konfigurationsprogramm](service-configuration-programs.md) verwendet die [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) -Funktion, um ein Handle für ein installiertes Dienst Objekt zu erhalten. Das Programm kann dann das Dienst Objekt Handle in der [**Delta**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) Service-Funktion verwenden, um den Dienst aus der SCM-Datenbank zu löschen.

Die Funktion dodelta etesvc im folgenden Beispiel zeigt, wie ein Dienst aus der SCM-Datenbank gelöscht wird. Die szsvcname-Variable ist eine globale Variable, die den Namen des zu löschenden dienstanens enthält. Das komplette Beispiel, in dem diese Variable festgelegt wird, finden Sie unter [svcconfig. cpp](svcconfig-cpp.md).


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dienst Installation, Entfernung und Enumeration](service-installation-removal-and-enumeration.md)
</dt> <dt>

[Das Complete Service-Beispiel](the-complete-service-sample.md)
</dt> </dl>

 

 



