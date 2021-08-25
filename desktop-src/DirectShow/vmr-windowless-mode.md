---
description: VMR-Modus ohne Fenster
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: VMR-Modus ohne Fenster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193f672e0fc1e3dced4bdff16da0e85123079eb94f2ac3c5fdb302b67c9432b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830584"
---
# <a name="vmr-windowless-mode"></a>VMR-Modus ohne Fenster

Der Fensterlose Modus ist die bevorzugte Methode für Anwendungen, um Videos in einem Anwendungsfenster zu rendern. Im fensterlosen Modus lädt der VideoMischungsrenderer seine Fenster-Manager-Komponente nicht und unterstützt daher die [**Schnittstellen IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) oder [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) nicht. Stattdessen stellt die Anwendung das Wiedergabefenster bereit und legt ein Zielrechteck im Clientbereich fest, damit die VMR das Video zeichnen kann. Die VMR verwendet ein DirectDraw-Clipper-Objekt, um sicherzustellen, dass das Video im Fenster der Anwendung abgeschnitten und nicht in anderen Fenstern angezeigt wird. Die VMR untergliedert das Fenster der Anwendung nicht und installiert keine System-/Prozesshooks.

Im fensterlosen Modus sieht die Abfolge der Ereignisse während der Verbindung und des Übergangs in den Ausführungszustand wie folgt aus:

-   Der Upstreamfilter schlägt einen Medientyp vor, den die VMR entweder akzeptiert oder ablehnt.
-   Wenn der Medientyp akzeptiert wird, ruft die VMR den Allocator-Presenter auf, um eine DirectDraw-Oberfläche zu erhalten. Wenn die Oberfläche erfolgreich erstellt wurde, stellen die Pins eine Verbindung her, und die VMR kann in den Ausführungszustand übergehen.
-   Wenn das Filterdiagramm ausgeführt wird, ruft der Decoder **GetBuffer** auf, um ein Medienbeispiel aus der Zuweisung abzurufen. Die VMR fragt den Allocator-Presenter ab, um sicherzustellen, dass die Pixeltiefe, rechteckige Größe und andere Parameter auf der DirectDraw-Oberfläche mit dem eingehenden Video kompatibel sind. Wenn sie kompatibel sind, gibt die VMR die DirectDraw-Oberfläche an den Decoder zurück. Nachdem der Decoder in die Oberfläche decodiert wurde, überprüft die Kernsynchronisierungseinheit der VMR die Zeitstempel. Diese Einheit  blockiert den Empfangsaufruf, bis die Präsentationszeit eingeht. An diesem Punkt ruft die VMR **PresentImage** auf dem Allocator-Presenter auf, wodurch die Oberfläche der Grafikkarte dargestellt wird.

Die folgende Abbildung zeigt die VMR im fensterlosen Modus mit mehreren Eingabestreams.

![vmr im fensterlosen Modus](images/vmr-windowless-mult-streams.png)

**Konfigurieren von VMR-7 für den fensterlosen Modus**

Führen Sie zum Konfigurieren von VMR-7 für den fensterlosen Modus alle folgenden Schritte aus, bevor Sie eine Der Eingabepins der VMR verbinden:

1.  Erstellen Sie den Filter, und fügen Sie ihn dem Diagramm hinzu.
2.  Rufen Sie die [**IVMRFilterConfig::SetRenderingMode-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) mit dem \_ VMRMode-Flag "Windowless" auf.
3.  Konfigurieren Sie optional die VMR für mehrere Eingabestreams, indem Sie [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams)aufrufen. Die VMR erstellt einen Eingabepin für jeden Stream. Verwenden Sie die [**IVMRMixerControl-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) um die Z-Reihenfolge und andere Parameter für den Stream festzulegen. Weitere Informationen finden Sie unter [VMR with Multiple Streams (Mixing Mode) (VMR mit mehreren Streams (Gemischter Modus)).](vmr-with-multiple-streams--mixing-mode.md)

    Wenn Sie **SetNumberOfStreams** nicht aufrufen, wird für VMR-7 standardmäßig ein Eingabepin verwendet. Nachdem die Eingabepins verbunden wurden, kann die Anzahl der Pins nicht mehr geändert werden.

4.  Rufen Sie [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) auf, um das Fenster anzugeben, in dem das gerenderte Video angezeigt wird.

Nach Abschluss dieser Schritte können Sie die Eingabepins des VMR-Filters verbinden. Es gibt verschiedene Möglichkeiten, den Graphen zu erstellen, z. B. das direkte Verbinden von Pins, die Verwendung von Intelligent Verbinden Methoden wie [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)oder die Verwendung der [**ICaptureGraphBuilder2::RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) von Capture Graph Builder. Weitere Informationen finden Sie unter [Allgemeine Graph-Building Techniken.](general-graph-building-techniques.md)

Um die Position des Videos im Anwendungsfenster festzulegen, rufen Sie die [**IVMRWindowlessControl::SetVideoPosition-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) auf. Die [**IVMRWindowlessControl::GetNativeVideoSize-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) gibt die native Videogröße zurück. Während der Wiedergabe sollte die Anwendung die VMR über die folgenden Windows Benachrichtigen:

-   WM \_ PAINT: Rufen Sie [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) auf, um das Bild neu zu zeichnen.
-   WM \_ DISPLAYCHANGE: Rufen Sie [**IVMRWindowlessControl::D isplayModeChanged auf.**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged) Die VMR führt alle Aktionen aus, die erforderlich sind, um das Video in der neuen Auflösung oder Farbtiefe anzuzeigen.
-   \_WM-GRÖßE: Berechnen Sie die Position des Videos neu, und rufen [**Sie SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) bei Bedarf erneut auf.

> [!Note]  
> MFC-Anwendungen müssen einen leeren WM \_ ERASEBKGND-Meldungshandler definieren, andernfalls wird der Videoanzeigebereich nicht ordnungsgemäß neu maliert.

 

**Konfigurieren von VMR-9 für den fensterlosen Modus**

Um VMR-9 für den fensterlosen Modus zu konfigurieren, verwenden Sie die für VMR-7 für den Fensterlosen Modus beschriebenen Schritte, verwenden Sie jedoch die Schnittstellen [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) und [**IVMRWindowlessControl9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) Der einzige wesentliche Unterschied besteht darin, dass VMR-9 standardmäßig vier Eingabepins anstelle eines Eingabepins erstellt. Daher müssen Sie **SetNumberOfStreams** nur aufrufen, wenn Sie mehr als vier Videostreams kombinieren.

**Beispielcode**

Der folgende Code zeigt, wie Sie einen VMR-7-Filter erstellen, ihn dem DirectShow-Filterdiagramm hinzufügen und die VMR dann in den fensterlosen Modus versetzen. Verwenden Sie für VMR-9 CLSID \_ VideoMixingRenderer9 in **CoCreateInstance** und die entsprechenden VMR-9-Schnittstellen.


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des fensterlosen Modus](using-windowless-mode.md)
</dt> </dl>

 

 



