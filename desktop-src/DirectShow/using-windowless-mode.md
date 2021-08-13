---
description: Verwenden des fensterlosen Modus
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Verwenden des fensterlosen Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5189fb52932a328493baec9a79ccd6598a9a0659c198ee3ce3d4d157574a63c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119271250"
---
# <a name="using-windowless-mode"></a>Verwenden des fensterlosen Modus

Sowohl der [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) als auch der [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) unterstützen den *fensterlosen Modus*, der eine wesentliche Verbesserung gegenüber der [**IVideoWindow-Schnittstelle**](/windows/desktop/api/Control/nn-control-ivideowindow) darstellt. In diesem Thema werden die Unterschiede zwischen dem fensterlosen Modus und dem Fenstermodus sowie die Verwendung des fensterlosen Modus beschrieben.

Um abwärtskompatibel mit vorhandenen Anwendungen zu bleiben, wird der VMR standardmäßig in den Fenstermodus versetzt. Im Fenstermodus erstellt der Renderer ein eigenes Fenster zum Anzeigen des Videos. In der Regel legt die Anwendung das Videofenster als untergeordnetes Element des Anwendungsfensters fest. Das Vorhandensein eines separaten Videofensters verursacht jedoch einige Probleme:

-   Am wichtigsten ist, dass deadlocks auftreten können, wenn Fenstermeldungen zwischen Threads gesendet werden.
-   Der Filter Graph Manager muss bestimmte Fenstermeldungen wie WM \_ PAINT an den Videorenderer weiterleiten. Die Anwendung muss die Implementierung von [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) des Filter-Graph-Managers (und nicht die des Videorenderers) verwenden, damit der Filter Graph Manager den richtigen internen Zustand beibehält.
-   Um Maus- oder Tastaturereignisse aus dem Videofenster zu empfangen, muss die Anwendung einen *Nachrichtenabfluss* festlegen, wodurch das Videofenster diese Nachrichten an die Anwendung weiterleitet.
-   Um Clippingprobleme zu vermeiden, muss das Videofenster über die richtigen Fensterstile verfügen.

Der fensterlose Modus vermeidet diese Probleme, indem die VMR direkt im Clientbereich des Anwendungsfensters gezeichnet wird, indem DirectDraw zum Beschneiden des Videorechtecks verwendet wird. Der Fensterlose Modus verringert die Wahrscheinlichkeit von Deadlocks erheblich. Außerdem muss die Anwendung das Besitzerfenster oder die Fensterstile nicht festlegen. Wenn sich die VMR im fensterlosen Modus befindet, macht sie nicht einmal die [**IVideoWindow-Schnittstelle**](/windows/desktop/api/Control/nn-control-ivideowindow) verfügbar, die nicht mehr benötigt wird.

Um den fensterlosen Modus zu verwenden, müssen Sie die VMR explizit konfigurieren. Sie werden jedoch feststellen, dass flexibler und einfacher zu verwenden ist als der Fenstermodus.

Der VMR-7-Filter und der VMR-9-Filter machen verschiedene Schnittstellen verfügbar, aber die Schritte sind für jede äquivalent.

## <a name="configure-the-vmr-for-windowless-mode"></a>Konfigurieren der VMR für den fensterlosen Modus

Um das Standardverhalten der VMR zu überschreiben, konfigurieren Sie die VMR vor dem Erstellen des Filterdiagramms:

**VMR-7**

1.  Erstellen Sie den Filter Graph Manager.
2.  Erstellen Sie die VMR-7, und fügen Sie sie dem Filterdiagramm hinzu.
3.  Rufen Sie [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) auf der VMR-7 mit dem **VMRMode-Flag \_ "Windowless"** auf.
4.  Fragen Sie VMR-7 nach der [**IVMRWindowlessControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) ab.
5.  Rufen Sie [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) auf der VMR-7 auf. Geben Sie ein Handle für das Fenster an, in dem das Video angezeigt werden soll.

**VMR-9**

1.  Erstellen Sie den Filter Graph Manager.
2.  Erstellen Sie die VMR-9, und fügen Sie sie dem Filterdiagramm hinzu.
3.  Rufen Sie [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) auf der VMR-9 mit dem **VMR9Mode-Flag \_ "Windowless"** auf.
4.  Fragen Sie VMR-9 nach der [**IVMRWindowlessControl9-Schnittstelle**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) ab.
5.  Rufen Sie [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) auf der VMR-9 auf. Geben Sie ein Handle für das Fenster an, in dem das Video angezeigt werden soll.

Erstellen Sie nun den Rest des Filterdiagramms, indem [**Sie IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) oder andere Grapherstellungsmethoden aufrufen. Der Filter Graph Manager verwendet automatisch die Instanz der VMR, die Sie dem Diagramm hinzugefügt haben. (Ausführliche Informationen dazu, warum dies geschieht, finden Sie unter [Intelligent Verbinden](intelligent-connect.md).)

Der folgende Code zeigt eine Hilfsfunktion, die VMR-7 erstellt, dem Diagramm hinzufügt und den fensterlosen Modus einrichten kann.


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



Diese Funktion geht davon aus, dass nur ein Videostream angezeigt wird und keine statische Bitmap über dem Video gemischt wird. Weitere Informationen finden Sie unter [VMR-Fensterloser Modus.](vmr-windowless-mode.md) Sie würden diese Funktion wie folgt aufrufen:


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a>Positionieren des Videos

Nach dem Konfigurieren der VMR wird im nächsten Schritt die Position des Videos festgelegt. Es gibt zwei zu berücksichtigende Rechtecke: das *Quellrechteck* und das *Zielrechteck.* Das Quellrechteck definiert, welcher Teil des Videos angezeigt werden soll. Das Zielrechteck gibt den Bereich im Clientbereich des Fensters an, der das Video enthalten soll. Die VMR fügt das Videobild in das Quellrechteck ein und streckt das zugeschnittene Bild so, dass es dem Zielrechteck entspricht.

**VMR-7**

1.  Rufen Sie die [**IVMRWindowlessControl::SetVideoPosition-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) auf, um beide Rechtecke anzugeben.
2.  Das Quellrechteck muss gleich oder kleiner als die native Videogröße sein. Sie können die [**IVMRWindowlessControl::GetNativeVideoSize-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) verwenden, um die native Videogröße abzurufen.

**VMR-9**

1.  Rufen Sie die [**IVMRWindowlessControl9::SetVideoPosition-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) auf, um beide Rechtecke anzugeben.
2.  Das Quellrechteck muss gleich oder kleiner als die native Videogröße sein. Sie können die [**IVMRWindowlessControl9::GetNativeVideoSize-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) verwenden, um die native Videogröße abzurufen.

Der folgende Code legt beispielsweise die Quell- und Zielrechtecke für VMR-7 fest. Das Quellrechteck wird auf das gesamte Videobild und das Zielrechteck auf den gesamten Fensterclientbereich festgelegt:


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



Wenn Sie video einen kleineren Teil des Clientbereichs belegen möchten, ändern Sie den *rcDest-Parameter.* Wenn Sie das Videobild zuschneiden möchten, ändern Sie den *rcSrc-Parameter.*

## <a name="handle-window-messages"></a>Verarbeiten von Fenstermeldungen

Da die VMR nicht über ein eigenes Fenster verfügt, muss sie benachrichtigt werden, wenn sie das Video neu malen oder dessen Größe ändern muss. Reagieren Sie auf die folgenden Fenstermeldungen, indem Sie die aufgelisteten VMR-Methoden aufrufen.

**VMR-7**

1.  [**WM \_ PAINT**](../gdi/wm-paint.md). Rufen Sie [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo)auf. Diese Methode bewirkt, dass VMR-7 den neuesten Videoframe neu malt.
2.  [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): Rufen Sie [**IVMRWindowlessControl::D isplayModeChanged auf.**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged) Diese Methode benachrichtigt VMR-7, dass das Video mit einer neuen Auflösung oder Farbtiefe angezeigt werden muss.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) oder [**WM \_ WINDOWPOSCHANGED:**](../winmsg/wm-windowposchanged.md)Berechnen Sie die Position des Videos neu, und rufen Sie [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) auf, um die Position bei Bedarf zu aktualisieren.

**VMR-9**

1.  [**WM \_ PAINT**](../gdi/wm-paint.md). Rufen Sie [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo)auf. Diese Methode bewirkt, dass VMR-9 den neuesten Videoframe neu malt.
2.  [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): Rufen Sie [**IVMRWindowlessControl9::D isplayModeChanged auf.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged) Diese Methode benachrichtigt VMR-9, dass das Video mit einer neuen Auflösung oder Farbtiefe angezeigt werden muss.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) oder [**WM \_ WINDOWPOSCHANGED:**](../winmsg/wm-windowposchanged.md)Berechnen Sie die Position des Videos neu, und rufen Sie [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) auf, um die Position bei Bedarf zu aktualisieren.

> [!Note]  
> Der Standardhandler für die [**WM \_ WINDOWPOSCHANGED-Nachricht**](../winmsg/wm-windowposchanged.md) sendet eine [**WM \_ SIZE-Nachricht.**](../winmsg/wm-size.md) Wenn Ihre Anwendung jedoch **WM \_ WINDOWPOSCHANGED** abfängt und nicht an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt, sollten Sie **SetVideoPosition** in Ihrem **WM \_ WINDOWPOSCHANGED-Handler** zusätzlich zu Ihrem **WM \_ SIZE-Handler** aufrufen.

 

Das folgende Beispiel zeigt einen [**WM \_ PAINT-Meldungshandler.**](../gdi/wm-paint.md) Es zeichnet einen bereich, der durch das Clientrechteck minus dem Videorechteck definiert wird. Zeichnen Sie nicht auf das Videorechteck, da die VMR darauf zeichnet, was zu Flackern führt. Legen Sie aus demselben Grund keinen Hintergrundpinsel in der Fensterklasse fest.


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



Obwohl Sie auf [**WM \_ PAINT-Nachrichten**](../gdi/wm-paint.md) reagieren müssen, müssen Sie zwischen **WM \_ PAINT-Nachrichten** nichts unternehmen, um das Video zu aktualisieren. Wie in diesem Beispiel gezeigt, können Sie das Videobild im fensterlosen Modus einfach als selbst zeichnenden Bereich im Fenster behandeln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Videomischungsrenderers](using-the-video-mixing-renderer.md)
</dt> <dt>

[Videorendering](video-rendering.md)
</dt> </dl>

 

 
