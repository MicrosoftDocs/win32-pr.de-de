---
title: Multichannel-Audiowiedergabe in DirectShow
description: Multichannel-Audiowiedergabe in DirectShow
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- Windows Medienformat-SDK, DirectShow
- Windows Medienformat-SDK, Multichannel-Audiowiedergabe
- Windows Medienformat-SDK, Audiowiedergabe
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Multichannel-Audiowiedergabe
- ASF (Advanced Systems Format), Multichannel-Audiowiedergabe
- Advanced Systems Format (ASF), Audiowiedergabe
- ASF (Advanced Systems Format), Audiowiedergabe
- DirectShow,Multichannel-Audiowiedergabe
- DirectShow,Audiowiedergabe
- Multichannelaudio, Wiedergabe
- Audiowiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99734ddf32be6e0340e26fafef0f22f1127ec3652cc0db0a9d2e94ce2f694b96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808160"
---
# <a name="multichannel-audio-playback-in-directshow"></a>Multichannel-Audiowiedergabe in DirectShow

Um eine Multichannel- Windows Media Audio-Datei in DirectShow wieder geben zu können, müssen Sie die Eigenschaft "HIRESOUTPUT" direkt auf dem Decoder festlegen, nachdem sie mit dem \_ WM ASF-Reader verbunden wurde. Es ist keine Konfiguration des Readerobjekts erforderlich. Um jedoch direkt mit dem DMO arbeiten zu können, benötigen Sie wmcodecconst.h aus dem Beispielcode für die Verwendung des Downloadpakets [Windows Media Audio and Video Codec Interfaces.](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en)

**Hinweis:** Dieses Konfigurationsverfahren wird nur für Dateien unterstützt, die nicht durch Digital Rights Management.

Die grundlegenden Schritte zum Aktivieren der Multichannelausgabe lauten wie folgt:

1.  Rufen Sie RenderFile auf, um das Filterdiagramm zu erstellen.
2.  Abrufen eines Zeigers auf den DMO Wrapperfilter
3.  Trennen des DMO Wrappers vom Audiorenderer
4.  Legen Sie die \_ HIRESOUTPUT-Eigenschaft für den Decoder fest.
5.  Verbinden Sie den DMO Wrapper und den Audiorenderer erneut.
6.  Führen Sie das Diagramm aus.

Die folgenden Codeausschnitte veranschaulichen diese Schritte. (Der Einfachheit halber wurden alle Fehlerüberprüfungen ausgelassen. Sie sollten ordnungsgemäße Fehlerbehandlungsroutinen hinzufügen, wenn Sie diesen Code in einer Anwendung verwenden.)


```C++
    ...
    //ENABLE MULTICHANNEL OUTPUT
    //Render the file
    hr = m_pGraphBuilder->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    hr = GetDMOWrapper(pGB, &m_pDMOBaseFilter, &m_pWrapper); 

    //Disconnect the DMO Wrapper from the Audio Renderer
    CComPtr<IPin> pDMOOut;
    CComPtr<IPin> pRendererIn;
    hr = GetPin(m_pDMOBaseFilter, PINDIR_OUTPUT, &pDMOOut);
    hr = pDMOOut->ConnectedTo(&pRendererIn);
    hr = pDMOOut->Disconnect();
    hr = pRendererIn->Disconnect();

    //Set the property on the DMO
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;
    CComQIPtr<IMediaObject, &IID_IMediaObject> pMediaObject(m_pWrapper);
    CComQIPtr<IPropertyBag, &IID_IPropertyBag> pPropertyBag(pMediaObject);
    hr = pPropertyBag->Write(g_wszWMACHiResOutput, &varg);

    // Reconnect the DMO Wrapper and the Audio Renderer
    hr = pGB->Connect(pDMOOut, pRendererIn);
    //END MULTICHANNEL (now the graph can be run)
...

```



Die GetDMOWrapper- und GetPin-Funktionen aus dem vorherigen Codeausschnitt werden wie folgt implementiert:


```C++
// In this example, the IBaseFilter and IDMOWrapperFilter interfaces are
// declared  at global scope
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** m_pDMOBaseFilter, IDMOWrapperFilter** m_pWrapper) 
{
    CComPtr<IEnumFilters> pEnum;
    CComPtr<IBaseFilter> pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        // If we find the IDMOWrapperFilter interface, that means we 
        // have the DMO Wrapper filter. Store both interfaces for future use.
        CComPtr<IDMOWrapperFilter> pWrapper;
        hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
        if (SUCCEEDED(hr))
        {
            *m_pWrapper = pWrapper.Detach();
            *m_pDMOBaseFilter = pFilter.Detach();
            return S_OK;
        }

        pFilter.Release();
    }

    return E_FAIL;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    CComPtr<IEnumPins>  pEnum;
    CComPtr<IPin>       pPin;

         HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        pPin->QueryDirection(&PinDirThis);
        if (PinDir == PinDirThis)
        {
            *ppPin = pPin.Detach();
            return S_OK;
        }
        pPin.Release();
    }
    
    return E_FAIL;
}
```



 

 




