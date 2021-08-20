---
title: Informationen zu Trackbar-Steuerelementen
description: Eine Trackbar ist ein Fenster, das einen Schieberegler (manchmal als Strich bezeichnet) in einem Kanal und optionale Teilstriche enthält. Wenn der Benutzer den Schieberegler mit der Maus oder den Richtungsschlüsseln bewegt, sendet die Trackleiste Benachrichtigungsmeldungen, um die Änderung anzugeben.
ms.assetid: 9fc7bef8-da1d-493b-9a9a-3770873713f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450fba1c9b41cf5789bcda08263ff7a0b8b2d2d17db3746cf5d47bdc5d0b6a4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967940"
---
# <a name="about-trackbar-controls"></a>Informationen zu Trackbar-Steuerelementen

Eine Trackbar ist ein Fenster, das einen Schieberegler (manchmal als Strich bezeichnet) in einem Kanal und optionale Teilstriche enthält. Wenn der Benutzer den Schieberegler mit der Maus oder den Richtungsschlüsseln bewegt, sendet die Trackleiste Benachrichtigungsmeldungen, um die Änderung anzugeben.

-   [Auswahlbereich](#selection-range)
-   [Trackbar-Meldungen](#trackbar-messages)
-   [Trackbar-Benachrichtigungsmeldungen](#trackbar-notification-messages)
-   [Standardverarbeitung von Trackbar-Nachrichten](#default-trackbar-message-processing)
-   [Trackbar-QuickInfos](#trackbar-tooltips)

Trackleisten sind nützlich, wenn Sie möchten, dass der Benutzer einen diskreten ganzzahligen Wert ohne Vorzeichen oder einen Satz aufeinanderfolgender ganzzahliger Werte ohne Vorzeichen in einem Bereich auswählt. Sie können z. B. eine Trackleiste verwenden, um dem Benutzer das Festlegen der Wiederholungsrate der Tastatur zu ermöglichen, indem Sie den Schieberegler auf ein bestimmtes Teilstrich bewegen. Die folgende Abbildung zeigt eine typische Trackleiste.

![Screenshot einer Trackleiste mit Bezeichnungen an den Enden für langsam und schnell](images/tkb-simple.png)

Der Schieberegler in einer Trackleiste wird in Schritten bewegt, die Sie beim Erstellen angeben. Die Werte in diesem Bereich werden als logische Einheiten bezeichnet. Wenn Sie beispielsweise angeben, dass die Trackleiste logische Einheiten im Bereich von 0 bis 5 haben soll, kann der Schieberegler nur sechs Positionen belegen: eine Position auf der linken Seite der Trackleiste und eine Position für jedes Inkrement im Bereich. In der Regel wird jede dieser Positionen durch ein Teilstrich identifiziert. Die Anzahl der Teilstriche ist jedoch beliebig und kann geringer als die Anzahl der logischen Positionen sein.

Sie erstellen eine Trackbar mithilfe der [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) und geben die [**TRACKBAR \_ CLASS-Fensterklasse**](common-control-window-classes.md) an. Nachdem Sie eine Trackleiste erstellt haben, können Sie trackbar-Meldungen verwenden, um viele ihrer Eigenschaften zu festlegen und abzurufen. Änderungen, die Sie vornehmen können, umfassen das Festlegen der minimalen und maximalen Positionen für den Schieberegler, das Zeichnen von Teilstrichen, das Festlegen eines Auswahlbereichs und das Neupositionieren des Schiebereglers.

## <a name="selection-range"></a>Auswahlbereich

Wenn Sie eine Trackleiste mit dem [**TBS \_ ENABLESELRANGE-Stil**](trackbar-control-styles.md) erstellen, können Sie einen Auswahlbereich angeben. Die Trackleiste hebt den Auswahlbereich hervor und zeigt dreieckige Teilstriche am Anfang und Ende an, wie in der folgenden Abbildung dargestellt.

![Screenshot einer Trackleiste mit hervorgehobenen Bereich](images/tkb-selrange.png)

Der Auswahlbereich der Trackleiste hat keinerlei Auswirkungen auf die Funktionalität. Es liegt an der Anwendung, den Bereich zu implementieren. Dies kann auf eine der folgenden Arten erfolgen:

-   Verwenden Sie einen Auswahlbereich, um dem Benutzer das Festlegen von Höchst- und Mindestwerten für einen Parameter zu ermöglichen. Beispielsweise könnte der Benutzer den Schieberegler an eine Position verschieben und dann auf eine Schaltfläche mit der Bezeichnung "Max" klicken. Die Anwendung legt dann den Auswahlbereich fest, um die vom Benutzer ausgewählten Werte zu zeigen.
-   Beschränken Sie die Bewegung des Schiebereglers auf einen vordefinierten Unterbereich innerhalb des Steuerelements, indem Sie die [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Benachrichtigung**](wm-vscroll.md) behandeln und jede Bewegung außerhalb des Auswahlbereichs nicht zu. Dies können Sie beispielsweise tun, wenn sich der Wertebereich, der dem Benutzer zur Verfügung steht, aufgrund anderer Entscheidungen des Benutzers oder entsprechend den verfügbaren Ressourcen ändern kann.

## <a name="trackbar-messages"></a>Trackbar-Meldungen

Die logischen Einheiten einer Trackleiste sind der Satz zusammenhängender Werte, die die Trackleiste darstellen kann. Sie werden normalerweise definiert, indem der Bereich möglicher Werte mit einer [**TBM \_ SETRANGE-Meldung**](tbm-setrange.md) angegeben wird, sobald die Trackleiste erstellt wurde. Anwendungen können den Bereich dynamisch ändern, indem **sie TBM \_ SETRANGE,** [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)oder [**TBM \_ SETRANGEMIN verwenden.**](tbm-setrangemin.md)

Um die Position des Schiebereglers (d. h. den vom Benutzer ausgewählten Wert) abzurufen, verwenden Sie die [**TBM \_ GETPOS-Nachricht.**](tbm-getpos.md) Verwenden Sie zum Festlegen der Position des Schiebereglers die [**TBM \_ SETPOS-Meldung.**](tbm-setpos.md)

Eine Trackleiste zeigt automatisch Teilstriche am Anfang und Ende an, es sei denn, Sie geben den [**TBS \_ NOTICKS-Stil**](trackbar-control-styles.md) an. (Im ressourcen Microsoft Visual Studio-Editor bedeutet dies, dass die Eigenschaft Teilstriche auf False festgelegt wird.) Sie können das [**TBS \_ AUTOTICKS-Format**](trackbar-control-styles.md) verwenden, um automatisch zusätzliche Teilstriche in regelmäßigen Abständen entlang der Trackleiste anzuzeigen. Standardmäßig zeigt eine **TBS \_ AUTOTICKS-Trackleiste** bei jedem Inkrement des Bereichs der Trackleiste einen Teilstrich an. Um ein anderes Intervall für die automatischen Teilstriche anzugeben, senden Sie die [**TBM \_ SETTICFREQ-Nachricht**](tbm-setticfreq.md) an die Trackleiste. Sie können diese Meldung beispielsweise verwenden, um nur 10 Teilstriche im Bereich von 1 bis 100 anzuzeigen.

Um die Position eines einzelnen Teilstrichs fest zu legen, senden Sie die [**\_ TBM SETTIC-Nachricht.**](tbm-settic.md) Eine Trackleiste verwaltet ein Array von DWORD-Werten, das die Position der einzelnen Teilstriche speichert. Das Array enthält nicht die ersten und letzten Teilstriche, die von der Trackleiste automatisch erstellt werden. Sie können einen Index in diesem Array angeben, wenn Sie die [**TBM \_ GETTIC-Nachricht**](tbm-gettic.md) senden, um die Position des entsprechenden Teilstrichs abzurufen. Alternativ können Sie die [**TBM \_ GETPTICS-Nachricht**](tbm-getptics.md) senden, um einen Zeiger auf das Array abzurufen. Die Anzahl der Elemente im Array ist gleich zwei kleiner als die Anzahl der Ticks, die von der [**TBM \_ GETNUMTICS-Nachricht zurückgegeben**](tbm-getnumtics.md) werden. Dies liegt daran, dass die von **TBM \_ GETNUMTICS** zurückgegebene Anzahl die ersten und letzten Teilstriche enthält, die nicht im Array enthalten sind. Um die physische Position eines Teilstrichs abzurufen, senden Sie in Clientkoordinaten des Fensters der Trackleiste die [**TBM \_ GETTICPOS-Nachricht.**](tbm-getticpos.md) Die [**\_ CLEARTICS-Nachricht von TBM**](tbm-cleartics.md) entfernt alle Teilstriche einer Trackleiste bis auf den ersten und letzten.

Die Liniengröße einer Trackleiste bestimmt, wie weit der Schieberegler als Reaktion auf Tastatureingaben von den Pfeiltasten bewegt wird, z. B. die NACH-RECHTS- oder NACH-UNTEN-TASTE. Zum Abrufen oder Festlegen der Zeilengröße senden Sie die [**TBM \_ GETLINESIZE-**](tbm-getlinesize.md) und [**TBM \_ SETLINESIZE-Meldungen.**](tbm-setlinesize.md) Die Trackleiste sendet auch die TB \_ LINEUP- und TB LINEDOWN-Benachrichtigungscodes an das übergeordnete Fenster, wenn der Benutzer \_ die Pfeiltasten drückt.

Die Seitengröße einer Trackleiste bestimmt, wie weit der Schieberegler als Reaktion auf Tastatureingaben bewegt wird, z. B. die BILD-NACH-OBEN- oder BILD-NACH-UNTEN-TASTE oder Mauseingaben, z. B. Klicks im Trackleistenkanal. Zum Abrufen oder Festlegen der Seitengröße senden Sie die [**TBM \_ GETPAGESIZE-**](tbm-getpagesize.md) und [**TBM \_ SETPAGESIZE-Meldungen.**](tbm-setpagesize.md) Die Trackleiste sendet auch die TB \_ PAGEUP- und TB PAGEDOWN-Benachrichtigungscodes an das übergeordnete Fenster, wenn sie Tastatur- oder Mauseingaben empfängt, die \_ auf der Seite scrollen. Weitere Informationen finden Sie unter [Trackbar-Benachrichtigungsmeldungen.](#trackbar-notification-messages)

Eine Anwendung kann Nachrichten senden, um die Dimensionen einer Trackleiste abzurufen. Die [**TBM \_ GETTHUMBRECT-Nachricht**](tbm-getthumbrect.md) ruft das umschließende Rechteck für den Schieberegler ab. Die [**TBM \_ GETTHUMBLENGTH-Nachricht**](tbm-getthumblength.md) ruft die Länge des Schiebereglers ab. Die [**TBM \_ GETCHANNELRECT-Nachricht**](tbm-getchannelrect.md) ruft das umgebundene Rechteck für den Kanal der Trackleiste ab. Dies ist der Bereich, über den sich der Schieberegler bewegt. Sie enthält die Hervorhebung, wenn ein Bereich ausgewählt wird. Wenn eine Trackleiste das [**TBS \_ FIXEDLENGTH-Format**](trackbar-control-styles.md) hat, können Sie die [**\_ TBM-Nachricht SETTHUMBLENGTH**](tbm-setthumblength.md) senden, um die Länge des Schiebereglers zu ändern.

Sie rufen den Auswahlbereich ab oder legen den Auswahlbereich fest, indem Sie Nachrichten an die Trackleiste senden. Verwenden Sie die [**TBM \_ SETSEL-Meldung,**](tbm-setsel.md) um die Anfangs- und Endpositionen einer Auswahl zu setzen. Um nur die Anfangsposition oder nur die Endposition einer Auswahl zu setzen, senden Sie eine [**TBM \_ SETSELSTART-**](tbm-setselstart.md) oder [**TBM \_ SETSELEND-Nachricht.**](tbm-setselend.md) Um die Anfangs- oder Endpositionen eines Auswahlbereichs abzurufen, senden Sie eine [**TBM \_ GETSELSTART-**](tbm-getselstart.md) oder [**TBM \_ GETSELEND-Nachricht.**](tbm-getselend.md) Um einen Auswahlbereich zu löschen und den ursprünglichen Bereich der Trackleiste wiederherzustellen, senden Sie die [**TBM \_ CLEARSEL-Nachricht.**](tbm-clearsel.md)

> [!Note]  
> Es liegt in der Verantwortung der Anwendung sicherzustellen, dass der Benutzer keine Werte außerhalb des Auswahlbereichs auswählen kann. Das Steuerelement selbst verhindert nicht, dass der Benutzer den Schieberegler außerhalb des Bereichs bewegt.

 

## <a name="trackbar-notification-messages"></a>Trackbar-Benachrichtigungsmeldungen

Eine Trackleiste benachrichtigt das übergeordnete Fenster über Benutzeraktionen, indem sie dem übergeordneten Element eine [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) sendet. Eine Trackleiste mit dem [**TBS \_ HORZ-Stil**](trackbar-control-styles.md) sendet **WM \_ HSCROLL-Nachrichten.** Eine Trackleiste im [**TBS \_ VERT-Stil**](trackbar-control-styles.md) sendet **WM \_ VSCROLL-Nachrichten.** Das niedrige Wort des *wParam-Parameters* von **WM \_ HSCROLL** oder **WM \_ VSCROLL** enthält den Benachrichtigungscode. Für die Benachrichtigungscodes TB THUMBPOSITION und TB THUMBTRACK gibt das obere Wort des \_ \_ *wParam-Parameters* die Position des Schiebereglers an. Für alle anderen Benachrichtigungscodes ist das obere Wort 0 (null). Senden Sie die [**TBM \_ GETPOS-Nachricht,**](tbm-getpos.md) um die Position des Schiebereglers zu bestimmen. Der *lParam-Parameter* ist das Handle für die Trackleiste.

Das System sendet die Benachrichtigungscodes TB BOTTOM, TB LINEDOWN, TB LINEUP und TB TOP nur, wenn der Benutzer mit einer Trackbar über die \_ \_ Tastatur \_ \_ interagiert. Die TB \_ THUMBPOSITION- und TB \_ THUMBTRACK-Benachrichtigungscodes werden nur gesendet, wenn der Benutzer die Maus verwendet. Die \_ TB-Benachrichtigungscodes ENDTRACK, TB PAGEDOWN und \_ TB \_ PAGEUP werden in beiden Fällen gesendet. In der folgenden Tabelle sind die Trackbar-Benachrichtigungscodes und die Ereignisse (Virtuelle Schlüsselcodes oder Mausereignisse) aufgeführt, die dazu führen, dass die [**Benachrichtigungen**](/windows/desktop/inputdev/virtual-key-codes)für virtuelle Schlüsselcodes gesendet werden.



| Benachrichtigungscode | Gesendete Ursache                                                                                                                     |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| TB \_ BOTTOM        | [**VK \_ END**](/windows/desktop/inputdev/virtual-key-codes)                                                                         |
| TB \_ ENDTRACK      | [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) (der Benutzer hat einen Schlüssel freigegeben, der einen relevanten virtuellen Schlüsselcode gesendet hat)                              |
| \_TB-LINEDOWN      | [**VK \_ RIGHT**](/windows/desktop/inputdev/virtual-key-codes) oder [ **VK \_ DOWN**](/windows/desktop/inputdev/virtual-key-codes)     |
| TB \_ LINEUP        | [**VK \_ LEFT**](/windows/desktop/inputdev/virtual-key-codes) oder [ **VK \_ UP**](/windows/desktop/inputdev/virtual-key-codes)              |
| TB \_ PAGEDOWN      | [**VK \_ WEITER**](/windows/desktop/inputdev/virtual-key-codes) (der Benutzer hat auf den Kanal unten oder rechts neben dem Schieberegler geklickt)   |
| TB \_ PAGEUP        | [**VK \_ PRIOR**](/windows/desktop/inputdev/virtual-key-codes) (der Benutzer hat auf den Kanal oben oder links vom Schieberegler geklickt) |
| TB \_ THUMBPOSITION | [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) nach einem \_ TB THUMBTRACK-Benachrichtigungscode                                         |
| TB \_ THUMBTRACK    | Schiebereglerbewegung (der Benutzer hat den Schieberegler gezogen)                                                                                   |
| TB \_ TOP           | [**VK \_ HOME**](/windows/desktop/inputdev/virtual-key-codes)                                                                      |



 

## <a name="default-trackbar-message-processing"></a>Standardverarbeitung von Trackbarnachrichten

In diesem Abschnitt wird die Fensternachrichtenverarbeitung beschrieben, die von einer Trackleiste ausgeführt wird.



| `Message`                                              | Verarbeitung erfolgt                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAPTURECHANGED**](/windows/desktop/inputdev/wm-capturechanged) | Kills the timer if one was set during [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) processing and sends the TB \_ THUMBPOSITION notification code, if if necessary. Er sendet immer den \_ TB-ENDTRACK-Benachrichtigungscode.                                     |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                   | Führt eine zusätzliche Initialisierung durch, z. B. festlegen der Zeilengröße, Seitengröße und Taktmarkierungshäufigkeit auf Standardwerte.                                                                                                                                 |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)                 | Gibt Ressourcen frei.                                                                                                                                                                                                                                         |
| [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)                   | Bemalt das Trackbarfenster neu.                                                                                                                                                                                                                            |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)           | Löscht den Fensterhintergrund unter Verwendung der aktuellen Hintergrundfarbe für die Trackleiste.                                                                                                                                                                       |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)           | Gibt den DLGC \_ WANTGC-WERT ZURÜCK.                                                                                                                                                                                                                      |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)               | Verarbeitet die Richtungsschlüssel und sendet nach Bedarf die \_ \_ Benachrichtigungscodes TB TOP, TB BOTTOM, TB \_ PAGEUP, TB \_ PAGEDOWN, TB \_ LINEUP und TB \_ LINEDOWN.                                                                                               |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)                   | Sendet den \_ TB-ENDTRACK-Benachrichtigungscode, wenn der Schlüssel einer der Richtungsschlüssel war.                                                                                                                                                                       |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)           | Bemalt das Trackbarfenster neu.                                                                                                                                                                                                                            |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)       | Legt den Fokus und die Mausaufnahme auf die Trackleiste fest. Bei Bedarf wird ein Timer festgelegt, der bestimmt, wie schnell sich der Schieberegler zum Mauszeiger bewegt, wenn der Benutzer die Maustaste im Fenster gedrückt hält.                                      |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)           | Gibt die Mauserfassung frei und beendet den Timer, wenn während der [**\_ WM-LBUTTONDOWN-Verarbeitung**](/windows/desktop/inputdev/wm-lbuttondown) ein Timer festgelegt wurde. Bei Bedarf wird der TB \_ THUMBPOSITION-Benachrichtigungscode gesendet. Er sendet immer den \_ TB-ENDTRACK-Benachrichtigungscode. |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)           | Verschiebt den Schieberegler und sendet den TB \_ THUMBTRACK-Benachrichtigungscode beim Nachverfolgen der Maus (siehe [**WM \_ TIMER**](/windows/desktop/winmsg/wm-timer)).                                                                                                                          |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                        | Zeichnet die Trackleiste. Wenn der wParam-Parameter ungleich NULL ist, geht das Steuerelement davon aus, dass der Wert ein HDC ist und zeichnet mit diesem Gerätekontext.                                                                                                             |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)             | Bemalt das Trackbarfenster neu.                                                                                                                                                                                                                            |
| [**\_WM-GRÖßE**](/windows/desktop/winmsg/wm-size)                       | Legt die Abmessungen der Trackleiste fest und entfernt den Schieberegler, wenn nicht genügend Platz zum Anzeigen vorhanden ist.                                                                                                                                                      |
| [**WM \_ TIMER**](/windows/desktop/winmsg/wm-timer)                     | Ruft die Mausposition ab und aktualisiert die Position des Schiebereglers. (Er wird nur empfangen, wenn der Benutzer den Schieberegler zieht.)                                                                                                                         |
| [**WM \_ WININICHANGE**](/windows/desktop/winmsg/wm-wininichange)       | Initialisiert Schiebereglerdimensionen.                                                                                                                                                                                                                           |



 

## <a name="trackbar-tooltips"></a>QuickInfos zur Trackbar

Eine Trackleiste, die mit dem [**TBS \_ TOOLTIPS-Stil**](trackbar-control-styles.md) erstellt wird, verfügt über ein Standard-QuickInfo-Steuerelement. Die QuickInfo bleibt sichtbar und zeigt den aktuellen Wert an, während der Benutzer den Schieberegler mit der Maus zieht.

Sie können einer Trackleiste ein neues QuickInfo-Steuerelement zuweisen, indem Sie die [**TBM \_ SETTOOLTIPS-Nachricht**](tbm-settooltips.md) senden. Verwenden Sie die [**TBM \_ GETTOOLTIPS-Nachricht,**](tbm-gettooltips.md) um das Handle für ein zugewiesenes QuickInfo-Steuerelement abzurufen.

 

 