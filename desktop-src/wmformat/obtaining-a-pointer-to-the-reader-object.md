---
title: Abrufen eines Zeigers auf das Readerobjekt (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über das Abrufen eines Zeigers auf das Reader-Objekt des Windows Media Format SDK mithilfe der IWMReaderAdvanced2-Schnittstelle.
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows Medienformat-SDK, DirectShow
- Windows Medienformat-SDK, Readerobjekte
- Windows Medienformat-SDK, IWMReaderAdvanced2-Schnittstelle
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
ms.openlocfilehash: 5e4b2829e56d08825234dcefdc4fb1012f48c894419e7c328f10afeb76cb6c4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808050"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a>Abrufen eines Zeigers auf das Readerobjekt (Windows Media Format 11 SDK)

In bestimmten Fällen, z. B. wenn Sie bestimmen, welche Dateneinheitserweiterungen für einen bestimmten Stream festgelegt sind, müssen Sie möglicherweise direkt auf das [Reader-Objekt](reader-object.md) des Windows Media Format SDK zugreifen. Die folgende Funktion zeigt, wie Sie die [**IWMReaderAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) für das Reader-Objekt selbst abrufen:


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



 

 




