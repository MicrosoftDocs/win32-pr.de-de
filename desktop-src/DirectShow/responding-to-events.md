---
description: In diesem Artikel wird beschrieben, wie Sie auf Ereignisse reagieren, die in einem Filter Diagramm auftreten.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Reagieren auf Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521400"
---
# <a name="responding-to-events"></a>Reagieren auf Ereignisse

In diesem Artikel wird beschrieben, wie Sie auf Ereignisse reagieren, die in einem Filter Diagramm auftreten.

## <a name="how-event-notification-works"></a>Funktionsweise der Ereignis Benachrichtigung

Während eine DirectShow-Anwendung ausgeführt wird, können Ereignisse innerhalb des Filter Diagramms auftreten. Ein Filter kann z. b. auf einen Streamingfehler stoßen. Filter benachrichtigen den Filter Graph-Manager durch das Senden von Ereignissen, die aus einem Ereignis Code und zwei Ereignis Parametern bestehen. Der Ereignis Code gibt den Typ des Ereignisses an, und die Ereignis Parameter stellen zusätzliche Informationen bereit. Die Bedeutung der Parameter hängt vom Ereignis Code ab. Eine umfassende Liste der Ereignis Codes finden Sie unter [Ereignis Benachrichtigungs Codes](event-notification-codes.md).

Einige Ereignisse werden vom Filter Graph-Manager automatisch verarbeitet, ohne dass die Anwendung benachrichtigt wird. Andere Ereignisse werden in eine Warteschlange für die Anwendung eingefügt. Abhängig von der Anwendung gibt es verschiedene Ereignisse, die Sie möglicherweise behandeln müssen. Dieser Artikel konzentriert sich auf drei häufige Ereignisse:

-   Das Ereignis [**EC \_ Complete**](ec-complete.md) gibt an, dass die Wiedergabe normal abgeschlossen wurde.
-   Das Ereignis " [**EC \_ userabort**](ec-userabort.md) " gibt an, dass der Benutzer die Wiedergabe unterbrochen hat. Videorenderer Senden dieses Ereignis, wenn der Benutzer das Videofenster schließt.
-   Das [**EC \_ errorabort**](ec-errorabort.md) -Ereignis gibt an, dass die Wiedergabe aufgrund eines Fehlers angehalten wurde.

## <a name="using-event-notification"></a>Verwenden der Ereignis Benachrichtigung

Eine Anwendung kann den Filter Graph-Manager anweisen, eine Windows-Meldung an ein bestimmtes Fenster zu senden, wenn ein neues Ereignis auftritt. Dadurch kann die Anwendung innerhalb der Nachrichten Schleife des Fensters Antworten. Definieren Sie zuerst die Nachricht, die an das Anwendungsfenster gesendet wird. Anwendungen können Nachrichtennummern im Bereich von WM- \_ app bis 0xbfff als private Nachrichten verwenden:


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



Fragen Sie als nächstes den Filter Graph-Manager nach der [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Schnittstelle ab, und nennen Sie die [**imediaeventex:: setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) -Methode:


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Diese Methode legt das angegebene Fenster (g \_ HWND) als Empfänger der Nachricht fest. Rufen Sie die-Methode auf, nachdem Sie das Filter Diagramm erstellt haben, aber bevor Sie das Diagramm ausführen.

WM \_ graphnotify ist eine gewöhnliche Windows-Meldung. Jedes Mal, wenn der Filter Graph-Manager ein neues Ereignis in der Ereignis Warteschlange einfügt, sendet er eine WM- \_ graphnotify-Meldung an das angegebene Anwendungsfenster. Der *LPARAM* -Parameter der Nachricht ist gleich dem dritten Parameter in [**setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Dieser Parameter ermöglicht es Ihnen, Instanzdaten mit der Nachricht zu senden. Der *wParam* -Parameter der Fenster Meldung ist immer 0 (null).

Fügen Sie in der **WindowProc** -Funktion Ihrer Anwendung eine Case-Anweisung für die WM- \_ graphnotify-Nachricht hinzu:


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



Rufen Sie in der Ereignishandlerfunktion die [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) -Methode auf, um Ereignisse aus der Warteschlange abzurufen:


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



Die [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) -Methode ruft den Ereignis Code und die beiden Ereignis Parameter ab. Der vierte **GetEvent** -Parameter gibt die Zeitdauer an, die auf ein Ereignis gewartet wird (in Millisekunden). Da die Anwendung diese Methode als Reaktion auf eine WM- \_ graphnotify-Nachricht aufruft, wird das Ereignis bereits in die Warteschlange eingereiht. Daher legen wir den Timeout Wert auf 0 (null) fest.

Die Ereignis Benachrichtigung und die Nachrichten Schleife sind asynchron, sodass die Warteschlange möglicherweise mehr als ein Ereignis enthält, wenn Ihre Anwendung auf die Nachricht antwortet. Der Filter Graph-Manager kann auch bestimmte Ereignisse aus der Warteschlange entfernen, wenn Sie ungültig werden. Daher sollten Sie [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) so lange aufzurufen, bis ein Fehlercode zurückgegeben wird, der angibt, dass die Warteschlange leer ist.

In diesem Beispiel reagiert die Anwendung auf [**EC \_ Complete**](ec-complete.md), [**EC \_ userabort**](ec-userabort.md)und [**EC \_ errorabort**](ec-errorabort.md) , indem Sie die Anwendungs definierte Bereinigungs Funktion aufruft, die bewirkt, dass die Anwendung ordnungsgemäß beendet wird. Im Beispiel werden die beiden Ereignis Parameter ignoriert. Nachdem Sie ein Ereignis abgerufen haben, rufen Sie [**imediaevent:: freeeventparser**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) für alle freien Ressourcen auf, die den Ereignis Parametern zugeordnet sind.

Beachten Sie, dass ein [**EC \_ Complete**](ec-complete.md) -Ereignis nicht dazu führt, dass das Filter Diagramm angehalten wird. Die Anwendung kann das Diagramm entweder anhalten oder anhalten. Wenn Sie das Diagramm abbrechen, gibt Filter alle Ressourcen frei, die Sie halten. Wenn Sie das Diagramm anhalten, enthalten Filter weiterhin Ressourcen. Wenn ein Videorenderer anhält, wird auch ein statisches Bild des letzten Frames angezeigt.

Bevor Sie den [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Zeiger freigeben, brechen Sie die Ereignis Benachrichtigung ab, indem Sie [**setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) mit einem **null** -Fenster Handle aufrufen:


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



\_Überprüfen Sie im "WM graphnotify"-Nachrichten Handler den [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Zeiger, bevor Sie " [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)" aufrufen:


```C++
if (g_pEvent == NULL) return;
```



Dadurch wird ein möglicher Fehler verhindert, der auftreten kann, wenn die Anwendung die Ereignis Benachrichtigung empfängt, nachdem der Zeiger losgelassen wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende DirectShow-Aufgaben](basic-directshow-tasks.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



