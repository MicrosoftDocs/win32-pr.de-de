---
description: Viewing World Standard Teletext
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Viewing World Standard Teletext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2129538d91a7ac48fea26fd5f1987473896760c164fb3e2b1d4a2b1d142a1f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078545"
---
# <a name="viewing-world-standard-teletext"></a>Viewing World Standard Teletext

> [!Note]  
> Diese Funktionalität wurde aus den Betriebssystemen Windows Vista und höher entfernt. Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.

 

World Standard Teletext (WST) wird im vertikalen Leerungsintervall (Vertical Blanking Interval, VBI) des analogen Fernsehsignals codiert. Das Filterdiagramm für die Vorschau von Teletext ähnelt dem Diagramm, das zum Anzeigen von Untertiteln verwendet wird. Das folgende Diagramm veranschaulicht dieses Diagramm.

![wst preview graph](images/vidcap10.png)

In diesem Diagramm werden die folgenden Filter für die WST-Anzeige verwendet:

-   [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md). Akzeptiert die VBI-Informationen aus dem Erfassungsfilter und teilt sie für jeden datendienst, der im Signal vorhanden ist, in separate Datenströme auf.
-   [WST-Codec](wst-codec-filter.md). Decodiert die Teletext-Daten aus den VBI-Beispielen.
-   [WST-Decoder](wst-decoder-filter.md). Übersetzt Teletextdaten und zeichnet den Text auf Bitmaps. Der Downstreamfilter (in diesem Fall der Overlay-Mixer) überlagert die Bitmaps auf dem Video.

Die RenderStream Graph Methode von **Capture** Graph Builder unterstützt die WST-Filter nicht direkt, sodass Ihre Anwendung zusätzliche Arbeit leistet.

1.  Fügen Sie dem Filterdiagramm Mixer Overlay-Filter hinzu. Im folgenden Code wird die AddFilterByCLSID-Funktion verwendet, die unter [Hinzufügen eines Filters nach CLSID beschrieben wird.](add-a-filter-by-clsid.md) (AddFilterByCLSID ist keine DirectShow-API.)
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  Verbinden sie den Vorschaupin an den Videorendererfilter über das Overlay-Mixer. Sie können die **RenderStream-Methode** wie folgt verwenden:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  Fügen Sie dem Filterdiagramm den Filter Tee/Sink-to-Sink Converter hinzu. Im folgenden Code wird die CreateKernelFilter-Funktion verwendet, die unter Creating Kernel-Mode Filters (Erstellen Kernel-Mode [Filter) beschrieben wird.](creating-kernel-mode-filters.md) (CreateKernelFilter ist keine DirectShow-API.)
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  Fügen Sie dem Filterdiagramm den WST-Codec-Filter hinzu:
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  Rufen **Sie RenderStream** auf, um den VBI-Pin des Erfassungsfilters mit dem Tee-/Sink-zu-Sink-Konverter und den Tee/Sink-to-Sink-Konverter mit dem WST-Codec-Filter zu verbinden:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  Rufen **Sie RenderStream erneut** auf, um den WST-Codec-Filter mit dem Overlay-Mixer. Der WST-Decoderfilter wird automatisch in das Diagramm ein gebracht.
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  Denken Sie daran, alle Filterschnittstellen frei zu lassen.
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> Derzeit unterstützt der WST-Decoderfilter keine Verbindungen mit dem VmR-Filter (Video Mixing Renderer). Daher müssen Sie den älteren Videorendererfilter verwenden, um Teletext anzeigen zu können.

 

Wenn der Erfassungsfilter über einen Videoport-VBI-Pin (PIN CATEGPORY VIDEOPORT VBI) verfügt, verbinden Sie ihn mit dem \_ \_ \_ [VBI Surface Allocator-Filter.](vbi-surface-allocator.md) Andernfalls wird das Diagramm nicht ordnungsgemäß ausgeführt. Im folgenden Codebeispiel werden die AddFilterByCLSID-Funktion, die unter Hinzufügen eines Filters [nach CLSID](add-a-filter-by-clsid.md)beschrieben wird, und die FindPinByCategory-Funktion verwendet, die unter Arbeiten mit Pinkategorien [beschrieben wird.](working-with-pin-categories.md) (Keine der Funktionen ist eine DirectShow-API.)


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Untertitel und Teletext](closed-captions-and-teletext.md)
</dt> </dl>

 

 



