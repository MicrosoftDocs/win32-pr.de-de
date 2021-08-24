---
description: Multichannel-WMA-Audiowiedergabe in DirectShow
ms.assetid: 99c69290-545a-4368-8f51-74e547c9466d
title: Multichannel-WMA-Audiowiedergabe in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e7f7841677a7b7bc4087b2644632bbf6ec9cd48bccc15274506c6c57f96f89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830980"
---
# <a name="multichannel-wma-audio-playback-in-directshow"></a>Multichannel-WMA-Audiowiedergabe in DirectShow

Um eine Multichannel-Windows-Medienaudiodatei in DirectShow wieder geben zu können, müssen Sie die **\_ MFPKEY W \_ TASTENKnaufEINSTELLUNGENOUTPUT-Eigenschaft** direkt im Decoder festlegen, nachdem sie mit dem WM ASF-Reader verbunden wurde. Diese Eigenschaft wird in der Headerdatei wmcodecdsp.h definiert, die im Windows SDK verfügbar ist.

> [!Note]  
> Dieses Konfigurationsverfahren wird nur für Dateien unterstützt, die nicht durch Digital Rights Management.

 

Die grundlegenden Schritte zum Aktivieren der Multichannelausgabe lauten wie folgt:

1.  Rufen Sie **RenderFile auf,** um das Filterdiagramm zu erstellen.
2.  Abrufen eines Zeigers auf den DMO Wrapperfilter.
3.  Trennen Sie DMO-Wrapper vom Audiorenderer.
4.  Verwenden Sie **die IPropertyBag-Schnittstelle,** um die **Eigenschaft \_ MFPKEY WKYC \_ HIRESOUTPUT** für den Decoder fest. Der Eigenschaftenname wird durch die globale Konstante **g \_ wszWMACHiResOutput definiert.**
5.  Verbinden Sie den DMO Wrapper und den Audiorenderer erneut.
6.  Führen Sie das Diagramm aus.

Die folgenden Codeausschnitte veranschaulichen diese Schritte. In diesem Code wird davon ausgegangen, dass die Quelldatei einen Audiostream und keinen Videostream enthält. Der Videocodec DMO unterstützt nicht die **Eigenschaft MFPKEY \_ WKYC \_ HIRESOUTPUT.**


```C++
HRESULT BuildGraph(IGraphBuilder *pGraph, const WCHAR *wFileName)
{
    HRESULT hr = S_OK;
    IBaseFilter       *pDmoWrapper = NULL;
    IPin              *pDmoOut = NULL;
    IPin              *pRendererIn = NULL;
    IPropertyBag      *pPropBag = NULL;

    hr = pGraph->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    if (SUCCEEDED(hr))
    {
        hr = GetDMOWrapper(pGraph, &pDmoWrapper); 
    }

    //Disconnect the DMO Wrapper from the Audio Renderer.
    if (SUCCEEDED(hr))
    {
        hr = GetPin(pDmoWrapper, PINDIR_OUTPUT, &pDmoOut);
    }
    if (SUCCEEDED(hr))
    {
        hr = DisconnectPin(pGraph, pDmoOut, &pRendererIn);
    }

    //Set the property on the DMO.
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;

    if (SUCCEEDED(hr))
    {
        hr = pDmoWrapper->QueryInterface(IID_IPropertyBag, (void**)&pPropBag);
    }
    if (SUCCEEDED(hr))
    {
        hr = pPropBag->Write(g_wszWMACHiResOutput, &varg);
    }

    // Reconnect the DMO Wrapper and the Audio Renderer
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Connect(pDmoOut, pRendererIn);
    }

    SAFE_RELEASE(pDmoWrapper);
    SAFE_RELEASE(pDmoOut);
    SAFE_RELEASE(pRendererIn);
    SAFE_RELEASE(pPropBag);
    return hr;
}
```



Die Hilfsfunktionen aus dem vorherigen Codeausschnitt werden wie folgt implementiert:


```C++
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** ppFilter) 
{
    BOOL bFound = FALSE;

    IEnumFilters *pEnum = NULL;
    IBaseFilter *pFilter = NULL;
    IDMOWrapperFilter *pWrapper = NULL;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (SUCCEEDED(hr))
    {
        while(pEnum->Next(1, &pFilter, NULL) == S_OK)
        {
            // If we find the IDMOWrapperFilter interface, that means we 
            // have the DMO Wrapper filter. 
            hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
            if (SUCCEEDED(hr))
            {
                bFound = TRUE;
                break;
            }
            SAFE_RELEASE(pFilter);
        }
    }

    if (bFound)
    {
        *ppFilter = pFilter;
        (*ppFilter)->AddRef();
    }
    else
    {
        hr = E_FAIL;
    }

    SAFE_RELEASE(pEnum);
    SAFE_RELEASE(pFilter);
    SAFE_RELEASE(pWrapper);
    return hr;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    BOOL bFound = FALSE;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;

    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (SUCCEEDED(hr))
    {
        while(pEnum->Next(1, &pPin, 0) == S_OK)
        {
            PIN_DIRECTION PinDirThis;
            hr = pPin->QueryDirection(&PinDirThis);
            if (FAILED(hr))
            {
                break;
            }
            if (PinDir == PinDirThis)
            {
                bFound = TRUE;
                break;
            }
            SAFE_RELEASE(pPin);
        }
    }

    if (bFound)
    {
        *ppPin = pPin;
        (*ppPin)->AddRef();
    }
    else
    {
        hr = E_FAIL;
    }

    SAFE_RELEASE(pPin);
    SAFE_RELEASE(pEnum);
    return hr;
}

HRESULT DisconnectPin(IGraphBuilder *pGraph, IPin *pPin, IPin **ppConnected)
{
    IPin *pConnected = NULL;

    HRESULT hr = pPin->ConnectedTo(&pConnected);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Disconnect(pPin);
    }
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Disconnect(pConnected);
    }
    if (SUCCEEDED(hr))
    {
        *ppConnected = pConnected;
        (*ppConnected)->AddRef();
    }

    SAFE_RELEASE(pConnected);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



