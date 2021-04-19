---
description: VDS werden geladen
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: VDS werden geladen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c66685668641f3036739c57bd7353f72052c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359150"
---
# <a name="loading-vds"></a>VDS werden geladen

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

**So laden und initialisieren Sie VDS**

1.  Freigeben von nicht-NULL-Schnittstellen.
2.  Rufen Sie die [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)-, [**cokreateinstanceex**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)-oder [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) -Funktion auf, um einen Zeiger auf das Dienst Lade Objekt zu erhalten.

    **CLSCTX \_ Die Deaktivierung von \_ AAA** kann in diesem-Befehl nicht angegeben werden. Wenn [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufgerufen wird, kann das **eoac- \_ Deaktivieren von \_ AAA** nicht im *dwfunktionen* -Parameter angegeben werden.

3.  Zum Laden von VDS wird die [**ivdsserviceloader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) -Methode aufgerufen.

    Wenn **null** als erster Parameter übergeben wird, werden VDS auf dem lokalen Host geladen und initialisiert.

4.  Aufrufen der [**ivdsservice:: waitforserviceready**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) -Methode, um auf den Abschluss der VDS-Initialisierung zu warten.

Im folgenden Codebeispiel wird der Dienst initialisiert, der einen Zeiger auf das Dienst Objekt zurückgibt.


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

[**Ivdsservice:: waitforserviceready**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[**Ivdsserviceloader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Setup und Dienst Objekte](startup-and-service-objects.md)
</dt> </dl>

 

 
