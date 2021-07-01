---
description: Steuern eines Erfassungsdiagramms
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Steuern eines Erfassungsdiagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00573256c1c010e23dfc598ceca5ac62d772711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119475"
---
# <a name="controlling-a-capture-graph"></a>Steuern eines Erfassungsdiagramms

Die [**IMediaControl-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediacontrol) des Filtergraph-Managers verfügt über Methoden zum Ausführen, Beenden und Anhalten des gesamten Graphen. Wenn das Filterdiagramm jedoch über Erfassungs- und Vorschaudatenströme verfügt, sollten Sie die beiden Datenströme unabhängig voneinander steuern. Es kann beispielsweise sein, dass Sie eine Vorschau des Videos anzeigen möchten, ohne es zu erfassen. Hierzu können Sie die [**ICaptureGraphBuilder2::ControlStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) verwenden.

> [!Note]  
> Diese Methode funktioniert nicht bei der Erfassung in einer ASF-Datei (Advanced Systems Format).

 

Steuern des Erfassungsstreams

Der folgende Code legt fest, dass der Videoaufzeichnungsstream vier Sekunden lang ausgeführt wird und eine Sekunde nach der Ausführung des Diagramms beginnt:


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



Der erste Parameter gibt an, welcher Stream als PIN-Kategorie-GUID gesteuert werden soll. Der zweite Parameter gibt den Medientyp an. Der dritte Parameter ist ein Zeiger auf den Erfassungsfilter. Um alle Erfassungsstreams im Diagramm zu steuern, legen Sie den zweiten und dritten Parameter auf **NULL** fest.

Die nächsten beiden Parameter definieren die Zeiten, zu denen der Stream gestartet und beendet wird, relativ zur Zeit, zu der das Diagramm ausgeführt wird. Rufen Sie [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) auf, um das Diagramm auszuführen. Bis sie das Diagramm ausführen, hat die **ControlStream-Methode** keine Auswirkungen. Wenn das Diagramm bereits ausgeführt wird, werden die Einstellungen sofort wirksam.

Die letzten beiden Parameter werden zum Abrufen von Ereignisbenachrichtigungen verwendet, wenn der Stream gestartet und beendet wird. Für jeden Stream, den Sie mit dieser Methode steuern, sendet das Filterdiagramm ein Ereignispaar: [**EC \_ STREAM CONTROL \_ \_ STARTED**](ec-stream-control-started.md) beim Starten des Streams und [**EC STREAM CONTROL \_ \_ \_ STOPPED,**](ec-stream-control-stopped.md) wenn der Stream beendet wird. Die Werte von **wStartCookie** und **wStopCookie** werden als zweiter Ereignisparameter verwendet. Daher entspricht *lParam2* im Startereignis **wStartCookie** und *lParam2* im Beendigungsereignis **wStopCookie**. Der folgende Code zeigt, wie diese Ereignisse abzurufen sind:


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



Die **ControlStream-Methode** definiert einige spezielle Werte für die Start- und Beendigungszeiten.



| Wert | Start                                  | Beenden                               |
|-------------|----------------------------------------|---------|
| MAXLONGLONG | Starten Sie diesen Stream nie.               | Beenden Sie nicht, bis das Diagramm beendet wird. |
| **NULL**    | Starten Sie sofort, wenn das Diagramm ausgeführt wird. | Beenden Sie sofort.                  |



 

Mit dem folgenden Code wird der Erfassungsstream beispielsweise sofort beendet:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



Sie können den Erfassungsstream zwar beenden und später neu starten, dies führt jedoch zu einer Lücke in den Zeitstempeln. Bei der Wiedergabe wird das Video während der Lücke angehalten (je nach Dateiformat).

Steuern des Vorschaudatenstroms

Um den Vorschaupin zu steuern, rufen **Sie ControlStream** auf, legen aber den ersten Parameter auf PIN \_ CATEGORY PREVIEW \_ fest. Dies funktioniert genauso wie bei PIN \_ CATEGORY \_ CAPTURE, mit der Ausnahme, dass Sie keine Verweiszeiten verwenden können, um start und stop anzugeben, da die Vorschauframes keine Zeitstempel aufweisen. Daher müssen Sie **NULL** oder MAXLONGLONG verwenden. Verwenden Sie **NULL,** um den Vorschaustream zu starten:


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



Verwenden Sie MAXLONGLONG, um den Vorschaustream zu beenden:


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



Es spielt keine Rolle, ob der Vorschaudatenstrom von einem Vorschaupin im Erfassungsfilter oder vom Smart Tee-Filter stammt. Die **ControlStream-Methode** funktioniert auf beide Weise.

Bei Videoport-Pins schlägt die -Methode jedoch fehl. In diesem Fall besteht ein anderer Ansatz darin, das Videofenster auszublenden. Fragen Sie das Diagramm nach **IVideoWindow** ab, und verwenden Sie die [**IVideoWindow::p ut \_ Visible-Methode,**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) um das Fenster ein- oder auszublenden.


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



Wenn Sie [**außerdem IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) mit dem Wert OAFALSE aufrufen, bevor Sie das Diagramm ausführen, blendet der Filter Videorenderer das Fenster aus, bis Sie dies anders angeben. Standardmäßig zeigt der Videorenderer das Fenster an, wenn Sie das Diagramm ausführen.

Hinweise zum Stream-Steuerelement

Das Standardverhalten für eine Stecknadel ist die Bereitstellung von Beispielen, wenn das Diagramm ausgeführt wird. Angenommen, Sie rufen **ControlStream** mit PIN \_ CATEGORY \_ CAPTURE, aber nicht mit PIN \_ CATEGORY \_ PREVIEW auf. Wenn Sie das Diagramm ausführen, wird der Vorschaustream sofort ausgeführt, während der Erfassungsstream zu einem beliebigen Zeitpunkt ausgeführt wird, den Sie in **ControlStream** angegeben haben.

Wenn Sie mehrere Streams erfassen und an einen Mux-Filter senden , z. B. wenn Sie Audio- und Videodaten in einer AVI-Datei erfassen, sollten Sie beide Streams zusammen steuern. Andernfalls kann der mux-Filter das Warten auf einen Stream blockieren, da er versucht, die beiden Streams zu verschachteln. Legen Sie die gleichen Start- und Stoppzeiten für alle Erfassungsstreams fest, bevor Sie den Graphen ausführen:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



Intern verwendet die **ControlStream-Methode** die [**IAMStreamControl-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) die an den Pins des Erfassungsfilters verfügbar gemacht wird, den Smart Tee-Filter (falls vorhanden) und möglicherweise den Mux-Filter. Sie können diese Schnittstelle direkt verwenden, anstatt **ControlStream** aufzurufen, obwohl dies keinen besonderen Vorteil bietet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 



