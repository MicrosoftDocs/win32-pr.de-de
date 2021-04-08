---
title: Antworten auf Mausklicks
description: Antworten auf Mausklicks
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101619"
---
# <a name="responding-to-mouse-clicks"></a>Antworten auf Mausklicks

Wenn der Benutzer auf eine Maustaste klickt, während sich der Cursor über dem Client Bereich eines Fensters befindet, empfängt das Fenster eine der folgenden Meldungen.



| Nachricht                                        | Bedeutung                   |
|------------------------------------------------|---------------------------|
| [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) | Linke Schaltfläche nach unten          |
| [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup)     | Linke Schaltfläche nach oben            |
| [**WM- \_ mbuttondown**](/windows/desktop/inputdev/wm-mbuttondown) | Mittlere Schaltfläche nach unten        |
| [**WM- \_ mbuttonup**](/windows/desktop/inputdev/wm-mbuttonup)     | Mittlere Schaltfläche nach oben          |
| [**WM- \_ rbuttondown**](/windows/desktop/inputdev/wm-rbuttondown) | Nach-rechts-Taste         |
| [**WM- \_ rbuttonup**](/windows/desktop/inputdev/wm-rbuttonup)     | Rechter Schaltfläche nach oben           |
| [**WM- \_ xbuttondown**](/windows/desktop/inputdev/wm-xbuttondown) | XButton1 oder XButton2 Down |
| [**WM- \_ xbuttonup**](/windows/desktop/inputdev/wm-xbuttonup)     | XButton1 oder XButton2 up   |



 

Beachten Sie, dass der Client Bereich der Teil des Fensters ist, in dem der Frame ausgeschlossen ist. Weitere Informationen zu Client Bereichen finden Sie unter [Was ist ein Fenster?](what-is-a-window-.md)

### <a name="mouse-coordinates"></a>Maus Koordinaten

In allen diesen Nachrichten enthält der *LPARAM* -Parameter die x-und y-Koordinaten des Mauszeigers. Die niedrigsten 16 Bits von *LPARAM* enthalten die x-Koordinate, und die nächsten 16 Bits enthalten die y-Koordinate. Verwenden Sie die lParam-Makros [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) , um die Koordinaten aus *LPARAM* zu entpacken.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Diese Makros sind in der Header Datei WINDOWSX. h definiert.

Bei 64-Bit-Fenstern ist *LPARAM* 64-Bit-Wert. Die oberen 32 Bits von *LPARAM* werden nicht verwendet. In der MSDN-Dokumentation werden das "nieder wertige Wort" und "High-Order Word" von *LPARAM* erwähnt. Im 64-Bit-Fall bedeutet dies, dass das niedrige und das hochwertige Wort der unteren 32 Bits ist. Die Makros extrahieren die richtigen Werte, sodass Sie sicher sind, wenn Sie Sie verwenden.

Maus Koordinaten werden in Pixel angegeben, nicht in geräteunabhängigen Pixeln (Dips) und werden relativ zum Client Bereich des Fensters gemessen. Koordinaten sind signierte Werte. Positionen oberhalb und Links vom Client Bereich haben negative Koordinaten, was wichtig ist, wenn Sie die Mausposition außerhalb des Fensters verfolgen. Dies wird in einem späteren Thema erläutert, wobei [die Mausbewegung außerhalb des Fensters erfasst](mouse-movement.md)wird.

### <a name="additional-flags"></a>Zusätzliche Flags

Der *wParam* -Parameter enthält ein bitweises **or** von-Flags, das den Zustand der anderen Maustasten sowie die UMSCHALTTASTE und die STRG-Taste angibt.



| Flag             | Bedeutung                          |
|------------------|----------------------------------|
| **MK- \_ Steuerelement**  | Die STRG-Taste ist nicht gedrückt.            |
| **MK \_ lbutton**  | Die linke Maustaste ist nicht mehr vorhanden.   |
| **MK- \_ MButton**  | Die mittlere Maustaste ist nicht mehr angezeigt. |
| **MK \_ rbutton**  | Die Rechte Maustaste ist nicht mehr angezeigt.  |
| **MK \_ UMSCHALT**    | Die UMSCHALTTASTE ist nicht mehr festgelegt.           |
| **MK \_ XButton1** | Die Schaltfläche XButton1 ist nicht angezeigt.     |
| **MK \_ XButton2** | Die Schaltfläche XButton2 ist nicht angezeigt.     |



 

Das Fehlen eines Flags bedeutet, dass die entsprechende Schaltfläche oder der entsprechende Schlüssel nicht gedrückt wurde. So können Sie beispielsweise testen, ob die STRG-Taste gedrückt ist:


```C++
if (wParam & MK_CONTROL) { ...
```



Wenn Sie neben STRG und UMSCHALT den Zustand anderer Schlüssel ermitteln müssen, verwenden Sie die [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) -Funktion, die in [Tastatureingaben](keyboard-input.md)beschrieben wird.

Die Nachrichten " [**WM \_ xbuttondown**](/windows/desktop/inputdev/wm-xbuttondown) " und " [**WM \_ xbuttonup" werden**](/windows/desktop/inputdev/wm-xbuttonup) sowohl auf XButton1 als auch auf XButton2 angewendet. Der *wParam* -Parameter gibt an, auf welche Schaltfläche geklickt wurde.


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a>Doppelte Klicks

Ein Fenster erhält standardmäßig keine Doppelklick-Benachrichtigungen. Um doppelte Klicks zu erhalten, legen Sie das **CS \_ dblclert** -Flag in der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur fest, wenn Sie die Fenster Klasse registrieren.


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



Wenn Sie das Flag **CS \_ dblclcs** wie gezeigt festlegen, empfängt das Fenster Doppelklick-Benachrichtigungen. Ein Doppelklick wird durch eine Fenster Meldung mit dem Namen "dblclk" angezeigt. Ein Doppelklick mit der linken Maustaste erzeugt beispielsweise die folgende Sequenz von Meldungen:

<dl>

[**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown)  
[**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup)  
[**WM \_ lbuttondblclk**](/windows/desktop/inputdev/wm-lbuttondblclk)  
[**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

Tatsächlich wird die zweite [**WM- \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Meldung, die normalerweise generiert wird, zu einer [**WM \_ lbuttondblclk**](/windows/desktop/inputdev/wm-lbuttondblclk) -Nachricht. Äquivalente Nachrichten werden für die Schaltflächen right, Middle und XButton definiert.

Bis Sie die Doppelklick Nachricht erhalten haben, gibt es keine Möglichkeit, zu erkennen, dass der erste Mausklick den Anfang eines Doppelklicks enthält. Aus diesem Grund sollte eine Doppelklick Aktion eine Aktion fortsetzen, die mit dem ersten Mausklick beginnt. Beispielsweise wird in der Windows-Shell mit einem einzigen Klick ein Ordner ausgewählt, während mit einem Doppelklick der Ordner geöffnet wird.

## <a name="non-client-mouse-messages"></a>Nicht-Client-Maus Meldungen

Für Mausereignisse, die im nicht-Client Bereich des Fensters auftreten, wird ein separater Satz von Meldungen definiert. Diese Nachrichten enthalten den Buchstaben "NC" im Namen. Beispielsweise ist [**WM \_ nclbuttondown**](/windows/desktop/inputdev/wm-nclbuttondown) die nicht-Client-Entsprechung von [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown). Diese Nachrichten werden von einer typischen Anwendung nicht abgefangen, da diese Nachrichten von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion ordnungsgemäß verarbeitet werden. Allerdings können Sie für bestimmte erweiterte Funktionen nützlich sein. Beispielsweise können Sie diese Nachrichten verwenden, um ein benutzerdefiniertes Verhalten in der Titelleiste zu implementieren. Wenn Sie diese Nachrichten verarbeiten, sollten Sie Sie in der Regel an **defwindowproc** weiterleiten. Andernfalls werden von der Anwendung Standardfunktionen wie z. b. ziehen oder Minimieren des Fensters unterbricht.

## <a name="next"></a>Nächste

[Mausbewegung](mouse-movement.md)

 

 