---
description: Verwenden des fensterlosen Modus
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Verwenden des fensterlosen Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866448"
---
# <a name="using-windowless-mode"></a>Verwenden des fensterlosen Modus

Sowohl der [Video Mischungs Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) als auch der [Video Mischungs Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) unterstützen den *fensterlosen Modus*, der eine bedeutende Verbesserung gegenüber der [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle darstellt. In diesem Thema werden die Unterschiede zwischen dem fensterlosen Modus und dem Fenstermodus sowie die Verwendung des fensterlosen Modus beschrieben.

Um Abwärtskompatibilität mit vorhandenen Anwendungen zu erhalten, wird für VMR standardmäßig der Fenster-Modus verwendet. Im Fenstermodus erstellt der Renderer ein eigenes Fenster, um das Video anzuzeigen. In der Regel legt die Anwendung das Videofenster als untergeordnetes Element des Anwendungsfensters fest. Das vorhanden sein eines separaten Videofensters verursacht jedoch einige Probleme:

-   Am wichtigsten ist, dass es zu Deadlocks kommen kann, wenn zwischen Threads Fenster Meldungen gesendet werden.
-   Der Filter Graph-Manager muss bestimmte Fenster Meldungen, z. b \_ . WM Paint, an den Videorenderer weiterleiten. Die Anwendung muss die Implementierung von [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) des Filter Diagramms (und nicht die des Videorenderers) verwenden, damit der Filter Graph-Manager den korrekten internen Zustand beibehält.
-   Um Maus-oder Tastatur Ereignisse aus dem Videofenster zu empfangen, muss die Anwendung eine *Nachrichten Ableitung* festlegen, sodass das Videofenster diese Nachrichten an die Anwendung weiterleiten kann.
-   Um clippingprobleme zu vermeiden, muss das Videofenster über die richtigen Fenster Stile verfügen.

Der fensterlose Modus vermeidet diese Probleme, indem der VMR direkt im Client Bereich des Anwendungsfensters gezeichnet wird. dabei wird DirectDraw zum Ausschneiden des Video Rechtecks verwendet. Der fensterlose Modus verringert die Wahrscheinlichkeit von Deadlocks erheblich. Außerdem muss die Anwendung das Besitzer Fenster oder die Fenster Stile nicht festlegen. Wenn sich VMR im fensterlosen Modus befindet, wird die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle nicht einmal verfügbar gemacht, da Sie nicht mehr benötigt wird.

Um den fensterlosen Modus zu verwenden, müssen Sie den VMR explizit konfigurieren. Sie werden jedoch feststellen, dass flexibler und einfacher zu verwenden ist als der Fenstermodus.

Der VMR-7-Filter und der VMR-9-Filter machen verschiedene Schnittstellen verfügbar, die Schritte sind jedoch gleichwertig.

## <a name="configure-the-vmr-for-windowless-mode"></a>Konfigurieren des VMR für den fensterlosen Modus

Um das VMR-Standardverhalten zu überschreiben, konfigurieren Sie VMR vor dem Aufbau des Filter Diagramms:

**VMR-7**

1.  Erstellen Sie den Filter Graph-Manager.
2.  Erstellen Sie VMR-7, und fügen Sie es dem Filter Diagramm hinzu.
3.  Wenden Sie [**ivmrfilterconfig:: setrenderingmode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) für VMR-7 mit dem **\_ Windows-Flag "vmrmode** " an.
4.  Fragen Sie VMR-7 nach der [**ivmrwindowlesscontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) -Schnittstelle ab.
5.  Aufrufen von [**ivmrwindowlesscontrol:: setvideoclippingwindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) für VMR-7. Geben Sie ein Handle für das Fenster an, in dem das Video angezeigt werden soll.

**VMR-9**

1.  Erstellen Sie den Filter Graph-Manager.
2.  Erstellen Sie VMR-9, und fügen Sie es dem Filter Diagramm hinzu.
3.  Wenden Sie [**IVMRFilterConfig9:: setrenderingmode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) auf VMR-9 mit dem **VMR9Mode \_ Windows less** -Flag an.
4.  Fragen Sie VMR-9 nach der [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) -Schnittstelle ab.
5.  Aufrufen von [**IVMRWindowlessControl9:: setvideoclippingwindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) für VMR-9. Geben Sie ein Handle für das Fenster an, in dem das Video angezeigt werden soll.

Erstellen Sie jetzt den Rest des Filter Diagramms, indem Sie [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) oder andere Graph-Erstellungs Methoden aufrufen. Der Filter Graph-Manager verwendet automatisch die Instanz von VMR, die Sie dem Diagramm hinzugefügt haben. (Ausführliche Informationen dazu, warum dies geschieht, finden Sie unter [Intelligent Connect](intelligent-connect.md).)

Der folgende Code zeigt eine Hilfsfunktion, die VMR-7 erstellt, Sie dem Diagramm hinzufügt und den fensterlosen Modus einrichtet.


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



Diese Funktion geht davon aus, dass nur einen Videodaten Strom anzeigt und keine statische Bitmap über das Video vermischt. Weitere Informationen finden Sie unter [Windows-VMR-Modus](vmr-windowless-mode.md). Diese Funktion wird wie folgt aufgerufen:


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

Nach dem Konfigurieren von VMR ist der nächste Schritt das Festlegen der Position des Videos. Es gibt zwei zu berücksichtigende Rechtecke, das *Quell* Rechteck und das *Ziel* Rechteck. Das Quell Rechteck definiert, welcher Teil des Videos angezeigt werden soll. Das Ziel Rechteck gibt den Bereich im Client Bereich des Fensters an, in dem das Video enthalten sein soll. Die VMR sorgt für das Video Bild für das Quell Rechteck und dehnt das abgeschnittene Bild so aus, dass es an das Ziel Rechteck angepasst wird.

**VMR-7**

1.  Um beide Rechtecke anzugeben, können Sie die [**ivmrwindowlesscontrol:: setvideoposition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) -Methode aufrufen.
2.  Das Quell Rechteck muss kleiner oder gleich der systemeigenen Videogröße sein. Sie können die [**ivmrwindowlesscontrol:: getnativevideosize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) -Methode verwenden, um die systemeigene Videogröße zu erhalten.

**VMR-9**

1.  Aufrufen der [**IVMRWindowlessControl9:: setvideoposition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) -Methode, um beide Rechtecke anzugeben.
2.  Das Quell Rechteck muss kleiner oder gleich der systemeigenen Videogröße sein. Sie können die [**IVMRWindowlessControl9:: getnativevideosize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) -Methode verwenden, um die systemeigene Videogröße zu erhalten.

Der folgende Code legt z. b. die Quell-und Ziel Rechtecke für VMR-7 fest. Das Quell Rechteck wird auf das gesamte Video Bild festgelegt, und das Ziel Rechteck entspricht dem gesamten Fenster Client Bereich:


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



Wenn Sie ein Video mit einem kleineren Teil des Client Bereichs belegen möchten, ändern Sie den *rcdest* -Parameter. Wenn Sie das Video Bild zuschneiden möchten, ändern Sie den *rcsrc* -Parameter.

## <a name="handle-window-messages"></a>Fenster Meldungen behandeln

Da VMR kein eigenes Fenster hat, muss es benachrichtigt werden, wenn das Video neu gezeichnet oder die Größe des Videos geändert werden muss. Reagieren Sie auf die folgenden Fenster Meldungen, indem Sie die aufgeführten VMR-Methoden aufrufen.

**VMR-7**

1.  [**WM \_ Paint**](../gdi/wm-paint.md). Nennen Sie [**ivmrwindowlesscontrol:: repaintvideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo). Diese Methode bewirkt, dass VMR-7 den neuesten Videoframe neu zeichnet.
2.  [**WM \_ Display Change**](../gdi/wm-displaychange.md): der Befehl [**ivmrwindowlesscontrol::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). Diese Methode benachrichtigt VMR-7, dass das Video mit einer neuen Auflösung oder Farbtiefe angezeigt werden muss.
3.  [**WM \_ Size**](../winmsg/wm-size.md) oder [**WM \_ windowposchge**](../winmsg/wm-windowposchanged.md): Berechnen Sie die Position des Videos neu, und wenden Sie [**ivmrwindowlesscontrol:: setvideoposition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) an, um die Position bei Bedarf zu aktualisieren.

**VMR-9**

1.  [**WM \_ Paint**](../gdi/wm-paint.md). Nennen Sie [**IVMRWindowlessControl9:: repaintvideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo). Diese Methode bewirkt, dass VMR-9 den neuesten Videorahmen neu zeichnet.
2.  [**WM \_ Display Change**](../gdi/wm-displaychange.md): IVMRWindowlessControl9 aufgerufen [**::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged). Diese Methode benachrichtigt VMR-9, dass das Video mit einer neuen Auflösung oder Farbtiefe angezeigt werden muss.
3.  [**WM \_ Size**](../winmsg/wm-size.md) oder [**WM \_ windowposchangi:**](../winmsg/wm-windowposchanged.md)berechnet die Position des Videos neu und ruft [**IVMRWindowlessControl9:: setvideoposition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) auf, um die Position bei Bedarf zu aktualisieren.

> [!Note]  
> Der Standard Handler für die [**WM- \_ windowposchge**](../winmsg/wm-windowposchanged.md) -Nachricht sendet eine [**WM- \_ Größen**](../winmsg/wm-size.md) Nachricht. Wenn Ihre Anwendung jedoch **WM \_ windowposchge** abfängt und Sie nicht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt, sollten Sie **setvideoposition** zusätzlich zu Ihrem WM- **\_ Größen** Handler in Ihrem **WM- \_ windowposchge** -Handler aufrufen.

 

Das folgende Beispiel zeigt einen [**WM \_ Paint**](../gdi/wm-paint.md) -Meldungs Handler. Es zeichnet einen Bereich, der durch das Client Rechteck abzüglich des Video Rechtecks definiert wird. Ziehen Sie nicht auf das Video Rechteck, da das VMR darauf zeigt, was zu einem Flimmern führt. Legen Sie aus demselben Grund keinen Hintergrund Pinsel in der Fenster Klasse fest.


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



Obwohl Sie auf [**WM \_ Paint**](../gdi/wm-paint.md) -Meldungen Antworten müssen, müssen Sie zwischen **WM \_ Paint** -Meldungen nichts tun, um das Video zu aktualisieren. Wie in diesem Beispiel gezeigt, können Sie das Video Bild im fensterlosen Modus einfach als selbst Zeichnungs Bereich im Fenster behandeln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Video Mischungs Renderers](using-the-video-mixing-renderer.md)
</dt> <dt>

[Videorendering](video-rendering.md)
</dt> </dl>

 

 
