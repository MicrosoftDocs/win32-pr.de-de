---
description: Ein Dienst Konfigurationsprogramm verwendet die OpenService-Funktion, um ein Handle mit Service \_ Query \_ config-Zugriff auf ein installiertes Dienst Objekt zu erhalten.
ms.assetid: e6633dc9-c9b6-457d-8adc-e751ec9cf71d
title: Abfragen einer Dienst Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efddea6ca590aa07b0c523588295d5f87ffefa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868396"
---
# <a name="querying-a-services-configuration"></a><span data-ttu-id="1b43a-103">Abfragen einer Dienst Konfiguration</span><span class="sxs-lookup"><span data-stu-id="1b43a-103">Querying a Service's Configuration</span></span>

<span data-ttu-id="1b43a-104">Ein [Dienst Konfigurationsprogramm](service-configuration-programs.md) verwendet die [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) -Funktion, um ein Handle mit Service \_ Query \_ config-Zugriff auf ein installiertes Dienst Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1b43a-104">A [service configuration program](service-configuration-programs.md) uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function to get a handle with SERVICE\_QUERY\_CONFIG access to an installed service object.</span></span> <span data-ttu-id="1b43a-105">Das Programm kann dann das Dienst Objekt Handle in den Funktionen [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) und [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) verwenden, um die aktuelle Konfiguration des Dienstanbieter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1b43a-105">The program can then use the service object handle in the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) functions to retrieve the current configuration of the service.</span></span>

<span data-ttu-id="1b43a-106">Im folgenden Beispiel verwendet die doquerysvc-Funktion [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) und [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) , um Konfigurationsinformationen abzurufen. Anschließend werden die ausgewählten Informationen in die Konsole geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1b43a-106">In the following example, the DoQuerySvc function uses [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) to retrieve configuration information, then writes selected information to the console.</span></span> <span data-ttu-id="1b43a-107">Die szsvcname-Variable ist eine globale Variable, die den Namen des Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="1b43a-107">The szSvcName variable is a global variable that contains the name of the service.</span></span> <span data-ttu-id="1b43a-108">Das komplette Beispiel, in dem diese Variable festgelegt wird, finden Sie unter [svcconfig. cpp](svcconfig-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="1b43a-108">For the complete example that sets this variable, see [SvcConfig.cpp](svcconfig-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Retrieves and displays the current service configuration.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoQuerySvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    LPQUERY_SERVICE_CONFIG lpsc; 
    LPSERVICE_DESCRIPTION lpsd;
    DWORD dwBytesNeeded, cbBufSize, dwError; 

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
        schSCManager,          // SCM database 
        szSvcName,             // name of service 
        SERVICE_QUERY_CONFIG); // need query config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }

    // Get the configuration information.
 
    if( !QueryServiceConfig( 
        schService, 
        NULL, 
        0, 
        &dwBytesNeeded))
    {
        dwError = GetLastError();
        if( ERROR_INSUFFICIENT_BUFFER == dwError )
        {
            cbBufSize = dwBytesNeeded;
            lpsc = (LPQUERY_SERVICE_CONFIG) LocalAlloc(LMEM_FIXED, cbBufSize);
        }
        else
        {
            printf("QueryServiceConfig failed (%d)", dwError);
            goto cleanup; 
        }
    }
  
    if( !QueryServiceConfig( 
        schService, 
        lpsc, 
        cbBufSize, 
        &dwBytesNeeded) ) 
    {
        printf("QueryServiceConfig failed (%d)", GetLastError());
        goto cleanup;
    }

    if( !QueryServiceConfig2( 
        schService, 
        SERVICE_CONFIG_DESCRIPTION,
        NULL, 
        0, 
        &dwBytesNeeded))
    {
        dwError = GetLastError();
        if( ERROR_INSUFFICIENT_BUFFER == dwError )
        {
            cbBufSize = dwBytesNeeded;
            lpsd = (LPSERVICE_DESCRIPTION) LocalAlloc(LMEM_FIXED, cbBufSize);
        }
        else
        {
            printf("QueryServiceConfig2 failed (%d)", dwError);
            goto cleanup; 
        }
    }
 
    if (! QueryServiceConfig2( 
        schService, 
        SERVICE_CONFIG_DESCRIPTION,
        (LPBYTE) lpsd, 
        cbBufSize, 
        &dwBytesNeeded) ) 
    {
        printf("QueryServiceConfig2 failed (%d)", GetLastError());
        goto cleanup;
    }
 
    // Print the configuration information.
 
    _tprintf(TEXT("%s configuration: \n"), szSvcName);
    _tprintf(TEXT("  Type: 0x%x\n"), lpsc->dwServiceType);
    _tprintf(TEXT("  Start Type: 0x%x\n"), lpsc->dwStartType);
    _tprintf(TEXT("  Error Control: 0x%x\n"), lpsc->dwErrorControl);
    _tprintf(TEXT("  Binary path: %s\n"), lpsc->lpBinaryPathName);
    _tprintf(TEXT("  Account: %s\n"), lpsc->lpServiceStartName);

    if (lpsd->lpDescription != NULL && lstrcmp(lpsd->lpDescription, TEXT("")) != 0)
        _tprintf(TEXT("  Description: %s\n"), lpsd->lpDescription);
    if (lpsc->lpLoadOrderGroup != NULL && lstrcmp(lpsc->lpLoadOrderGroup, TEXT("")) != 0)
        _tprintf(TEXT("  Load order group: %s\n"), lpsc->lpLoadOrderGroup);
    if (lpsc->dwTagId != 0)
        _tprintf(TEXT("  Tag ID: %d\n"), lpsc->dwTagId);
    if (lpsc->lpDependencies != NULL && lstrcmp(lpsc->lpDependencies, TEXT("")) != 0)
        _tprintf(TEXT("  Dependencies: %s\n"), lpsc->lpDependencies);
 
    LocalFree(lpsc); 
    LocalFree(lpsd);

cleanup:
    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a><span data-ttu-id="1b43a-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b43a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b43a-110">Dienstkonfiguration:</span><span class="sxs-lookup"><span data-stu-id="1b43a-110">Service Configuration</span></span>](service-configuration.md)
</dt> <dt>

[<span data-ttu-id="1b43a-111">Das Complete Service-Beispiel</span><span class="sxs-lookup"><span data-stu-id="1b43a-111">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



