---
description: Steuern eines Erfassungs-Graph
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Steuern eines Erfassungs-Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d678e00452fbf90591fbc187039ddbbc37cc4fde446e2e285c77fcaab415e815
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652140"
---
# <a name="controlling-a-capture-graph"></a>Steuern eines Erfassungs-Graph

Die [**IMediaControl Graph-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediacontrol) des Filter-Managers verfügt über Methoden zum Ausführen, Beenden und Anhalten des gesamten Graphen. Wenn das Filterdiagramm jedoch Erfassungs- und Vorschaustreams auflistet, möchten Sie die beiden Datenströme wahrscheinlich unabhängig voneinander steuern. Sie können z. B. eine Vorschau des Videos anzeigen, ohne es zu erfassen. Hierzu können Sie die [**ICaptureGraphBuilder2::ControlStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) verwenden.

> [!Note]  
> Diese Methode funktioniert nicht, wenn sie in einer ASF-Datei (Advanced Systems Format) erfasst wird.

 

Steuern des Erfassungsstreams

Der folgende Code legt fest, dass der Videoaufzeichnungsstream vier Sekunden lang ausgeführt wird, beginnend eine Sekunde nach der Ausführung des Diagramms:


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



Der erste Parameter gibt an, welcher Stream als PIN-Kategorie-GUID zu steuern ist. Der zweite Parameter gibt den Medientyp an. Der dritte Parameter ist ein Zeiger auf den Erfassungsfilter. Um alle Erfassungsstreams im Diagramm zu steuern, legen Sie den zweiten und dritten Parameter auf **NULL fest.**

Die nächsten beiden Parameter definieren die Zeiten, zu denen der Stream gestartet und stoppt, relativ zur Zeit, zu der die Ausführung des Diagramms beginnt. Rufen [**Sie IMediaControl::Run auf,**](/windows/desktop/api/Control/nf-control-imediacontrol-run) um den Graphen ausführen zu können. Bis sie das Diagramm ausführen, hat die **ControlStream-Methode** keine Auswirkungen. Wenn das Diagramm bereits ausgeführt wird, werden die Einstellungen sofort wirksam.

Die letzten beiden Parameter werden zum Abrufen von Ereignisbenachrichtigungen verwendet, wenn der Stream gestartet und beendet wird. Für jeden Stream, den Sie mit dieser Methode steuern, sendet das Filterdiagramm ein Ereignispaar: [**EC \_ STREAM CONTROL \_ \_ STARTED**](ec-stream-control-started.md) beim Start des Streams und [**EC STREAM CONTROL \_ \_ \_ STOPPED,**](ec-stream-control-stopped.md) wenn der Stream beendet wird. Die Werte **von wStartCookie** und **wStopCookie** werden als zweiter Ereignisparameter verwendet. Daher entspricht *lParam2* im Startereignis **wStartCookie** und *lParam2* im Stop-Ereignis **wStopCookie**. Der folgende Code zeigt, wie sie diese Ereignisse erhalten:


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



Die **ControlStream-Methode** definiert einige spezielle Werte für die Start- und Stoppzeiten.



| Wert | Starten                                  | Beenden                               |
|-------------|----------------------------------------|---------|
| MAXLONGLONGLONG | Starten Sie diesen Stream nie.               | Halten Sie erst an, wenn das Diagramm beendet wird. |
| **NULL**    | Starten Sie sofort, wenn das Diagramm ausgeführt wird. | Halten Sie sofort an.                  |



 

Der folgende Code beendet z. B. sofort den Erfassungsstream:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



Obwohl Sie den Erfassungsstream beenden und später neu starten können, wird dadurch eine Lücke in den Zeitstempeln erstellt. Bei der Wiedergabe scheint das Video während der Lücke zu stehen (je nach Dateiformat).

Steuern des Vorschaustreams

Um den Vorschaupin zu steuern, rufen **Sie ControlStream auf,** legen aber den ersten Parameter auf PIN \_ CATEGORY PREVIEW \_ fest. Dies funktioniert genauso wie bei PIN CATEGORY CAPTURE, mit der Ausnahme, dass Sie keine Verweiszeiten verwenden können, um start und stop anzugeben, da die Vorschauframes keine \_ \_ Zeitstempel haben. Daher müssen Sie NULL **oder** MAXLONGLONG verwenden. Verwenden **Sie NULL,** um den Vorschaustream zu starten:


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



Es spielt keine Rolle, ob der Vorschaustream von einem Vorschaupin auf dem Erfassungsfilter oder vom Smart Tee-Filter stammt. Die **ControlStream-Methode** funktioniert in beiden Richtungen.

Bei Videoport-Pins ist die -Methode jedoch fehlgeschlagen. In diesem Fall besteht ein anderer Ansatz im Ausblenden des Videofensters. Fragen Sie das Diagramm **nach IVideoWindow** ab, und verwenden Sie die [**IVideoWindow::p ut \_ Visible-Methode,**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) um das Fenster anzuzeigen oder auszublenden.


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



Wenn Sie [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) mit dem Wert OAFALSE aufrufen, bevor Sie das Diagramm ausführen, blendet der Videorendererfilter das Fenster aus, bis Sie etwas anderes angeben. Standardmäßig zeigt der Videorenderer das Fenster an, wenn Sie das Diagramm ausführen.

Hinweise zum Stream-Steuerelement

Das Standardverhalten für eine Stecknadel ist das Ausliefern von Stichproben, wenn der Graph ausgeführt wird. Angenommen, Sie rufen **ControlStream** mit PIN \_ CATEGORY \_ CAPTURE auf, aber nicht mit PIN \_ CATEGORY \_ PREVIEW. Wenn Sie das Diagramm ausführen, wird der Vorschaustream sofort ausgeführt, während der Erfassungsstream zu dem Zeitpunkt ausgeführt wird, den Sie in **ControlStream angegeben haben.**

Wenn Sie mehr als einen Stream erfassen und an einen Muxfilter senden , z. B. wenn Sie Audio- und Videodaten in einer AVI-Datei erfassen, sollten Sie beide Streams gemeinsam steuern. Andernfalls kann der Muxfilter das Warten auf einen Stream blockieren, da er versucht, die beiden Streams zu verweben. Legen Sie die gleichen Start- und Stoppzeiten für alle Erfassungsstreams fest, bevor Sie den Graphen ausführen:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



Intern verwendet die **ControlStream-Methode** die [**IAMStreamControl-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) die auf den Pins des Erfassungsfilters, dem Smart Tee-Filter (falls vorhanden) und möglicherweise dem Muxfilter verfügbar gemacht wird. Sie können diese Schnittstelle direkt verwenden, anstatt **ControlStream** auf aufruft, obwohl dies keinen besonderen Vorteil bietet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 



