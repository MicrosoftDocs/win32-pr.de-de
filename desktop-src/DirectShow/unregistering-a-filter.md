---
description: Aufheben der Registrierung eines Filters
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Aufheben der Registrierung eines Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e26f2d524ff501fcff1db645c9ccdf1a1c9c80c4056af1af206b996f801207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049680"
---
# <a name="unregistering-a-filter"></a>Aufheben der Registrierung eines Filters

Um die Registrierung eines Filters aufzuheben, implementieren Sie die **DllUnregisterServer-Funktion.** Rufen Sie in dieser Funktion die [**DirectShow-Funktion AMovieDllRegisterServer2**](amoviedllregisterserver2.md) mit dem Wert **FALSE** auf. Wenn Sie **IFilterMapper2::RegisterFilter** beim Registrieren des Filters aufgerufen haben, rufen Sie hier die [**IFilterMapper2::UnregisterFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) auf.

Das folgende Beispiel zeigt, wie Sie die Registrierung eines Filters aufheben:


```C++
STDAPI DllUnregisterServer()
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
        return hr;
 
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_SomeFilter);

    pFM2->Release();
    return hr;
}
```



 

 



