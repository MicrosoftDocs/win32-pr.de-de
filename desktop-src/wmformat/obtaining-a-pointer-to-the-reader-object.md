---
title: Abrufen eines Zeigers auf das Readerobjekt (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über das Abrufen eines Zeigers auf das Readerobjekt des Windows Media Format SDK mithilfe der IWMReaderAdvanced2-Schnittstelle.
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, Readerobjekte
- Windows Media Format SDK,IWMReaderAdvanced2-Schnittstelle
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Readerobjekte
- ASF (Advanced Systems Format), Readerobjekte
- Advanced Systems Format (ASF), IWMReaderAdvanced2-Schnittstelle
- ASF (Advanced Systems Format), IWMReaderAdvanced2-Schnittstelle
- DirectShow,Reader-Objekte
- DirectShow, Zeiger auf Readerobjekte
- DirectShow,IWMReaderAdvanced2-Schnittstelle
- Readerobjekte,Abrufen von Zeigern
- streams,Reader Objects
- Streams, Zeiger auf Readerobjekte
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd31bd868365b87b38eefd0c0c81e8beafef51c
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989135"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a><span data-ttu-id="5ec5c-119">Abrufen eines Zeigers auf das Readerobjekt (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="5ec5c-119">Obtaining a Pointer to the Reader Object (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="5ec5c-120">In bestimmten Fällen, z. B. wenn Sie bestimmen, welche Dateneinheitserweiterungen für einen bestimmten Stream festgelegt sind, müssen Sie möglicherweise direkt auf das [Reader-Objekt](reader-object.md) des Windows Media Format SDK zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5ec5c-120">In certain cases, for example when determining which data unit extensions are set on a given stream, you may need to access the [Reader Object](reader-object.md) of the Windows Media Format SDK directly.</span></span> <span data-ttu-id="5ec5c-121">Die folgende Funktion zeigt, wie Sie die [**IWMReaderAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) für das Reader-Objekt selbst abrufen:</span><span class="sxs-lookup"><span data-stu-id="5ec5c-121">The following function shows how to obtain the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface on the Reader Object itself:</span></span>


```C++
HRESULT GetReaderAdvanced (IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
  // We use CComPtr's to avoid headaches at cleanup time
  CComPtr<IEnumFilters> pEnum;
  CComPtr<IBaseFilter> pFilter;
  ULONG cFetched;

  HRESULT hr = pGraph->EnumFilters(&pEnum);
  if (FAILED(hr)) 
  {
    return hr;
  }

  while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
  {
    IWMHeaderInfo *pHI = NULL;
    // Only the WM ASF Reader will have interface. This filter should be
    // the first one returned in this loop.
    hr = pFilter->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHI);
    if (SUCCEEDED(hr))
    {
      // We use the IWMDRMReader interface only as a way to get
      // a pointer to the Reader Object.
      CComPtr<IWMDRMReader> pWMDRMReader;
      CComQIPtr<IServiceProvider, &IID_IServiceProvider> pSP;

      hr = pHI->QueryInterface(__uuidof(IServiceProvider), (void**)&pSP);
      if (!pSP)
      {
        return E_NOINTERFACE;
      }
      
      hr = pSP->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader);
      if (FAILED(hr))
      {
        return hr;
      }

      CComQIPtr<IWMReaderAdvanced2, &IID_IWMReaderAdvanced2> pRA2(pWMDRMReader);
      if (pRA2)
      {
        *pReaderAdvanced2 = pRA2.Detach();
        return S_OK;
      }

    }
    pFilter.Release();
  }
  
  //if we get here, we didn't find the WM ASF Reader
  return E_FAIL;
}
```



 

 




