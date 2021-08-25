---
title: Reagieren auf Mausklicks
description: Reagieren auf Mausklicks
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947b50726e79fbf29c4f013d4ac0a449c009c1817b74b1a8063e63a68c4dd6c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897210"
---
# <a name="responding-to-mouse-clicks"></a>Reagieren auf Mausklicks

Wenn der Benutzer auf eine Maustaste klickt, während sich der Cursor über dem Clientbereich eines Fensters befindet, empfängt das Fenster eine der folgenden Meldungen.



| Nachricht                                        | Bedeutung                   |
|------------------------------------------------|---------------------------|
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) | Linke Schaltfläche nach unten          |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)     | Linke Schaltfläche nach oben            |
| [**WM \_ MBUTTONDOWN**](/windows/desktop/inputdev/wm-mbuttondown) | Mittlere Schaltfläche nach unten        |
| [**WM \_ MBUTTONUP**](/windows/desktop/inputdev/wm-mbuttonup)     | Mittlere Schaltfläche nach oben          |
| [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown) | Schaltfläche "Rechts nach unten"         |
| [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)     | Rechte Schaltfläche nach oben           |
| [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) | XBUTTON1 oder XBUTTON2 nach unten |
| [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup)     | XBUTTON1 oder XBUTTON2 nach oben   |



 

Denken Sie daran, dass der Clientbereich der Teil des Fensters ist, der den Rahmen ausschließt. Weitere Informationen zu Clientbereichen finden Sie unter [Was ist ein Fenster?](what-is-a-window-.md)

### <a name="mouse-coordinates"></a>Mauskoordinaten

In all diesen Nachrichten enthält der *lParam-Parameter* die x- und y-Koordinaten des Mauszeigers. Die niedrigsten 16 Bits von *lParam* enthalten die x-Koordinate, und die nächsten 16 Bits enthalten die y-Koordinate. Verwenden Sie die [**Makros GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**GET \_ Y \_ LPARAM,**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) um die Koordinaten aus *lParam* zu entpacken.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Diese Makros werden in der Headerdatei WindowsX.h definiert.

Bei 64-Bit-Windows ist *lParam* ein 64-Bit-Wert. Die oberen 32 Bits von *lParam* werden nicht verwendet. In der MSDN-Dokumentation werden die Wörter "Wort mit niedriger Ordnung" und "Wort in hoher Reihenfolge" von *lParam* erwähnt. Im 64-Bit-Fall bedeutet dies die Wörter in niedriger und hoher Reihenfolge der unteren 32 Bits. Die Makros extrahieren die richtigen Werte. Wenn Sie sie also verwenden, sind Sie sicher.

Mauskoordinaten werden in Pixel und nicht in geräteunabhängigen Pixeln (DIPs) angegeben und relativ zum Clientbereich des Fensters gemessen. Koordinaten sind signierte Werte. Positionen oberhalb und links vom Clientbereich weisen negative Koordinaten auf. Dies ist wichtig, wenn Sie die Mausposition außerhalb des Fensters nachverfolgen. Dies erfahren Sie in einem späteren Thema, [Erfassen von Mausbewegungen außerhalb des Fensters.](mouse-movement.md)

### <a name="additional-flags"></a>Zusätzliche Flags

Der *wParam-Parameter* enthält ein bitweises **OR** von Flags, das den Zustand der anderen Maustasten sowie die UMSCHALT- und STRG-Taste angibt.



| Flag             | Bedeutung                          |
|------------------|----------------------------------|
| **\_MK-STEUERUNG**  | Die STRG-TASTE ist gedrückt.            |
| **MK \_ LBUTTON**  | Die linke Maustaste ist nach unten geschaltet.   |
| **MK \_ MBUTTON**  | Die mittlere Maustaste ist gedrückt. |
| **MK \_ RBUTTON**  | Die rechte Maustaste ist nach unten geschaltet.  |
| **MK \_ SHIFT**    | Die UMSCHALTTASTE ist nicht mehr gedrückt.           |
| **MK \_ XBUTTON1** | Die XBUTTON1-Schaltfläche ist ausgeschaltet.     |
| **MK \_ XBUTTON2** | Die XBUTTON2-Schaltfläche ist ausgeschaltet.     |



 

Das Fehlen eines Flags bedeutet, dass die entsprechende Schaltfläche oder Taste nicht gedrückt wurde. So testen Sie beispielsweise, ob die STRG-TASTE gedrückt ist:


```C++
if (wParam & MK_CONTROL) { ...
```



Wenn Sie den Zustand anderer Tasten neben STRG und UMSCHALT suchen müssen, verwenden Sie die [**GetKeyState-Funktion,**](/windows/desktop/api/winuser/nf-winuser-getkeystate) die unter [Tastatureingabe](keyboard-input.md)beschrieben wird.

Die Wm [**\_ XBUTTONDOWN-**](/windows/desktop/inputdev/wm-xbuttondown) und [**WM \_ XBUTTONUP-Fenstermeldungen**](/windows/desktop/inputdev/wm-xbuttonup) gelten sowohl für XBUTTON1 als auch für XBUTTON2. Der *wParam-Parameter* gibt an, auf welche Schaltfläche geklickt wurde.


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



## <a name="double-clicks"></a>Doppelklicken

Ein Fenster empfängt standardmäßig keine Doppelklickbenachrichtigungen. Um Doppelklicks zu erhalten, legen Sie das **CS \_ DBLCLKS-Flag** in der [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) fest, wenn Sie die Fensterklasse registrieren.


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



Wenn Sie das **CS \_ DBLCLKS-Flag** wie gezeigt festlegen, empfängt das Fenster Doppelklickbenachrichtigungen. Ein Doppelklick wird durch eine Fenstermeldung mit "DBLCLK" im Namen angezeigt. Ein Doppelklick auf die linke Maustaste erzeugt z. B. die folgende Sequenz von Nachrichten:

<dl>

[**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)  
[**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)  
[**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)  
[**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

Tatsächlich wird die zweite [**\_ WM-LBUTTONDOWN-Nachricht,**](/windows/desktop/inputdev/wm-lbuttondown) die normalerweise generiert wird, zu einer [**\_ WM-LBUTTONDBLCLK-Nachricht.**](/windows/desktop/inputdev/wm-lbuttondblclk) Äquivalente Nachrichten werden für rechte, mittlere und XBUTTON-Schaltflächen definiert.

Bis sie die Doppelklicknachricht erhalten, gibt es keine Möglichkeit, zu erkennen, dass der erste Mausklick der Anfang eines Doppelklicks ist. Daher sollte eine Doppelklickaktion eine Aktion fortsetzen, die mit dem ersten Mausklick beginnt. In der Windows Shell wählt beispielsweise ein einziger Klick einen Ordner aus, während ein Doppelklick den Ordner öffnet.

## <a name="non-client-mouse-messages"></a>Nicht-Client-Mausnachrichten

Für Mausereignisse, die im Nicht-Clientbereich des Fensters auftreten, wird ein separater Satz von Nachrichten definiert. Diese Nachrichten enthalten die Buchstaben "NC" im Namen. WM [**\_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) ist beispielsweise die Nicht-Cliententsprechung von [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown). Eine typische Anwendung fängt diese Nachrichten nicht ab, da die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) diese Nachrichten ordnungsgemäß verarbeitet. Sie können jedoch für bestimmte erweiterte Funktionen nützlich sein. Sie können diese Meldungen beispielsweise verwenden, um benutzerdefiniertes Verhalten in der Titelleiste zu implementieren. Wenn Sie diese Nachrichten verarbeiten, sollten Sie sie im Allgemeinen später an **DefWindowProc** übergeben. Andernfalls unterbricht Ihre Anwendung die Standardfunktionalität, z. B. das Ziehen oder Minimieren des Fensters.

## <a name="next"></a>Nächste

[Mausbewegung](mouse-movement.md)

 

 