---
title: Informationen zur Mauseingabe
description: In diesem Thema wird die Mauseingabe erläutert.
ms.assetid: 1f945a31-76d5-4e23-a55a-769ca114dbe9
keywords:
- Benutzereingabe, Mauseingabe
- Erfassen von Benutzereingaben, Mauseingaben
- Mauseingabe
- Mauszeiger
- Cursor, Mauseingabe
- Mauserfassung
- Mouse ClickLock
- XBUTTONs
- Mauskonfiguration
- Mausnachrichten
- WM_NCHITTEST Meldung
- Mouse Vanish-Barrierefreiheitsfeature
- Barrierefreiheitsfeature für Maus-Sonar
- Mausrad
- WM_MOUSEWHEEL Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c4978babd6322102908699dbf88b68e2d3b92f57fa9bfa79b9b8c3eae88931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105789"
---
# <a name="about-mouse-input"></a>Informationen zur Mauseingabe

Die Maus ist ein wichtiges, aber optionales Benutzereingabegerät für Anwendungen. Eine gut geschriebene Anwendung sollte eine Mausschnittstelle enthalten, aber sie sollte nicht ausschließlich von der Maus abhängen, um Benutzereingaben zu erhalten. Die Anwendung sollte auch vollständige Tastaturunterstützung bieten.

Eine Anwendung empfängt Mauseingaben in Form von Nachrichten, die an ihre Fenster gesendet oder gesendet werden.

Dieser Abschnitt enthält die folgenden Themen:

-   [Mauscursor](#mouse-cursor)
-   [Mausaufzeichnung](#mouse-capture)
-   [Mouse ClickLock](#mouse-clicklock)
-   [Mauskonfiguration](#mouse-configuration)
-   [XBUTTONs](#xbuttons)
-   [Mausnachrichten](#mouse-messages)
    -   [Clientbereichs-Mausmeldungen](#client-area-mouse-messages)
    -   [Nichtclientbereichs-Mausmeldungen](#nonclient-area-mouse-messages)
    -   [\_Wm-NCHITTEST-Nachricht](/windows)
-   [Mouse Sonar](#mouse-sonar)
-   [Mouse Vanish](#mouse-vanish)
-   [Das Mausrad](#the-mouse-wheel)
-   [Fensteraktivierung](#window-activation)

## <a name="mouse-cursor"></a>Mauscursor

Wenn der Benutzer die Maus bewegt, verschiebt das System eine Bitmap auf dem Bildschirm, die als *Mauscursor* bezeichnet wird. Der Mauscursor enthält einen Punkt mit einem Pixel, der als *Hotspots* bezeichnet wird. Dies ist ein Punkt, den das System verfolgt und als Position des Cursors erkennt. Wenn ein Mausereignis auftritt, empfängt das Fenster, das den Hotspots enthält, in der Regel die Mausnachricht, die sich aus dem Ereignis ergibt. Das Fenster muss nicht aktiv sein oder den Tastaturfokus haben, um eine Mausnachricht zu empfangen.

Das System verwaltet eine Variable, die die Mausgeschwindigkeit steuert, d. h. den Abstand, den der Cursor bewegt, wenn der Benutzer die Maus bewegt. Sie können die [**SystemParametersInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) mit dem **SPI \_ GETMOUSE-** oder **SPI \_ SETMOUSE-Flag** verwenden, um die Mausgeschwindigkeit abzurufen oder festzulegen. Weitere Informationen zu Mauscursorn finden Sie unter [Cursor.](/windows/desktop/menurc/cursors)

## <a name="mouse-capture"></a>Mausaufzeichnung

Das System sendet in der Regel eine Mausnachricht an das Fenster, das den Cursor-Hot Spot enthält, wenn ein Mausereignis auftritt. Eine Anwendung kann dieses Verhalten ändern, indem sie die [**SetCapture-Funktion**](/windows/win32/api/winuser/nf-winuser-setcapture) verwendet, um Mausnachrichten an ein bestimmtes Fenster weiterzuleiten. Das Fenster empfängt alle Mausmeldungen, bis die Anwendung die [**ReleaseCapture-Funktion**](/windows/win32/api/winuser/nf-winuser-releasecapture) aufruft oder ein anderes Erfassungsfenster angibt oder bis der Benutzer auf ein von einem anderen Thread erstelltes Fenster klickt.

Wenn sich die Mauserfassung ändert, sendet das System eine [**WM \_ CAPTURECHANGED-Meldung**](wm-capturechanged.md) an das Fenster, in dem die Mauserfassung verloren geht. Der *lParam-Parameter* der Nachricht gibt ein Handle für das Fenster an, das die Mausaufnahme erhält.

Nur das Vordergrundfenster kann Mauseingaben erfassen. Wenn ein Hintergrundfenster versucht, Mauseingaben zu erfassen, empfängt es Meldungen nur für Mausereignisse, die auftreten, wenn sich der Cursor-Hot spot innerhalb des sichtbaren Teils des Fensters befindet.

Das Erfassen von Mauseingaben ist nützlich, wenn ein Fenster alle Mauseingaben empfangen muss, auch wenn der Cursor sich außerhalb des Fensters bewegt. Eine Anwendung verfolgt z. B. in der Regel die Cursorposition nach einem Ereignis mit der Maustaste nach unten und folgt dem Cursor, bis ein Mouse Button Up-Ereignis auftritt. Wenn eine Anwendung keine Mauseingabe erfasst hat und der Benutzer die Maustaste außerhalb des Fensters freigibt, empfängt das Fenster die Schaltflächen-up-Meldung nicht.

Ein Thread kann die [**GetCapture-Funktion**](/windows/win32/api/winuser/nf-winuser-getcapture) verwenden, um zu bestimmen, ob eines seiner Fenster die Maus erfasst hat. Wenn eines der Threadfenster die Maus erfasst hat, ruft **GetCapture** ein Handle für das Fenster ab.

## <a name="mouse-clicklock"></a>Mouse ClickLock

Die Barrierefreiheitsfunktion Mouse ClickLock ermöglicht es einem Benutzer, die primäre Maustaste nach einem einzigen Klick zu sperren. Für eine Anwendung scheint die Schaltfläche weiterhin gedrückt zu sein. Um die Schaltfläche zu entsperren, kann eine Anwendung eine beliebige Mausnachricht senden, oder der Benutzer kann auf eine beliebige Maustaste klicken. Mit diesem Feature können Benutzer komplexere Mauskombinationen einfacher durchführen. Beispielsweise können Personen mit bestimmten physischen Einschränkungen Text hervorheben, Objekte ziehen oder Menüs einfacher öffnen. Weitere Informationen finden Sie unter den folgenden Flags und den Hinweisen in [**SystemParametersInfo:**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)

-   **SPI \_ GETMOUSECLICKLOCK**
-   **SPI \_ SETMOUSECLICKLOCK**
-   **SPI \_ GETMOUSECLICKLOCKTIME**
-   **SPI \_ SETMOUSECLICKLOCKTIME**

## <a name="mouse-configuration"></a>Mauskonfiguration

Obwohl die Maus ein wichtiges Eingabegerät für Anwendungen ist, verfügt nicht jeder Benutzer notwendigerweise über eine Maus. Eine Anwendung kann bestimmen, ob das System eine Maus enthält, indem der **SM \_ MOUSEPRESENT-Wert** an die [**GetSystemMetrics-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) übergeben wird.

Windows unterstützt eine Maus mit bis zu drei Schaltflächen. Mit einer Maus mit drei Tasten werden die Schaltflächen als linke, mittlere und rechte Schaltflächen festgelegt. Nachrichten und benannte Konstanten im Zusammenhang mit den Maustasten verwenden die Buchstaben L, M und R, um die Schaltflächen zu identifizieren. Die Schaltfläche mit einer einzelnen Maustaste wird als linke Schaltfläche betrachtet. Obwohl Windows eine Maus mit mehreren Schaltflächen unterstützt, verwenden die meisten Anwendungen die linke Schaltfläche in erster Linie und die anderen minimal, wenn überhaupt.

Anwendungen können auch ein Mausrad unterstützen. Das Mausrad kann gedrückt oder gedreht werden. Wenn das Mausrad gedrückt wird, fungiert es als mittlere (dritte) Schaltfläche und sendet normale Nachrichten der mittleren Schaltfläche an Ihre Anwendung. Wenn sie gedreht wird, wird eine Wheelnachricht an Ihre Anwendung gesendet. Weitere Informationen finden Sie im Abschnitt [Das Mausrad.](#the-mouse-wheel)

Anwendungen können Anwendungsbefehlsschaltflächen unterstützen. Diese Schaltflächen, die als X-Schaltflächen bezeichnet werden, sind so konzipiert, dass sie den Zugriff auf einen Internetbrowser, E-Mail- und Mediendienste vereinfachen. Wenn eine X-Schaltfläche gedrückt wird, wird eine [**\_ WM-APPCOMMAND-Nachricht**](wm-appcommand.md) an Ihre Anwendung gesendet. Weitere Informationen finden Sie in der Beschreibung in der **WM \_ APPCOMMAND-Meldung.**

Eine Anwendung kann die Anzahl der Schaltflächen auf der Maus ermitteln, indem sie den **SM \_ CMOUSEBUTTONS-Wert** an die [**GetSystemMetrics-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) übergibt. Um die Maus für einen linkshändigen Benutzer zu konfigurieren, kann die Anwendung die [**SwapMouseButton-Funktion**](/windows/win32/api/winuser/nf-winuser-swapmousebutton) verwenden, um die Bedeutung der linken und rechten Maustasten umzukehren. Die Übergabe des **SPI \_ SETMOUSEBUTTONSWAP-Werts** an die [**SystemParametersInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) ist eine weitere Möglichkeit, die Bedeutung der Schaltflächen umzukehren. Beachten Sie jedoch, dass die Maus eine freigegebene Ressource ist, sodass sich die Umkehrung der Bedeutung der Schaltflächen auf alle Anwendungen auswirkt.

## <a name="xbuttons"></a>XBUTTONs

Windows unterstützt eine Maus mit fünf Schaltflächen. Zusätzlich zu den Schaltflächen links, mitte und rechts gibt es XBUTTON1 und XBUTTON2, die rückwärts und vorwärts navigieren, wenn Sie Ihren Browser verwenden.

Der Fenster-Manager unterstützt XBUTTON1 und XBUTTON2 über die **MELDUNGEN WM \_ XBUTTON \* *_ und _* WM \_ NCXBUTTON \* *_ . Das HIWORD des _WPARAM*** in diesen Meldungen enthält ein Flag, das angibt, auf welche X-Schaltfläche gedrückt wurde. Da diese Mausnachrichten auch zwischen den Konstanten **WM \_ MOUSEFIRST** und **WM \_ MOUSELAST** passen, kann eine Anwendung alle Mausnachrichten mit [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) oder [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)filtern.

Die folgenden Unterstützen XBUTTON1 und XBUTTON2:

-   [**WM \_ APPCOMMAND**](wm-appcommand.md)
-   [**WM \_ NCXBUTTONDBLCLK**](wm-ncxbuttondblclk.md)
-   [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)
-   [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
-   [**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md)
-   [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)
-   [**WM \_ XBUTTONUP**](wm-xbuttonup.md)
-   [**MOUSEHOOKSTRUCTEX**](/windows/win32/api/winuser/ns-winuser-mousehookstructex)

Die folgenden APIs wurden geändert, um diese Schaltflächen zu unterstützen:

-   [**\_Mausereignis**](/windows/win32/api/winuser/nf-winuser-mouse_event)
-   [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
-   [**MSLLHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-msllhookstruct)
-   [**MOUSEINPUT**](/windows/win32/api/winuser/ns-winuser-mouseinput)
-   [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)

Es ist unwahrscheinlich, dass ein untergeordnetes Fenster in einer Komponentenanwendung Befehle für XBUTTON1 und XBUTTON2 direkt implementieren kann. [**DefWindowProc sendet also**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) eine [**WM \_ APPCOMMAND-Nachricht**](wm-appcommand.md) an ein Fenster, wenn auf eine X-Schaltfläche geklickt wird. **DefWindowProc sendet** auch die **WM \_ APPCOMMAND-Nachricht** an das übergeordnete Fenster. Dies ähnelt der Art und Weise, wie Kontextmenüs mit einem Rechtsklick aufgerufen werden.**DefWindowProc** sendet eine [**WM \_ CONTEXTMENU-Nachricht**](/windows/desktop/menurc/wm-contextmenu) an das Menü und sendet sie auch an das übergeordnete Element. Wenn **DefWindowProc** außerdem eine **WM \_ APPCOMMAND-Nachricht** für ein Fenster der obersten Ebene empfängt, wird ein Shellhook mit Dem Code HSHELL \_ APPCOMMANDaufgerufen.

Tastaturen mit zusätzlichen Tasten für Browserfunktionen, Medienfunktionen, Anwendungsstart und Energieverwaltung werden unterstützt. Weitere Informationen finden Sie unter [Tastaturtasten für das Durchsuchen und andere Funktionen.](about-keyboard-input.md)

## <a name="mouse-messages"></a>Mausnachrichten

Die Maus generiert ein Eingabeereignis, wenn der Benutzer die Maus bewegt oder eine Maustaste drückt oder loslässt. Das System konvertiert Mauseingabeereignisse in Nachrichten und übermittelt sie an die Nachrichtenwarteschlange des entsprechenden Threads. Wenn Mausnachrichten schneller gesendet werden, als ein Thread sie verarbeiten kann, verwirft das System alle bis auf die letzte Mausnachricht.

Ein Fenster empfängt eine Mausmeldung, wenn ein Mausereignis auftritt, während sich der Cursor innerhalb der Rahmen des Fensters befindet oder wenn das Fenster die Maus erfasst hat. Mausnachrichten sind in zwei Gruppen unterteilt: Clientbereichsmeldungen und Nicht-Clientbereichsmeldungen. In der Regel verarbeitet eine Anwendung Clientbereichsmeldungen und ignoriert Nichtclientbereichsnachrichten.

Dieser Abschnitt enthält die folgenden Themen:

-   [Clientbereichs-Mausmeldungen](#client-area-mouse-messages)
-   [Nichtclientbereichs-Mausmeldungen](#nonclient-area-mouse-messages)
-   [Die WM \_ NCHITTEST-Nachricht](/windows)

### <a name="client-area-mouse-messages"></a>Clientbereichs-Mausmeldungen

Ein Fenster empfängt eine Clientbereichsmausmeldung, wenn ein Mausereignis im Clientbereich des Fensters auftritt. Das System übermittelt die [**WM \_ MOUSEMOVE-Nachricht**](wm-mousemove.md) an das Fenster, wenn der Benutzer den Cursor innerhalb des Clientbereichs bewegt. Es wird eine der folgenden Meldungen gesendet, wenn der Benutzer eine Maustaste drückt oder loslässt, während sich der Cursor im Clientbereich befindet.



| Nachricht                                       | Bedeutung                                     |
|-----------------------------------------------|---------------------------------------------|
| [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md) | Auf die linke Maustaste wurde doppelklicken.   |
| [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md)     | Die linke Maustaste wurde gedrückt.          |
| [**WM \_ LBUTTONUP**](wm-lbuttonup.md)         | Die linke Maustaste wurde losgelassen.         |
| [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md) | Die mittlere Maustaste wurde doppelt angeklickt. |
| [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md)     | Die mittlere Maustaste wurde gedrückt.        |
| [**WM \_ MBUTTONUP**](wm-mbuttonup.md)         | Die mittlere Maustaste wurde losgelassen.       |
| [**WM \_ RBUTTONDBLCLK**](wm-rbuttondblclk.md) | Auf die rechte Maustaste wurde doppelklicken.  |
| [**WM \_ RBUTTONDOWN**](wm-rbuttondown.md)     | Die rechte Maustaste wurde gedrückt.         |
| [**WM \_ RBUTTONUP**](wm-rbuttonup.md)         | Die rechte Maustaste wurde losgelassen.        |
| [**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md) | Es wurde auf eine X-Maustaste doppelklickt.       |
| [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)     | Eine X-Maustaste wurde gedrückt.              |
| [**WM \_ XBUTTONUP**](wm-xbuttonup.md)         | Eine X-Maustaste wurde losgelassen.             |



 

Darüber hinaus kann eine Anwendung die [**TrackMouseEvent-Funktion**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) aufrufen, damit das System zwei weitere Nachrichten sendet. Es wird die [**WM \_ MOUSEHOVER-Meldung**](wm-mousehover.md) gesendet, wenn der Cursor für einen bestimmten Zeitraum über den Clientbereich bewegt wird. Es wird die [**WM \_ MOUSELEAVE-Nachricht**](wm-mouseleave.md) gesendet, wenn der Cursor den Clientbereich verlässt.

### <a name="message-parameters"></a>Meldungsparameter

Der *lParam-Parameter* einer Clientbereichsmausmeldung gibt die Position des Cursor-Hotspots an. Das niedrige Wort gibt die x-Koordinate des Hotspots an, und das obere Wort gibt die y-Koordinate an. Die Koordinaten werden in Clientkoordinaten angegeben. Im Clientkoordinatensystem werden alle Punkte auf dem Bildschirm relativ zu den Koordinaten (0,0) der oberen linken Ecke des Clientbereichs angegeben.

Der *wParam-Parameter* enthält Flags, die den Status der anderen Maustasten sowie die STRG- und UMSCHALTTASTEn zum Zeitpunkt des Mausereignisses angeben. Sie können diese Flags überprüfen, wenn die Verarbeitung von Mausnachrichten vom Zustand einer anderen Maustaste oder der STRG- oder UMSCHALTTASTE abhängt. Der *wParam-Parameter* kann eine Kombination der folgenden Werte sein.



| Wert            | Beschreibung                      |
|------------------|----------------------------------|
| **\_MK-STEUERELEMENT**  | Die STRG-TASTE ist gedrückt.            |
| **MK \_ LBUTTON**  | Die linke Maustaste ist nach unten.   |
| **MK \_ MBUTTON**  | Die mittlere Maustaste ist nach unten. |
| **MK \_ RBUTTON**  | Die rechte Maustaste ist nach unten.  |
| **MK \_ SHIFT**    | Die UMSCHALTTASTE ist heruntergefahren.           |
| **MK \_ XBUTTON1** | Die erste X-Schaltfläche ist nicht mehr zu sehen.      |
| **MK \_ XBUTTON2** | Die zweite X-Schaltfläche ist nicht mehr zu sehen.     |



 

### <a name="double-click-messages"></a>Double-Click Nachrichten

Das System generiert eine Doppelklickmeldung, wenn der Benutzer in schneller Folge zweimal auf eine Maustaste klickt. Wenn der Benutzer auf eine Schaltfläche klickt, richtet das System ein Rechteck ein, das um den Hotspot des Cursors zentriert ist. Außerdem wird der Zeitpunkt markiert, zu dem der Klick aufgetreten ist. Wenn der Benutzer ein zweites Mal auf dieselbe Schaltfläche klickt, bestimmt das System, ob sich der Hotspot noch innerhalb des Rechtecks befindet, und berechnet die seit dem ersten Klick verstrichene Zeit. Wenn sich der Hotspot noch innerhalb des Rechtecks befindet und die verstrichene Zeit den Time out-Wert für Doppelklicks nicht überschreitet, generiert das System eine Doppelklickmeldung.

Eine Anwendung kann mithilfe der Funktionen [**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime) bzw. [**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime) Time Time-Werte für Doppelklicks erhalten und festlegen. Alternativ kann die Anwendung den Wert für das Doppelklicktimeout mithilfe des SPI-Flags **\_ SETDOUBLECLICKTIME** mit der [**SystemParametersInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) festlegen. Sie kann auch die Größe des Rechtecks festlegen, das das System zum Erkennen von Doppelklicks verwendet, indem die **FLAGs SPI \_ SETDOUBLECLKWIDTH** und **SPI \_ SETDOUBLECLKHEIGHT** an **SystemParametersInfo** übergeben werden. Beachten Sie jedoch, dass sich das Festlegen des Double-Click-Time out-Werts und des Rechtecks auf alle Anwendungen auswirken.

Ein anwendungsdefiniertes Fenster erhält standardmäßig keine Doppelklicknachrichten. Aufgrund des Systemaufwands beim Generieren von Doppelklicknachrichten werden diese Meldungen nur für Fenster generiert, die Klassen im **CS \_ DBLCLKS-Klassenstil** angehören. Die Anwendung muss diesen Stil beim Registrieren der Fensterklasse festlegen. Weitere Informationen finden Sie unter [Fensterklassen](/windows/desktop/winmsg/window-classes).

Eine Doppelklicknachricht ist immer die dritte Nachricht in einer Vier-Nachrichten-Reihe. Die ersten beiden Meldungen sind die durch den ersten Klick generierten Button-down- und Button-up-Meldungen. Beim zweiten Klick wird die Doppelklicknachricht gefolgt von einer weiteren Schaltflächen-Up-Meldung generiert. Wenn Sie beispielsweise auf die linke Maustaste doppelklicken, wird die folgende Meldungssequenz generiert:

1.  [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md)
2.  [**WM \_ LBUTTONUP**](wm-lbuttonup.md)
3.  [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md)
4.  [**WM \_ LBUTTONUP**](wm-lbuttonup.md)

Da ein Fenster immer eine Schaltflächen-nach-unten-Nachricht empfängt, bevor eine Doppelklicknachricht empfangen wird, verwendet eine Anwendung in der Regel eine Doppelklicknachricht, um eine Aufgabe zu erweitern, die während einer Schaltflächen-Down-Nachricht gestartet wurde. Wenn der Benutzer beispielsweise auf eine Farbe in der Farbpalette von Microsoft Paint klickt, zeigt Paint die ausgewählte Farbe neben der Palette an. Wenn der Benutzer auf eine Farbe doppelklickt, zeigt Paint die Farbe an und öffnet das Dialogfeld **Farben bearbeiten.**

### <a name="nonclient-area-mouse-messages"></a>Nichtclientbereichs-Mausmeldungen

Ein Fenster empfängt eine Nicht-Clientbereich-Mausmeldung, wenn ein Mausereignis in einem beliebigen Teil eines Fensters mit Ausnahme des Clientbereichs auftritt. Der Nichtclientbereich eines Fensters besteht aus Rahmen, Menüleiste, Titelleiste, Scrollleiste, Fenstermenü, Schaltfläche "Minimieren" und Schaltfläche "Maximieren".

Das System generiert Nicht-Clientbereichsmeldungen in erster Linie für die eigene Verwendung. Das System verwendet beispielsweise Nicht-Clientbereichsmeldungen, um den Cursor in einen Pfeil mit zwei Pfeilen zu ändern, wenn der Cursor-Hot Spot in den Rahmen eines Fensters verschoben wird. Ein Fenster muss Nicht-Clientbereich-Mausmeldungen an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben, um die integrierte Mausschnittstelle nutzen zu können.

Für jede Clientbereichsmausmeldung gibt es eine entsprechende Nicht-Clientbereichsmausmeldung. Die Namen dieser Nachrichten sind ähnlich, außer dass die benannten Konstanten für die Nicht-Clientbereichsnachrichten die Buchstaben NC enthalten. Wenn Sie z. B. den Cursor im Nichtclientbereich bewegen, wird eine [**WM \_ NCMOUSEMOVE-Nachricht**](wm-ncmousemove.md) generiert, und wenn Sie die linke Maustaste drücken, während sich der Cursor im Nichtclientbereich befindet, wird eine [**\_ WM-NCLBUTTONDOWN-Meldung**](wm-nclbuttondown.md) generiert.

Der *lParam-Parameter* einer Nicht-Clientbereich-Mausnachricht ist eine -Struktur, die die x- und y-Koordinaten des Cursor-Hotspots enthält. Im Gegensatz zu Koordinaten von Clientbereich-Mausnachrichten werden die Koordinaten in Bildschirmkoordinaten und nicht in Clientkoordinaten angegeben. Im Bildschirmkoordinatensystem sind alle Punkte auf dem Bildschirm relativ zu den Koordinaten (0,0) der oberen linken Ecke des Bildschirms.

Der *wParam-Parameter* enthält einen Treffertestwert, einen Wert, der angibt, wo im Nicht-Clientbereich das Mausereignis aufgetreten ist. Im folgenden Abschnitt wird der Zweck von Treffertestwerten erläutert.

### <a name="the-wm_nchittest-message"></a>\_Wm-NCHITTEST-Nachricht

Jedes Mal, wenn ein Mausereignis auftritt, sendet das System eine [**\_ WM-NCHITTEST-Nachricht**](wm-nchittest.md) an das Fenster, das den Cursor-Hot spot enthält, oder an das Fenster, das die Maus erfasst hat. Das System verwendet diese Meldung, um zu bestimmen, ob ein Clientbereich oder eine Nicht-Clientbereich-Mausnachricht gesendet werden soll. Eine Anwendung, die Mausbewegungen und Maustastennachrichten empfangen muss, muss die **WM \_ NCHITTEST-Nachricht** an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben.

Der *lParam-Parameter* der [**WM \_ NCHITTEST-Nachricht**](wm-nchittest.md) enthält die Bildschirmkoordinaten des Cursor-Hotspots. Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) untersucht die Koordinaten und gibt einen Treffertestwert zurück, der die Position des Hotspots angibt. Der Treffertestwert kann einer der folgenden Werte sein.



| Wert             | Speicherort des Hotspots                                                                                                                                                                                |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HTBORDER**      | Im Rahmen eines Fensters, das keinen Größenrahmen besitzt.                                                                                                                                       |
| **HTBOTTOM**      | Im unteren horizontalen Rahmen eines Fensters.                                                                                                                                                         |
| **HTBOTTOMLEFT**  | In der unteren linken Ecke eines Fensterrahmens.                                                                                                                                                        |
| **HTBOTTOMRIGHT** | In der unteren rechten Ecke eines Fensterrahmens.                                                                                                                                                       |
| **ICEAPTION**     | In einer Titelleiste.                                                                                                                                                                                     |
| **HTCLIENT**      | In einem Clientbereich.                                                                                                                                                                                   |
| **NOKIALOSE**       | In einer Schaltfläche **Schließen.**                                                                                                                                                                              |
| **HTERROR**       | Auf dem Bildschirmhintergrund oder auf einer Trennlinie zwischen Fenstern (identisch mit HTNOWHERE, mit der Ausnahme, dass die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) einen Systemsignal erzeugt, um auf einen Fehler hinzuweisen). |
| **HTGROWBOX**     | In einem Größenfeld (identisch mit **HTSIZE**).                                                                                                                                                                 |
| **HTHELP**        | In  einer Hilfeschaltfläche.                                                                                                                                                                               |
| **HTHSCROLL**     | In einer horizontalen Bildlaufleiste.                                                                                                                                                                         |
| **HTLEFT**        | Im linken Rahmen eines Fensters.                                                                                                                                                                     |
| **HTMENU**        | In einem Menü.                                                                                                                                                                                          |
| **HTMAXBUTTON**   | In einer Schaltfläche **Maximieren.**                                                                                                                                                                           |
| **HTMINBUTTON**   | In einer Schaltfläche **Minimieren.**                                                                                                                                                                           |
| **HTNOWHERE**     | Auf dem Bildschirmhintergrund oder auf einer Trennlinie zwischen Fenstern.                                                                                                                                     |
| **HTREDUCE**      | In einer Schaltfläche **Minimieren.**                                                                                                                                                                           |
| **HTRIGHT**       | Im rechten Rahmen eines Fensters.                                                                                                                                                                    |
| **HTSIZE**        | In einem Größenfeld (identisch mit **HTGROWBOX**).                                                                                                                                                              |
| **HTSYSMENU**     | In einem **Systemmenü** oder in einer Schaltfläche **Schließen** in einem untergeordneten Fenster.                                                                                                                                    |
| **HTTOP**         | Im oberen horizontalen Rahmen eines Fensters.                                                                                                                                                         |
| **HTTOPLEFT**     | In der oberen linken Ecke eines Fensterrahmens.                                                                                                                                                        |
| **HTTOPRIGHT**    | In der oberen rechten Ecke eines Fensterrahmens.                                                                                                                                                       |
| **HTTRANSPARENT** | In einem Fenster, das derzeit von einem anderen Fenster im gleichen Thread abgedeckt wird.                                                                                                                                 |
| **HTVSCROLL**     | In der vertikalen Bildlaufleiste.                                                                                                                                                                         |
| **HTZOOM**        | In einer Schaltfläche **Maximieren.**                                                                                                                                                                           |



 

Wenn sich der Cursor im Clientbereich eines Fensters befindet, gibt [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) den **HTCLIENT-Treffertestwert** an die Fensterprozedur zurück. Wenn die Fensterprozedur diesen Code an das System zurückgibt, konvertiert das System die Bildschirmkoordinaten des Cursor-Hotspots in Clientkoordinaten und sendet dann die entsprechende Clientbereich-Mausnachricht.

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gibt einen der anderen Treffertestwerte zurück, wenn sich der Cursor-Hot Spot im Nichtclientbereich eines Fensters befindet. Wenn die Fensterprozedur einen dieser Treffertestwerte zurückgibt, sendet das System eine Nicht-Clientbereich-Mausnachricht, wobei der Treffertestwert im *wParam-Parameter* der Nachricht und die Cursorkoordinaten im *lParam-Parameter* platziert werden.

## <a name="mouse-sonar"></a>Mouse Sonar

Die Barrierefreiheitsfunktion Mouse Sonar zeigt kurz mehrere konzentrische Kreise um den Zeiger, wenn der Benutzer die STRG-TASTE drückt und freigibt. Dieses Feature hilft einem Benutzer, den Mauszeiger auf einem Bildschirm zu finden, der überladen ist oder dessen Auflösung auf hoch, auf einem Monitor mit schlechter Qualität oder für Benutzer mit sehbehinderter Sehfähigkeit festgelegt ist. Weitere Informationen finden Sie in den folgenden Flags in [**SystemParametersInfo:**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)

**SPI \_ GETMOUSESONAR**

**SPI \_ SETMOUSESONAR**

## <a name="mouse-vanish"></a>Mouse Vanish

Die Barrierefreiheitsfunktion Mouse Vanish blendet den Zeiger aus, wenn der Benutzer eingibt. Der Mauszeiger wird erneut angezeigt, wenn der Benutzer die Maus bewegt. Dieses Feature verhindert, dass der Zeiger den eingegebenen Text verdeckt, z. B. in einer E-Mail oder einem anderen Dokument. Weitere Informationen finden Sie in den folgenden Flags in [**SystemParametersInfo:**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)

**SPI \_ GETMOUSEVANISH**

**SPI \_ SETMOUSEVANISH**

## <a name="the-mouse-wheel"></a>Das Mausrad

Das Mausrad kombiniert die Features eines Rads und einer Maustaste. Das Rad verfügt über diskrete Notches mit gleichmäßigen Leerräumen. Wenn Sie das Rad drehen, wird eine Radmeldung an Ihre Anwendung gesendet, wenn jede Notch gefunden wird. Die Radschaltfläche kann auch als normale Windows mittlere (dritte) Schaltfläche ausgeführt werden. Wenn Sie das Mausrad drücken und loslassen, werden die Standardmeldungen [**WM \_ MBUTTONUP**](wm-mbuttonup.md) und [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md) gesendet. Wenn Sie auf die dritte Schaltfläche doppelklicken, wird die [**\_ WM-Standardmeldung MBUTTONDBLCLK**](wm-mbuttondblclk.md) gesendet.

Das Mausrad wird über die [**WM \_ MOUSEWHEEL-Meldung**](wm-mousewheel.md) unterstützt.

Durch Drehen der Maus wird die [**WM \_ MOUSEWHEEL-Nachricht**](wm-mousewheel.md) an das Fokusfenster gesendet. Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gibt die Nachricht an das übergeordnete Element des Fensters weiter. Es sollte keine interne Weiterleitung der Nachricht erfolgen, da **DefWindowProc** sie in der übergeordneten Kette weiterleitet, bis ein Fenster gefunden wird, das sie verarbeitet.

### <a name="determining-the-number-of-scroll-lines"></a>Bestimmen der Anzahl von Bildlauflinien

Anwendungen sollten die [**SystemParametersInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) verwenden, um die Anzahl der Zeilen abzurufen, die ein Dokument für jeden Scrollvorgang (Wheel Notch) scrollt. Um die Anzahl der Zeilen abzurufen, ruft eine Anwendung den folgenden Aufruf ab:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



Die Variable "pulScrollLines" zeigt auf einen ganzzahligen Wert ohne Vorzeichen, der die vorgeschlagene Anzahl von Zeilen empfängt, die gescrollt werden sollen, wenn das Mausrad ohne Modifizierertasten gedreht wird:

-   Wenn diese Zahl 0 ist, sollte kein Bildlauf erfolgen.
-   Wenn diese Zahl **WHEEL \_ PAGESCROLL** ist, sollte ein Radroll so interpretiert werden, dass er einmal in den Seitenab- oder Seitenupbereichen der Scrollleiste klickt.
-   Wenn die Anzahl der Zeilen, für die ein Bildlauf durchgeführt werden soll, größer als die Anzahl der anzuzeigenden Zeilen ist, sollte der Bildlaufvorgang auch als Bildlauf nach unten oder nach oben interpretiert werden.

Der Standardwert für die Anzahl der Bildlaufzeilen ist 3. Wenn ein Benutzer die Anzahl der Bildlauflinien mithilfe des Blatts Mauseigenschaften in Systemsteuerung ändert, überträgt das Betriebssystem eine [**WM \_ SETTINGCHANGE-Meldung**](../winmsg/wm-settingchange.md) an alle Fenster der obersten Ebene, wobei **SPI \_ SETWHEELSCROLLLINES** angegeben ist. Wenn eine Anwendung die **WM \_ SETTINGCHANGE-Nachricht** empfängt, kann sie die neue Anzahl von Scrollzeilen abrufen, indem sie Folgendes aufruft:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



### <a name="controls-that-scroll"></a>Steuerelemente, die scrollen

In der folgenden Tabelle sind die Steuerelemente mit Scrollfunktionen (einschließlich vom Benutzer festgelegter Scrollzeilen) aufgeführt. 

| Control                 | Bildlauf                                                                                                                                                               |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Steuerelement bearbeiten            | Vertikal und horizontal.                                                                                                                                                |
| Listenfeld-Steuerelement        | Vertikal und horizontal.                                                                                                                                                |
| Kombinationsfeld               | Wenn sie nicht gelöscht wird, ruft jeder Bildlauf das nächste oder vorherige Element ab. Wenn sie nach unten verschoben wird, führt jeder Bildlauf die Nachricht nach vorn zum Listenfeld aus, in dem entsprechend gescrollt wird. |
| CMD (Befehlszeile)      | Vertikal.                                                                                                                                                               |
| Strukturansicht               | Vertikal und horizontal.                                                                                                                                                |
| Listenansicht               | Vertikal und horizontal.                                                                                                                                                |
| Bildlauf nach oben/unten         | Ein Element nach dem anderen.                                                                                                                                                     |
| Trackbar-Scrolls        | Ein Element nach dem anderen.                                                                                                                                                     |
| Microsoft Rich Edit 1.0 | Vertikal. Beachten Sie, dass der Exchange-Client über eigene Versionen der Listenansichts- und Strukturansichtssteuerelemente verfügt, die keine Radunterstützung aufweisen.                                        |
| Microsoft Rich Edit 2.0 | Vertikal.                                                                                                                                                               |



 

### <a name="detecting-a-mouse-with-a-wheel"></a>Erkennen einer Maus mit einem Rad

Um zu bestimmen, ob eine Maus mit einem Rad verbunden ist, rufen [**Sie GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) mit **SM \_ MOUSEWHEELPRESENT** auf. Der Rückgabewert **TRUE** gibt an, dass die Maus verbunden ist.

Das folgende Beispiel stammt aus der Fensterprozedur für ein mehrzeiliges Bearbeitungssteuerelement:


```
BOOL ScrollLines(
     PWNDDATA pwndData,   //scrolls the window indicated
     int cLinesToScroll); //number of times

short gcWheelDelta; //wheel delta from roll
PWNDDATA pWndData; //pointer to structure containing info about the window
UINT gucWheelScrollLines=0;//number of lines to scroll on a wheel rotation

gucWheelScrollLines = SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 
                             0, 
                             pulScrollLines, 
                             0);

case WM_MOUSEWHEEL:
    /*
     * Do not handle zoom and datazoom.
     */
    if (wParam & (MK_SHIFT | MK_CONTROL)) {
        goto PassToDefaultWindowProc;
    }

    gcWheelDelta -= (short) HIWORD(wParam);
    if (abs(gcWheelDelta) >= WHEEL_DELTA && gucWheelScrollLines > 0) 
    {
        int cLineScroll;

        /*
         * Limit a roll of one (1) WHEEL_DELTA to
         * scroll one (1) page.
         */
        cLineScroll = (int) min(
                (UINT) pWndData->ichLinesOnScreen - 1,
                gucWheelScrollLines);

        if (cLineScroll == 0) {
            cLineScroll++;
        }

        cLineScroll *= (gcWheelDelta / WHEEL_DELTA);
        assert(cLineScroll != 0);

        gcWheelDelta = gcWheelDelta % WHEEL_DELTA;
        return ScrollLines(pWndData, cLineScroll);
    }

    break;
```



## <a name="window-activation"></a>Aktivieren von Fenstern

Wenn der Benutzer auf ein inaktives Fenster der obersten Ebene oder auf das untergeordnete Fenster eines inaktiven Fensters der obersten Ebene klickt, sendet das System die [**WM \_ MOUSEACTIVATE-Nachricht**](wm-mouseactivate.md) (unter anderem) an das Fenster der obersten Ebene oder an das untergeordnete Fenster. Das System sendet diese Nachricht, nachdem die [**\_ WM-NCHITTEST-Nachricht**](wm-nchittest.md) an das Fenster gesendet wurde, aber bevor die Schaltflächen-down-Nachricht gepostet wird. Wenn **WM \_ MOUSEACTIVATE** an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben wird, aktiviert das System das Fenster der obersten Ebene und sendet dann die Schaltflächen-nach-unten-Meldung an das Fenster der obersten Ebene oder des untergeordneten Fensters.

Durch die Verarbeitung von [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md)kann ein Fenster steuern, ob das Fenster der obersten Ebene als Ergebnis eines Mausklicks zum aktiven Fenster wird und ob das fenster, auf das geklickt wurde, die nachfolgende Schaltflächen-Down-Meldung empfängt. Dazu wird einer der folgenden Werte zurückgegeben, nachdem **WM \_ MOUSEACTIVATE** verarbeitet wurde.



| Wert                    | Bedeutung                                                              |
|--------------------------|----------------------------------------------------------------------|
| **MA \_ ACTIVATE**         | Aktiviert das Fenster und verwirft die Mausnachricht nicht.         |
| **MA \_ NOACTIVATE**       | Aktiviert das Fenster nicht und verwirft die Mausnachricht nicht. |
| **MA \_ ACTIVATEANDEAT**   | Aktiviert das Fenster und verwirft die Mausnachricht.                 |
| **MA \_ NOACTIVATEANDEAT** | Aktiviert das Fenster nicht, sondern verwirft die Mausnachricht.         |

## <a name="see-also"></a>Weitere Informationen

[Nutzen von High-Definition Mausbewegung](../dxtecharts/taking-advantage-of-high-dpi-mouse-movement.md)