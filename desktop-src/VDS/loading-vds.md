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
# <a name="loading-vds"></a><span data-ttu-id="ad251-103">VDS werden geladen</span><span class="sxs-lookup"><span data-stu-id="ad251-103">Loading VDS</span></span>

<span data-ttu-id="ad251-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="ad251-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="ad251-105">**So laden und initialisieren Sie VDS**</span><span class="sxs-lookup"><span data-stu-id="ad251-105">**To load and initialize VDS**</span></span>

1.  <span data-ttu-id="ad251-106">Freigeben von nicht-NULL-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="ad251-106">Release non-null interfaces.</span></span>
2.  <span data-ttu-id="ad251-107">Rufen Sie die [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)-, [**cokreateinstanceex**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)-oder [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) -Funktion auf, um einen Zeiger auf das Dienst Lade Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ad251-107">Call the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex), or [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) function to obtain a pointer to the service loader object.</span></span>

    <span data-ttu-id="ad251-108">**CLSCTX \_ Die Deaktivierung von \_ AAA** kann in diesem-Befehl nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ad251-108">**CLSCTX\_DISABLE\_AAA** cannot be specified in this call.</span></span> <span data-ttu-id="ad251-109">Wenn [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufgerufen wird, kann das **eoac- \_ Deaktivieren von \_ AAA** nicht im *dwfunktionen* -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ad251-109">If [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is called, **EOAC\_DISABLE\_AAA** cannot be specified in the *dwCapabilities* parameter.</span></span>

3.  <span data-ttu-id="ad251-110">Zum Laden von VDS wird die [**ivdsserviceloader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ad251-110">Call the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method to load VDS.</span></span>

    <span data-ttu-id="ad251-111">Wenn **null** als erster Parameter übergeben wird, werden VDS auf dem lokalen Host geladen und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="ad251-111">Passing **NULL** as the first parameter loads and initializes VDS on the local host.</span></span>

4.  <span data-ttu-id="ad251-112">Aufrufen der [**ivdsservice:: waitforserviceready**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) -Methode, um auf den Abschluss der VDS-Initialisierung zu warten.</span><span class="sxs-lookup"><span data-stu-id="ad251-112">Call the [**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) method to wait for VDS initialization to complete.</span></span>

<span data-ttu-id="ad251-113">Im folgenden Codebeispiel wird der Dienst initialisiert, der einen Zeiger auf das Dienst Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ad251-113">The following code example initializes the service that returns a pointer to the service object.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ad251-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad251-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad251-115">Verwenden von VDS</span><span class="sxs-lookup"><span data-stu-id="ad251-115">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="ad251-116">**Ivdsservice:: waitforserviceready**</span><span class="sxs-lookup"><span data-stu-id="ad251-116">**IVdsService::WaitForServiceReady**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[<span data-ttu-id="ad251-117">**Ivdsserviceloader:: loadservice**</span><span class="sxs-lookup"><span data-stu-id="ad251-117">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="ad251-118">Setup und Dienst Objekte</span><span class="sxs-lookup"><span data-stu-id="ad251-118">Setup and Service Objects</span></span>](startup-and-service-objects.md)
</dt> </dl>

 

 
