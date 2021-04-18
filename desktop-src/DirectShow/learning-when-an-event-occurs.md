---
description: Lernen, wenn ein Ereignis eintritt
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Lernen, wenn ein Ereignis eintritt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed537430fd66818687b142f059399292c923e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522067"
---
# <a name="learning-when-an-event-occurs"></a>Lernen, wenn ein Ereignis eintritt

Um DirectShow-Ereignisse zu verarbeiten, benötigt eine Anwendung eine Methode, um herauszufinden, wann Ereignisse in der Warteschlange warten. Der Filter Graph-Manager bietet zwei Möglichkeiten, dies zu erreichen:

-   **Fenster Benachrichtigung:** Der Filter Graph-Manager sendet eine benutzerdefinierte Windows-Meldung an ein Anwendungsfenster, wenn ein neues Ereignis vorhanden ist.
-   **Ereignis Signalisierung:** Der Filter Graph-Manager signalisiert einem Windows-Ereignis, wenn sich DirectShow-Ereignisse in der Warteschlange befinden, und setzt das Ereignis zurück, wenn die Warteschlange leer ist.

Eine Anwendung kann beide Techniken verwenden. Die Fenster Benachrichtigung ist in der Regel einfacher.

**Fenster Benachrichtigung**

Um eine Fenster Benachrichtigung einzurichten, müssen Sie die [**imediaeventex:: setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) -Methode aufrufen und eine private Meldung angeben. Anwendungen können Nachrichtennummern im Bereich von WM- \_ app bis 0xbfff als private Nachrichten verwenden. Jedes Mal, wenn der Filter Diagramm-Manager eine neue Ereignis Benachrichtigung in der Warteschlange eingibt, wird diese Nachricht an das angegebene Fenster gesendet. Die Anwendung antwortet innerhalb der Nachrichten Schleife des Fensters auf die Nachricht.

Im folgenden Codebeispiel wird gezeigt, wie das Benachrichtigungsfenster festgelegt wird.


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Die Meldung ist eine normale Windows-Meldung und wird separat von der DirectShow-Ereignis Benachrichtigungs Warteschlange gepostet. Der Vorteil dieses Ansatzes besteht darin, dass die meisten Anwendungen bereits eine Nachrichten Schleife implementiert haben. Daher können Sie die DirectShow-Ereignis Behandlung ohne viel zusätzliche Arbeit integrieren.

Im folgenden Codebeispiel wird gezeigt, wie auf die Benachrichtigungs Meldung reagiert wird. Ein umfassendes Beispiel finden Sie unter [reagieren auf Ereignisse](responding-to-events.md).


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



Da Ereignis Benachrichtigung und Nachrichten Schleife asynchron sind, kann die Warteschlange mehr als ein Ereignis enthalten, wenn die Anwendung auf die Nachricht antwortet. Außerdem können Ereignisse manchmal aus der Warteschlange gelöscht werden, wenn Sie ungültig werden. Daher wird in Ihrem Ereignis Behandlungs Code [**iammediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) aufgerufen, bis ein Fehlercode zurückgegeben wird, der angibt, dass die Warteschlange leer ist.

Bevor Sie den [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Zeiger freigeben, brechen Sie die Ereignis Benachrichtigung ab, indem Sie [**setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) mit einem **null** -Zeiger aufrufen. Überprüfen Sie im Ereignis Verarbeitungs Code, ob der **imediaeventex** -Zeiger gültig ist, bevor Sie [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)aufrufen. Diese Schritte verhindern einen möglichen Fehler, bei dem die Anwendung die Ereignis Benachrichtigung empfängt, nachdem Sie den **imediaeventex** -Zeiger freigegeben hat.

**Ereignissignal**

Der Filter Graph-Manager speichert ein manuelles Zurücksetzungs Ereignis, das den Status der Ereignis Warteschlange widerspiegelt. Wenn die Warteschlange ausstehende Ereignis Benachrichtigungen enthält, signalisiert der Filter Graph-Manager das Ereignis für manuelles Zurücksetzen. Wenn die Warteschlange leer ist, wird das Ereignis durch einen Aufrufe der [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) -Methode zurückgesetzt. Eine Anwendung kann dieses Ereignis verwenden, um den Status der Warteschlange zu ermitteln.

> [!Note]  
> Die Terminologie kann hier verwirrend sein. Das Ereignis für manuelles Zurücksetzen ist der Typ des Ereignisses, das von der Windows-Funktion " [**kreateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) " erstellt wurde. Dies hat nichts mit den Ereignissen zu tun, die von DirectShow definiert werden.

 

Ruft die [**imediaevent:: geteventhandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) -Methode auf, um ein Handle für das manuelle Zurücksetzungs Ereignis zu erhalten. Warten Sie, bis das Ereignis signalisiert wird, indem Sie eine Funktion wie [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)aufrufen. Nachdem das Ereignis signalisiert wurde, wenden Sie [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) an, um das DirectShow-Ereignis abzurufen.

Das folgende Codebeispiel veranschaulicht diese Vorgehensweise. Er ruft das Ereignis Handle ab und wartet dann in Intervallen von 100 Millisekunden, bis das Ereignis signalisiert wird. Wenn das Ereignis signalisiert wird, ruft es **GetEvent** auf und druckt den Ereignis Code und die Ereignis Parameter im Konsolenfenster. Die Schleife wird beendet, wenn das [**EC \_ Complete**](ec-complete.md) -Ereignis auftritt, das angibt, dass die Wiedergabe abgeschlossen wurde.


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



Da das Filter Diagramm das Ereignis nach Bedarf automatisch festlegt oder zurücksetzt, sollte Ihre Anwendung dies nicht tun. Beim Freigeben des Filter Diagramms schließt das Filter Diagramm auch das Ereignis handle. verwenden Sie daher nach diesem Punkt nicht das Ereignis handle.

 

 
