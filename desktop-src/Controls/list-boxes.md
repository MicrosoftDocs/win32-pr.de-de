---
title: Listenfeld
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Listenfeldern verwendet werden. Ein Listenfeld ist ein Steuerelement Fenster, das eine einfache Liste von Elementen enthält, aus denen der Benutzer auswählen kann.
ms.assetid: vs|controls|~\controls\listboxes\listboxes.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fda5e6bb2d1d4c3c4f23e506900257c1b2ce64b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102394"
---
# <a name="list-box"></a>Listenfeld

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Listenfeldern verwendet werden. Ein Listenfeld ist ein Steuerelement Fenster, das eine einfache Liste von Elementen enthält, aus denen der Benutzer auswählen kann. Verwenden Sie für komplexere Listen stattdessen die [Listenansicht](list-view-control-reference.md) .

### <a name="overviews"></a>Übersichten



| Thema                                    | Inhalte                                                              |
|------------------------------------------|-----------------------------------------------------------------------|
| [Informationen zu Listenfeldern](about-list-boxes.md) | Beschreibt die Listenfeld Features.<br/>                               |
| [Verwenden von Listenfeldern](using-list-boxes.md) | Erläutert das Ausführen von Aufgaben, die mit Listenfeldern verknüpft sind. <br/> |



 

### <a name="functions"></a>Functions



| Thema                                    | Inhalte                                                                                                                |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Dlgdirlist**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)         | Ersetzt den Inhalt eines Listen Felds durch die Namen der Unterverzeichnisse und Dateien in einem angegebenen Verzeichnis.<br/> |
| [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) | Ruft die aktuelle Auswahl aus einem Listenfeld mit einer einzelnen Auswahl ab.<br/>                                            |
| [**Drawinsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert)         | Zeichnet das Einfügesymbol im übergeordneten Fenster des angegebenen Drag-Listen Felds. <br/>                                  |
| [**Getlistboxinfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) | Ruft Informationen zum angegebenen Listenfeld ab.<br/>                                                          |
| [**Lbitemfrompt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt)     | Ruft den Index des Elements an der angegebenen Stelle in einem Listenfeld ab. <br/>                                       |
| [**Makedraglist**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist)     | Ändert das angegebene Listenfeld für die einfache Auswahl in ein Drag-Listenfeld. <br/>                                         |



 

### <a name="messages"></a>Meldungen



| Thema                                                     | Inhalte                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LB- \_ AddFile**](lb-addfile.md)                         | Fügt einem Listenfeld, das eine Verzeichnisliste enthält, den angegebenen Dateinamen hinzu. <br/>                                                                                                                                                                                     |
| [**LB- \_ AddString**](lb-addstring.md)                     | Fügt einem Listenfeld eine Zeichenfolge hinzu. <br/>                                                                                                                                                                                                                                      |
| [**LB- \_ deletestring**](lb-deletestring.md)               | Löscht eine Zeichenfolge in einem Listenfeld. <br/>                                                                                                                                                                                                                                   |
| [**LB- \_ dir**](lb-dir.md)                                 | Fügt der Liste Namen hinzu, die von einem Listenfeld angezeigt werden. <br/>                                                                                                                                                                                                                   |
| [**LB- \_ FindString**](lb-findstring.md)                   | Sucht die erste Zeichenfolge in einem Listenfeld, das mit der angegebenen Zeichenfolge beginnt. <br/>                                                                                                                                                                                       |
| [**LB- \_ FindStringExact**](lb-findstringexact.md)         | Sucht die erste Listenfeld Zeichenfolge, die exakt mit der angegebenen Zeichenfolge übereinstimmt <br/>                                                                                                                                          |
| [**LB- \_ getanchorindex**](lb-getanchorindex.md)           | Ruft den Index des Anker Elements ab, das das Element ist, aus dem eine Mehrfachauswahl beginnt. <br/>                                                                                                                                                                       |
| [**LB \_ getcaretindex**](lb-getcaretindex.md)             | Ruft den Index des Elements ab, das über das Fokus Rechteck in einem Listenfeld für Mehrfachauswahl verfügt. Das Element ist möglicherweise nicht ausgewählt. <br/>                                                                                                                               |
| [**LB- \_ GetCount**](lb-getcount.md)                       | Ruft die Anzahl der Elemente in einem Listenfeld ab. <br/>                                                                                                                                                                                                                           |
| [**LB- \_ getcurrsel**](lb-getcursel.md)                     | Ruft den Index des derzeit ausgewählten Elements (sofern vorhanden) in einem Listenfeld mit einer einzelnen Auswahl ab. <br/>                                                                                                                                                                            |
| [**LB- \_ gethorizontalblock**](lb-gethorizontalextent.md) | Ruft die Breite in Pixel ab, in der ein Listenfeld Horizontal (die scrollbare Breite) gescrollt werden kann, wenn das Listenfeld eine horizontale Schiebe Leiste hat. <br/>                                                                                                                       |
| [**LB- \_ GetItemData**](lb-getitemdata.md)                 | Ruft den Anwendungs definierten Wert ab, der dem angegebenen Listenfeld Element zugeordnet ist. <br/>                                                                                                                                                                                   |
| [**LB- \_ GetItemHeight**](lb-getitemheight.md)             | Ruft die Höhe der Elemente in einem Listenfeld ab. <br/>                                                                                                                                                                                                                           |
| [**LB- \_ GetItemRect**](lb-getitemrect.md)                 | Ruft die Abmessungen des Rechtecks ab, das ein Listenfeld Element umschließt, das gerade im Listenfeld angezeigt wird. <br/>                                                                                                                                                    |
| [**LB \_ getlistboxinfo**](lb-getlistboxinfo.md)           | Ruft die Anzahl der Elemente pro Spalte in einem angegebenen Listenfeld ab. <br/>                                                                                                                                                                                                      |
| [**LB \_ getLocale**](lb-getlocale.md)                     | Ruft das aktuelle Gebiets Schema des Listen Felds ab. <br/>                                                                                                                                                                                                                          |
| [**LB- \_ GetSEL**](lb-getsel.md)                           | Ruft den Auswahl Zustand eines Elements ab. <br/>                                                                                                                                                                                                                              |
| [**LB- \_ getselcount**](lb-getselcount.md)                 | Ruft die Gesamtanzahl der ausgewählten Elemente in einem Listenfeld mit Mehrfachauswahl ab. <br/>                                                                                                                                                                                         |
| [**LB- \_ getselitems**](lb-getselitems.md)                 | Füllt einen Puffer mit einem Array von ganzen Zahlen, die die Element Nummern ausgewählter Elemente in einem Listenfeld mit Mehrfachauswahl angeben. <br/>                                                                                                                                        |
| [**LB- \_ gettext**](lb-gettext.md)                         | Ruft eine Zeichenfolge aus einem Listenfeld ab. <br/>                                                                                                                                                                                                                                    |
| [**LB- \_ gettextlen**](lb-gettextlen.md)                   | Ruft die Länge einer Zeichenfolge in einem Listenfeld ab. <br/>                                                                                                                                                                                                                        |
| [**LB- \_ gettopindex**](lb-gettopindex.md)                 | Ruft den Index des ersten sichtbaren Elements in einem Listenfeld ab. <br/>                                                                                                                                                                                                           |
| [**LB- \_ InitStorage**](lb-initstorage.md)                 | Ordnet Arbeitsspeicher zum Speichern von Listenfeld Elementen zu. Diese Meldung wird verwendet, bevor eine Anwendung eine große Anzahl von Elementen zu einem Listenfeld hinzufügt.<br/>                                                                                                                                |
| [**LB- \_ InsertString**](lb-insertstring.md)               | Fügt eine Zeichenfolge oder Elementdaten in ein Listenfeld ein. Anders als bei der [**lb \_ AddString**](lb-addstring.md) -Nachricht bewirkt die [**lb- \_ InsertString**](lb-insertstring.md) -Nachricht nicht, dass eine Liste mit dem [**lbs- \_ Sortier**](list-box-styles.md) Stil sortiert wird. <br/> |
| [**LB- \_ itemfrompoint**](lb-itemfrompoint.md)             | Ruft den NULL basierten Index des Elements ab, das dem angegebenen Punkt in einem Listenfeld am nächsten liegt.<br/>                                                                                                                                                                                   |
| [**LB- \_ resetcontent**](lb-resetcontent.md)               | Entfernt alle Elemente aus einem Listenfeld. <br/>                                                                                                                                                                                                                                |
| [**LB- \_ SelectString**](lb-selectstring.md)               | Durchsucht ein Listenfeld nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt. <br/>                                                                                                                                                                            |
| [**LB- \_ selitemrange**](lb-selitemrange.md)               | Aktiviert oder deaktiviert ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit Mehrfachauswahl. <br/>                                                                                                                                                                              |
| [**LB- \_ selitemrangeex**](lb-selitemrangeex.md)           | Wählt ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit Mehrfachauswahl aus. <br/>                                                                                                                                                                                           |
| [**LB- \_ Zielindex**](lb-setanchorindex.md)           | Legt das Anker Element fest, das das Element ist, aus dem eine Mehrfachauswahl beginnt. Eine Mehrfachauswahl umfasst alle Elemente vom Anker Element bis zum Caretzeichen.<br/>                                                                                                        |
| [**LB- \_ setcaretindex**](lb-setcaretindex.md)             | Legt das Fokus Rechteck auf das Element am angegebenen Index in einem Mehrfachauswahl-Listenfeld fest. Wenn das Element nicht sichtbar ist, wird es in die Ansicht gescrollt. <br/>                                                                                                               |
| [**LB- \_ setcolumnwidth**](lb-setcolumnwidth.md)           | Legt die Breite aller Spalten in einem Listenfeld mit mehreren Spalten in Pixel fest. <br/>                                                                                                                                                                                          |
| [**LB- \_ SetCount**](lb-setcount.md)                       | Legt die Anzahl von Elementen in einem Listenfeld fest, das mit dem [**lbs \_ NODATA**](list-box-styles.md) -Stil erstellt wurde und nicht mit dem [**lbs \_ hasstrings**](list-box-styles.md) -Stil erstellt wurde. <br/>                                                          |
| [**LB- \_ setcurrsel**](lb-setcursel.md)                     | Wählt eine Zeichenfolge aus und führt ggf. einen Bildlauf in die Ansicht aus. <br/>                                                                                                                                                                                                          |
| [**LB-Abbild \_ Umfang**](lb-sethorizontalextent.md) | Legt die Breite (in Pixel) fest, um die ein Listenfeld Horizontal (die scrollbare Breite) gescrollt werden kann. <br/>                                                                                                                                                               |
| [**LB- \_ Daten**](lb-setitemdata.md)                 | Legt einen Wert fest, der dem angegebenen Element in einem Listenfeld zugeordnet ist. <br/>                                                                                                                                                                                            |
| [**LB- \_ Größe**](lb-setitemheight.md)             | Legt die Höhe von Elementen in einem Listenfeld in Pixel fest. <br/>                                                                                                                                                                                                               |
| [**LB- \_ setlocale**](lb-setlocale.md)                     | Legt das aktuelle Gebiets Schema des Listen Felds fest. <br/>                                                                                                                                                                                                                          |
| [**LB- \_ Sekunden**](lb-setsel.md)                           | Wählt eine Zeichenfolge in einem Listenfeld mit Mehrfachauswahl aus. <br/>                                                                                                                                                                                                                |
| [**LB- \_ settabstopps**](lb-settabstops.md)                 | Legt die Position der Tabstopps in einem Listenfeld fest. <br/>                                                                                                                                                                                                                        |
| [**LB- \_ settopindex**](lb-settopindex.md)                 | Stellt sicher, dass das angegebene Element in einem Listenfeld sichtbar ist. <br/>                                                                                                                                                                                                         |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                             | Inhalte                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LBN- \_ dblclk](lbn-dblclk.md)                     | Benachrichtigt die Anwendung, dass der Benutzer auf ein Element in einem Listenfeld Doppel geklickt hat. <br/>                                                                                                                                                                                                                                         |
| [LBN- \_ errspace](lbn-errspace.md)                 | Benachrichtigt die Anwendung, dass das Listenfeld nicht genügend Arbeitsspeicher zuordnen kann, um eine bestimmte Anforderung zu erfüllen. <br/>                                                                                                                                                                                                                     |
| [LBN- \_ killfokus](lbn-killfocus.md)               | Benachrichtigt die Anwendung, dass das Listenfeld den Tastaturfokus verloren hat. <br/>                                                                                                                                                                                                                                                  |
| [LBN \_ selcancel](lbn-selcancel.md)               | Benachrichtigt die Anwendung, dass der Benutzer die Auswahl in einem Listenfeld abgebrochen hat. <br/>                                                                                                                                                                                                                                         |
| [LBN \_ selChange](lbn-selchange.md)               | Benachrichtigt die Anwendung, dass sich die Auswahl in einem Listenfeld geändert hat. <br/>                                                                                                                                                                                                                                                   |
| [LBN- \_ SetFocus](lbn-setfocus.md)                 | Benachrichtigt die Anwendung, dass das Listenfeld den Tastaturfokus erhalten hat. <br/>                                                                                                                                                                                                                                              |
| [**WM- \_ Diagramm**](wm-chartoitem.md)           | Wird von einem Listenfeld mit dem [**lbs- \_ wantkeyboardinput**](list-box-styles.md) -Stil als Reaktion auf eine [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht an seinen Besitzer gesendet. <br/>                                                                                                                                        |
| [**WM \_ ctlcolorlistbox**](wm-ctlcolorlistbox.md) | Wird an das übergeordnete Fenster eines Listen Felds gesendet, bevor das System das Listenfeld zeichnet. Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster die Text-und Hintergrundfarben des Listen Felds mit dem angegebenen Kontext Handle für den Anzeigegerät festlegen. <br/>                                                                              |
| [**WM- \_ DeleteItem**](wm-deleteitem.md)           | Wird an den Besitzer eines Listen Felds oder Kombinations Felds gesendet, wenn das Listenfeld oder Kombinations Feld zerstört wird oder wenn Elemente von der [**lb- \_ deletestring**](lb-deletestring.md)- [**, lb \_ resetcontent**](lb-resetcontent.md)-, [**CB \_ deletestring**](cb-deletestring.md)-oder [**CB \_ resetcontent**](cb-resetcontent.md) -Nachricht entfernt werden. <br/> |
| [**WM \_ vkeytoitem**](wm-vkeytoitem.md)           | Wird von einem Listenfeld mit dem [**lbs- \_ wantkeyboardinput**](list-box-styles.md) -Stil an seinen Besitzer als Antwort auf eine [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Nachricht gesendet. <br/>                                                                                                                                  |
| [DL- \_ BeginDrag](dl-begindrag.md)                 | Benachrichtigt das übergeordnete Fenster des Zieh Listen Felds, dass der Benutzer mit der linken Maustaste auf ein Element geklickt hat. <br/>                                                                                                                                                                                                                   |
| [DL- \_ Abbruch](dl-canceldrag.md)               | Signalisiert, dass der Benutzer einen Zieh Vorgang abgebrochen hat, indem er auf die Rechte Maustaste klickt oder die ESC-Taste gedrückt hat. <br/>                                                                                                                                                                                                          |
| [DL- \_ Zieh Vorgänge](dl-dragging.md)                   | Signalisiert, dass der Benutzer beim Ziehen eines Elements die Maus bewegt hat. <br/>                                                                                                                                                                                                                                                        |
| [DL \_ gelöscht](dl-dropped.md)                     | Signalisiert, dass der Benutzer einen Zieh Vorgang durch Loslassen der linken Maustaste abgeschlossen hat. <br/>                                                                                                                                                                                                                                 |



 

### <a name="structures"></a>Strukturen



| Thema                                        | Inhalte                                                                                                                                                               |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) | Enthält Informationen zu einem gelöschten Listenfeld oder Kombinations Feld Element.<br/>                                                                                            |
| [**Draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)         | Enthält Informationen zu einem Drag-Ereignis. Der Zeiger auf [**draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) wird als *LPARAM* -Parameter der Drag List-Nachricht übergeben. <br/> |



 

### <a name="constants"></a>Konstanten



| Thema                                  | Inhalte                                                                |
|----------------------------------------|-------------------------------------------------------------------------|
| [Listenfeld Stile](list-box-styles.md) | Beschreibt die Fenster Stile, die ein Listenfeld-Steuerelement definieren. <br/> |



 

 

