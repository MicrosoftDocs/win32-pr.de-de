---
description: Learning Wenn ein Ereignis auftritt
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Learning Wenn ein Ereignis auftritt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58696055bdf1e3cbf3cf36c4db4ae2258bda334956fcaa14f33eda96db249773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397216"
---
# <a name="learning-when-an-event-occurs"></a>Learning Wenn ein Ereignis auftritt

Zum Verarbeiten von DirectShow-Ereignissen benötigt eine Anwendung eine Möglichkeit, um herauszufinden, wann Ereignisse in der Warteschlange warten. Der Filter Graph-Manager bietet zwei Möglichkeiten:

-   **Fensterbenachrichtigung:** Der Filter Graph Manager sendet eine benutzerdefinierte Windows an ein Anwendungsfenster, wenn ein neues Ereignis vor liegt.
-   **Ereignissignalisierung:** Der Filter Graph-Manager signalisiert ein Windows-Ereignis, wenn DirectShow-Ereignisse in der Warteschlange sind, und setzt das Ereignis zurück, wenn die Warteschlange leer ist.

Eine Anwendung kann beide Verfahren verwenden. Die Fensterbenachrichtigung ist in der Regel einfacher.

**Fensterbenachrichtigung**

Rufen Sie zum Einrichten der Fensterbenachrichtigung die [**IMediaEventEx::SetNotifyWindow-Methode**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) auf, und geben Sie eine private Nachricht an. Anwendungen können Nachrichtennummern im Bereich von WM APP bis 0xBFFF \_ als private Nachrichten verwenden. Wenn der Filter Graph Manager eine neue Ereignisbenachrichtigung in der Warteschlange platziert, wird diese Nachricht an das designierte Fenster gesendet. Die Anwendung antwortet innerhalb der Meldungsschleife des Fensters auf die Nachricht.

Das folgende Codebeispiel zeigt, wie das Benachrichtigungsfenster festgelegt wird.


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Die Nachricht ist eine normale Windows Nachricht und wird getrennt von der DirectShow-Ereignisbenachrichtigungswarteschlange veröffentlicht. Der Vorteil dieses Ansatzes ist, dass die meisten Anwendungen bereits eine Nachrichtenschleife implementieren. Aus diesem Grund können Sie die DirectShow-Ereignisbehandlung ohne viel zusätzliche Arbeit integrieren.

Das folgende Codebeispiel zeigt eine Gliederung der Reaktion auf die Benachrichtigungsnachricht. Ein vollständiges Beispiel finden Sie unter [Reagieren auf Ereignisse.](responding-to-events.md)


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



Da die Ereignisbenachrichtigung und die Nachrichtenschleife asynchron sind, kann die Warteschlange bis zu dem Zeitpunkt, zu dem Ihre Anwendung auf die Nachricht antwortet, mehr als ein Ereignis enthalten. Außerdem können Ereignisse manchmal aus der Warteschlange gelöscht werden, wenn sie ungültig werden. Rufen Sie daher in Ihrem Ereignisbehandlungscode [**IAMMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) auf, bis ein Fehlercode zurückgegeben wird, der angibt, dass die Warteschlange leer ist.

Bevor Sie den [**IMediaEventEx-Zeiger**](/windows/desktop/api/Control/nn-control-imediaeventex) veröffentlichen, brechen Sie die Ereignisbenachrichtigung ab, indem [**Sie SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) mit einem **NULL-Zeiger** aufrufen. Überprüfen Sie in Ihrem Ereignisverarbeitungscode, ob der **IMediaEventEx-Zeiger** gültig ist, bevor Sie [**GetEvent aufrufen.**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) Diese Schritte verhindern einen möglichen Fehler, bei dem die Anwendung die Ereignisbenachrichtigung empfängt, nachdem sie den **IMediaEventEx-Zeiger freigegeben** hat.

**Ereignissignal**

Der Filter Graph Manager behält ein Ereignis für die manuelle Zurücksetzung bei, das den Status der Ereigniswarteschlange widerspiegelt. Wenn die Warteschlange ausstehende Ereignisbenachrichtigungen enthält, signalisiert der Graph-Manager das Ereignis für die manuelle Zurücksetzung. Wenn die Warteschlange leer ist, setzt ein Aufruf der [**IMediaEvent::GetEvent-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) das Ereignis zurück. Eine Anwendung kann dieses Ereignis verwenden, um den Status der Warteschlange zu bestimmen.

> [!Note]  
> Die Terminologie kann hier verwirrend sein. Das Ereignis zum manuellen Zurücksetzen ist der Typ des Ereignisses, das von der [**CreateEvent Windows funktion erstellt**](/windows/win32/api/synchapi/nf-synchapi-createeventa) wird. sie hat nichts mit den ereignissen zu tun, die von DirectShow definiert werden.

 

Rufen Sie [**die IMediaEvent::GetEventHandle-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) auf, um ein Handle für das Manuelle Zurücksetzen-Ereignis zu erhalten. Warten Sie, bis das Ereignis signalisiert wird, indem Sie eine Funktion wie [**WaitForMultipleObjects aufrufen.**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects) Nachdem das Ereignis signalisiert wurde, rufen [**Sie IMediaEvent::GetEvent auf,**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) um das DirectShow-Ereignis zu erhalten.

Das folgende Codebeispiel veranschaulicht diese Vorgehensweise. Er ruft das Ereignishandle ab und wartet dann in Intervallen von 100 Millisekunden, bis das Ereignis signalisiert wird. Wenn das Ereignis signalisiert wird, ruft es **GetEvent auf** und gibt den Ereigniscode und die Ereignisparameter im Konsolenfenster aus. Die -Schleife wird beendet, wenn [**das EC \_ COMPLETE-Ereignis**](ec-complete.md) auftritt, was angibt, dass die Wiedergabe abgeschlossen wurde.


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



Da das Filterdiagramm das Ereignis bei Entsprechendkeit automatisch ein- oder zurückgesetzt, sollte Ihre Anwendung dies nicht tun. Wenn Sie das Filterdiagramm frei geben, schließt das Filterdiagramm auch das Ereignishand handle. Verwenden Sie daher nicht das Ereignishand handle nach diesem Punkt.

 

 
