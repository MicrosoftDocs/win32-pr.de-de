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
# <a name="unregistering-a-filter"></a><span data-ttu-id="dd4da-103">Aufheben der Registrierung eines Filters</span><span class="sxs-lookup"><span data-stu-id="dd4da-103">Unregistering a Filter</span></span>

<span data-ttu-id="dd4da-104">Um die Registrierung eines Filters aufzuheben, implementieren Sie die **DllUnregisterServer** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="dd4da-104">To unregister a filter, implement the **DllUnregisterServer** function.</span></span> <span data-ttu-id="dd4da-105">In dieser Funktion wird die DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) -Funktion mit dem Wert **false** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dd4da-105">Within this function, call the DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function with a value of **FALSE**.</span></span> <span data-ttu-id="dd4da-106">Wenn Sie **IFilterMapper2:: registerfilter** beim Registrieren des Filters aufgerufen haben, müssen Sie hier die [**IFilterMapper2:: unregisterfilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dd4da-106">If you called **IFilterMapper2::RegisterFilter** when you registered the filter, call the [**IFilterMapper2::UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) method here.</span></span>

<span data-ttu-id="dd4da-107">Im folgenden Beispiel wird gezeigt, wie die Registrierung eines Filters aufgehoben wird:</span><span class="sxs-lookup"><span data-stu-id="dd4da-107">The following example shows how to unregister a filter:</span></span>


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



 

 



