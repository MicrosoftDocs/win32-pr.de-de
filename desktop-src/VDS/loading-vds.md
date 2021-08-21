---
description: Laden von VDS
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: Laden von VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec6a757b57c8e06e53862b3d36b9d54f291e4b07693dff008ecc2bbbb961c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125940"
---
# <a name="loading-vds"></a>Laden von VDS

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

**So laden und initialisieren Sie VDS**

1.  Geben Sie Schnittstellen frei, die nicht NULL sind.
2.  Rufen Sie [**die Funktion CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)oder [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) auf, um einen Zeiger auf das Dienstladeobjekt zu erhalten.

    **CLSCTX \_ DISABLE \_ AAA** kann in diesem Aufruf nicht angegeben werden. Wenn [**CoInitializeSecurity aufgerufen**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) wird, **kann EOAC \_ DISABLE \_ AAA** nicht im *dwCapabilities-Parameter angegeben* werden.

3.  Rufen Sie die [**IVdsServiceLoader::LoadService-Methode auf,**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) um VDS zu laden.

    Das **Übergeben von NULL** als erster Parameter lädt und initialisiert VDS auf dem lokalen Host.

4.  Rufen Sie die [**IVdsService::WaitForServiceReady-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) auf, um auf den Abschluss der VDS-Initialisierung zu warten.

Im folgenden Codebeispiel wird der Dienst initialisiert, der einen Zeiger auf das Dienstobjekt zurückgibt.


```C++
#include "initguid.h"
#include "vds.h"
#include <stdio.h>

#pragma comment( lib, "ole32.lib" )

//
// Simple macro to release non-null interfaces.
//
#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

void __cdecl main(void) 
{
    HRESULT hResult;
    IVdsService *pService = NULL;
    IVdsServiceLoader *pLoader = NULL;

    // For this, you first get a pointer to the VDS Loader
    // Launch the VDS service. 
    //

    hResult = CoInitialize(NULL);

    if (SUCCEEDED(hResult)) 
    {
    
        hResult = CoCreateInstance(CLSID_VdsLoader,
            NULL,
            CLSCTX_LOCAL_SERVER,
            IID_IVdsServiceLoader,
            (void **) &pLoader);

        // 
        // And then load VDS on the local computer.
        //
        if (SUCCEEDED(hResult)) 
        {
            hResult = pLoader->LoadService(NULL, &pService);
        }

        //
        // You're done with the Loader interface at this point.
        //
        _SafeRelease(pLoader); 
        
        if (SUCCEEDED(hResult)) 
        {
            hResult = pService->WaitForServiceReady();
            if (SUCCEEDED(hResult)) 
            {
                //
                // You obtained an interface to the service: pService.
                // This interface can now be used to query for providers 
                // and perform other operations. 
                //
                printf("VDS Service Loaded");
            }

        } 
        else 
        {
            printf("VDS Service failed hr=%x\n",hResult);
        }
    }
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VDS](using-vds.md)
</dt> <dt>

[**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Setup- und Dienstobjekte](startup-and-service-objects.md)
</dt> </dl>

 

 
