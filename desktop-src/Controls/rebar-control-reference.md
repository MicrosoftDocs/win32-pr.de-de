---
title: Bewehrung
description: Dieser Abschnitt enthält Informationen zum Programmieren von Elementen, die mit Steuerelementen für die Neuleiste verwendet werden.
ms.assetid: vs|controls|~\controls\rebar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ac71ea71b5e0b0bd1e222d46c070a62512f0f5ff3b885fe13b19fad10f7bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434840"
---
# <a name="rebar"></a>Bewehrung

Dieser Abschnitt enthält Informationen zum Programmieren von Elementen, die mit Steuerelementen für die Neuleiste verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                            | Inhalte                                                                               |
|--------------------------------------------------|----------------------------------------------------------------------------------------|
| [Neuleistensteuerelemente](rebar-controls.md)             | *Neuleistensteuerelemente* fungieren als Container für untergeordnete Fenster.<br/>                       |
| [Verwenden von Rebar-Steuerelementen](using-rebar-controls.md) | Dieser Abschnitt enthält Beispielcode, der zeigt, wie Steuerelemente für die Neuleiste implementiert werden.<br/> |



 

### <a name="messages"></a>Meldungen



| Thema                                               | Inhalte                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RB \_ BEGINDRAG**](rb-begindrag.md)               | Versetzt das Rebar-Steuerelement in den Drag & Drop-Modus. Diese Meldung bewirkt nicht, dass eine [RBN \_ BEGINDRAG-Benachrichtigung](rbn-begindrag.md) gesendet wird. <br/>                                                 |
| [**RB \_ DELETEBAND**](rb-deleteband.md)             | Löscht ein Band aus einem Rebar-Steuerelement. <br/>                                                                                                                                                     |
| [**RB \_ DRAGMOVE**](rb-dragmove.md)                 | Aktualisiert die Ziehposition im Rebar-Steuerelement nach einer vorherigen [**RB \_ BEGINDRAG-Meldung.**](rb-begindrag.md) <br/>                                                                           |
| [**RB \_ ENDDRAG**](rb-enddrag.md)                   | Beendet den Drag & Drop-Vorgang des Steuerelements auf der Leiste. Diese Meldung bewirkt nicht, dass eine [ \_ RBN-ENDDRAG-Benachrichtigung](rbn-enddrag.md) gesendet wird. <br/>                                          |
| [**RB \_ GETBANDBORDERS**](rb-getbandborders.md)     | Ruft die Rahmen eines Bands ab. Das Ergebnis dieser Meldung kann verwendet werden, um den verwendbaren Bereich in einem Band zu berechnen. <br/>                                                                          |
| [**RB \_ GETBANDCOUNT**](rb-getbandcount.md)         | Ruft die Anzahl der Bänder ab, die sich derzeit im Rebar-Steuerelement befinden. <br/>                                                                                                                             |
| [**RB \_ GETBANDINFO**](rb-getbandinfo.md)           | Ruft Informationen zu einem angegebenen Band in einem Rebar-Steuerelement ab. <br/>                                                                                                                         |
| [**RB \_ GETBANDMARGINS**](rb-getbandmargins.md)     | Ruft die Ränder eines Bands ab.<br/>                                                                                                                                                          |
| [**RB \_ GETBARHEIGHT**](rb-getbarheight.md)         | Ruft die Höhe des Rebar-Steuerelements ab. <br/>                                                                                                                                               |
| [**RB \_ GETBARINFO**](rb-getbarinfo.md)             | Ruft Informationen zum Rebar-Steuerelement und der verwendeten Bildliste ab. <br/>                                                                                                                |
| [**RB \_ GETBKCOLOR**](rb-getbkcolor.md)             | Ruft die Standardhintergrundfarbe eines Rebar-Steuerelements ab. <br/>                                                                                                                                    |
| [**RB \_ GETCOLORSCHEME**](rb-getcolorscheme.md)     | Ruft die Farbschemainformationen aus dem Steuerelement für die Neuleiste ab. <br/>                                                                                                                           |
| [**RB \_ GETDROPTARGET**](rb-getdroptarget.md)       | Ruft den [**IDropTarget-Schnittstellenzeiger**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) eines Rebar-Steuerelements ab. <br/>                                                                                                        |
| [**RB \_ GETEXTENDEDSTYLE**](rb-getextendedstyle.md) | Ruft den erweiterten Stil ab. <br/>                                                                                                                                                                 |
| [**RB \_ GETPALETTE**](rb-getpalette.md)             | Ruft die aktuelle Palette des Rebar-Steuerelements ab. <br/>                                                                                                                                           |
| [**RB \_ GETRECT**](rb-getrect.md)                   | Ruft das umschließende Rechteck für ein bestimmtes Band in einem Rebar-Steuerelement ab. <br/>                                                                                                                    |
| [**RB \_ GETROWCOUNT**](rb-getrowcount.md)           | Ruft die Anzahl der Zeilen von Bändern in einem Rebar-Steuerelement ab. <br/>                                                                                                                                |
| [**RB \_ GETROWHEIGHT**](rb-getrowheight.md)         | Ruft die Höhe einer angegebenen Zeile in einem Rebar-Steuerelement ab. <br/>                                                                                                                              |
| [**RB \_ GETTEXTCOLOR**](rb-gettextcolor.md)         | Ruft die Standardtextfarbe eines Rebar-Steuerelements ab. <br/>                                                                                                                                          |
| [**RB \_ GETTOOLTIPS**](rb-gettooltips.md)           | Ruft das Handle für jedes QuickInfo-Steuerelement ab, das dem Steuerelement für die Neuleiste zugeordnet ist. <br/>                                                                                                           |
| [**RB \_ GETUNICODEFORMAT**](rb-getunicodeformat.md) | Ruft das Unicode-Zeichenformatflag für das Steuerelement ab. <br/>                                                                                                                             |
| [**RB \_ HITTEST**](rb-hittest.md)                   | Bestimmt, welcher Teil eines Leistenbands sich an einem bestimmten Punkt auf dem Bildschirm befindet, wenn an diesem Punkt ein Rebarband vorhanden ist. <br/>                                                                        |
| [**RB \_ IDTOINDEX**](rb-idtoindex.md)               | Konvertiert einen Bandbezeichner in einen Bandindex in einem Rebar-Steuerelement. <br/>                                                                                                                           |
| [**RB \_ INSERTBAND**](rb-insertband.md)             | Fügt ein neues Band in ein Rebar-Steuerelement ein. <br/>                                                                                                                                                   |
| [**RB \_ MAXIMIZEBAND**](rb-maximizeband.md)         | Die Größe eines Bands in einem Rebar-Steuerelement wird auf die ideale oder die größte Größe geändert. <br/>                                                                                                                   |
| [**RB \_ MINIMIZEBAND**](rb-minimizeband.md)         | Die Größe eines Bands in einem Rebar-Steuerelement wird auf seine kleinste Größe geändert. <br/>                                                                                                                                  |
| [**RB \_ MOVEBAND**](rb-moveband.md)                 | Verschiebt ein Band von einem Index in einen anderen. <br/>                                                                                                                                                  |
| [**RB \_ PUSHCHEVRON**](rb-pushchevron.md)           | Wird an ein Rebar-Steuerelement gesendet, um ein Chevron programmgesteuert zu pushen.<br/>                                                                                                                               |
| [**RB \_ SETBANDINFO**](rb-setbandinfo.md)           | Legt Die Merkmale eines vorhandenen Bands in einem Rebar-Steuerelement fest. <br/>                                                                                                                             |
| [**RB \_ SETBANDWIDTH**](rb-setbandwidth.md)         | Legt die Breite für ein angedocktes Band fest.<br/>                                                                                                                                                         |
| [**RB \_ SETBARINFO**](rb-setbarinfo.md)             | Legt die Merkmale eines Rebar-Steuerelements fest. <br/>                                                                                                                                             |
| [**RB \_ SETBKCOLOR**](rb-setbkcolor.md)             | Legt die Standardhintergrundfarbe eines Rebar-Steuerelements fest. <br/>                                                                                                                                         |
| [**RB \_ SETCOLORSCHEME**](rb-setcolorscheme.md)     | Legt die Farbschemainformationen für das Rebar-Steuerelement fest. <br/>                                                                                                                                 |
| [**RB \_ SETEXTENDEDSTYLE**](rb-setextendedstyle.md) | Legt den erweiterten Stil fest. Diese Meldung ist nicht implementiert.<br/>                                                                                                                                 |
| [**RB \_ SETPALETTE**](rb-setpalette.md)             | Legt die aktuelle Palette des Rebar-Steuerelements fest. <br/>                                                                                                                                                |
| [**RB \_ SETPARENT**](rb-setparent.md)               | Legt das übergeordnete Fenster eines Rebar-Steuerelements fest. <br/>                                                                                                                                                    |
| [**RB \_ SETTEXTCOLOR**](rb-settextcolor.md)         | Legt die Standardtextfarbe eines Rebar-Steuerelements fest. <br/>                                                                                                                                               |
| [**RB \_ SETTOOLTIPS**](rb-settooltips.md)           | Ordnet dem Steuerelement für die Neuleiste ein QuickInfo-Steuerelement zu. <br/>                                                                                                                                     |
| [**RB \_ SETUNICODEFORMAT**](rb-setunicodeformat.md) | Legt das Unicode-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen. <br/> |
| [**RB \_ SETWINDOWTHEME**](rb-setwindowtheme.md)     | Legt den visuellen Stil eines Rebar-Steuerelements fest.<br/>                                                                                                                                                 |
| [**RB \_ SHOWBAND**](rb-showband.md)                 | Zeigt ein bestimmtes Band in einem Rebar-Steuerelement an oder blendet es aus. <br/>                                                                                                                                          |
| [**RB \_ SIZETORECT**](rb-sizetorect.md)             | Versucht, das beste Layout der Bänder für das gegebene Rechteck zu finden. <br/>                                                                                                                   |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                        | Inhalte                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (Leiste)](nm-customdraw-rebar.md)            | Wird vom Rebar-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                                                                                               |
| [NM \_ NCHITTEST (Leiste)](nm-nchittest-rebar.md)              | Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine [**WM \_ NCHITTEST-Nachricht**](/windows/desktop/inputdev/wm-nchittest) empfängt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                 |
| [NM \_ RELEASEDCAPTURE (Leiste)](nm-releasedcapture-rebar-.md) | Benachrichtigt das übergeordnete Fenster eines Rebar-Steuerelements, dass das Steuerelement die Mausaufnahme frei gibt. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                        |
| [RBN \_ AUTOBREAK](rbn-autobreak.md)                          | Benachrichtigt das übergeordnete Element [einer Rebar,](rebar-controls.md) dass eine Unterbrechung in der Leiste angezeigt wird. Das übergeordnete Element bestimmt, ob die Unterbrechung festgelegt werden soll. <br/>                                                                                                                            |
| [RBN \_ AUTOIZE](rbn-autosize.md)                            | Wird von einem Rebar-Steuerelement gesendet, das mit dem [**RBS \_ AUTOSIZE-Stil**](rebar-control-styles.md) erstellt wurde, wenn die Größe der Leiste automatisch selbst geändert wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                  |
| [RBN \_ BEGINDRAG](rbn-begindrag.md)                          | Wird von einem Rebar-Steuerelement gesendet, wenn der Benutzer mit dem Ziehen eines Bandes beginnt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                           |
| [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md)                  | Wird von einem Rebar-Steuerelement gesendet, wenn ein Chevron per Push übermittelt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                                                                                                                        |
| [RBN \_ CHILDSIZE](rbn-childsize.md)                          | Wird von einem Rebar-Steuerelement gesendet, wenn die Größe des untergeordneten Fensters eines Bandes geändert wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                          |
| [RBN \_ DELETEDBAND](rbn-deletedband.md)                      | Wird von einem Rebar-Steuerelement gesendet, nachdem ein Band gelöscht wurde. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                  |
| [RBN \_ DELETINGBAND](rbn-deletingband.md)                    | Wird von einem Rebar-Steuerelement gesendet, wenn ein Band gelöscht werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                             |
| [RBN \_ ENDDRAG](rbn-enddrag.md)                              | Wird von einem Rebar-Steuerelement gesendet, wenn der Benutzer das Ziehen eines Bandes beendet. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                            |
| [RBN \_ GETOBJECT](rbn-getobject.md)                          | Wird von einem Rebar-Steuerelement gesendet, das mit dem [**RBS \_ REGISTERDROP-Stil**](rebar-control-styles.md) erstellt wurde, wenn ein Objekt über ein Band im Steuerelement gezogen wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/> |
| [RBN \_ HEIGHTCHANGE](rbn-heightchange.md)                    | Wird von einem Rebar-Steuerelement gesendet, wenn sich seine Höhe geändert hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                    |
| [RBN \_ LAYOUTCHANGED](rbn-layoutchanged.md)                  | Wird von einem Rebar-Steuerelement gesendet, wenn der Benutzer das Layout der Bänder des Steuerelements ändert. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                        |
| [RBN \_ MINMAX](rbn-minmax.md)                                | Wird von einem Rebar-Steuerelement gesendet, bevor ein Band maximiert oder minimiert wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                       |
| [RBN \_ SPLITTERDRAG](rbn-splitterdrag.md)                    | Wird von einem Rebar-Steuerelement gesendet, wenn der Benutzer einen Splitter zieht. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                 |



 

### <a name="structures"></a>Strukturen



| Thema                                        | Inhalte                                                                                                                                      |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize)         | Enthält Informationen zur Behandlung der [ \_ RBN-AUTOIZE-Benachrichtigungscodes.](rbn-autosize.md) <br/>                                   |
| [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)                   | Enthält Informationen, die bei der Behandlung verschiedener Benachrichtigungscodes für die Leiste verwendet werden. <br/>                                                           |
| [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) | Enthält Informationen, die mit der [RBN \_ AUTOBREAK-Benachrichtigung verwendet](rbn-autobreak.md) werden.<br/>                                               |
| [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)     | Enthält Informationen zur Behandlung des [RBN-CHEVRONPUSHED-Benachrichtigungscodes. \_ ](rbn-chevronpushed.md) <br/>                          |
| [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) | Enthält Informationen zur Behandlung des [RBN \_ CHILDSIZE-Benachrichtigungscodes.](rbn-childsize.md) <br/>                                  |
| [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter)   | Enthält Informationen zur Behandlung eines [RBN-SPLITTERDRAG-Benachrichtigungscodes. \_ ](rbn-splitterdrag.md)<br/>                                |
| [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)       | Enthält informationen, die für einen Treffertestvorgang spezifisch sind. Diese Struktur wird mit der [**RB \_ HITTEST-Nachricht**](rb-hittest.md) verwendet. <br/> |
| [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)       | Enthält Informationen, die ein Band in einem Rebar-Steuerelement definieren. <br/>                                                                      |
| [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)               | Enthält Informationen, die Eigenschaften des Rebar-Steuerelements beschreiben. <br/>                                                                |



 

### <a name="constants"></a>Konstanten



| Thema                                            | Inhalte                                                                                              |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Steuerelementstile für die Leiste](rebar-control-styles.md) | Beleisten-Steuerelemente unterstützen zusätzlich zu standarden Fensterstilen eine Vielzahl von Steuerelementstilen. <br/> |



 

 

