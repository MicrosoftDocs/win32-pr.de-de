---
title: Grund leisten
description: Dieser Abschnitt enthält Informationen zu Programmier Elementen, die mit Grund leisten-Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\rebar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef14343d33fb5ae45a2d93df74a9b915aca6d7b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474453"
---
# <a name="rebar"></a>Grund leisten

Dieser Abschnitt enthält Informationen zu Programmier Elementen, die mit Grund leisten-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                            | Inhalte                                                                               |
|--------------------------------------------------|----------------------------------------------------------------------------------------|
| [Grund leisten-Steuerelemente](rebar-controls.md)             | Die Grund leisten-Steuer *Elemente* fungieren als Container für untergeordnete Fenster.<br/>                       |
| [Verwenden von Grund leisten-Steuerelementen](using-rebar-controls.md) | Dieser Abschnitt enthält Beispielcode, der zeigt, wie Sie die Grund leisten Steuerelemente implementieren.<br/> |



 

### <a name="messages"></a>Meldungen



| Thema                                               | Inhalte                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RB \_ BeginDrag**](rb-begindrag.md)               | Versetzt das Grund leisten-Steuerelement in den Drag & Drop-Modus. Diese Meldung bewirkt nicht, dass eine [RBN- \_ BeginDrag](rbn-begindrag.md) -Benachrichtigung gesendet wird. <br/>                                                 |
| [**RB \_ DeleteBand**](rb-deleteband.md)             | Löscht ein Band aus einem Grund leisten-Steuerelement. <br/>                                                                                                                                                     |
| [**RB \_ DragMove**](rb-dragmove.md)                 | Aktualisiert die Zieh Position im Grund leisten-Steuerelement nach einer vorherigen [**RB \_ BeginDrag**](rb-begindrag.md) -Nachricht. <br/>                                                                           |
| [**RB- \_ EndDrag**](rb-enddrag.md)                   | Beendet den Drag & Drop-Vorgang des Grund leisten-Steuer Elements. Diese Meldung bewirkt nicht, dass eine [RBN- \_ EndDrag](rbn-enddrag.md) -Benachrichtigung gesendet wird. <br/>                                          |
| [**RB \_ getBandBorders**](rb-getbandborders.md)     | Ruft die Rahmen eines Bands ab. Das Ergebnis dieser Nachricht kann verwendet werden, um den nutzbaren Bereich in einem Band zu berechnen. <br/>                                                                          |
| [**RB \_ GetBandCount**](rb-getbandcount.md)         | Ruft die Anzahl der Bänder ab, die sich derzeit im Grund leisten-Steuerelement befinden. <br/>                                                                                                                             |
| [**RB \_ GetBandInfo**](rb-getbandinfo.md)           | Ruft Informationen zu einem angegebenen Band in einem Grund leisten-Steuerelement ab. <br/>                                                                                                                         |
| [**RB \_ getbandmargin**](rb-getbandmargins.md)     | Ruft die Ränder eines Bands ab.<br/>                                                                                                                                                          |
| [**RB \_ getbarheight**](rb-getbarheight.md)         | Ruft die Höhe des Grund leisten-Steuer Elements ab. <br/>                                                                                                                                               |
| [**RB \_ getbarinfo**](rb-getbarinfo.md)             | Ruft Informationen zum Grund leisten-Steuerelement und der von ihm verwendeten Bildliste ab. <br/>                                                                                                                |
| [**RB \_ GetBkColor**](rb-getbkcolor.md)             | Ruft die Standard Hintergrundfarbe eines Grund leisten-Steuer Elements ab. <br/>                                                                                                                                    |
| [**RB \_ getcolorscheme**](rb-getcolorscheme.md)     | Ruft die Farbschema Informationen aus dem Grund leisten-Steuerelement ab. <br/>                                                                                                                           |
| [**RB \_ getdroptarget**](rb-getdroptarget.md)       | Ruft den [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Schnittstellen Zeiger eines Grund leisten-Steuer Elements ab. <br/>                                                                                                        |
| [**RB \_ getextendecodstyle**](rb-getextendedstyle.md) | Ruft den erweiterten Stil ab. <br/>                                                                                                                                                                 |
| [**RB \_ getpalette**](rb-getpalette.md)             | Ruft die aktuelle Palette des Grund leisten-Steuer Elements ab. <br/>                                                                                                                                           |
| [**RB \_ GetRect**](rb-getrect.md)                   | Ruft das umschließende Rechteck für ein bestimmtes Band in einem Grund leisten-Steuerelement ab. <br/>                                                                                                                    |
| [**RB \_ GetRowCount**](rb-getrowcount.md)           | Ruft die Anzahl der Zeilen der Bänder in einem Grund leisten-Steuerelement ab. <br/>                                                                                                                                |
| [**RB \_ getRowHeight**](rb-getrowheight.md)         | Ruft die Höhe einer angegebenen Zeile in einem Grund leisten-Steuerelement ab. <br/>                                                                                                                              |
| [**RB \_ gettextcolor**](rb-gettextcolor.md)         | Ruft die Standard Textfarbe eines Grund leisten-Steuer Elements ab. <br/>                                                                                                                                          |
| [**RB \_ gettooltips**](rb-gettooltips.md)           | Ruft das Handle für ein QuickInfo-Steuerelement ab, das dem Grund leisten-Steuerelement zugeordnet ist. <br/>                                                                                                           |
| [**RB \_ getunicodeformat**](rb-getunicodeformat.md) | Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab. <br/>                                                                                                                             |
| [**RB- \_ HitTest**](rb-hittest.md)                   | Bestimmt, welcher Teil eines Grund leisten Bands an einem bestimmten Punkt auf dem Bildschirm angezeigt wird, wenn ein Info leisten-Band an diesem Punkt vorhanden ist. <br/>                                                                        |
| [**RB \_ ID$ Index**](rb-idtoindex.md)               | Konvertiert einen Band Bezeichner in einen Band-Index in einem Grund leisten-Steuerelement. <br/>                                                                                                                           |
| [**RB \_ InsertBand**](rb-insertband.md)             | Fügt ein neues Band in ein Grund leisten-Steuerelement ein. <br/>                                                                                                                                                   |
| [**RB \_ maximizeband**](rb-maximizeband.md)         | Ändert die Größe eines Bands in einem Grund leisten-Steuerelement entweder auf seine ideale oder größte Größe. <br/>                                                                                                                   |
| [**RB \_ minimizeband**](rb-minimizeband.md)         | Ändert die Größe eines Bands in einem Grund leisten-Steuerelement auf seine kleinste Größe. <br/>                                                                                                                                  |
| [**RB- \_ muveband**](rb-moveband.md)                 | Verschiebt ein Band von einem Index zu einem anderen. <br/>                                                                                                                                                  |
| [**RB \_ pushchevron**](rb-pushchevron.md)           | Wird an ein Grund leisten-Steuerelement gesendet, um ein Chevron Programm gesteuert zu pushen.<br/>                                                                                                                               |
| [**RB \_ SetBandInfo**](rb-setbandinfo.md)           | Legt die Eigenschaften eines vorhandenen Bands in einem Grund leisten-Steuerelement fest. <br/>                                                                                                                             |
| [**RB \_ setbandwidth**](rb-setbandwidth.md)         | Legt die Breite für ein angedocktes Band fest.<br/>                                                                                                                                                         |
| [**RB \_ setbarinfo**](rb-setbarinfo.md)             | Legt die Eigenschaften eines Grund leisten-Steuer Elements fest. <br/>                                                                                                                                             |
| [**RB \_ SetBkColor**](rb-setbkcolor.md)             | Legt die Standard Hintergrundfarbe eines Grund leisten-Steuer Elements fest. <br/>                                                                                                                                         |
| [**RB \_ SetColorScheme**](rb-setcolorscheme.md)     | Legt die Farbschema Informationen für das Grund leisten-Steuerelement fest. <br/>                                                                                                                                 |
| [**RB- \_ textendecodstyle**](rb-setextendedstyle.md) | Legt den erweiterten Stil fest. Diese Meldung ist nicht implementiert.<br/>                                                                                                                                 |
| [**RB- \_ SetPalette**](rb-setpalette.md)             | Legt die aktuelle Palette des Grund leisten-Steuer Elements fest. <br/>                                                                                                                                                |
| [**RB \_ SetParent**](rb-setparent.md)               | Legt das übergeordnete Fenster eines Info leisten Steuer Elements fest. <br/>                                                                                                                                                    |
| [**RB \_ SetTextColor**](rb-settextcolor.md)         | Legt die Standard Textfarbe eines Grund leisten-Steuer Elements fest. <br/>                                                                                                                                               |
| [**RB- \_ SetToolTips**](rb-settooltips.md)           | Ordnet dem Grund leisten-Steuerelement ein QuickInfo-Steuerelement zu. <br/>                                                                                                                                     |
| [**RB- \_ Format**](rb-setunicodeformat.md) | Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen. <br/> |
| [**RB \_ SetWindowTheme**](rb-setwindowtheme.md)     | Legt den visuellen Stil eines Grund leisten-Steuer Elements fest.<br/>                                                                                                                                                 |
| [**RB \_ Showband**](rb-showband.md)                 | Zeigt ein bestimmtes Band in einem Grund leisten-Steuerelement an oder blendet es aus. <br/>                                                                                                                                          |
| [**RB \_ sizetorect**](rb-sizetorect.md)             | Versucht, das beste Layout der Bänder für das angegebene Rechteck zu finden. <br/>                                                                                                                   |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                        | Inhalte                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ customdraw (Info)](nm-customdraw-rebar.md)            | Wird vom Info leisten-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)<br/>                                                                                               |
| [NM \_ nchittest (Info Leiste)](nm-nchittest-rebar.md)              | Wird von einem Grund leisten-Steuerelement gesendet, wenn das Steuerelement eine [**WM- \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) -Nachricht empfängt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                 |
| [NM \_ releasedcapture (Rebar)](nm-releasedcapture-rebar-.md) | Benachrichtigt das übergeordnete Fenster eines Info leisten Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md) <br/>                                                                                        |
| [RBN- \_ autobreak](rbn-autobreak.md)                          | Benachrichtigt das übergeordnete Element einer übergeordneten [Leiste](rebar-controls.md) , dass eine Unterbrechung in der Leiste angezeigt wird. Das übergeordnete Element bestimmt, ob die Unterbrechung vorgenommen werden soll. <br/>                                                                                                                            |
| [RBN- \_ AutoSize](rbn-autosize.md)                            | Wird von einem Grund leisten-Steuerelement gesendet, das mit der automatischen [**\_ Größenanpassung von RB**](rebar-control-styles.md) erstellt wird, wenn sich der grundbalken automatisch ändert. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                  |
| [RBN- \_ BeginDrag](rbn-begindrag.md)                          | Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer mit dem Ziehen eines Bands beginnt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                           |
| [RBN \_ chevronpushübertragung](rbn-chevronpushed.md)                  | Wird von einem Grund leisten-Steuerelement gesendet, wenn ein Chevron gepusht wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                                        |
| [RBN \_ childsize](rbn-childsize.md)                          | Wird von einem Grund leisten-Steuerelement gesendet, wenn die Größe des untergeordneten Fensters eines Bands geändert wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                          |
| [RBN \_ deletedband](rbn-deletedband.md)                      | Wird von einem Grund leisten-Steuerelement gesendet, nachdem ein Band gelöscht wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                  |
| [RBN- \_ Delta-Band](rbn-deletingband.md)                    | Wird von einem Grund leisten-Steuerelement gesendet, wenn ein Band im Begriff ist, gelöscht zu werden. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                             |
| [RBN- \_ EndDrag](rbn-enddrag.md)                              | Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer das Ziehen eines Bands beendet. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                            |
| [RBN- \_ GetObject](rbn-getobject.md)                          | Wird von einem Grund leisten-Steuerelement gesendet, das mit dem [**\_ Register Drop**](rebar-control-styles.md) -Stil von RB erstellt wird, wenn ein Objekt über ein Band im-Steuerelement gezogen wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/> |
| [RBN- \_ heightChange](rbn-heightchange.md)                    | Wird von einem Grund leisten-Steuerelement gesendet, wenn sich seine Höhe geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                    |
| [RBN \_ layoutchanged](rbn-layoutchanged.md)                  | Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer das Layout der Bänder eines Steuer Elements ändert. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                        |
| [RBN- \_ MinMax](rbn-minmax.md)                                | Wird von einem Grund leisten-Steuerelement gesendet, bevor ein Band maximiert oder minimiert wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                       |
| [RBN- \_ splitterdrag](rbn-splitterdrag.md)                    | Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer einen Splitter zieht. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                 |



 

### <a name="structures"></a>Strukturen



| Thema                                        | Inhalte                                                                                                                                      |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nmrbautresize**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize)         | Enthält Informationen, die zum Verarbeiten der RBN-Benachrichtigungs Codes für [ \_ Automatische Größen](rbn-autosize.md) verwendet werden. <br/>                                   |
| [**Nminfo-Leiste**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)                   | Enthält Informationen, die zum Verarbeiten verschiedener Benachrichtigungs Codes für die Info Leiste verwendet werden <br/>                                                           |
| [**Nmrebarautobreak**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) | Enthält Informationen, die mit der RBN-Benachrichtigung zum [ \_ autobreak](rbn-autobreak.md) verwendet werden.<br/>                                               |
| [**Nmrebarchevron**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)     | Enthält Informationen, die zum Verarbeiten des [RBN- \_ chevronpushbenachrichtigungscodes](rbn-chevronpushed.md) verwendet werden. <br/>                          |
| [**Nmrebarchildsize**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) | Enthält Informationen, die beim Verarbeiten des [RBN \_ childsize](rbn-childsize.md) -Benachrichtigungs Codes verwendet werden. <br/>                                  |
| [**Nmrebarsplitter**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter)   | Enthält Informationen, die zum Verarbeiten eines [RBN- \_ splitterdrag](rbn-splitterdrag.md) -Benachrichtigungs Codes verwendet werden.<br/>                                |
| [**Rbhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)       | Enthält Informationen, die für einen Treffer Testvorgang spezifisch sind. Diese Struktur wird mit der [**RB \_ HitTest**](rb-hittest.md) -Nachricht verwendet. <br/> |
| [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)       | Enthält Informationen, die ein Band in einem Grund leisten-Steuerelement definieren. <br/>                                                                      |
| [**Rebarinfo**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)               | Enthält Informationen, die die Eigenschaften des Grund leisten-Steuer Elements beschreiben. <br/>                                                                |



 

### <a name="constants"></a>Konstanten



| Thema                                            | Inhalte                                                                                              |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Grund leisten-Steuerelement Stile](rebar-control-styles.md) | Grund leisten-Steuerelemente unterstützen zusätzlich zu Standardfenster Stilen eine Reihe von Steuerelement Stilen. <br/> |



 

 

