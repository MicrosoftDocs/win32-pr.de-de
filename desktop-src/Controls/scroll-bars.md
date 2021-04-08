---
title: Bildlaufleiste
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Bild Lauf leisten verwendet werden.
ms.assetid: vs|controls|~\controls\scrollbars\scrollbars.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38cf549a37fd5d4a271f6e12642a9bfd45b65d79
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730608"
---
# <a name="scroll-bar"></a>Bildlaufleiste

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Bild Lauf leisten verwendet werden. Ein Fenster kann ein Datenobjekt anzeigen, z. b. ein Dokument oder eine Bitmap, das größer ist als der Client Bereich des Fensters. Bei Bereitstellung mit einer Schiebe *Leiste* kann der Benutzer einen Bildlauf in einem Datenobjekt im Client Bereich durchführen, um die Teile des Objekts anzuzeigen, die über die Rahmen des Fensters hinausgehen.

### <a name="overviews"></a>Übersichten



| Thema                                      | Inhalte                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Scrollleisten](about-scroll-bars.md) | Eine Schiebe Leiste besteht aus einer schattierten Welle mit einer Pfeil Schaltfläche an jedem Ende und einem Bild Lauf *Feld* (manchmal auch als Ziehpunkt bezeichnet) zwischen den Pfeil Schaltflächen.<br/>                                                                                                                                                                     |
| [Verwenden von Scrollleisten](using-scroll-bars.md) | Beim Erstellen eines überlappenden, Popup-oder untergeordneten Fensters können Sie Standard Scrollleisten hinzufügen, indem Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden und " [**WS \_ HScroll**](/windows/desktop/winmsg/window-styles)", " [**WS \_ VScroll**](/windows/desktop/winmsg/window-styles)" oder beide Stile angeben.<br/> |



 

### <a name="functions"></a>Functions



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>Inhalte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>Enablescrollbar</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>enablescrollbar</strong></a> -Funktion aktiviert oder deaktiviert einen oder beide ScrollBar-Pfeile. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>getscrollbarinfo</strong></a> -Funktion Ruft Informationen über die angegebene Scrollleiste ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>Getscrollinfo</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>getscrollinfo</strong></a> -Funktion Ruft die Parameter einer Schiebe Leiste ab, einschließlich der minimalen und maximalen scrollpositionen, der Seitengröße und der Position des Bild Lauf Felds (Thumb).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>Getscrollpos</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>getscrollpos</strong></a> -Funktion Ruft die aktuelle Position des Bild Lauf Felds (Ziehpunkt) in der angegebenen Scrollleiste ab. Die aktuelle Position ist ein relativer Wert, der vom aktuellen scrollbereich abhängig ist. Wenn der scrollbereich z. b. zwischen 0 und 100 liegt und sich das Bild Lauf Feld in der Mitte des Balkens befindet, ist die aktuelle Position 50.
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>getscrollpos</strong></a> -Funktion wird aus Gründen der Abwärtskompatibilität bereitgestellt. Neue Anwendungen sollten die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>getscrollinfo</strong></a> -Funktion verwenden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>Getscrollrange</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>getscrollrange</strong></a> -Funktion Ruft die aktuellen minimalen und maximalen Schiebe leisten Positionen (Ziehpunkt) für die angegebene Scrollleiste ab.
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>getscrollrange</strong></a> -Funktion wird nur aus Kompatibilitätsgründen bereitgestellt. Neue Anwendungen sollten die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>getscrollinfo</strong></a> -Funktion verwenden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>Scrolldc</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>scrolldc</strong></a> -Funktion scrollt ein Rechteck von Bits horizontal und vertikal. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>Scrollwindow</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>scrollwindow</strong></a> -Funktion führt einen Bildlauf für den Inhalt des Client Bereichs des angegebenen Fensters durch.
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>scrollwindow</strong></a> -Funktion wird aus Gründen der Abwärtskompatibilität bereitgestellt. Neue Anwendungen sollten die <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>scrollwindowex</strong></a> -Funktion verwenden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>Scrollwindowex</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>scrollwindowex</strong></a> -Funktion führt einen Bildlauf durch den Inhalt des Client Bereichs des angegebenen Fensters durch. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>setScrollInfo</strong></a> -Funktion legt die Parameter einer Schiebe Leiste fest, einschließlich der minimalen und maximalen scrollpositionen, der Seitengröße und der Position des Bild Lauf Felds (Thumb). Die Funktion zeichnet die Scrollleiste auch neu, wenn Sie angefordert wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>Setscrollpos</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>setscrollpos</strong></a> -Funktion legt die Position des Bild Lauf Felds (Ziehpunkt) in der angegebenen Bild Lauf Leiste fest und zeichnet bei Bedarf die Schiebe Leiste neu, um die neue Position des Bild Lauf Felds widerzuspiegeln.
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>setscrollpos</strong></a> -Funktion wird aus Gründen der Abwärtskompatibilität bereitgestellt. Neue Anwendungen sollten die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>setScrollInfo</strong></a> -Funktion verwenden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>Setscrollrange</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>setscrollrange</strong></a> -Funktion legt die minimalen und maximalen Bild Lauf Feldpositionen für die angegebene Bild Lauf Leiste fest.
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>setscrollrange</strong></a> -Funktion wird aus Gründen der Abwärtskompatibilität bereitgestellt. Neue Anwendungen sollten die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>setScrollInfo</strong></a> -Funktion verwenden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollbar</strong></a> -Funktion zeigt die angegebene Scrollleiste an oder blendet sie aus. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Meldungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SBM- \_ Aktivier \_ Pfeile**](sbm-enable-arrows.md)      | Eine Anwendung sendet die [**SBM-Option \_ \_ Pfeile aktivieren**](sbm-enable-arrows.md) , um einen oder beide Pfeile eines ScrollBar-Steuer Elements zu aktivieren oder zu deaktivieren.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SBM- \_ GetPos**](sbm-getpos.md)                     | Die [**SBM- \_ GetPos**](sbm-getpos.md) -Nachricht wird gesendet, um die aktuelle Position des Bild Lauf Felds eines ScrollBar-Steuer Elements abzurufen. Die aktuelle Position ist ein relativer Wert, der vom aktuellen scrollbereich abhängig ist. Wenn der scrollbereich z. b. zwischen 0 und 100 liegt und sich das Bild Lauf Feld in der Mitte des Balkens befindet, ist die aktuelle Position 50. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**getscrollpos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **getscrollpos** -Funktion ordnungsgemäß funktioniert.<br/> |
| [**SBM- \_ GetRange**](sbm-getrange.md)                 | Die [**SBM- \_ GetRange**](sbm-getrange.md) -Nachricht wird gesendet, um die minimalen und maximalen Positionswerte für das ScrollBar-Steuerelement abzurufen. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**getscrollrange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **getscrollrange** -Funktion ordnungsgemäß funktioniert.<br/>                                                                                                                                                                                                              |
| [**SBM \_ getscrollbarinfo**](sbm-getscrollbarinfo.md) | Wird von einer Anwendung gesendet, um Informationen über die angegebene Scrollleiste abzurufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SBM \_ getscrollinfo**](sbm-getscrollinfo.md)       | Die [**SBM \_ getscrollinfo**](sbm-getscrollinfo.md) -Nachricht wird gesendet, um die Parameter einer Schiebe Leiste abzurufen. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Nachrichten reagieren, damit die Funktion **getscrollinfo** ordnungsgemäß funktioniert.<br/>                                                                                                                                                                                                                                           |
| [**SBM- \_ SetPos**](sbm-setpos.md)                     | Die [**SBM- \_ SetPos**](sbm-setpos.md) -Nachricht wird gesendet, um die Position des Bild Lauf Felds (Thumb) festzulegen, und, falls angefordert, die Schiebe Leiste neu gezeichnet, um die neue Position des Bild Lauf Felds widerzuspiegeln. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **setscrollpos** -Funktion ordnungsgemäß funktioniert.<br/>                                                                                                                                                                  |
| [**SBM-über \_ Tragung**](sbm-setrange.md)                 | Die [**SBM- \_ SetRange**](sbm-setrange.md) -Nachricht wird gesendet, um die minimalen und maximalen Positionswerte für das ScrollBar-Steuerelement festzulegen. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**setscrollrange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die Funktion **setscrollrange** ordnungsgemäß funktioniert.<br/>                                                                                                                                                                                                                   |
| [**SBM- \_ abzeichnende**](sbm-setrangeredraw.md)     | Eine Anwendung sendet die [**SBM \_ setrangeredraw**](sbm-setrangeredraw.md) -Nachricht an ein ScrollBar-Steuerelement, um die minimalen und maximalen Positionswerte festzulegen und das Steuerelement neu zu zeichnen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**SBM \_ setScrollInfo**](sbm-setscrollinfo.md)       | Die [**SBM- \_ setScrollInfo**](sbm-setscrollinfo.md) -Nachricht wird gesendet, um die Parameter einer Schiebe Leiste festzulegen. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Nachrichten reagieren, damit die Funktion **setScrollInfo** ordnungsgemäß funktioniert.<br/>                                                                                                                                                                                                                                            |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ ctlcolorscrollbar**](wm-ctlcolorscrollbar.md) | Die [**WM- \_ ctlcolorscrollbar**](wm-ctlcolorscrollbar.md) -Meldung wird an das übergeordnete Fenster eines ScrollBar-Steuer Elements gesendet, wenn das Steuerelement gezeichnet wird. Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster den Kontext Zieh Punkt der Anzeige verwenden, um die Hintergrundfarbe des ScrollBar-Steuer Elements festzulegen. <br/> Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. <br/> |
| [**WM- \_ HScroll**](wm-hscroll.md)                     | Die [**WM- \_ HScroll**](wm-hscroll.md) -Nachricht wird an ein Fenster gesendet, wenn ein scrollereignis in der horizontalen Standard Scrollleiste des Fensters auftritt. Diese Meldung wird auch an den Besitzer eines horizontalen Schiebe leisten-Steuer Elements gesendet, wenn im-Steuerelement ein scrollereignis auftritt. <br/> Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. <br/>                                        |
| [**WM- \_ VScroll**](wm-vscroll.md)                     | Die [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht wird an ein Fenster gesendet, wenn ein scrollereignis in der vertikalen Standard Scrollleiste des Fensters auftritt. Diese Meldung wird auch an den Besitzer eines vertikalen Schiebe leisten-Steuer Elements gesendet, wenn im-Steuerelement ein scrollereignis auftritt. <br/> Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. <br/>                                            |



 

### <a name="structures"></a>Strukturen



| Thema                                  | Inhalte                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Scrollbarinfo**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) | Die [**scrollbarinfo**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) -Struktur enthält ScrollBar-Informationen.<br/>                                                                                                                                                                                                                                                           |
| [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo)       | Die [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) -Struktur enthält ScrollBar-Parameter, die von der [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion (oder [**SBM \_ setScrollInfo**](sbm-setscrollinfo.md) -Nachricht) festgelegt oder von der [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) -Funktion (oder [**SBM \_ getscrollinfo**](sbm-getscrollinfo.md) -Nachricht) abgerufen werden. <br/> |



 

### <a name="constants"></a>Konstanten



| Thema                                                      | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ScrollBar-Steuerelement Stile](scroll-bar-control-styles.md) | Zum Erstellen eines Schiebe leisten-Steuer Elements mithilfe der Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**deatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " geben Sie die ScrollBar-Klasse, die entsprechenden Fenster Stil Konstanten und eine Kombination der folgenden Stile für ScrollBar-Steuerelemente an. Einige der Stile erstellen ein ScrollBar-Steuerelement, das eine Standardbreite oder-Höhe verwendet. Allerdings müssen Sie immer die x-und y-Koordinaten und die anderen Dimensionen der Bild Lauf Leiste angeben, wenn Sie "up **Window** " oder " **kreatewindowex**" aufrufen. <br/> |



 

 

