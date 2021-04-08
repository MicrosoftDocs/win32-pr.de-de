---
description: Verwalten von asynchronen Vorgängen
ms.assetid: e5136e15-3ae1-4e0a-ae97-fcf16203b21d
title: Verwalten von asynchronen Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d220c5633f9ee044dbf9cdb6a63b563747620afd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960103"
---
# <a name="managing-asynchronous-operations"></a><span data-ttu-id="fc711-103">Verwalten von asynchronen Vorgängen</span><span class="sxs-lookup"><span data-stu-id="fc711-103">Managing Asynchronous Operations</span></span>

<span data-ttu-id="fc711-104">\[Ab Windows 8 und Windows Server 2012 wird der [Dienst für virtuelle](virtual-disk-service-portal.md) Datenträger von der Windows- [Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)abgelöst.\]</span><span class="sxs-lookup"><span data-stu-id="fc711-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="fc711-105">Das folgende Codebeispiel veranschaulicht die Funktionsweise eines Aufrufers mit einem Async-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fc711-105">The code example that follows demonstrates how a caller works with an async object.</span></span> <span data-ttu-id="fc711-106">Hier Ruft die **synchronouscreatelun-** Funktion mit den angegebenen Parametern die asynchrone [**ivdssubsystem:: samatelun-**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) Methode auf.</span><span class="sxs-lookup"><span data-stu-id="fc711-106">Here, the **SynchronousCreateLun** function calls the asynchronous [**IVdsSubSystem::CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) method using the given parameters.</span></span> <span data-ttu-id="fc711-107">Die-Funktion wartet auf das Async-Objekt, um den asynchronen Vorgang der Methode " **samatelun** " abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="fc711-107">The function will wait on the async object for the asynchronous **CreateLun** method call to finish.</span></span> <span data-ttu-id="fc711-108">Wenn die [**ivdsasync:: Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) -Methode zurückgibt, ruft **synchronouscreatelun** die [**ivdslun**](/windows/desktop/api/Vds/nn-vds-ivdslun) -Schnittstelle für die neu erstellte LUN ab und gibt Sie als out-Argument zurück.</span><span class="sxs-lookup"><span data-stu-id="fc711-108">When the [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) method returns, **SynchronousCreateLun** gets the [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) interface for the newly created LUN and returns it as an out argument.</span></span>


```C++
//
// Simple macro to release non-null interfaces.
//
#include <windows.h>
#include "vds.h"
#include <stdio.h>

#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

HRESULT SynchronousCreateLun(
    IVdsSubSystem *pSubsystem,
    VDS_LUN_TYPE  type,
    ULONGLONG     ullSize,
    VDS_OBJECT_ID *pDriveIdArray,
    LONG          lNumberOfDrives,
    LPWSTR        pwszUnmaskingList,
    VDS_HINTS     *pHints,
    IVdsLun       **ppLun)
{
    HRESULT hResult = S_OK;
    HRESULT hResult2 = S_OK;
    IVdsAsync *pAsync = NULL;
    VDS_ASYNC_OUTPUT AsyncOut;
    IUnknown* pUnknown = NULL;

    ZeroMemory( &AsyncOut, sizeof(VDS_ASYNC_OUTPUT));

    hResult = pSubsystem->CreateLun(
        type,
        ullSize,
        pDriveIdArray,
        lNumberOfDrives,
        pwszUnmaskingList,
        pHints,
        &pAsync);

    if (SUCCEEDED(hResult) && (!pAsync)) {
        hResult = E_UNEXPECTED; // Errant provider, returned S_OK 
                                // with a NULL pointer.
    }

    if (SUCCEEDED(hResult)) {
        // Wait until the Async is done.
        hResult2 = pAsync->Wait( &hResult, &AsyncOut);
        if (SUCCEEDED(hResult) && FAILED(hResult2)) {
            hResult = hResult2;
        }
    }

    if (SUCCEEDED(hResult) && (VDS_ASYNCOUT_CREATELUN != AsyncOut.type)) {
        hResult = E_UNEXPECTED; // Errant provider, returned S_OK  
                                // with an unexpected type.
    }

    if (SUCCEEDED(hResult)) {
        pUnknown = AsyncOut.cl.pLunUnk;
        if (!pUnknown) {
            hResult = E_UNEXPECTED; // Errant provider, returned 
                                    // S_OK with a NULL pointer.
        }
    }

    if (SUCCEEDED(hResult)) {
        hResult = pUnknown->QueryInterface(IID_IVdsLun, (void **)ppLun);
    }

    _SafeRelease(pAsync);
    _SafeRelease(pUnknown);

    return hResult;
}
```



## <a name="related-topics"></a><span data-ttu-id="fc711-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc711-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc711-110">Verwenden von VDS</span><span class="sxs-lookup"><span data-stu-id="fc711-110">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="fc711-111">Hilfsobjekte</span><span class="sxs-lookup"><span data-stu-id="fc711-111">Helper Objects</span></span>](helper-objects.md)
</dt> <dt>

[<span data-ttu-id="fc711-112">**Ivdssubsystem:: unatelun**</span><span class="sxs-lookup"><span data-stu-id="fc711-112">**IVdsSubSystem::CreateLun**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun)
</dt> <dt>

[<span data-ttu-id="fc711-113">**Ivdsasync:: Wait**</span><span class="sxs-lookup"><span data-stu-id="fc711-113">**IVdsAsync::Wait**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[<span data-ttu-id="fc711-114">**Ivdslun**</span><span class="sxs-lookup"><span data-stu-id="fc711-114">**IVdsLun**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> </dl>

 

 
