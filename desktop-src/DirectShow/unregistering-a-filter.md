---
description: Aufheben der Registrierung eines Filters
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Aufheben der Registrierung eines Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d161b7d1f169b84ba43ac734bf01708a37eb700a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866464"
---
# <a name="unregistering-a-filter"></a>Aufheben der Registrierung eines Filters

Um die Registrierung eines Filters aufzuheben, implementieren Sie die **DllUnregisterServer** -Funktion. In dieser Funktion wird die DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) -Funktion mit dem Wert **false** aufgerufen. Wenn Sie **IFilterMapper2:: registerfilter** beim Registrieren des Filters aufgerufen haben, müssen Sie hier die [**IFilterMapper2:: unregisterfilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) -Methode aufrufen.

Im folgenden Beispiel wird gezeigt, wie die Registrierung eines Filters aufgehoben wird:


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



 

 



