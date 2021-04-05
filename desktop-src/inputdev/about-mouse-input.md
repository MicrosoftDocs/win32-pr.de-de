---
title: Informationen zur Mauseingabe
description: In diesem Thema werden Maus Eingaben behandelt.
ms.assetid: 1f945a31-76d5-4e23-a55a-769ca114dbe9
keywords:
- Benutzereingabe, Mauseingabe
- Erfassen von Benutzereingaben, Maus Eingaben
- Mauseingabe
- Mauszeiger
- Cursor, Maus Eingaben
- Maus Erfassung
- Maus mit ClickLock
- Xbuttons
- Maus Konfiguration
- Maus Meldungen
- WM_NCHITTEST Meldung
- Barrierefreiheits Feature der Maus nicht mehr
- "\"Mouse"
- Mausrad
- WM_MOUSEWHEEL Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2294027cb4ca2c97371a7a06c90a7e46188e3b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726984"
---
# <a name="about-mouse-input"></a>Informationen zur Mauseingabe

Die Maus ist ein wichtiges, aber optionales Benutzereingabe Gerät für Anwendungen. Eine gut geschriebene Anwendung sollte eine Maus Schnittstelle enthalten, sollte jedoch nicht allein von der Maus zum Abrufen von Benutzereingaben abhängen. Die Anwendung sollte auch vollständige Tastatur Unterstützung bereitstellen.

Eine Anwendung empfängt Maus Eingaben in Form von Nachrichten, die an Ihre Fenster gesendet oder an diese gesendet werden.

Dieser Abschnitt enthält die folgenden Themen:

-   [Mauszeiger](#mouse-cursor)
-   [Mausaufzeichnung](#mouse-capture)
-   [Maus mit ClickLock](#mouse-clicklock)
-   [Maus Konfiguration](#mouse-configuration)
-   [Xbuttons](#xbuttons)
-   [Maus Meldungen](#mouse-messages)
    -   [Client Bereich-Maus Meldungen](#client-area-mouse-messages)
    -   [Nicht-Client-Bereich-Maus Meldungen](#nonclient-area-mouse-messages)
    -   [Die WM- \_ nchittest-Meldung](/windows)
-   [Maus, Sonar](#mouse-sonar)
-   [Maus verschwindet](#mouse-vanish)
-   [Das Mausrad](#the-mouse-wheel)
-   [Aktivieren von Fenstern](#window-activation)

## <a name="mouse-cursor"></a>Mauszeiger

Wenn der Benutzer die Maus bewegt, verschiebt das System eine Bitmap auf dem Bildschirm mit dem *Mauszeiger*. Der Mauszeiger enthält einen Single-Pixel-Punkt, der als *Hot-Spot* bezeichnet wird, einen Punkt, den das System nachverfolgt und als Position des Cursors erkennt. Wenn ein Maus Ereignis auftritt, empfängt das Fenster, das den Hotspot enthält, in der Regel die Maus Nachricht, die sich aus dem Ereignis ergibt. Das Fenster muss nicht aktiv sein oder den Tastaturfokus haben, um eine Maus Meldung zu empfangen.

Das System verwaltet eine Variable, die die Maus Geschwindigkeit steuert – d. h. die Entfernung, die der Cursor bewegt, wenn der Benutzer die Maus bewegt. Sie können die [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion mit dem **SPI \_ getmouse** -oder **SPI \_ setmouse** -Flag verwenden, um die Geschwindigkeit abzurufen oder festzulegen. Weitere Informationen zu Maus Cursorn finden Sie unter [Cursors](/windows/desktop/menurc/cursors).

## <a name="mouse-capture"></a>Mausaufzeichnung

Das System sendet in der Regel eine Maus Meldung an das Fenster, das den Cursor Hotspot enthält, wenn ein Maus Ereignis auftritt. Eine Anwendung kann dieses Verhalten ändern, indem Sie die [**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture) -Funktion verwendet, um Maus Meldungen an ein bestimmtes Fenster weiterzuleiten. Das Fenster empfängt alle Maus Meldungen, bis die Anwendung die [**releasecapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) -Funktion aufruft oder ein anderes Erfassungsfenster angibt, oder bis der Benutzer auf ein Fenster klickt, das von einem anderen Thread erstellt wurde.

Wenn sich die Maus Aufzeichnung ändert, sendet das System eine [**WM \_ capturechanged**](wm-capturechanged.md) -Meldung an das Fenster, das die Maus Aufzeichnung verliert. Der *LPARAM* -Parameter der Meldung gibt ein Handle für das Fenster an, das die Maus Aufzeichnung gewinnt.

Nur im Vordergrund Fenster können Maus Eingaben erfasst werden. Wenn ein Hintergrund Fenster versucht, Maus Eingaben zu erfassen, empfängt es nur Meldungen für Mausereignisse, die auftreten, wenn sich der Cursor-Hotspot innerhalb des sichtbaren Teils des Fensters befindet.

Das Erfassen von Maus Eingaben ist nützlich, wenn ein Fenster alle Maus Eingaben empfangen muss, auch wenn der Cursor außerhalb des Fensters bewegt wird. Beispielsweise verfolgt eine Anwendung in der Regel die Cursorposition nach einem MouseButton-Down-Ereignis nach dem Cursor, bis ein mausbuttonup-Ereignis auftritt. Wenn eine Anwendung keine Maus Eingaben erfasst hat und der Benutzer die Maustaste außerhalb des Fensters loslässt, empfängt das Fenster die Schaltfläche nicht.

Ein Thread kann die [**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture) -Funktion verwenden, um zu bestimmen, ob eines seiner Fenster die Maus erfasst hat. Wenn eines der Fenster des Threads die Maus erfasst hat, ruft **GetCapture** ein Handle für das Fenster ab.

## <a name="mouse-clicklock"></a>Maus mit ClickLock

Mit dem Barrierefreiheits Feature "Mausklicks" können Benutzer die primäre Maustaste nach einem einzigen Mausklick sperren. Für eine Anwendung scheint die Schaltfläche nach unten gedrückt zu werden. Zum Entsperren der Schaltfläche kann eine Anwendung jede beliebige Maus Nachricht senden, oder der Benutzer kann auf eine beliebige Maustaste klicken. Mit dieser Funktion können Benutzer komplexe Maus Kombinationen einfacher ausführen. Beispielsweise können solche mit bestimmten physischen Einschränkungen Text hervorheben, Objekte ziehen oder Menüs leichter öffnen. Weitere Informationen finden Sie unter den folgenden Flags und den Hinweisen in [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

-   **SPI \_ getmoucclicklock**
-   **SPI-abversions- \_ ClickLock**
-   **SPI \_ getmou\clicklocktime**
-   **SPI- \_ Sekunden-/Uhrzeitangabe**

## <a name="mouse-configuration"></a>Maus Konfiguration

Obwohl es sich bei der Maus um ein wichtiges Eingabegerät für Anwendungen handelt, hat nicht jeder Benutzer notwendigerweise eine Maus. Eine Anwendung kann ermitteln, ob das System eine Maus enthält, indem der **SM- \_ mousepresent** -Wert an die [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion übergeben wird.

Windows unterstützt eine Maus mit bis zu drei Schaltflächen. Bei einer drei-Schaltflächen-Maus werden die Schaltflächen als linke, mittlere und Rechte Schaltfläche bezeichnet. Bei Nachrichten und benannten Konstanten, die sich auf die Maustasten beziehen, werden die Schaltflächen mit den Buchstaben L, M und R identifiziert. Die Schaltfläche auf einer Einzel Schaltfläche-Maus wird als linke Schaltfläche betrachtet. Obwohl Windows eine Maus mit mehreren Schaltflächen unterstützt, verwenden die meisten Anwendungen die linke Schaltfläche Primär und die anderen minimal, wenn überhaupt.

Anwendungen können auch ein Mausrad unterstützen. Das Mausrad kann gedrückt oder gedreht werden. Wenn das Mausrad gedrückt ist, fungiert es als die mittlere (dritte) Schaltfläche und sendet normale Meldungen der mittleren Schaltfläche an die Anwendung. Beim Drehen wird eine radnachricht an Ihre Anwendung gesendet. Weitere Informationen finden Sie [im Mausrad](#the-mouse-wheel) Abschnitt.

Anwendungen können Anwendungs Befehls Schaltflächen unterstützen. Diese Schaltflächen, die als X-Schaltflächen bezeichnet werden, sind so konzipiert, dass Sie einen einfacheren Zugriff auf einen Internet Browser, elektronische e-Mails und Media Services ermöglichen. Wenn eine X-Schaltfläche gedrückt wird, wird eine [**WM \_ appcommand**](wm-appcommand.md) -Meldung an die Anwendung gesendet. Weitere Informationen finden Sie in der Beschreibung in der **WM- \_ appcommand** -Nachricht.

Eine Anwendung kann die Anzahl der Schaltflächen auf der Maus ermitteln, indem der Wert von **SM \_ cmousebuttons** an die [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion übergeben wird. Um die Maus für einen links gerichteten Benutzer zu konfigurieren, kann die Anwendung mithilfe der Funktion " [**Swap**](/windows/win32/api/winuser/nf-winuser-swapmousebutton) " die Bedeutung der linken und rechten Maustasten umkehren. Das Übergeben des **SPI \_ setmousebuttonswap** -Werts an die [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion ist eine andere Möglichkeit, die Bedeutung der Schaltflächen umzukehren. Beachten Sie jedoch, dass es sich bei der Maus um eine freigegebene Ressource handelt, sodass das Umkehren der Bedeutung der Schaltflächen alle Anwendungen betrifft.

## <a name="xbuttons"></a>Xbuttons

Windows unterstützt eine Maus mit fünf Schaltflächen. Zusätzlich zu den Schaltflächen Left, Middle und right gibt es XButton1 und XButton2, die die rückwärts-und Vorwärtsnavigation bei Verwendung Ihres Browsers bereitstellen.

Der Fenster-Manager unterstützt XButton1 und XButton2 über die Nachrichten **WM \_ XButton \*** und **WM \_ ncxbutton \*** . Das HIWORD des **wParam** in diesen Meldungen enthält ein Flag, das angibt, welche X-Schaltfläche gedrückt wurde. Da diese Maus Meldungen auch zwischen den Konstanten **WM \_ mousefirst** und **WM \_ mouselast** passen, kann eine Anwendung alle Maus Meldungen mit [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) oder [**Peer Message**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)filtern.

Die folgenden unterstützten XButton1-und XButton2-Unterstützung:

-   [**WM- \_ appcommand**](wm-appcommand.md)
-   [**WM \_ ncxbuttondblclk**](wm-ncxbuttondblclk.md)
-   [**WM- \_ ncxbuttondown**](wm-ncxbuttondown.md)
-   [**WM- \_ ncxbuttonup**](wm-ncxbuttonup.md)
-   [**WM- \_ xbuttondblclk**](wm-xbuttondblclk.md)
-   [**WM- \_ xbuttondown**](wm-xbuttondown.md)
-   [**WM- \_ xbuttonup**](wm-xbuttonup.md)
-   [**Mouselhuokstructex**](/windows/win32/api/winuser/ns-winuser-mousehookstructex)

Die folgenden APIs wurden geändert, um diese Schaltflächen zu unterstützen:

-   [**Maus \_ Ereignis**](/windows/win32/api/winuser/nf-winuser-mouse_event)
-   [**Shellproc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
-   [**Msllhuokstruct**](/windows/win32/api/winuser/ns-winuser-msllhookstruct)
-   [**Mouseinput**](/windows/win32/api/winuser/ns-winuser-mouseinput)
-   [**WM- \_ Parser**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)

Es ist unwahrscheinlich, dass ein untergeordnetes Fenster in einer Komponenten Anwendung Befehle für XButton1 und XButton2 direkt implementieren kann. Daher sendet [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) eine [**WM- \_ appcommand**](wm-appcommand.md) -Meldung an ein Fenster, wenn auf eine X-Schaltfläche geklickt wird. **Defwindowproc** sendet außerdem die **WM- \_ appcommand** -Nachricht an das übergeordnete Fenster. Dies ähnelt der Art und Weise, wie Kontextmenüs mit einem Rechtsklick aufgerufen werden –**defwindowproc** sendet eine [**WM- \_ ContextMenu**](/windows/desktop/menurc/wm-contextmenu) -Meldung an das Menü und sendet Sie an das übergeordnete Element. Wenn **defwindowproc** außerdem eine WM- **\_ appcommand** -Nachricht für ein Fenster der obersten Ebene empfängt, wird ein ShellHook mit dem Code hshell \_ appcommand aufgerufen.

Es gibt Unterstützung für die Tastaturen mit zusätzlichen Schlüsseln für Browserfunktionen, Medienfunktionen, Anwendungs Starts und die Energie Verwaltung. Weitere Informationen finden Sie unter [Tastaturtasten für das Browsen und andere Funktionen](about-keyboard-input.md).

## <a name="mouse-messages"></a>Maus Meldungen

Die Maus generiert ein Eingabe Ereignis, wenn der Benutzer die Maus bewegt oder eine Maustaste drückt oder loslässt. Das System konvertiert Mauseingabe Ereignisse in Nachrichten und sendet Sie in der Meldungs Warteschlange des entsprechenden Threads. Wenn Maus Meldungen schneller gepostet werden, als Sie von einem Thread verarbeitet werden können, verwirft das System alle bis auf die aktuellste Maus Nachricht.

Ein Fenster empfängt eine Maus Meldung, wenn ein Maus Ereignis auftritt, während sich der Cursor innerhalb der Rahmen des Fensters befindet oder wenn das Fenster die Maus erfasst hat. Maus Nachrichten werden in zwei Gruppen unterteilt: Client Bereichs Meldungen und nicht-Client Bereichs Nachrichten. In der Regel verarbeitet eine Anwendung Client Bereichs Nachrichten und ignoriert nicht-Client Bereichs Nachrichten.

Dieser Abschnitt enthält die folgenden Themen:

-   [Client Bereich-Maus Meldungen](#client-area-mouse-messages)
-   [Nicht-Client-Bereich-Maus Meldungen](#nonclient-area-mouse-messages)
-   [Die WM- \_ nchittest-Meldung](/windows)

### <a name="client-area-mouse-messages"></a>Client Bereich-Maus Meldungen

Ein Fenster empfängt eine Client Bereich-Maus Nachricht, wenn ein Maus Ereignis innerhalb des Client Bereichs des Fensters auftritt. Das System stellt die [**WM- \_ mousetmove**](wm-mousemove.md) -Meldung an das Fenster an, wenn der Benutzer den Cursor innerhalb des Client Bereichs verschiebt. Sie sendet eine der folgenden Meldungen, wenn der Benutzer eine Maustaste drückt oder loslässt, während sich der Cursor im Client Bereich befindet.



| Nachricht                                       | Bedeutung                                     |
|-----------------------------------------------|---------------------------------------------|
| [**WM \_ lbuttondblclk**](wm-lbuttondblclk.md) | Es wurde auf die linke Maustaste Doppel geklickt.   |
| [**WM \_ lbuttondown**](wm-lbuttondown.md)     | Die linke Maustaste wurde gedrückt.          |
| [**WM- \_ lbuttonup**](wm-lbuttonup.md)         | Die linke Maustaste wurde losgelassen.         |
| [**WM- \_ mbuttondblclk**](wm-mbuttondblclk.md) | Es wurde auf die mittlere Maustaste Doppel geklickt. |
| [**WM- \_ mbuttondown**](wm-mbuttondown.md)     | Die mittlere Maustaste wurde gedrückt.        |
| [**WM- \_ mbuttonup**](wm-mbuttonup.md)         | Die mittlere Maustaste wurde losgelassen.       |
| [**WM- \_ rbuttondblclk**](wm-rbuttondblclk.md) | Auf die Rechte Maustaste wurde Doppel geklickt.  |
| [**WM- \_ rbuttondown**](wm-rbuttondown.md)     | Die rechte Maustaste wurde gedrückt.         |
| [**WM- \_ rbuttonup**](wm-rbuttonup.md)         | Die Rechte Maustaste wurde losgelassen.        |
| [**WM- \_ xbuttondblclk**](wm-xbuttondblclk.md) | Es wurde auf eine X-Maustaste Doppel geklickt.       |
| [**WM- \_ xbuttondown**](wm-xbuttondown.md)     | Eine X-Maustaste wurde gedrückt.              |
| [**WM- \_ xbuttonup**](wm-xbuttonup.md)         | Eine X-Maustaste wurde losgelassen.             |



 

Außerdem kann eine Anwendung die [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) -Funktion aufrufen, damit das System zwei andere Nachrichten sendet. Sie sendet die [**WM- \_ MouseHover**](wm-mousehover.md) -Nachricht, wenn der Cursor für einen bestimmten Zeitraum über den Client Bereich bewegt wird. Sie sendet die [**WM- \_ MouseLeave**](wm-mouseleave.md) -Nachricht, wenn der Cursor den Client Bereich verlässt.

### <a name="message-parameters"></a>Nachrichten Parameter

Der *LPARAM* -Parameter einer Client Bereich-Maus Meldung gibt die Position des Cursor-Hot-Spots an. Das nieder wertige Wort gibt die x-Koordinate des Hotspots an, und das hochwertige Wort gibt die y-Koordinate an. Die Koordinaten werden in Client Koordinaten angegeben. Im Client Koordinatensystem werden alle Punkte auf dem Bildschirm relativ zu den Koordinaten (0,0) der oberen linken Ecke des Client Bereichs angegeben.

Der *wParam* -Parameter enthält Flags, die den Status der anderen Maustasten und die STRG-Taste und die UMSCHALTTASTE zum Zeitpunkt des Maus Ereignisses angeben. Sie können diese Flags überprüfen, wenn die Maus Nachrichtenverarbeitung vom Zustand einer anderen Maustaste oder von der STRG-oder der Umschalttaste abhängt. Der *wParam* -Parameter kann eine Kombination der folgenden Werte sein.



| Wert            | BESCHREIBUNG                      |
|------------------|----------------------------------|
| **MK- \_ Steuerelement**  | Die STRG-Taste ist nicht gedrückt.            |
| **MK \_ lbutton**  | Die linke Maustaste ist nicht mehr vorhanden.   |
| **MK- \_ MButton**  | Die mittlere Maustaste ist nicht mehr angezeigt. |
| **MK \_ rbutton**  | Die Rechte Maustaste ist nicht mehr angezeigt.  |
| **MK \_ UMSCHALT**    | Die UMSCHALTTASTE ist nicht mehr festgelegt.           |
| **MK \_ XButton1** | Die erste X-Schaltfläche ist nicht angezeigt.      |
| **MK \_ XButton2** | Die zweite X-Schaltfläche ist nicht mehr festgelegt.     |



 

### <a name="double-click-messages"></a>Double-Click Meldungen

Das System generiert eine Doppelklick Nachricht, wenn der Benutzer zweimal in der schnell Folge auf eine Maustaste klickt. Wenn der Benutzer auf eine Schaltfläche klickt, erstellt das System ein Rechteck, das sich um den Cursor-Hotspot dreht. Außerdem wird die Uhrzeit gekennzeichnet, zu der der Klick aufgetreten ist. Wenn der Benutzer ein zweites Mal auf dieselbe Schaltfläche klickt, bestimmt das System, ob sich der Hotspot noch innerhalb des Rechtecks befindet, und berechnet die verstrichene Zeit seit dem ersten klicken. Wenn sich der Hotspot noch innerhalb des Rechtecks befindet und die verstrichene Zeit den Doppelklick-Timeout Wert nicht überschreitet, generiert das System eine Doppelklick Nachricht.

Eine Anwendung kann Timeout Werte für den Doppelklick mithilfe der Funktionen [**getdoubleclicktime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime) und [**setdoubleclicktime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime) erhalten und festlegen. Alternativ kann die Anwendung den Timeout Wert für den Doppelklick – mit dem SPI-Flag **\_ setdoubleclicktime** und der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion festlegen. Sie kann auch die Größe des Rechtecks festlegen, das vom System zum Erkennen von Doppelklicks verwendet wird, indem die SPI-Flags **\_ setdoubleclkwidth** und **SPI \_ setdoubleclkheight** an **SystemParametersInfo** übergeben werden. Beachten Sie jedoch, dass das Festlegen des Timeout Werts für den Doppelklick – und das Rechteck alle Anwendungen betrifft.

Ein von der Anwendung definiertes Fenster empfängt standardmäßig keine Doppelklick Nachrichten. Aufgrund des System Aufwands beim Generieren von Doppelklick-Nachrichten werden diese Nachrichten nur für Windows generiert, die zu Klassen gehören, die über den Klassen Stil **CS \_ dblclert** verfügen. Die Anwendung muss diesen Stil festlegen, wenn die Fenster Klasse registriert wird. Weitere Informationen finden Sie unter [Fenster Klassen](/windows/desktop/winmsg/window-classes).

Eine Doppelklick Nachricht ist immer die dritte Nachricht in einer Serie mit vier Nachrichten. Bei den ersten beiden Nachrichten handelt es sich um die Schaltflächen-und Schaltflächen, die durch den ersten Mausklick generiert werden. Mit dem zweiten Klick wird die Doppelklick Nachricht generiert, gefolgt von einer weiteren Schaltfläche nach oben. Wenn Sie z. b. mit der linken Maustaste doppelklicken, wird die folgende Nachrichten Sequenz generiert:

1.  [**WM \_ lbuttondown**](wm-lbuttondown.md)
2.  [**WM- \_ lbuttonup**](wm-lbuttonup.md)
3.  [**WM \_ lbuttondblclk**](wm-lbuttondblclk.md)
4.  [**WM- \_ lbuttonup**](wm-lbuttonup.md)

Da ein Fenster immer eine Schaltfläche nach unten empfängt, bevor eine Doppelklick Nachricht empfangen wird, verwendet eine Anwendung in der Regel eine Doppelklick Nachricht, um eine Aufgabe zu erweitern, die Sie während einer Schaltfläche nach unten gestartet hat. Wenn der Benutzer z. b. in der Farbpalette von Microsoft Paint auf eine Farbe klickt, zeigt Paint die ausgewählte Farbe neben der Palette an. Wenn der Benutzer auf eine Farbe doppelklickt, zeigt Paint die Farbe an und öffnet das Dialogfeld **Farben bearbeiten** .

### <a name="nonclient-area-mouse-messages"></a>Nicht-Client-Bereich-Maus Meldungen

Ein Fenster empfängt eine nicht-Client Bereichs Maus, wenn ein Maus Ereignis in einem beliebigen Teil eines Fensters mit Ausnahme des Client Bereichs auftritt. Der nicht-Client Bereich eines Fensters besteht aus dessen Rahmen, Menüleiste, Titelleiste, Schiebe Leiste, Fenstermenü, minimieren und Schaltfläche maximieren.

Das System generiert nicht-Client Bereichs Nachrichten in erster Linie für die eigene Verwendung. Beispielsweise verwendet das System nicht-Client Bereichs Nachrichten, um den Cursor in einen Pfeil mit zwei Spitzen zu ändern, wenn der Cursor-Hotspot in den Rahmen eines Fensters verschoben wird. Ein Fenster muss nicht-Client Bereichs Maus-Meldungen an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben, um die integrierte Maus Oberfläche zu nutzen.

Es ist eine entsprechende nicht-Client-Bereich-Maus Meldung für jede Client Bereichs-Maus Nachricht vorhanden. Die Namen dieser Meldungen sind ähnlich, mit der Ausnahme, dass die benannten Konstanten für die nicht-Client Bereichs Nachrichten die Buchstaben NC enthalten. Wenn Sie z. b. den Cursor in den nicht-Client Bereich bewegen, wird eine [**WM- \_ ncmousemove**](wm-ncmousemove.md) -Nachricht generiert. Wenn Sie die linke Maustaste drücken, während sich der Cursor im nicht-Client Bereich befindet, generiert eine [**WM- \_ nclbuttondown**](wm-nclbuttondown.md) -Meldung.

Der *LPARAM* -Parameter einer nicht-Client Bereich-Maus Nachricht ist eine Struktur, die die x-und y-Koordinaten des Cursor-Hot-Spots enthält. Anders als Koordinaten von Client Bereich-Maus Nachrichten werden die Koordinaten in Bildschirm Koordinaten anstelle von Client Koordinaten angegeben. Im Bildschirm Koordinatensystem sind alle Punkte auf dem Bildschirm relativ zu den Koordinaten (0,0) der oberen linken Ecke des Bildschirms.

Der *wParam* -Parameter enthält einen Treffer Test Wert, einen Wert, der angibt, an welcher Stelle im nicht-Client Bereich das Maus Ereignis aufgetreten ist. Im folgenden Abschnitt wird der Zweck von Treffer Testwerten erläutert.

### <a name="the-wm_nchittest-message"></a>Die WM- \_ nchittest-Meldung

Jedes Mal, wenn ein Maus Ereignis auftritt, sendet das System eine [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht an das Fenster, das den Cursor Hotspot enthält, oder an das Fenster, das die Maus erfasst hat. Das System verwendet diese Meldung, um zu bestimmen, ob ein Client Bereich oder eine nicht-Client Bereich-Maus Nachricht gesendet werden soll. Eine Anwendung, die Mausbewegung und Maustasten Meldungen empfangen muss, muss die **WM- \_ nchittest** -Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben.

Der *LPARAM* -Parameter der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht enthält die Bildschirm Koordinaten des Cursor-Hot-Spots. Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion untersucht die Koordinaten und gibt einen Treffer Test Wert zurück, der den Speicherort des Hotspots angibt. Der Treffer Test Wert kann einer der folgenden Werte sein.



| Wert             | Speicherort des Hotspots                                                                                                                                                                                |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Htborder"**      | Im Rahmen eines Fensters ohne Größen Anpassungsrahmen.                                                                                                                                       |
| **Htbottom**      | Am unteren horizontalen Rand eines Fensters.                                                                                                                                                         |
| **Htbottomleft**  | In der unteren linken Ecke eines Fensterrahmens.                                                                                                                                                        |
| **Htbottomright** | In der unteren rechten Ecke eines Fensterrahmens.                                                                                                                                                       |
| **Htcaption**     | In einer Titelleiste.                                                                                                                                                                                     |
| **Htclient**      | In einem Client Bereich.                                                                                                                                                                                   |
| **"Htclose"**       | In einer Schaltfläche **Schließen** .                                                                                                                                                                              |
| **HTError**       | Auf dem Bildschirm Hintergrund oder in einer Trennlinie zwischen Fenstern (identisch mit "htnirgendwo", mit der Ausnahme, dass die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion ein Systemsignal erzeugt, um einen Fehler anzugeben). |
| **"Htgrowbox"**     | In einem Größen Feld (identisch mit " **htsize**").                                                                                                                                                                 |
| **Hthelp**        | In einer **Hilfe** Schaltfläche.                                                                                                                                                                               |
| **Hthscroll**     | In einer horizontalen Schiebe Leiste.                                                                                                                                                                         |
| **Htleft**        | Am linken Rand eines Fensters.                                                                                                                                                                     |
| **"Htmenu"**        | In einem Menü.                                                                                                                                                                                          |
| **Htmaxbutton**   | Auf der Schaltfläche **maximieren** .                                                                                                                                                                           |
| **Htminbutton**   | Auf der Schaltfläche **minimieren** .                                                                                                                                                                           |
| **Htnirgendwo**     | Auf dem Bildschirm Hintergrund oder auf einer Trennlinie zwischen Fenstern.                                                                                                                                     |
| **Htreduce**      | Auf der Schaltfläche **minimieren** .                                                                                                                                                                           |
| **Htright**       | Am rechten Rand eines Fensters.                                                                                                                                                                    |
| **"Htsize"**        | In einem Größen Feld (identisch mit " **htgrowbox**").                                                                                                                                                              |
| **"Htsysmenu"**     | In einem **System** Menü oder in einer Schaltfläche **Schließen** in einem untergeordneten Fenster.                                                                                                                                    |
| **Httop**         | Am oberen horizontalen Rand eines Fensters.                                                                                                                                                         |
| **Httopleft**     | In der oberen linken Ecke eines Fensterrahmens.                                                                                                                                                        |
| **Httopright**    | In der oberen rechten Ecke eines Fensterrahmens.                                                                                                                                                       |
| **Httransparent** | In einem Fenster, das zurzeit von einem anderen Fenster im gleichen Thread abgedeckt wird.                                                                                                                                 |
| **Htvscroll**     | Auf der vertikalen Schiebe Leiste.                                                                                                                                                                         |
| **Htzoom**        | Auf der Schaltfläche **maximieren** .                                                                                                                                                                           |



 

Wenn sich der Cursor im Client Bereich eines Fensters befindet, gibt [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) den Wert von " **htclient** Hit-Test" an die Fenster Prozedur zurück. Wenn die Fenster Prozedur diesen Code an das System zurückgibt, konvertiert das System die Bildschirm Koordinaten des Cursor-Hotspots in Client Koordinaten und stellt dann die entsprechende Client Bereich-Maus Nachricht zur Auswahl.

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt einen der anderen Treffer Test Werte zurück, wenn sich der Cursor-Hotspot im nicht-Client Bereich eines Fensters befindet. Wenn die Fenster Prozedur einen dieser Treffer Test Werte zurückgibt, stellt das System eine nicht-Client-Bereich-Maus Nachricht zur Verfügung, wobei der Treffer Test Wert im *wParam* -Parameter der Meldung und die Cursor Koordinaten im *LPARAM* -Parameter abgelegt werden.

## <a name="mouse-sonar"></a>Maus, Sonar

Die Funktion "Mouse Sonar Accessibility" zeigt kurz einige konzentrische Kreise um den Zeiger an, wenn der Benutzer die STRG-Taste drückt und freigibt. Mit dieser Funktion kann ein Benutzer den Mauszeiger auf einem Bildschirm, der überlastet ist, oder mit Auflösung auf hoch, auf einem schlechtesten Qualitäts Monitor oder für Benutzer mit eingeschränkter Sehfähigkeit suchen. Weitere Informationen finden Sie unter den folgenden Flags in [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**SPI \_ getmousesonar**

**SPI- \_ abversions Analyse**

## <a name="mouse-vanish"></a>Maus verschwindet

Mit der Funktion zur Barrierefreiheit der Maus verschwindet wird der Zeiger ausgeblendet, wenn der Benutzer die Eingabe durchläuft Der Mauszeiger wird erneut angezeigt, wenn der Benutzer die Maus bewegt. Diese Funktion verhindert, dass der Zeiger den eingegebenen Text verdeckt, z. b. in einer e-Mail oder einem anderen Dokument. Weitere Informationen finden Sie unter den folgenden Flags in [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**SPI \_ getmouseelvanish**

**SPI-abversions Ausgabe \_**

## <a name="the-mouse-wheel"></a>Das Mausrad

Das Mausrad kombiniert die Funktionen eines Rades und einer Maustaste. Das Rad verfügt über diskrete, gleichmäßig mit Abstand getrennte Notches. Wenn Sie das Rad drehen, wird eine radnachricht an Ihre Anwendung gesendet, sobald jede Kerb gefunden wird. Die Radtaste kann auch als normale Windows-Schaltfläche in der Mitte (dritte) fungieren. Beim Drücken und Freigeben des Mausrades werden Standard- [**WM- \_ mbuttonup**](wm-mbuttonup.md) -und [**WM- \_ mbuttondown**](wm-mbuttondown.md) -Meldungen gesendet. Durch Doppelklicken auf die dritte Schaltfläche wird die standardmäßige [**WM- \_ mbuttondblclk**](wm-mbuttondblclk.md) -Nachricht gesendet.

Das Mausrad wird durch die [**WM- \_ MouseWheel**](wm-mousewheel.md) -Meldung unterstützt.

Beim Drehen der Maus wird die [**WM- \_ MouseWheel**](wm-mousewheel.md) -Meldung an das Fokus Fenster gesendet. Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt die Nachricht an das übergeordnete Fenster des Fensters weiter. Es sollte keine interne Weiterleitung der Nachricht vorhanden sein, da **defwindowproc** Sie in der übergeordneten Kette weitergibt, bis ein Fenster, in dem Sie verarbeitet wird, gefunden wird.

### <a name="determining-the-number-of-scroll-lines"></a>Festlegen der Anzahl der scrolllinien

Anwendungen sollten die [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion verwenden, um die Anzahl der Zeilen abzurufen, die für die einzelnen Bild Lauf Vorgänge in einem Dokument gefiltert werden. Zum Abrufen der Zeilen Anzahl führt eine Anwendung den folgenden Befehl aus:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



Die Variable "pulscrolllines" verweist auf einen ganzzahligen Wert ohne Vorzeichen, der die empfohlene Anzahl von Zeilen für den Bildlauf empfängt, wenn das Mausrad ohne Modifizierertasten gedreht wird:

-   Wenn diese Zahl 0 ist, sollte kein Bildlauf ausgeführt werden.
-   Wenn diese Zahl ein **Rad- \_ PageScroll** ist, sollte ein radrollup so interpretiert werden, dass es in der Bild-ab-oder der Bild Lauf Leiste der Bild Lauf Leiste auf einmal klickt.
-   Wenn die Anzahl der auszuscrollenden Zeilen größer als die Anzahl der angezeigten Zeilen ist, sollte der scrollvorgang auch als Bild-auf-oder Bild-ab-Vorgang interpretiert werden.

Der Standardwert für die Anzahl der scrollzeilen ist 3. Wenn ein Benutzer die Anzahl der Bild Lauf Linien mithilfe des Maus Eigenschaften Blatts in der Systemsteuerung ändert, überträgt das Betriebssystem eine [**WM- \_ settingchange**](../winmsg/wm-settingchange.md) -Meldung an alle Fenster der obersten Ebene, wobei **SPI \_ setwheelscrolllines** angegeben ist. Wenn eine Anwendung die **WM- \_ settingchange** -Nachricht empfängt, kann Sie die neue Anzahl von scrollzeilen abrufen, indem Sie Folgendes aufrufen:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



### <a name="controls-that-scroll"></a>Steuerelemente zum Scrollen

In der folgenden Tabelle sind die Steuerelemente mit scrollfunktionen (einschließlich der vom Benutzer festgelegten Bild Lauf Zeilen) aufgelistet. 

| Control                 | Bildlauf                                                                                                                                                               |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Steuerelement bearbeiten            | Vertikal und horizontal.                                                                                                                                                |
| Listenfeld-Steuerelement        | Vertikal und horizontal.                                                                                                                                                |
| Kombinationsfeld               | Wenn die Option nicht gelöscht wird, ruft jeder Bild Lauf das nächste oder vorherige Element ab. Beim Ablegen leitet jeder scrollvorgang die Nachricht an das Listenfeld weiter, das entsprechend einen Bildlauf durchführt. |
| Cmd (Befehlszeile)      | Vertikal.                                                                                                                                                               |
| Strukturansicht               | Vertikal und horizontal.                                                                                                                                                |
| Listenansicht               | Vertikal und horizontal.                                                                                                                                                |
| Bildlauf nach oben/nach unten         | Ein Element gleichzeitig.                                                                                                                                                     |
| TrackBar-Scrollleiste        | Ein Element gleichzeitig.                                                                                                                                                     |
| Microsoft Rich Edit 1,0 | Vertikal. Beachten Sie, dass der Exchange-Client seine eigenen Versionen der Listenansicht und Strukturansicht-Steuerelemente enthält, die keine Wheel-Unterstützung haben.                                        |
| Microsoft Rich Edit 2,0 | Vertikal.                                                                                                                                                               |



 

### <a name="detecting-a-mouse-with-a-wheel"></a>Erkennen einer Maus mit einem Rad

Um zu ermitteln, ob eine Maus mit einem Rad verbunden ist, müssen Sie [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) mit **SM \_ MouseWheelPresent** aufrufen. Der Rückgabewert **true** gibt an, dass die Maus verbunden ist.

Das folgende Beispiel erfolgt aus der Fenster Prozedur für ein mehrzeilige Bearbeitungs Steuerelement:


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

Wenn der Benutzer auf ein inaktives Fenster der obersten Ebene oder das untergeordnete Fenster eines inaktiven Fensters der obersten Ebene klickt, sendet das System die [**WM- \_ mouseaktivierungs**](wm-mouseactivate.md) -Nachricht (unter anderem) an das Fenster der obersten Ebene oder an das untergeordnete Fenster. Das System sendet diese Nachricht nach dem Bereitstellen der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht an das Fenster, jedoch vor dem Veröffentlichen der Schaltfläche mit der Schaltfläche. Wenn **WM \_ mouseaktivierungs** an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion weitergegeben wird, aktiviert das System das Fenster der obersten Ebene und stellt dann die Schaltfläche auf der obersten Ebene oder im untergeordneten Fenster wieder her.

Durch die Verarbeitung von [**WM \_ mouseaktivierungs**](wm-mouseactivate.md)kann ein Fenster steuern, ob das Fenster der obersten Ebene das aktive Fenster ist, das durch einen Mausklick angezeigt wird, und ob das Fenster, auf das geklickt wurde, die nachfolgende Schaltfläche nach unten empfängt. Dies erfolgt durch Zurückgeben eines der folgenden Werte nach der Verarbeitung von **WM \_ mousaktivierungs**.



| Wert                    | Bedeutung                                                              |
|--------------------------|----------------------------------------------------------------------|
| **MA- \_ Aktivierung**         | Aktiviert das Fenster, und die Maus Meldung wird nicht verworfen.         |
| **MA \_ noaktivierungs**       | Das Fenster wird nicht aktiviert, und die Maus Meldung wird nicht verworfen. |
| **MA \_ activateandeat**   | Aktiviert das Fenster und verwirft die Maus Meldung.                 |
| **MA \_ noactivateandeat** | Aktiviert das Fenster nicht, sondern verwirft die Maus Nachricht.         |

## <a name="see-also"></a>Siehe auch

[Nutzen der High-Definition Mausbewegung](../dxtecharts/taking-advantage-of-high-dpi-mouse-movement.md)