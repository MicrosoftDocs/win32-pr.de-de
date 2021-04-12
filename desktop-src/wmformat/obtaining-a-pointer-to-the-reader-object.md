---
title: Abrufen eines Zeigers auf das Reader-Objekt (Windows Media Format 11 SDK)
description: Abrufen eines Zeigers auf das Reader-Objekt
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Reader-Objekte
- Windows Media-Format-SDK, IWMReaderAdvanced2-Schnittstelle
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Reader-Objekte
- ASF (Advanced Systems Format), Reader-Objekte
- Advanced Systems Format (ASF), IWMReaderAdvanced2-Schnittstelle
- ASF (Advanced Systems Format), IWMReaderAdvanced2-Schnittstelle
- DirectShow, Reader-Objekte
- DirectShow, Zeiger auf Reader-Objekte
- DirectShow, IWMReaderAdvanced2-Schnittstelle
- Reader-Objekte, Abrufen von Zeigern
- Streams, Reader-Objekte
- Streams, Zeiger auf Reader-Objekte
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e0bb6611ba1d4e3c41fb2c00a68dd9c898505f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340107"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a>Abrufen eines Zeigers auf das Reader-Objekt (Windows Media Format 11 SDK)

In bestimmten Fällen, z. b. bei der Ermittlung, welche Dateneinheiten Erweiterungen für einen bestimmten Stream festgelegt werden, müssen Sie möglicherweise direkt auf das [Reader-Objekt](reader-object.md) des Windows Media SDK-SDKs zugreifen. Die folgende Funktion zeigt, wie Sie die [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) -Schnittstelle für das Reader-Objekt selbst abrufen:


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



 

 




