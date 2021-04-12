---
description: Anzeigen von World Standard-Teletext
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Anzeigen von World Standard-Teletext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b0885c08403de9578a8dee1eca6e000408ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344378"
---
# <a name="viewing-world-standard-teletext"></a>Anzeigen von World Standard-Teletext

> [!Note]  
> Diese Funktion wurde aus Windows Vista und höheren Betriebssystemen entfernt. Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.

 

Der Standard-Teletext (WST) ist im vertikalen Auslassungs Intervall (VBI) des analogen Fernsehsignals codiert. Das Filter Diagramm für die Vorschau von Teletext ähnelt dem Diagramm, das zum Anzeigen von Untertiteln verwendet wird. Dieses Diagramm wird im folgenden Diagramm veranschaulicht.

![WST-Vorschau Diagramm](images/vidcap10.png)

In diesem Diagramm werden die folgenden Filter für die WST-Anzeige verwendet:

-   [Tee/Sink-zu-Sink-Konverter](tee-sink-to-sink-converter.md). Akzeptiert die VBI-Informationen aus dem Erfassungs Filter und teilt Sie für jeden der Datendienste, die im Signal vorhanden sind, in separate Streams auf.
-   [WST-Codec](wst-codec-filter.md). Decodiert die Teletextdaten aus den VBI-Beispielen.
-   [WST-Decoder](wst-decoder-filter.md). Übersetzt Teletextdaten und zeichnet den Text auf Bitmaps. Der Downstream-Filter (in diesem Fall der Überlagerungs-Mixer) überlagert die Bitmaps auf dem Video.

Die **RenderStream** -Methode des Capture Graph-Generators unterstützt die WST-Filter nicht direkt, sodass Ihre Anwendung einige zusätzliche Aufgaben ausführen muss.

1.  Fügen Sie den Filter für den Overlay-Mixer dem Filter Diagramm hinzu. Der folgende Code verwendet die addfilterbyclsid-Funktion, die unter [Hinzufügen eines Filters nach CLSID beschrieben wird](add-a-filter-by-clsid.md). (Addfilterbyclsid ist keine DirectShow-API.)
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  Verbinden Sie die Vorschau-PIN mit dem Videorendererfilter über den Überlagerungs-Mixer. Sie können die **RenderStream** -Methode wie folgt verwenden:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  Fügen Sie dem Filter Diagramm den Filter Tee/Sink-to-Sink Converter hinzu. Der folgende Code verwendet die Funktion "-Funktion", die unter [Erstellen von Kernel-Mode filtern](creating-kernel-mode-filters.md)beschrieben wird. (Bei "kreatekernelfilter" handelt es sich nicht um eine DirectShow-API.)
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  Fügen Sie den WST-Codec-Filter dem Filter Diagramm hinzu:
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  Nennen Sie **RenderStream** , um die VBI-PIN des Erfassungs Filters mit dem "Tee/Sink-to-Sink Converter" und dem "Tee/Sink-to-Sink Converter" an den WST-Codec-Filter zu verbinden:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  **RenderStream** erneut aufgerufen, um den WST-Codec-Filter mit dem Überlagerungs-Mixer zu verbinden. Der WST-Decoderfilter wird automatisch in das Diagramm eingefügt.
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  Denken Sie daran, alle Filter Schnittstellen freizugeben.
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> Der WST-Decoderfilter unterstützt derzeit keine Verbindungen mit dem Filter für den Video Mischungs-Renderer (VMR). Daher müssen Sie den Legacy-Videorenderer-Filter verwenden, um Teletext anzuzeigen.

 

Wenn der Erfassungs Filter eine Video Port-VBI-PIN (PIN \_ CATEGPORY \_ Videoport \_ VBI) aufweist, verbinden Sie ihn mit dem [VBI-Oberflächen zuordnerfilter](vbi-surface-allocator.md) . Andernfalls wird das Diagramm nicht ordnungsgemäß ausgeführt. Im folgenden Codebeispiel wird die addfilterbyclsid-Funktion verwendet, die unter " [Hinzufügen eines Filters nach CLSID](add-a-filter-by-clsid.md)" und die Funktion "findpinbycategory" beschrieben wird. diese Funktion wird in verwenden [von PIN-Kategorien](working-with-pin-categories.md)beschrieben. (Keine der Funktionen ist eine DirectShow-API.)


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

 

 



