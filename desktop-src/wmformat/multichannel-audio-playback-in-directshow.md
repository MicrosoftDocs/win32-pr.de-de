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
# <a name="multichannel-audio-playback-in-directshow"></a><span data-ttu-id="d7368-116">Multichannel-Audiowiedergabe in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d7368-116">Multichannel Audio Playback in DirectShow</span></span>

<span data-ttu-id="d7368-117">Wenn Sie eine Multichannel-Windows Media Audio Datei in DirectShow wiedergeben möchten, müssen Sie die \_ Eigenschaft "hiresoutput" direkt auf den Decoder festlegen, nachdem Sie mit dem WM-ASF-Reader verbunden wurde.</span><span class="sxs-lookup"><span data-stu-id="d7368-117">To play back a multichannel Windows Media Audio file in DirectShow, you must set the "\_HIRESOUTPUT" property directly on the decoder after it has been connected to the WM ASF Reader.</span></span> <span data-ttu-id="d7368-118">Es ist keine Konfiguration des Reader-Objekts erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d7368-118">No configuration of the Reader Object is necessary.</span></span> <span data-ttu-id="d7368-119">Wenn Sie jedoch direkt mit dem DMO arbeiten möchten, benötigen Sie wmcodecinst. h aus dem [Beispiel Code für die Verwendung des Download Pakets für die Windows Media Audio-und Video Codec-Schnittstellen](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="d7368-119">However, to work with the DMO directly, you need wmcodecconst.h from the [Sample Code for Using the Windows Media Audio and Video Codec Interfaces](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) download package.</span></span>

<span data-ttu-id="d7368-120">**Hinweis** Diese Konfigurations Prozedur wird nur für Dateien unterstützt, die nicht durch digitale Rights Management geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="d7368-120">**Note** This configuration procedure is supported only for files that are not protected by Digital Rights Management.</span></span>

<span data-ttu-id="d7368-121">Die grundlegenden Schritte zum Aktivieren der Multichannel-Ausgabe lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d7368-121">The basic steps to enable multichannel output are as follows:</span></span>

1.  <span data-ttu-id="d7368-122">Rufen Sie RenderFile auf, um das Filter Diagramm zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d7368-122">Call RenderFile to create the filter graph.</span></span>
2.  <span data-ttu-id="d7368-123">Abrufen eines Zeigers auf den DMO-Wrapper Filter</span><span class="sxs-lookup"><span data-stu-id="d7368-123">Obtain a pointer to the DMO Wrapper filter</span></span>
3.  <span data-ttu-id="d7368-124">Trennen des DMO-Wrappers vom audiorenderer</span><span class="sxs-lookup"><span data-stu-id="d7368-124">Disconnect the DMO Wrapper from the Audio Renderer</span></span>
4.  <span data-ttu-id="d7368-125">Legen Sie die \_ Eigenschaft "hiresoutput" für den Decoder fest.</span><span class="sxs-lookup"><span data-stu-id="d7368-125">Set the "\_HIRESOUTPUT" property on the decoder.</span></span>
5.  <span data-ttu-id="d7368-126">Verbinden Sie den DMO-Wrapper und den audiorenderer erneut.</span><span class="sxs-lookup"><span data-stu-id="d7368-126">Reconnect the DMO Wrapper and the Audio Renderer.</span></span>
6.  <span data-ttu-id="d7368-127">Führen Sie das Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="d7368-127">Run the graph.</span></span>

<span data-ttu-id="d7368-128">Diese Schritte werden in den folgenden Code Ausschnitten veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d7368-128">The following code snippets demonstrate these steps.</span></span> <span data-ttu-id="d7368-129">(Die gesamte Fehlerüberprüfung wurde aus Gründen der Einfachheit ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="d7368-129">(All error checking has been omitted for the sake of simplicity.</span></span> <span data-ttu-id="d7368-130">Wenn Sie diesen Code in einer Anwendung verwenden, sollten Sie die richtigen Fehlerbehandlungsroutinen hinzufügen.)</span><span class="sxs-lookup"><span data-stu-id="d7368-130">You should add proper error handling routines if you use this code in an application.)</span></span>


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



<span data-ttu-id="d7368-131">Die Funktionen "getdmuwrapper" und "getpin" aus dem vorherigen Code Ausschnitt werden wie folgt implementiert:</span><span class="sxs-lookup"><span data-stu-id="d7368-131">The GetDMOWrapper and GetPin functions from the previous code snippet are implemented as follows:</span></span>


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



 

 




