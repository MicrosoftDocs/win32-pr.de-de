---
title: Informationen zu TrackBar-Steuerelementen
description: Eine TrackBar ist ein Fenster, das einen Schieberegler (manchmal als Ziehpunkt bezeichnet) in einem Kanal und optionale Teil Striche enthält. Wenn der Benutzer den Schieberegler mit der Maus oder der Richtungs Taste verschiebt, sendet die TrackBar Benachrichtigungs Meldungen, um die Änderung anzuzeigen.
ms.assetid: 9fc7bef8-da1d-493b-9a9a-3770873713f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e364f57a094ed5a29369a00a112150d0282f24
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730489"
---
# <a name="about-trackbar-controls"></a>Informationen zu TrackBar-Steuerelementen

Eine TrackBar ist ein Fenster, das einen Schieberegler (manchmal als Ziehpunkt bezeichnet) in einem Kanal und optionale Teil Striche enthält. Wenn der Benutzer den Schieberegler mit der Maus oder der Richtungs Taste verschiebt, sendet die TrackBar Benachrichtigungs Meldungen, um die Änderung anzuzeigen.

-   [Auswahlbereich](#selection-range)
-   [TrackBar-Meldungen](#trackbar-messages)
-   [TrackBar-Benachrichtigungs Meldungen](#trackbar-notification-messages)
-   [Standard Verarbeitung der TrackBar-Nachricht](#default-trackbar-message-processing)
-   [TrackBar-Quick Infos](#trackbar-tooltips)

Trackbars sind nützlich, wenn Sie möchten, dass der Benutzer einen diskreten ganzzahligen Wert ohne Vorzeichen oder einen Satz aufeinander folgender ganzzahliger Werte ohne Vorzeichen in einem Bereich auswählt. Beispielsweise können Sie eine TrackBar verwenden, um dem Benutzer die Möglichkeit zu geben, die Wiederholungsrate der Tastatur festzulegen, indem Sie den Schieberegler auf einen bestimmten Teil Strich verschieben. Die folgende Abbildung zeigt eine typische TrackBar.

![Screenshot einer TrackBar mit Bezeichnungen an den Enden für langsam und schnell](images/tkb-simple.png)

Der Schieberegler in einer TrackBar wird in Inkrementen verschoben, die Sie bei der Erstellung angeben. Die Werte in diesem Bereich werden als logische Einheiten bezeichnet. Wenn Sie z. b. angeben, dass die TrackBar über logische Einheiten verfügen soll, die zwischen 0 und 5 liegen, kann der Schieberegler nur sechs Positionen belegen: eine Position auf der linken Seite der TrackBar und eine Position für jedes Inkrement im Bereich. In der Regel wird jede dieser Positionen durch einen Teil Strich gekennzeichnet. Allerdings ist die Anzahl der Teil Striche willkürlich und kann weniger als die Anzahl logischer Positionen sein.

Sie erstellen eine TrackBar mithilfe der Funktion " [**roatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", die die Fenster Klasse " [**TrackBar \_ Class**](common-control-window-classes.md) " angibt. Nachdem Sie eine TrackBar erstellt haben, können Sie mit TrackBar-Meldungen viele ihrer Eigenschaften festlegen und abrufen. Zu den Änderungen, die Sie vornehmen können, gehören das Festlegen der minimalen und maximalen Positionen für den Schieberegler, das Zeichnen von Teil Strichen, das Festlegen eines Auswahl Bereichs und das Neupositionieren des Schiebereglers

## <a name="selection-range"></a>Auswahlbereich

Wenn Sie eine TrackBar mit dem TSB-Stil " [**\_ enableselrange**](trackbar-control-styles.md) " erstellen, können Sie einen Auswahlbereich angeben. Die TrackBar hebt den Auswahlbereich hervor und zeigt am Anfang und am Ende dreieckige Teil Striche an, wie in der folgenden Abbildung dargestellt.

![Screenshot einer TrackBar mit hervorgehobenem Bereich](images/tkb-selrange.png)

Der Auswahlbereich der TrackBar wirkt sich in keiner Weise auf seine Funktionalität aus. Die Anwendung kann den Bereich implementieren. Dies kann auf eine der folgenden Arten erfolgen:

-   Verwenden Sie einen Auswahlbereich, um dem Benutzer zu ermöglichen, die maximalen und minimalen Werte für einen Parameter festzulegen. Beispielsweise kann der Benutzer den Schieberegler an eine Position verschieben und dann auf eine Schaltfläche mit der Bezeichnung "Max" klicken. Die Anwendung legt dann den Auswahlbereich so fest, dass die vom Benutzer ausgewählten Werte angezeigt werden.
-   Beschränken Sie die Verschiebung des Schiebereglers auf einen vordefinierten Unterbereich im-Steuerelement, indem Sie die [**WM- \_ HScroll**](wm-hscroll.md) -oder [**WM \_ VScroll**](wm-vscroll.md) -Benachrichtigung verarbeiten und eine Bewegung außerhalb des Auswahl Bereichs deaktivieren. Dies kann z. b. der Fall sein, wenn sich der Bereich der für den Benutzer verfügbaren Werte aufgrund anderer Auswahlmöglichkeiten des Benutzers oder anhand der verfügbaren Ressourcen ändern kann.

## <a name="trackbar-messages"></a>TrackBar-Meldungen

Die logischen Einheiten einer TrackBar sind der Satz zusammenhängender Werte, den die TrackBar darstellen kann. Sie werden in der Regel definiert, indem Sie den Bereich möglicher Werte mit einer [**TBM \_**](tbm-setrange.md) -Nachricht zum Festlegen einer Nachricht angeben, sobald die TrackBar erstellt wurde. Anwendungen können den Bereich dynamisch ändern, indem Sie **TBM \_**-Server Server, TBM-Server-Max oder [**TBM \_**](tbm-setrangemin.md)-Server-Server- [**/zielmax \_**](tbm-setrangemax.md)verwenden.

Um die Position des Schiebereglers (d. h. den Wert, den der Benutzer ausgewählt hat) abzurufen, verwenden Sie die [**TBM- \_ GetPos**](tbm-getpos.md) -Nachricht. Um die Position des Schiebereglers festzulegen, verwenden Sie die [**TBM- \_ SetPos**](tbm-setpos.md) -Nachricht.

In einer TrackBar werden am Anfang und am Ende automatisch Teil Striche angezeigt, es sei denn, Sie geben den [**TSB- \_ noticks**](trackbar-control-styles.md) -Stil an. (Im Ressourcen-Editor von Microsoft Visual Studio bedeutet dies, dass die Tick-Eigenschaft auf false festgelegt wird.) Sie können den TSB-Stil " [**\_ autoticks**](trackbar-control-styles.md) " verwenden, um in regelmäßigen Abständen auf der Trackleiste automatisch zusätzliche Teil Striche anzuzeigen. Standardmäßig zeigt ein **TSB \_** -TrackBar-Steuerzeichen einen Teil Strich bei jedem Inkrement des TrackBar-Bereichs an. Wenn Sie ein anderes Intervall für die automatischen Teil Striche angeben möchten, senden Sie die TBM-Nachricht " [**\_ cfreq**](tbm-setticfreq.md) " an die TrackBar. Beispielsweise können Sie diese Meldung verwenden, um nur 10 Teil Striche in einem Bereich von 1 bis 100 anzuzeigen.

Um die Position eines einzelnen Teil Strichs festzulegen, senden Sie die [**TBM- \_ SetTic**](tbm-settic.md) -Nachricht. Eine TrackBar verwaltet ein Array von DWORD-Werten, die die Position jedes Teil Strichs speichern. Das Array enthält nicht die ersten und letzten Teil Striche, die von der TrackBar automatisch erstellt werden. Sie können einen Index in diesem Array angeben, wenn Sie die [**TBM- \_ GetTic**](tbm-gettic.md) -Nachricht senden, um die Position des entsprechenden Teil Strichs abzurufen. Alternativ können Sie die [**TBM- \_ getptics**](tbm-getptics.md) -Nachricht senden, um einen Zeiger auf das Array abzurufen. Die Anzahl der Elemente im Array ist gleich zwei kleiner als die von der [**TBM \_ GetNumTics**](tbm-getnumtics.md) -Nachricht zurückgegebene Tick-Anzahl. Dies liegt daran, dass die von **TBM \_ getnumtik** zurückgegebene Anzahl den ersten und den letzten Teil Strich enthält, die nicht im Array enthalten sind. Um die physische Position eines Teil Strichs abzurufen, senden Sie in den Client Koordinaten des TrackBar-Fensters die [**TBM \_ GetTicPos**](tbm-getticpos.md) -Nachricht. Die [**TBM- \_ ClearTics**](tbm-cleartics.md) -Nachricht entfernt alle außer der ersten und letzten eines TrackBar-Teil Strichs.

Die Zeilengröße einer TrackBar legt fest, wie weit der Schieberegler in Reaktion auf Tastatureingaben aus den Pfeiltasten verschoben wird, z. b. die nach-rechts-oder nach-unten-Taste. Zum Abrufen oder Festlegen der Zeilengröße senden Sie die [**TBM \_ getlinesize**](tbm-getlinesize.md) -und [**TBM \_ setlinesize**](tbm-setlinesize.md) -Meldungen. Die TrackBar sendet die TB \_ -und TB- \_ linealbenachrichtigungscodes auch an das übergeordnete Fenster, wenn der Benutzer die Pfeiltasten drückt.

Die Seitengröße einer TrackBar legt fest, wie weit der Schieberegler in Reaktion auf Tastatureingaben verschoben wird, wie z. b. die Bild-auf-oder Bild-ab-Taste oder Maus Eingaben, z. b. Klicks im TrackBar-Kanal. Zum Abrufen oder Festlegen der Seitengröße senden Sie die [**TBM-Meldungen " \_ getpagesize**](tbm-getpagesize.md) " und " [**TBM \_ setPageSize**](tbm-setpagesize.md) ". Die TrackBar sendet außerdem die \_ Benachrichtigungs Codes "TB PageUp" und "TB" \_ an das übergeordnete Fenster, wenn Sie Tastatur-oder Maus Eingaben empfängt, die die Seite scrollen. Weitere Informationen finden Sie unter [TrackBar-Benachrichtigungs Meldungen](#trackbar-notification-messages).

Eine Anwendung kann Nachrichten senden, um die Dimensionen einer TrackBar abzurufen. Die [**TBM \_ getthumbrect**](tbm-getthumbrect.md) -Nachricht Ruft das umgebende Rechteck für den Schieberegler ab. Die [**TBM \_ getthumblength**](tbm-getthumblength.md) -Meldung Ruft die Länge des Schiebereglers ab. Die [**TBM \_ GetChannelRect**](tbm-getchannelrect.md) -Nachricht Ruft das umschließende Rechteck für den Kanal der TrackBar ab. Dies ist der Bereich, in dem der Schieberegler verschoben wird. Sie enthält die Hervorhebung, wenn ein Bereich ausgewählt wird. Wenn eine TrackBar den [**TSB- \_ FixedLength**](trackbar-control-styles.md) -Stil hat, können Sie die [**TBM \_ setthumblength**](tbm-setthumblength.md) -Nachricht senden, um die Länge des Schiebereglers zu ändern.

Sie können den Auswahlbereich abrufen oder festlegen, indem Sie Nachrichten an die TrackBar senden. Verwenden Sie die [**TBM \_ SetSel**](tbm-setsel.md) -Nachricht, um die Anfangs-und Endpositionen einer Auswahl festzulegen. Um nur die Anfangsposition oder nur die Endposition einer Auswahl festzulegen, senden Sie eine [**TBM- \_ setselstart**](tbm-setselstart.md) -oder [**TBM- \_ setselend**](tbm-setselend.md) -Nachricht. Um die Anfangs-oder Endpositionen eines Auswahl Bereichs abzurufen, senden Sie eine [**TBM \_ getselstart**](tbm-getselstart.md) -oder [**TBM \_ getselend**](tbm-getselend.md) -Nachricht. Wenn Sie einen Auswahlbereich löschen und die TrackBar im ursprünglichen Bereich wiederherstellen möchten, senden Sie die [**TBM \_ ClearSEL**](tbm-clearsel.md) -Nachricht.

> [!Note]  
> Es liegt in der Verantwortung der Anwendung sicherzustellen, dass der Benutzer keine Werte außerhalb des Auswahl Bereichs auswählen kann. Das Steuerelement selbst hindert den Benutzer daran, den Schieberegler außerhalb des Bereichs zu verschieben.

 

## <a name="trackbar-notification-messages"></a>TrackBar-Benachrichtigungs Meldungen

Eine TrackBar benachrichtigt das übergeordnete Fenster von Benutzeraktionen, indem das übergeordnete Element eine [**WM \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht sendet. Eine TrackBar mit dem Stil von [**TSB \_ Horz**](trackbar-control-styles.md) sendet **WM- \_ HScroll** -Nachrichten. Eine TrackBar mit dem [**TSB \_**](trackbar-control-styles.md) -Format "Vert" sendet **WM- \_ VScroll** -Nachrichten. Das nieder wertige Wort des *wParam* -Parameters von **WM \_ HScroll** oder **WM \_ VScroll** enthält den Benachrichtigungs Code. Für die \_ fingerpositions-und TB-Finger \_ Abdruck-Benachrichtigungs Codes gibt das hochwertige Wort des *wParam* -Parameters die Position des Schiebereglers an. Für alle anderen Benachrichtigungs Codes ist das höchst wertige Wort 0 (null). sendet die [**TBM- \_ GetPos**](tbm-getpos.md) -Nachricht, um die Position des Schiebereglers zu ermitteln Der *LPARAM* -Parameter ist das Handle für die TrackBar.

Das System sendet die obersten Benachrichtigungs Codes für TB, TB, TB, \_ \_ TB \_ und TB \_ nur dann, wenn der Benutzer mit einer TrackBar über die Tastatur interagiert. Die Finger \_ Positions-und TB-Finger \_ Abdruck-Benachrichtigungs Codes werden nur gesendet, wenn der Benutzer die Maus verwendet. \_ \_ In beiden Fällen werden die Benachrichtigungs Codes "TB EndTrack", "TB" und "TB- \_ PageUp" gesendet. In der folgenden Tabelle werden die TrackBar-Benachrichtigungs Codes und-Ereignisse (virtuelle Schlüsselcodes oder Mausereignisse) aufgelistet, die bewirken, dass die Benachrichtigungen zu den [**virtuellen Schlüsselcodes**](/windows/desktop/inputdev/virtual-key-codes)gesendet werden.



| Benachrichtigungs Code | Grund gesendet                                                                                                                     |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| TB \_ unten        | [**VK- \_ Ende**](/windows/desktop/inputdev/virtual-key-codes)                                                                         |
| TB- \_ EndTrack      | [**WM \_ KeyUp**](/windows/desktop/inputdev/wm-keyup) (der Benutzer hat einen Schlüssel freigegeben, der einen relevanten virtuellen Schlüsselcode gesendet hat)                              |
| TB \_ nach unten      | [**VK \_ Rechts**](/windows/desktop/inputdev/virtual-key-codes) oder [ **VK \_ nach unten**](/windows/desktop/inputdev/virtual-key-codes)     |
| TB \_ -Auflistung        | [**VK \_ Links**](/windows/desktop/inputdev/virtual-key-codes) oder nach [ **\_ oben**](/windows/desktop/inputdev/virtual-key-codes)              |
| TB- \_ PageDown      | [**VK \_ Danach**](/windows/desktop/inputdev/virtual-key-codes) (der Benutzer hat auf den Kanal unten oder rechts neben dem Schieberegler geklickt)   |
| TB- \_ PageUp        | [**VK \_ Vor**](/windows/desktop/inputdev/virtual-key-codes) (der Benutzer hat auf den Kanal oberhalb oder links neben dem Schieberegler geklickt) |
| TB-Finger \_ Position | [**WM \_ Lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) nach einem TB-Finger \_ Abdruck-Benachrichtigungs Code                                         |
| TB-Finger \_ Abdruck    | Schieberegler-Bewegung (der Benutzer hat den Schieberegler gezogen)                                                                                   |
| TB ( \_ oben)           | [**VK- \_ Startseite**](/windows/desktop/inputdev/virtual-key-codes)                                                                      |



 

## <a name="default-trackbar-message-processing"></a>Standard Verarbeitung der TrackBar-Nachricht

In diesem Abschnitt wird die von einer TrackBar ausgeführte Fenster Nachrichtenverarbeitung beschrieben.



| `Message`                                              | Verarbeitung wird ausgeführt                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM- \_ capturechanged**](/windows/desktop/inputdev/wm-capturechanged) | Beendet den Timer, wenn während der [**WM- \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Verarbeitung ein solcher festgelegt wurde, und sendet ggf. den TB-Finger \_ Positions Benachrichtigungs Code. Er sendet immer den TB- \_ EndTrack-Benachrichtigungs Code.                                     |
| [**WM \_ Erstellen**](/windows/desktop/winmsg/wm-create)                   | Führt eine zusätzliche Initialisierung aus, z. b. das Festlegen der Zeilengröße, der Seitengröße und der Teil Strich Frequenz auf Standardwerte.                                                                                                                                 |
| [**WM \_ zerstören**](/windows/desktop/winmsg/wm-destroy)                 | Gibt Ressourcen frei.                                                                                                                                                                                                                                         |
| [**WM \_ aktivieren**](/windows/desktop/winmsg/wm-enable)                   | Zeichnet das TrackBar-Fenster auf.                                                                                                                                                                                                                            |
| [**WM- \_ erasebkgnd**](/windows/desktop/winmsg/wm-erasebkgnd)           | Löscht den Fenster Hintergrund unter Verwendung der aktuellen Hintergrundfarbe für die TrackBar.                                                                                                                                                                       |
| [**WM \_ getdlgcode**](/windows/desktop/dlgbox/wm-getdlgcode)           | Gibt den dlgc- \_ wantpfeile-Wert zurück.                                                                                                                                                                                                                      |
| [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown)               | Verarbeitet die Tastenkombinationen und sendet ggf \_ . die Nachrichten oben, TB \_ unten, TB \_ PageUp, TB \_ PageDown, TB-Zusammenführung \_ und TB- \_ LineDown-Benachrichtigungs Codes.                                                                                               |
| [**WM- \_ KeyUp**](/windows/desktop/inputdev/wm-keyup)                   | Sendet den TB- \_ EndTrack-Benachrichtigungs Code, wenn es sich bei dem Schlüssel um einen der Richtungs Schlüssel handelt.                                                                                                                                                                       |
| [**WM- \_ killfokus**](/windows/desktop/inputdev/wm-killfocus)           | Zeichnet das TrackBar-Fenster auf.                                                                                                                                                                                                                            |
| [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown)       | Legt den Fokus und die Maus Aufzeichnung auf die TrackBar fest. Bei Bedarf wird ein Timer festgelegt, der bestimmt, wie schnell der Schieberegler zum Mauszeiger bewegt wird, wenn der Benutzer die Maustaste gedrückt hält.                                      |
| [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup)           | Gibt die Maus Aufzeichnung frei und beendet den Timer, wenn während der [**WM- \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Verarbeitung ein solcher festgelegt wurde. \_Bei Bedarf wird der TB-fingerpositions-Benachrichtigungs Code gesendet. Er sendet immer den TB- \_ EndTrack-Benachrichtigungs Code. |
| [**WM- \_ mouseelmove**](/windows/desktop/inputdev/wm-mousemove)           | Verschiebt den Schieberegler und sendet den TB-Finger \_ Abdruck-Benachrichtigungs Code beim Nachverfolgen der Maus (siehe [**WM- \_ Timer**](/windows/desktop/winmsg/wm-timer)).                                                                                                                          |
| [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint)                        | Zeichnet die TrackBar. Wenn der wParam-Parameter ungleich NULL ist, geht das Steuerelement davon aus, dass es sich bei dem Wert um einen HDC handelt und zeichnet sich durch den Gerätekontext aus.                                                                                                             |
| [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)             | Zeichnet das TrackBar-Fenster auf.                                                                                                                                                                                                                            |
| [**WM- \_ Größe**](/windows/desktop/winmsg/wm-size)                       | Legt die Dimensionen der TrackBar fest, wobei der Schieberegler entfernt wird, wenn nicht genügend Platz vorhanden ist, um ihn anzuzeigen.                                                                                                                                                      |
| [**WM- \_ Timer**](/windows/desktop/winmsg/wm-timer)                     | Ruft die Mausposition ab und aktualisiert die Position des Schiebereglers. (Sie wird nur empfangen, wenn der Schieberegler vom Benutzer gezogen wird.)                                                                                                                         |
| [**WM- \_ wininichange**](/windows/desktop/winmsg/wm-wininichange)       | Initialisiert die Schieberegler-Abmessungen.                                                                                                                                                                                                                           |



 

## <a name="trackbar-tooltips"></a>TrackBar-Quick Infos

Eine TrackBar, die im [**TSB- \_ Tooltips**](trackbar-control-styles.md) -Format erstellt wird, verfügt über ein Standardmäßiges QuickInfo-Steuerelement. Die QuickInfo bleibt sichtbar und zeigt den aktuellen Wert an, wenn der Benutzer den Schieberegler mit der Maus zieht.

Sie können einer TrackBar ein neues QuickInfo-Steuerelement zuweisen, indem Sie die [**TBM- \_ SetToolTips**](tbm-settooltips.md) -Nachricht senden. Um das Handle für ein zugewiesenes QuickInfo-Steuerelement abzurufen, verwenden Sie die [**TBM \_ gettooltips**](tbm-gettooltips.md) -Nachricht.

 

 