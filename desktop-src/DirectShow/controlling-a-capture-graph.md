---
description: Steuern eines Aufzeichnungs Diagramms
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Steuern eines Aufzeichnungs Diagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6366645f14822a770b828e59b2201e378a0e1e8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522032"
---
# <a name="controlling-a-capture-graph"></a>Steuern eines Aufzeichnungs Diagramms

Die [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) -Schnittstelle des Filter Graph-Managers verfügt über Methoden zum Ausführen, beenden und Anhalten des gesamten Diagramms. Wenn das Filter Diagramm jedoch Erfassungs-und Vorschau Datenströme enthält, sollten Sie die beiden Streams wahrscheinlich unabhängig voneinander steuern. Beispielsweise können Sie eine Vorschau des Videos anzeigen, ohne es zu erfassen. Hierfür können Sie die [**ICaptureGraphBuilder2:: controlstream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) -Methode verwenden.

> [!Note]  
> Diese Methode funktioniert nicht, wenn Sie in einer ASF-Datei (Advanced Systems Format) erfasst wird.

 

Steuern des Erfassungsdaten Stroms

Mit dem folgenden Code wird der Video Erfassungsdaten Strom so festgelegt, dass er vier Sekunden lang ausgeführt wird:


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



Der erste Parameter gibt an, welcher Stream als PIN-Kategorie-GUID zu steuern ist. Der zweite Parameter gibt den Medientyp an. Der dritte Parameter ist ein Zeiger auf den Erfassungs Filter. Legen Sie den zweiten und den dritten Parameter auf **null** fest, um alle Aufzeichnungsdaten Ströme im Diagramm zu steuern.

Die folgenden beiden Parameter definieren die Zeiten, zu denen der Stream gestartet und beendet wird, relativ zu dem Zeitpunkt, zu dem die Ausführung des Diagramms beginnt. Nennen Sie [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) , um das Diagramm auszuführen. Die **controlstream** -Methode hat keine Auswirkungen, bis Sie das Diagramm ausführen. Wenn das Diagramm bereits ausgeführt wird, werden die Einstellungen sofort wirksam.

Die letzten beiden Parameter werden zum erhalten von Ereignis Benachrichtigungen verwendet, wenn der Stream gestartet und beendet wird. Für jeden Datenstrom, den Sie mit dieser Methode steuern, sendet das Filter Diagramm ein Ereignispaar: das [**EC- \_ \_ streamsteuerelement \_**](ec-stream-control-started.md) wurde beim Start des Streams gestartet, und das EC-Stream-Steuerelement wurde [**\_ \_ \_ beendet**](ec-stream-control-stopped.md) , wenn der Stream beendet wird. Die Werte von **wstartcookie** und **wstopcookie** werden als zweiter Ereignis Parameter verwendet. Daher ist *lParam2* im Start Ereignis mit **wstartcookie identisch**, und *lParam2* im Stop-Ereignis entspricht **wstopcookie**. Der folgende Code zeigt, wie diese Ereignisse angezeigt werden:


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



Die **controlstream** -Methode definiert einige besondere Werte für Start-und Endzeit.



|             |                                        |                                    |
|-------------|----------------------------------------|------------------------------------|
|             | Start                                  | Stop                               |
| Maxlonglong | Starten Sie diesen Stream nie.               | Beenden Sie nicht, bis das Diagramm angehalten wird. |
| **NULL**    | Sofort starten, wenn das Diagramm ausgeführt wird. | Sofort beendet werden.                  |



 

Mit dem folgenden Code wird der Aufzeichnungsdaten Strom beispielsweise sofort beendet:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



Obwohl Sie den Erfassungsdaten Strom abbrechen und später neu starten können, wird dadurch eine Lücke in den Zeitstempeln erzeugt. Bei der Wiedergabe erscheint das Video während der Lücke (abhängig vom Dateiformat).

Steuern des Vorschau Datenstroms

Um die Vorschau-PIN zu steuern, wenden Sie **controlstream** an, und legen Sie den ersten Parameter auf Pin \_ Category \_ Preview fest. Dies funktioniert genauso wie bei der \_ Erfassung der PIN-Kategorie \_ , mit dem Unterschied, dass Sie keine Verweis Zeiten zum Angeben des Starts und Stopps verwenden können, da die Vorschau Rahmen keine Zeitstempel aufweisen. Daher muss **null** oder maxlonglong verwendet werden. Verwenden Sie **null** , um den Vorschau Datenstrom zu starten:


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



Verwenden Sie maxlonglong, um den Vorschau Datenstrom anzuhalten:


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



Es spielt keine Rolle, ob der Vorschau Datenstrom aus einer Vorschau-PIN im Erfassungs Filter oder aus dem Smart Tee-Filter stammt. Die **controlstream** -Methode funktioniert in jedem Fall.

Bei Video Port Pins schlägt die Methode jedoch fehl. In diesem Fall besteht ein anderer Ansatz darin, das Videofenster auszublenden. Fragen Sie das Diagramm nach **IVideoWindow** ab, und verwenden Sie die [**\_ sichtbare IVideoWindow::p UT**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) -Methode, um das Fenster anzuzeigen oder auszublenden.


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



Wenn Sie [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) mit dem Wert oafalse vor dem Ausführen des Diagramms aufgerufen haben, blendet der Videorenderer-Filter das Fenster aus, bis Sie andernfalls angeben. Standardmäßig zeigt der Videorenderer das Fenster an, wenn Sie das Diagramm ausführen.

Hinweise zur Datenstrom Steuerung

Das Standardverhalten für eine PIN besteht darin, bei der Ausführung des Diagramms Beispiele zu liefern. Nehmen Sie beispielsweise an, dass Sie **controlstream** mit PIN \_ Category Capture, \_ aber nicht mit der Vorschau der PIN-Kategorie aufgerufen haben \_ \_ . Wenn Sie das Diagramm ausführen, wird der vorschaustream sofort ausgeführt, während der Erfassungsdaten Strom zu jedem Zeitpunkt ausgeführt wird, den Sie in **controlstream** angegeben haben.

Wenn Sie mehr als einen Stream erfassen und an einen MUX-Filter senden – wenn Sie z. b. Audiodaten und Videos in einer AVI-Datei erfassen – sollten Sie beide Streams zusammen steuern. Andernfalls blockiert der Mux-Filter möglicherweise das warten auf einen Stream, da er versucht, die beiden Streams zu überdenken. Legen Sie vor dem Ausführen des Diagramms die gleichen Start-und Endzeiten für alle Erfassungsdaten Ströme fest:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



Intern verwendet die **controlstream** -Methode die [**iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) -Schnittstelle, die auf den Pins des Erfassungs Filters verfügbar ist, den intelligenten Tee-Filter (falls vorhanden) und ggf. den MUX-Filter. Sie können diese Schnittstelle direkt verwenden, anstatt **controlstream** aufrufen zu müssen, obwohl es keinen besonderen Vorteil gibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 



