---
title: Multichannel-Audiowiedergabe in DirectShow
description: Multichannel-Audiowiedergabe in DirectShow
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Multichannel-Audiowiedergabe
- Windows Media-Format-SDK, Audiowiedergabe
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Multichannel-Audiowiedergabe
- ASF (Advanced Systems Format), Multichannel-Audiowiedergabe
- Advanced Systems Format (ASF), Audiowiedergabe
- ASF (Advanced Systems Format), Audiowiedergabe
- DirectShow, Multichannel-Audiowiedergabe
- DirectShow, Audiowiedergabe
- Multichannel-Audiodatei, Wiedergabe
- Audiowiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c6eec473c8bbbff81d35f4127d5d132d0b6cd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389946"
---
# <a name="multichannel-audio-playback-in-directshow"></a>Multichannel-Audiowiedergabe in DirectShow

Wenn Sie eine Multichannel-Windows Media Audio Datei in DirectShow wiedergeben möchten, müssen Sie die \_ Eigenschaft "hiresoutput" direkt auf den Decoder festlegen, nachdem Sie mit dem WM-ASF-Reader verbunden wurde. Es ist keine Konfiguration des Reader-Objekts erforderlich. Wenn Sie jedoch direkt mit dem DMO arbeiten möchten, benötigen Sie wmcodecinst. h aus dem [Beispiel Code für die Verwendung des Download Pakets für die Windows Media Audio-und Video Codec-Schnittstellen](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) .

**Hinweis** Diese Konfigurations Prozedur wird nur für Dateien unterstützt, die nicht durch digitale Rights Management geschützt sind.

Die grundlegenden Schritte zum Aktivieren der Multichannel-Ausgabe lauten wie folgt:

1.  Rufen Sie RenderFile auf, um das Filter Diagramm zu erstellen.
2.  Abrufen eines Zeigers auf den DMO-Wrapper Filter
3.  Trennen des DMO-Wrappers vom audiorenderer
4.  Legen Sie die \_ Eigenschaft "hiresoutput" für den Decoder fest.
5.  Verbinden Sie den DMO-Wrapper und den audiorenderer erneut.
6.  Führen Sie das Diagramm aus.

Diese Schritte werden in den folgenden Code Ausschnitten veranschaulicht. (Die gesamte Fehlerüberprüfung wurde aus Gründen der Einfachheit ausgelassen. Wenn Sie diesen Code in einer Anwendung verwenden, sollten Sie die richtigen Fehlerbehandlungsroutinen hinzufügen.)


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



Die Funktionen "getdmuwrapper" und "getpin" aus dem vorherigen Code Ausschnitt werden wie folgt implementiert:


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



 

 




