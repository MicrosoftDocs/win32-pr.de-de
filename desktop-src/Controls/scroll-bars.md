---
title: Bildlaufleiste
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Bildlaufleisten verwendet werden.
ms.assetid: vs|controls|~\controls\scrollbars\scrollbars.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca1aa4dc1b676cd5ce4f98c23035e462b9f4f87f8c20265848a8f0bcde80964
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636990"
---
# <a name="scroll-bar"></a>Bildlaufleiste

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Bildlaufleisten verwendet werden. In einem Fenster kann ein Datenobjekt angezeigt werden, z. B. ein Dokument oder eine Bitmap, das größer als der Clientbereich des Fensters ist. Wenn eine *Bildlaufleiste* bereitgestellt wird, kann der Benutzer einen Bildlauf für ein Datenobjekt im Clientbereich durchführen, um die Teile des Objekts anzuzeigen, die über die Rahmen des Fensters hinausgehen.

### <a name="overviews"></a>Übersichten



| Thema                                      | Inhalte                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Scrollleisten](about-scroll-bars.md) | Eine Scrollleiste besteht aus einem schattierten Strich  mit einer Pfeilschaltfläche an jedem Ende und einem Bildlauffeld (manchmal als Strich bezeichnet) zwischen den Pfeilschaltflächen.<br/>                                                                                                                                                                     |
| [Verwenden von Bildlaufleisten](using-scroll-bars.md) | Beim Erstellen eines überlappenden, Popup- oder untergeordneten Fensters können Sie Standardscrollleisten hinzufügen, indem Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden und [**WS \_ HSCROLL,**](/windows/desktop/winmsg/window-styles) [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)oder beide Stile angeben.<br/> |



 

### <a name="functions"></a>Funktionen



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
<td><a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar-Funktion</strong></a> aktiviert oder deaktiviert einen oder beide Bildlaufleistenpfeile. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo-Funktion</strong></a> ruft Informationen über die angegebene Scrollleiste ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo-Funktion</strong></a> ruft die Parameter einer Scrollleiste ab, einschließlich der minimalen und maximalen Bildlaufpositionen, der Seitengröße und der Position des Bildlauffelds (Strich).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos-Funktion</strong></a> ruft die aktuelle Position des Bildlauffelds (Strich) in der angegebenen Bildlaufleiste ab. Die aktuelle Position ist ein relativer Wert, der vom aktuellen Bildlaufbereich abhängt. Wenn der Bildlaufbereich beispielsweise zwischen 0 und 100 liegt und sich das Bildlauffeld in der Mitte der Leiste befindet, ist die aktuelle Position 50.
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos-Funktion</strong></a> wird aus Gründen der Abwärtskompatibilität bereitgestellt. Neue Anwendungen sollten die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo-Funktion</strong></a> verwenden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange-Funktion</strong></a> ruft die aktuellen minimalen und maximalen Scrollfeldpositionen (Thumb) für die angegebene Scrollleiste ab.
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange-Funktion</strong></a> wird nur zur Kompatibilität bereitgestellt. Neue Anwendungen sollten die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo-Funktion</strong></a> verwenden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC-Funktion</strong></a> führt einen horizontalen und vertikalen Bildlauf für ein Rechteck aus Bits durch. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow-Funktion</strong></a> führt einen Bildlauf durch den Inhalt des Clientbereichs des angegebenen Fensters durch.
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow-Funktion</strong></a> wird aus Gründen der Abwärtskompatibilität bereitgestellt. Neue Anwendungen sollten die <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx-Funktion</strong></a> verwenden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx-Funktion</strong></a> führt einen Bildlauf durch den Inhalt des angegebenen Clientbereichs des Fensters durch. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo-Funktion</strong></a> legt die Parameter einer Bildlaufleiste fest, einschließlich der minimalen und maximalen Bildlaufpositionen, der Seitengröße und der Position des Bildlauffelds (Strich). Die Funktiondrawn auch die Scrollleiste neu, wenn dies angefordert wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos-Funktion</strong></a> legt die Position des Bildlauffelds (Strich) in der angegebenen Scrollleiste fest und zeichnet die Scrollleiste bei Entsprechender entsprechend der neuen Position des Bildlauffelds neu.
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos-Funktion</strong></a> wird aus Gründen der Abwärtskompatibilität bereitgestellt. Neue Anwendungen sollten die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo-Funktion</strong></a> verwenden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange-Funktion</strong></a> legt die minimalen und maximalen Scrollfeldpositionen für die angegebene Scrollleiste fest.
<blockquote>
[!Note]<br />
Die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange-Funktion</strong></a> wird aus Gründen der Abwärtskompatibilität bereitgestellt. Neue Anwendungen sollten die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo-Funktion</strong></a> verwenden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a></td>
<td>Die <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar-Funktion</strong></a> zeigt die angegebene Scrollleiste an oder blendet sie aus. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Meldungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SBM \_ ENABLE \_ ARROWS**](sbm-enable-arrows.md)      | Eine Anwendung sendet die [**SBM \_ ENABLE \_ ARROWS-Meldung,**](sbm-enable-arrows.md) um einen oder beide Pfeile eines Bildlaufleisten-Steuerelements zu aktivieren oder zu deaktivieren.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SBM \_ GETPOS**](sbm-getpos.md)                     | Die [**SBM \_ GETPOS-Nachricht**](sbm-getpos.md) wird gesendet, um die aktuelle Position des Bildlauffelds eines Bildlaufleisten-Steuerelements abzurufen. Die aktuelle Position ist ein relativer Wert, der vom aktuellen Bildlaufbereich abhängt. Wenn der Bildlaufbereich beispielsweise zwischen 0 und 100 liegt und sich das Bildlauffeld in der Mitte der Leiste befindet, ist die aktuelle Position 50. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten sie die [**GetScrollPos-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) verwenden. Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Anwendungen, die ein benutzerdefiniertes Scrollleisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **GetScrollPos-Funktion** ordnungsgemäß funktioniert.<br/> |
| [**SBM \_ GETRANGE**](sbm-getrange.md)                 | Die [**SBM \_ GETRANGE-Nachricht**](sbm-getrange.md) wird gesendet, um die minimalen und maximalen Positionswerte für das Bildlaufleisten-Steuerelement abzurufen. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten sie die [**GetScrollRange-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) verwenden. Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Anwendungen, die ein benutzerdefiniertes Scrollleisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **GetScrollRange-Funktion** ordnungsgemäß funktioniert.<br/>                                                                                                                                                                                                              |
| [**SBM \_ GETSCROLLBARINFO**](sbm-getscrollbarinfo.md) | Wird von einer Anwendung gesendet, um Informationen über die angegebene Scrollleiste abzurufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md)       | Die [**SBM \_ GETSCROLLINFO-Nachricht**](sbm-getscrollinfo.md) wird gesendet, um die Parameter einer Scrollleiste abzurufen. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten sie die [**GetScrollInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) verwenden. Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Anwendungen, die ein benutzerdefiniertes Scrollleisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **GetScrollInfo-Funktion** ordnungsgemäß funktioniert.<br/>                                                                                                                                                                                                                                           |
| [**SBM \_ SETPOS**](sbm-setpos.md)                     | Die [**SBM \_ SETPOS-Nachricht**](sbm-setpos.md) wird gesendet, um die Position des Bildlauffelds (Strich) und, falls angefordert, die Scrollleiste neu zu zeichnet, um die neue Position des Bildlauffelds widerzuerkennen. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten sie die [**SetScrollPos-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) verwenden. Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Anwendungen, die ein benutzerdefiniertes Scrollleisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **SetScrollPos-Funktion** ordnungsgemäß funktioniert.<br/>                                                                                                                                                                  |
| [**SBM \_ SETRANGE**](sbm-setrange.md)                 | Die [**SBM \_ SETRANGE-Nachricht**](sbm-setrange.md) wird gesendet, um die minimalen und maximalen Positionswerte für das Bildlaufleisten-Steuerelement zu festlegen. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten sie die [**SetScrollRange-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) verwenden. Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Anwendungen, die ein benutzerdefiniertes Scrollleisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **SetScrollRange-Funktion** ordnungsgemäß funktioniert.<br/>                                                                                                                                                                                                                   |
| [**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)     | Eine Anwendung sendet die [**SBM \_ SETRANGEREDRAW-Nachricht**](sbm-setrangeredraw.md) an ein Bildlaufleisten-Steuerelement, um die minimalen und maximalen Positionswerte und das Steuerelement neu zu zeichnet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)       | Die [**SBM \_ SETSCROLLINFO-Nachricht**](sbm-setscrollinfo.md) wird gesendet, um die Parameter einer Bildlaufleiste festlegen. <br/> Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten sie die [**SetScrollInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) verwenden. Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Anwendungen, die ein benutzerdefiniertes Scrollleisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **SetScrollInfo-Funktion** ordnungsgemäß funktioniert.<br/>                                                                                                                                                                                                                                            |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                 | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CTLCOLORSCROLLBAR**](wm-ctlcolorscrollbar.md) | Die [**WM \_ CTLCOLORSCROLLBAR-Nachricht**](wm-ctlcolorscrollbar.md) wird an das übergeordnete Fenster eines Bildlaufleisten-Steuerelements gesendet, wenn das Steuerelement gezeichnet werden soll. Durch Reagieren auf diese Meldung kann das übergeordnete Fenster das Anzeigekontexthandle verwenden, um die Hintergrundfarbe des Bildlaufleisten-Steuerelements festzulegen. <br/> Ein Fenster empfängt diese Meldung über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) <br/> |
| [**WM \_ HSCROLL**](wm-hscroll.md)                     | Die [**WM \_ HSCROLL-Nachricht**](wm-hscroll.md) wird an ein Fenster gesendet, wenn ein Bildlaufereignis in der standardmäßigen horizontalen Scrollleiste des Fensters auftritt. Diese Meldung wird auch an den Besitzer eines horizontalen Bildlaufleisten-Steuerelements gesendet, wenn ein Bildlaufereignis im -Steuerelement auftritt. <br/> Ein Fenster empfängt diese Meldung über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) <br/>                                        |
| [**WM \_ VSCROLL**](wm-vscroll.md)                     | Die [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) wird an ein Fenster gesendet, wenn ein Bildlaufereignis in der standardmäßigen vertikalen Bildlaufleiste des Fensters auftritt. Diese Meldung wird auch an den Besitzer eines vertikalen Bildlaufleisten-Steuerelements gesendet, wenn ein Bildlaufereignis im -Steuerelement auftritt. <br/> Ein Fenster empfängt diese Meldung über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) <br/>                                            |



 

### <a name="structures"></a>Strukturen



| Thema                                  | Inhalte                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) | Die [**SCROLLBARINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) enthält Scrollleisteninformationen.<br/>                                                                                                                                                                                                                                                           |
| [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)       | Die [**SCROLLINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-scrollinfo) enthält Scrollleistenparameter, die von der [**SetScrollInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) (oder [**SBM \_ SETSCROLLINFO-Nachricht)**](sbm-setscrollinfo.md) festgelegt oder von der [**GetScrollInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) (oder [**SBM \_ GETSCROLLINFO-Nachricht)**](sbm-getscrollinfo.md) abgerufen werden sollen. <br/> |



 

### <a name="constants"></a>Konstanten



| Thema                                                      | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bildlaufleisten-Steuerelementstile](scroll-bar-control-styles.md) | Um ein Bildlaufleisten-Steuerelement mit der [**CreateWindow-**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) zu erstellen, geben Sie die SCROLLBAR-Klasse, die entsprechenden Fensterformatkonstanten und eine Kombination der folgenden Bildlaufleisten-Steuerelementstile an. Einige der Stile erstellen ein Bildlaufleisten-Steuerelement, das eine Standardbreite oder -höhe verwendet. Sie müssen jedoch immer die x- und y-Koordinaten und die anderen Dimensionen der Scrollleiste angeben, wenn Sie **CreateWindow** oder **CreateWindowEx** aufrufen. <br/> |



 

 

