---
description: Fensterloser VMR-Modus
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Fensterloser VMR-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b137fbc1351f2bbe5ed38673b681e45558675d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344369"
---
# <a name="vmr-windowless-mode"></a>Fensterloser VMR-Modus

Der fensterlose Modus ist die bevorzugte Methode für Anwendungen zum renderingvideo in einem Anwendungsfenster. Im fensterlosen Modus lädt der Video Mischungs-Renderer seine Fenster-Manager-Komponente nicht und unterstützt daher nicht die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -oder [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstellen. Stattdessen stellt die Anwendung das Wiedergabe Fenster bereit und legt ein Ziel Rechteck im Client Bereich fest, damit das Video vom VMR gezeichnet werden kann. VMR verwendet ein DirectDraw-clipperobjekt, um sicherzustellen, dass das Video auf das Fenster der Anwendung zugeschnitten und nicht in anderen Fenstern angezeigt wird. Der VMR unterstützt das Fenster der Anwendung nicht oder installiert keine System-/prozesshooks.

Im fensterlosen Modus lautet die Sequenz von Ereignissen während der Verbindung und der Übergang in den Ausführungs Status wie folgt:

-   Der upstreamfilter schlägt einen Medientyp vor, den VMR entweder akzeptiert oder ablehnt.
-   Wenn der Medientyp akzeptiert wird, ruft VMR den "zuordcator-Presenter" auf, um eine DirectDraw-Oberfläche zu erhalten. Wenn die Oberfläche erfolgreich erstellt wurde, sind die Pins Connect und VMR bereit für den Übergang in den Ausführungs Status.
-   Wenn das Filter Diagramm ausgeführt wird, ruft der Decoder **GetBuffer** auf, um ein Medien Beispiel aus der Zuweisung zu erhalten. VMR fragt den Zuweiser-Presenter ab, um sicherzustellen, dass die Pixel Tiefe, die Rechteck Größe und andere Parameter auf der DirectDraw-Oberfläche mit dem eingehenden Video kompatibel sind. Wenn Sie kompatibel sind, gibt der VMR die DirectDraw-Oberfläche an den Decoder zurück. Nachdem der Decoder in die-Oberfläche decodiert wurde, überprüft die Kern Synchronisierungs Einheit von VMR die Zeitstempel. Diese Einheit blockiert den **Empfangs** Aufruf, bis die Präsentationszeit erreicht ist. An diesem Punkt ruft der VMR " **presentimage** " auf dem "zuordcator-Presenter" auf, der die Oberfläche auf der Grafikkarte darstellt.

Die folgende Abbildung zeigt VMR im fensterlosen Modus mit mehreren Eingabedaten strömen.

![VMR im fensterlosen Modus](images/vmr-windowless-mult-streams.png)

**Konfigurieren von VMR-7 für den fensterlosen Modus**

Um VMR-7 für den fensterlosen Modus zu konfigurieren, führen Sie die folgenden Schritte aus, bevor Sie eine der VMR-Eingabe Pins verbinden:

1.  Erstellen Sie den Filter, und fügen Sie ihn dem Diagramm hinzu.
2.  Wenden Sie die [**ivmrfilterconfig:: setrenderingmode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) -Methode mit dem Windows-Flag "vmrmode" an \_ .
3.  Optional können Sie den VMR für mehrere Eingabedaten Ströme konfigurieren, indem Sie [**ivmrfilterconfig:: setnumofstreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams)aufrufen. VMR erstellt eine Eingabe-PIN für jeden Stream. Verwenden Sie die [**ivmrmixercontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) -Schnittstelle, um die Z-Reihenfolge und andere Parameter für den Stream festzulegen. Weitere Informationen finden Sie unter [VMR mit mehreren Streams (Mischungs Modus)](vmr-with-multiple-streams--mixing-mode.md).

    Wenn Sie **setnumofstreams** nicht aufrufen, wird VMR-7 standardmäßig auf eine Eingabe-PIN festgelegt. Nachdem die Eingabe Pins verbunden sind, kann die Anzahl der Pins nicht mehr geändert werden.

4.  Aufrufen von [**ivmrwindowlesscontrol:: setvideoclippingwindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) zum Angeben des Fensters, in dem das gerenderte Video angezeigt wird.

Nachdem Sie diese Schritte abgeschlossen haben, können Sie die Eingabe Pins des VMR-Filters verbinden. Es gibt verschiedene Möglichkeiten, das Diagramm zu erstellen, z. b. das direkte Verbinden von Pins, die Verwendung von intelligenten Verbindungsmethoden wie [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)oder die Verwendung der [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode des Capture Graph-Generators. Weitere Informationen finden Sie unter [Allgemeine Graph-Building Techniken](general-graph-building-techniques.md).

Um die Position des Videos innerhalb des Anwendungsfensters festzulegen, können Sie die [**ivmrwindowlesscontrol:: setvideoposition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) -Methode aufrufen. Die [**ivmrwindowlesscontrol:: getnativevideosize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) -Methode gibt die systemeigene Videogröße zurück. Während der Wiedergabe sollte die Anwendung den VMR der folgenden Windows-Meldungen Benachrichtigen:

-   WM \_ Paint: nennen Sie [**ivmrwindowlesscontrol:: repaintvideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) , um das Bild neu zu zeichnen.
-   WM \_ displaychange: der Befehl [**ivmrwindowlesscontrol::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). VMR führt alle Aktionen aus, die erforderlich sind, um das Video mit der neuen Auflösung oder Farbtiefe anzuzeigen.
-   WM \_ size: berechnet die Position des Videos neu und ruft [**setvideoposition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) bei Bedarf erneut auf.

> [!Note]  
> MFC-Anwendungen müssen einen leeren "WM \_ erasebkgnd"-Nachrichten Handler definieren, oder der Videoanzeige Bereich wird nicht ordnungsgemäß neu gezeichnet.

 

**Konfigurieren von VMR-9 für den fensterlosen Modus**

Verwenden Sie zum Konfigurieren von VMR-9 für den fensterlosen Modus die für VMR-7 beschriebenen Schritte für den fensterlosen Modus, aber verwenden Sie die Schnittstellen [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) und [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) . Der einzige bedeutende Unterschied besteht darin, dass VMR-9 standardmäßig vier Eingabe Pins erstellt, anstelle einer Eingabe-PIN. Daher müssen Sie **setnumofstreams** nur aufrufen, wenn Sie mehr als vier Videostreams mischen.

**Beispiel Code**

Der folgende Code zeigt, wie ein VMR-7-Filter erstellt, dem DirectShow-Filter Diagramm hinzugefügt und anschließend der VMR in den fensterlosen Modus versetzt wird. Verwenden Sie für VMR-9 CLSID \_ VideoMixingRenderer9 in **cokreateinstance** und die entsprechenden VMR-9-Schnittstellen.


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

 

 



