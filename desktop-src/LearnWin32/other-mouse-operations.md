---
title: Verschiedene Maus Vorgänge
description: In den vorherigen Abschnitten wurden Mausklicks und Mausbewegung erläutert. Im folgenden finden Sie einige andere Vorgänge, die mit der Maus ausgeführt werden können.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfba63dce8116d79a557cbbbf8895f17d2a8f1b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315068"
---
# <a name="miscellaneous-mouse-operations"></a>Verschiedene Maus Vorgänge

In den vorherigen Abschnitten wurden Mausklicks und Mausbewegung erläutert. Im folgenden finden Sie einige andere Vorgänge, die mit der Maus ausgeführt werden können.

## <a name="dragging-ui-elements"></a>Ziehen von UI-Elementen

Wenn Ihre Benutzeroberfläche das Ziehen von UI-Elementen unterstützt, gibt es eine andere Funktion, die Sie in Ihrem MouseDown-Meldungs Handler aufzurufen: [**dragdetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect). Die **dragdetect** -Funktion gibt **true** zurück, wenn der Benutzer eine Mausbewegung initiiert, die als Drag & amp; Drop interpretiert werden soll. Der folgende Code zeigt, wie Sie diese Funktion verwenden.


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



Hier ist die Idee: Wenn ein Programm Drag & Drop unterstützt, möchten Sie nicht, dass alle Mausklicks als Drag & amp; Drop interpretiert werden. Andernfalls kann der Benutzer versehentlich etwas ziehen, wenn er einfach darauf klickt (z. b. um ihn auszuwählen). Wenn eine Maus jedoch besonders empfindlich ist, kann es schwierig sein, die Maus beim Klicken immer noch perfekt zu halten. Daher definiert Windows einen Zieh Schwellenwert von einigen Pixeln. Wenn der Benutzer die Maustaste drückt, wird er nicht als Drag-Vorgang betrachtet, es sei denn, der Mauszeiger überschreitet diesen Schwellenwert. Die [**dragdetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) -Funktion testet, ob dieser Schwellenwert erreicht ist. Wenn die Funktion **true** zurückgibt, können Sie den Mauszeiger als Drag & amp; Drop interpretieren. Andernfalls ist dies nicht der Fall.

> [!Note]  
> Wenn [**dragdetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) **false** zurückgibt, unterdrückt Windows die [**WM \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldung, wenn der Benutzer die Maustaste loslässt. Verwenden Sie daher nicht **dragdetect** , es sei denn, Ihr Programm befindet sich derzeit in einem Modus, der das Ziehen unterstützt. (Z. b. Wenn ein Draggable-Element bereits ausgewählt ist.) Am Ende dieses Moduls wird ein längeres Codebeispiel angezeigt, in dem die **dragdetect** -Funktion verwendet wird.

 

## <a name="confining-the-cursor"></a>Einschränken des Cursors

Manchmal möchten Sie möglicherweise den Cursor auf den Client Bereich oder einen Teil des Client Bereichs einschränken. Die [**clipcursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) -Funktion schränkt die Bewegung des Cursors auf ein angegebenes Rechteck ein. Dieses Rechteck wird anstelle von Client Koordinaten in Bildschirm Koordinaten angegeben, sodass der Punkt (0,0) die obere linke Ecke des Bildschirms bedeutet. Wenn Sie Client Koordinaten in Bildschirm Koordinaten übersetzen möchten, müssen Sie die Funktion [**clientumscreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen)aufzurufen.

Der folgende Code schränkt den Cursor auf den Client Bereich des Fensters ein.


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



[**Clipcursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) nimmt eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, aber [**clientchanscreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) übernimmt eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur. Ein Rechteck wird durch seine oberen linken und unteren rechten Punkte definiert. Sie können den Cursor auf einen beliebigen rechteckigen Bereich beschränken, einschließlich Bereiche außerhalb des Fensters, aber das Einschränken des Cursors auf den Client Bereich ist eine typische Methode zur Verwendung der Funktion. Die Beschränkung des Cursors auf eine Region außerhalb des Fensters wäre ungewöhnlich, und Benutzer würden Sie wahrscheinlich als Fehler betrachten.

Um die Einschränkung zu entfernen, wenden Sie [**clipcursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) mit dem Wert **null** an.


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a>Maus Verfolgungs Ereignisse: hover und Leave

Zwei andere Maus Meldungen sind standardmäßig deaktiviert, können aber für einige Anwendungen nützlich sein:

-   [**WM \_ MouseHover**](/windows/desktop/inputdev/wm-mousehover): der Cursor befindet sich für einen bestimmten Zeitraum über den Client Bereich.
-   [**WM \_ MouseLeave**](/windows/desktop/inputdev/wm-mouseleave): der Cursor hat den Client Bereich verlassen.

Um diese Nachrichten zu aktivieren, müssen Sie die [**trackmousevent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) -Funktion aufrufen.


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



Die [**trackmousevent**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) -Struktur enthält die Parameter für die Funktion. Der **dwFlags** -Member der-Struktur enthält Bitflags, die angeben, an welchen nach Verfolgungs Meldungen Sie interessiert sind. Sie können sowohl [**WM \_ moust Hover**](/windows/desktop/inputdev/wm-mousehover) als auch [**WM \_ MouseLeave**](/windows/desktop/inputdev/wm-mouseleave)erhalten, wie hier gezeigt, oder nur eine der beiden Optionen. Der **dwhovertime** -Member gibt an, wie lange der Mauszeiger bewegen muss, bevor das System eine Hover-Nachricht generiert. Dieser Wert wird in Millisekunden angegeben. Der **\_ Standard** Wert der Konstanten Hover bedeutet, dass die Standardeinstellung des Systems verwendet wird

Nachdem Sie eine der angeforderten Nachrichten erhalten haben, setzt die [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) -Funktion zurück. Sie müssen ihn erneut abrufen, um eine weitere nach Verfolgungs Meldung zu erhalten. Sie sollten jedoch bis zur nächsten Mausbewegung warten, bevor Sie **TrackMouseEvent** erneut aufrufen. Andernfalls wird das Fenster möglicherweise mit nach Verfolgungs Meldungen überflutet. Wenn der Mauszeiger z. b. mit der Maus bewegt wird, generiert das System weiterhin einen Stream von [**WM- \_ MouseHover**](/windows/desktop/inputdev/wm-mousehover) -Nachrichten, während die Maus stationär ist. Sie möchten keine weitere **WM- \_ MouseHover** -Nachricht, bis der Mauszeiger an eine andere Stelle bewegt wird, und dann erneut darauf zeigen.

Hier ist eine kleine Hilfsklasse, die Sie zum Verwalten von Maus Verfolgungs Ereignissen verwenden können.


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



Im nächsten Beispiel wird gezeigt, wie Sie diese Klasse in der Fenster Prozedur verwenden.


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



Maus Verfolgungs Ereignisse erfordern eine zusätzliche Verarbeitung durch das System, sodass Sie deaktiviert bleiben, wenn Sie Sie nicht benötigen.

Aus Gründen der Vollständigkeit ist hier eine Funktion, die das System auf das standardmäßige Hover-Timeout abfragt.


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



Wenn der Benutzer das Mausrad dreht, empfängt das Fenster mit dem Fokus eine [**WM- \_ MouseWheel**](/windows/desktop/inputdev/wm-mousewheel) -Nachricht. Der *wParam* -Parameter dieser Nachricht enthält einen ganzzahligen Wert, der als *Delta* bezeichnet wird und misst, wie weit das Rad gedreht wurde. Das Delta verwendet beliebige Einheiten, wobei 120 Einheiten als Drehung definiert werden, die zum Ausführen einer Aktion erforderlich ist. Die Definition einer Aktion hängt natürlich von Ihrem Programm ab. Wenn das Mausrad z. b. zum Scrollen von Text verwendet wird, werden die einzelnen 120 Einheiten der Drehung in einer Textzeile angezeigt.

Das Vorzeichen des Deltas gibt die Richtung der Drehung an:

-   Positiv: Drehen Sie vorwärts, vom Benutzer entfernt.
-   Negativ: Drehen Sie rückwärts zu dem Benutzer.

Der Wert des Deltas wird zusammen mit einigen zusätzlichen Flags in *wParam* platziert. Verwenden Sie das [**get \_ Wheel \_ Delta \_ wParam**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) -Makro, um den Wert des Deltas zu erhalten.


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Wenn das Mausrad eine hohe Auflösung aufweist, kann der absolute Wert des Deltas kleiner als 120 sein. Wenn es in diesem Fall sinnvoll ist, die Aktion in kleineren Schritten durchzuführen, können Sie dies tun. Beispielsweise kann Text durch Inkremente von weniger als einer Zeile scrollen. Akkumulieren Sie andernfalls das gesamte Delta, bis das Rad genug dreht, um die Aktion auszuführen. Speichern Sie das nicht verwendete Delta in einer Variablen, und führen Sie die Aktion aus, wenn 120 Einheiten akkumuliert werden (entweder positiv oder negativ).

## <a name="next"></a>Nächste

[Tastatureingabe](keyboard-input.md)

 

 