---
description: Verwalten von asynchronen Vorgängen
ms.assetid: e5136e15-3ae1-4e0a-ae97-fcf16203b21d
title: Verwalten von asynchronen Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537a52a41e73bae7035789176bb65b125c105f691bf654ed3c0ded4e6a73f70d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999449"
---
# <a name="managing-asynchronous-operations"></a>Verwalten von asynchronen Vorgängen

\[Ab Windows 8 und Windows Server 2012 wird der [Dienst](virtual-disk-service-portal.md) für virtuelle Datenträger durch den virtuellen [Datenträgerdienst Windows Storage Verwaltungs-API.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Im folgenden Codebeispiel wird veranschaulicht, wie ein Aufrufer mit einem asynchronen Objekt arbeitet. Hier ruft die **SynchronousCreateLun-Funktion** die asynchrone [**IVdsSubSystem::CreateLun-Methode**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) unter Verwendung der angegebenen Parameter auf. Die Funktion wartet auf das asynchrone Objekt, bis der **asynchrone CreateLun-Methodenaufruf** abgeschlossen ist. Wenn die [**IVdsAsync::Wait-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) zurückgegeben wird, ruft **SynchronousCreateLun** die [**IVdsLun-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdslun) für die neu erstellte LUN ab und gibt sie als out-Argument zurück.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VDS](using-vds.md)
</dt> <dt>

[Hilfsobjekte](helper-objects.md)
</dt> <dt>

[**IVdsSubSystem::CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun)
</dt> <dt>

[**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> </dl>

 

 
