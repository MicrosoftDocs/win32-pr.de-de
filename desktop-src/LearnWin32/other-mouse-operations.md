---
title: Verschiedene Mausvorgänge
description: In den vorherigen Abschnitten wurden Mausklicks und Mausbewegungen erläutert. Im Folgenden finden Sie einige weitere Vorgänge, die mit der Maus ausgeführt werden können.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31877ab5a71819fa896fd1253e7391f9ed748dffff636ab9d3e8591669b7fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387966"
---
# <a name="miscellaneous-mouse-operations"></a>Verschiedene Mausvorgänge

In den vorherigen Abschnitten wurden Mausklicks und Mausbewegungen erläutert. Im Folgenden finden Sie einige weitere Vorgänge, die mit der Maus ausgeführt werden können.

## <a name="dragging-ui-elements"></a>Ziehen von Benutzeroberflächenelementen

Wenn Die Benutzeroberfläche das Ziehen von UI-Elementen unterstützt, sollten Sie im Mauszeiger-Meldungshandler eine weitere Funktion aufrufen: [**DragDetect.**](/windows/desktop/api/winuser/nf-winuser-dragdetect) Die **DragDetect-Funktion** gibt **TRUE** zurück, wenn der Benutzer eine Mausbewegung initiiert, die als Ziehen interpretiert werden soll. Der folgende Code zeigt, wie diese Funktion verwendet wird.


```C++
    case WM_LBUTTONDOWN: 
        {
            POINT pt = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam) };
            if (DragDetect(m_hwnd, pt))
            {
                // Start dragging.
            }
        }
        return 0;
```



Dies ist die Idee: Wenn ein Programm Drag & Drop unterstützt, möchten Sie nicht, dass jeder Mausklick als Ziehpunkt interpretiert wird. Andernfalls kann der Benutzer versehentlich etwas ziehen, wenn er einfach darauf klicken wollte (z. B. um es auszuwählen). Wenn eine Maus jedoch besonders sensibel ist, kann es schwierig sein, die Maus während des Klickens perfekt zu halten. Daher definiert Windows einen Ziehschwellenwert von einigen Pixeln. Wenn der Benutzer die Maustaste drückt, wird dies nicht als Ziehpunkt betrachtet, es sei denn, die Maus überschreitet diesen Schwellenwert. Die [**DragDetect-Funktion**](/windows/desktop/api/winuser/nf-winuser-dragdetect) testet, ob dieser Schwellenwert erreicht wird. Wenn die Funktion **TRUE** zurückgibt, können Sie den Mausklick als Ziehpunkt interpretieren. Andernfalls nicht.

> [!Note]  
> Wenn [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) **FALSE** zurückgibt, unterdrückt Windows die [**\_ WM-LBUTTONUP-Meldung,**](/windows/desktop/inputdev/wm-lbuttonup) wenn der Benutzer die Maustaste freigibt. Rufen Sie daher **DragDetect** nicht auf, es sei denn, ihr Programm befindet sich derzeit in einem Modus, der ziehen unterstützt. (Wenn z. B. bereits ein dragable UI-Element ausgewählt ist.) Am Ende dieses Moduls sehen wir ein längeres Codebeispiel, das die **DragDetect-Funktion** verwendet.

 

## <a name="confining-the-cursor"></a>Einbeigen des Cursors

Manchmal möchten Sie den Cursor auf den Clientbereich oder einen Teil des Clientbereichs beschränken. Die [**ClipCursor-Funktion**](/windows/desktop/api/winuser/nf-winuser-clipcursor) schränkt die Bewegung des Cursors auf ein angegebenes Rechteck ein. Dieses Rechteck wird in Bildschirmkoordinaten und nicht in Clientkoordinaten angegeben, sodass der Punkt (0, 0) die obere linke Ecke des Bildschirms bedeutet. Um Clientkoordinaten in Bildschirmkoordinaten zu übersetzen, rufen Sie die Funktion [**ClientToScreen auf.**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen)

Der folgende Code beschränkt den Cursor auf den Clientbereich des Fensters.


```C++
    // Get the window client area.
    RECT rc;
    GetClientRect(m_hwnd, &rc);

    // Convert the client area to screen coordinates.
    POINT pt = { rc.left, rc.top };
    POINT pt2 = { rc.right, rc.bottom };
    ClientToScreen(m_hwnd, &pt);
    ClientToScreen(m_hwnd, &pt2);
    SetRect(&rc, pt.x, pt.y, pt2.x, pt2.y);

    // Confine the cursor.
    ClipCursor(&rc);
```



[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) übernimmt eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) [**aber ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) eine [**POINT-Struktur.**](/previous-versions//dd162805(v=vs.85)) Ein Rechteck wird durch die Punkte oben links und unten rechts definiert. Sie können den Cursor auf einen beliebigen rechteckigen Bereich beschränken, einschließlich Bereichen außerhalb des Fensters, aber das Beschränken des Cursors auf den Clientbereich ist eine typische Möglichkeit, die Funktion zu verwenden. Das Wiederherstellen des Cursors in einen Bereich außerhalb Ihres Fensters wäre ungewöhnlich, und Benutzer würden ihn wahrscheinlich als Fehler merken.

Um die Einschränkung zu entfernen, rufen [**Sie ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) mit dem Wert **NULL** auf.


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a>Mausnachverfolgungsereignisse: Zeigen und Verlassen

Zwei andere Mausnachrichten sind standardmäßig deaktiviert, können aber für einige Anwendungen nützlich sein:

-   [**WM \_ MOUSEHOVER:**](/windows/desktop/inputdev/wm-mousehover)Der Cursor hat über einen festen Zeitraum auf den Clientbereich zeigen können.
-   [**WM \_ MOUSELEAVE:**](/windows/desktop/inputdev/wm-mouseleave)Der Cursor hat den Clientbereich verlassen.

Um diese Nachrichten zu aktivieren, rufen Sie die [**TrackMouseEvent-Funktion**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) auf.


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



Die [**TRACKMOUSEEVENT-Struktur**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) enthält die Parameter für die Funktion. Der **dwFlags-Member** der -Struktur enthält Bitflags, die angeben, an welchen Nachverfolgungsmeldungen Sie interessiert sind. Sie können sowohl [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) als auch [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave)abrufen, wie hier gezeigt, oder nur eine der beiden. Der **dwHoverTime-Member** gibt an, wie lange die Maus zeigen muss, bevor das System eine Hovermeldung generiert. Dieser Wert wird in Millisekunden angegeben. Die Konstante **HOVER \_ DEFAULT** bedeutet, dass die Systemstandardeinstellung verwendet wird.

Nachdem Sie eine der angeforderten Nachrichten erhalten haben, wird die [**TrackMouseEvent-Funktion**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) zurückgesetzt. Sie müssen sie erneut aufrufen, um eine weitere Nachverfolgungsmeldung zu erhalten. Sie sollten jedoch warten, bis die nächste Mauszeigermeldung angezeigt wird, bevor **Sie TrackMouseEvent** erneut aufrufen. Andernfalls wird Ihr Fenster möglicherweise mit Nachverfolgungsmeldungen überflutet. Wenn die Maus z. B. mit dem Mauszeiger darauf zeigen würde, würde das System weiterhin einen Stream von [**WM \_ MOUSEHOVER-Nachrichten**](/windows/desktop/inputdev/wm-mousehover) generieren, während die Maus stationär ist. Sie möchten eigentlich keine weitere **WM \_ MOUSEHOVER-Nachricht,** bis die Maus an eine andere Stelle bewegt und wieder bewegt wird.

Hier ist eine kleine Hilfsklasse, mit der Sie Mausnachverfolgungsereignisse verwalten können.


```C++
class MouseTrackEvents
{
    bool m_bMouseTracking;

public:
    MouseTrackEvents() : m_bMouseTracking(false)
    {
    }
    
    void OnMouseMove(HWND hwnd)
    {
        if (!m_bMouseTracking)
        {
            // Enable mouse tracking.
            TRACKMOUSEEVENT tme;
            tme.cbSize = sizeof(tme);
            tme.hwndTrack = hwnd;
            tme.dwFlags = TME_HOVER | TME_LEAVE;
            tme.dwHoverTime = HOVER_DEFAULT;
            TrackMouseEvent(&tme);
            m_bMouseTracking = true;
        }
    }
    void Reset(HWND hwnd)
    {
        m_bMouseTracking = false;
    }
};
```



Das nächste Beispiel zeigt, wie Sie diese Klasse in Ihrer Fensterprozedur verwenden.


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_MOUSEMOVE:
        mouseTrack.OnMouseMove(m_hwnd);  // Start tracking.

        // TODO: Handle the mouse-move message.

        return 0;

    case WM_MOUSELEAVE:

        // TODO: Handle the mouse-leave message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    case WM_MOUSEHOVER:

        // TODO: Handle the mouse-hover message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



Mausverfolgungsereignisse erfordern eine zusätzliche Verarbeitung durch das System. Lassen Sie sie daher deaktiviert, wenn Sie sie nicht benötigen.

Aus Gründen der Vollständigkeit finden Sie hier eine Funktion, die das System nach dem Standardmäßigen Timeout für das Hovern abfragt.


```C++
UINT GetMouseHoverTime()
{
    UINT msec; 
    if (SystemParametersInfo(SPI_GETMOUSEHOVERTIME, 0, &msec, 0))
    {   
        return msec;
    }
    else
    {
        return 0;
    }
}
```



## <a name="mouse-wheel"></a>Mausrad

Die folgende Funktion überprüft, ob ein Mausrad vorhanden ist.


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



Wenn der Benutzer das Mausrad dreht, erhält das Fenster mit dem Fokus eine [**WM \_ MOUSEWHEEL-Meldung.**](/windows/desktop/inputdev/wm-mousewheel) Der *wParam-Parameter* dieser Nachricht enthält einen ganzzahligen Wert namens *Delta,* der misst, wie weit das Rad gedreht wurde. Das Delta verwendet beliebige Einheiten, wobei 120 Einheiten als Drehung definiert sind, die erforderlich ist, um eine "Aktion" auszuführen. Natürlich hängt die Definition einer Aktion von Ihrem Programm ab. Wenn z. B. das Mausrad zum Scrollen von Text verwendet wird, führt jede 120 Drehungseinheit einen Bildlauf um eine Textzeile aus.

Das Vorzeichen des Deltas gibt die Drehrichtung an:

-   Positiv: Drehen Sie vorwärts, weg vom Benutzer.
-   Negativ: Drehen Sie rückwärts in Richtung des Benutzers.

Der Wert des Deltas wird zusammen mit einigen zusätzlichen Flags in *wParam* platziert. Verwenden Sie das [**GET \_ WHEEL DELTA \_ \_ WPARAM-Makro,**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) um den Wert des Deltas abzurufen.


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Wenn das Mausrad eine hohe Auflösung auf hat, kann der absolute Wert des Deltas kleiner als 120 sein. Wenn es in diesem Fall sinnvoll ist, dass die Aktion in kleineren Schritten ausgeführt wird, können Sie dies tun. Beispielsweise kann Text in Schritten von weniger als einer Zeile scrollen. Andernfalls akkumulieren Sie das gesamte Delta, bis das Rad so lange gedreht wird, um die Aktion auszuführen. Store das nicht verwendete Delta in einer Variablen, und wenn sich 120 Einheiten ansammeln (entweder positiv oder negativ), führen Sie die Aktion aus.

## <a name="next"></a>Nächste

[Tastatureingaben](keyboard-input.md)

 

 