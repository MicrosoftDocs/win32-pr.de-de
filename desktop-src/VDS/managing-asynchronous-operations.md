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
# <a name="managing-asynchronous-operations"></a>Verwalten von asynchronen Vorgängen

\[Ab Windows 8 und Windows Server 2012 wird der [Dienst für virtuelle](virtual-disk-service-portal.md) Datenträger von der Windows- [Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)abgelöst.\]

Das folgende Codebeispiel veranschaulicht die Funktionsweise eines Aufrufers mit einem Async-Objekt. Hier Ruft die **synchronouscreatelun-** Funktion mit den angegebenen Parametern die asynchrone [**ivdssubsystem:: samatelun-**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) Methode auf. Die-Funktion wartet auf das Async-Objekt, um den asynchronen Vorgang der Methode " **samatelun** " abzuschließen. Wenn die [**ivdsasync:: Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) -Methode zurückgibt, ruft **synchronouscreatelun** die [**ivdslun**](/windows/desktop/api/Vds/nn-vds-ivdslun) -Schnittstelle für die neu erstellte LUN ab und gibt Sie als out-Argument zurück.


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

[**Ivdssubsystem:: unatelun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun)
</dt> <dt>

[**Ivdsasync:: Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**Ivdslun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> </dl>

 

 
