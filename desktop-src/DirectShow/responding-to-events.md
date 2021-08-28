---
description: In diesem Artikel wird beschrieben, wie Sie auf Ereignisse reagieren, die in einem Filterdiagramm auftreten.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Reagieren auf Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb0325af2e216a3679d3e15a293aa6bfe1c100f2271d089e982b295df791130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050560"
---
# <a name="responding-to-events"></a>Reagieren auf Ereignisse

In diesem Artikel wird beschrieben, wie Sie auf Ereignisse reagieren, die in einem Filterdiagramm auftreten.

## <a name="how-event-notification-works"></a>Funktionsweise von Ereignisbenachrichtigungen

Während eine DirectShow-Anwendung ausgeführt wird, können Ereignisse innerhalb des Filterdiagramms auftreten. Beispielsweise kann bei einem Filter ein Streamingfehler auftreten. Filter warnen den Filter Graph Manager durch Senden von Ereignissen, die aus einem Ereigniscode und zwei Ereignisparametern bestehen. Der Ereigniscode gibt den Ereignistyp an, und die Ereignisparameter stellen zusätzliche Informationen zur Verfügung. Die Bedeutung der Parameter hängt vom Ereigniscode ab. Eine vollständige Liste der Ereigniscodes finden Sie unter [Ereignisbenachrichtigungscodes.](event-notification-codes.md)

Einige Ereignisse werden vom Filter Graph Manager im Hintergrund behandelt, ohne dass die Anwendung benachrichtigt wird. Andere Ereignisse werden in einer Warteschlange für die Anwendung platziert. Je nach Anwendung gibt es verschiedene Ereignisse, die Sie möglicherweise behandeln müssen. Dieser Artikel konzentriert sich auf drei Ereignisse, die sehr häufig vorkommen:

-   Das [**EC \_ COMPLETE-Ereignis**](ec-complete.md) gibt an, dass die Wiedergabe normal abgeschlossen wurde.
-   Das [**EC \_ USERABORT-Ereignis**](ec-userabort.md) gibt an, dass der Benutzer die Wiedergabe unterbrochen hat. Videorenderer senden dieses Ereignis, wenn der Benutzer das Videofenster schließt.
-   Das [**EC \_ ERRORABORT-Ereignis**](ec-errorabort.md) gibt an, dass die Wiedergabe aufgrund eines Fehlers angehalten wurde.

## <a name="using-event-notification"></a>Verwenden von Ereignisbenachrichtigungen

Eine Anwendung kann den Filter Graph Manager anweisen, immer dann eine Windows Nachricht an ein festgelegtes Fenster zu senden, wenn ein neues Ereignis auftritt. Dadurch kann die Anwendung innerhalb der Meldungsschleife des Fensters reagieren. Definieren Sie zunächst die Nachricht, die an das Anwendungsfenster gesendet wird. Anwendungen können Nachrichtennummern im Bereich von \_ WM-APP bis 0xBFFF als private Nachrichten verwenden:


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



Fragen Sie als Nächstes den Filter Graph Manager für die [**IMediaEventEx-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediaeventex) ab, und rufen Sie die [**IMediaEventEx::SetNotifyWindow-Methode**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) auf:


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Diese Methode bestimmt das angegebene Fenster (g \_ hwnd) als Empfänger der Nachricht. Rufen Sie die -Methode auf, nachdem Sie das Filterdiagramm erstellt haben, aber bevor Sie das Diagramm ausführen.

WM \_ GRAPHNOTIFY ist eine gewöhnliche Windows Meldung. Wenn der Filter Graph Manager ein neues Ereignis in die Ereigniswarteschlange eingibt, sendet er eine WM \_ GRAPHNOTIFY-Nachricht an das angegebene Anwendungsfenster. Der *lParam-Parameter* der Nachricht entspricht dem dritten Parameter in [**SetNotifyWindow.**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) Mit diesem Parameter können Sie Instanzdaten mit der Nachricht senden. Der *wParam-Parameter* der Fenstermeldung ist immer 0 (null).

Fügen Sie in der **WindowProc-Funktion** Ihrer Anwendung eine case-Anweisung für die WM \_ GRAPHNOTIFY-Nachricht hinzu:


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



Rufen Sie in der Ereignishandlerfunktion die [**IMediaEvent::GetEvent-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) auf, um Ereignisse aus der Warteschlange abzurufen:


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



Die [**GetEvent-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) ruft den Ereigniscode und die beiden Ereignisparameter ab. Der vierte **GetEvent-Parameter** gibt die Wartezeit auf ein Ereignis in Millisekunden an. Da die Anwendung diese Methode als Reaktion auf eine WM \_ GRAPHNOTIFY-Nachricht aufruft, wird das Ereignis bereits in die Warteschlange eingereiht. Daher legen wir den Time out-Wert auf 0 (null) fest.

Die Ereignisbenachrichtigung und die Nachrichtenschleife sind asynchron, sodass die Warteschlange bis zu dem Zeitpunkt, zu dem Ihre Anwendung auf die Nachricht reagiert, möglicherweise mehr als ein Ereignis enthält. Außerdem kann der Filter Graph Manager bestimmte Ereignisse aus der Warteschlange entfernen, wenn sie ungültig werden. Daher sollten Sie [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) aufrufen, bis ein Fehlercode zurückgegeben wird, der angibt, dass die Warteschlange leer ist.

In diesem Beispiel antwortet die Anwendung auf [**EC \_ COMPLETE,**](ec-complete.md) [**EC \_ USERABORT**](ec-userabort.md)und [**EC \_ ERRORABORT,**](ec-errorabort.md) indem sie die von der Anwendung definierte CleanUp-Funktion aufruft, wodurch die Anwendung ordnungsgemäß beendet wird. Im Beispiel werden die beiden Ereignisparameter ignoriert. Nachdem Sie ein Ereignis abgerufen haben, rufen Sie [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) für alle freien Ressourcen auf, die den Ereignisparametern zugeordnet sind.

Beachten Sie, dass ein [**EC \_ COMPLETE-Ereignis**](ec-complete.md) nicht dazu führt, dass das Filterdiagramm beendet wird. Die Anwendung kann das Diagramm entweder beenden oder anhalten. Wenn Sie das Diagramm beenden, geben Filter alle Ressourcen frei, die sie innehaben. Wenn Sie das Diagramm anhalten, enthalten Filter weiterhin Ressourcen. Wenn ein Videorenderer angehalten wird, wird außerdem ein statisches Bild des letzten Frames angezeigt.

Bevor Sie den [**IMediaEventEx-Zeiger**](/windows/desktop/api/Control/nn-control-imediaeventex) freigeben, brechen Sie die Ereignisbenachrichtigung ab, indem [**Sie SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) mit einem **NULL-Fensterhandle** aufrufen:


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



Überprüfen Sie im WM \_ GRAPHNOTIFY-Meldungshandler den [**IMediaEventEx-Zeiger,**](/windows/desktop/api/Control/nn-control-imediaeventex) bevor [**Sie GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)aufrufen:


```C++
if (g_pEvent == NULL) return;
```



Dadurch wird ein möglicher Fehler verhindert, der auftreten kann, wenn die Anwendung die Ereignisbenachrichtigung empfängt, nachdem der Zeiger freigegeben wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende DirectShow-Aufgaben](basic-directshow-tasks.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



