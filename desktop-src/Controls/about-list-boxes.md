---
title: Informationen zu Listenfeldern
description: In diesem Abschnitt werden die Listenfeld Features beschrieben.
ms.assetid: 359bb363-5b97-4e0c-bdc4-bfa6a6504a76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674712226a79960e44ab99ed8e59c88b27984efb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474325"
---
# <a name="about-list-boxes"></a>Informationen zu Listenfeldern

Ein Listenfeld-Steuerelement enthält eine einfache Liste, aus der der Benutzer in der Regel ein oder mehrere Elemente auswählen kann. Listenfelder bieten im Vergleich zu [Listenansicht](list-view-control-reference.md) -Steuerelementen eingeschränkte Flexibilität.

Listenfeld Elemente können durch Text Zeichenfolgen, Bitmaps oder beides dargestellt werden. Wenn das Listenfeld nicht groß genug ist, um alle Listenfeld Elemente gleichzeitig anzuzeigen, stellt das Listenfeld eine Bild Lauf Leiste bereit. Der Benutzer scrollt durch die Listenfeld Elemente und wendet den Auswahl Status nach Bedarf an oder entfernt ihn. Wenn Sie ein Listenfeld Element auswählen, ändert es sich in der Regel durch Ändern der Text-und Hintergrundfarben in die Werte, die von den relevanten betriebssystemmetriken angegeben werden. Wenn der Benutzer ein Element auswählt oder deaktiviert, sendet das System eine Benachrichtigungs Meldung an das übergeordnete Fenster des Listen Felds.

Für eine ANSI-Anwendung konvertiert das System den Text in einem Listenfeld mithilfe der **CP \_ ACP-** Codepage in Unicode. Dies kann zu Problemen führen. Wenn Sie z. b. in einem nicht-Unicode-Listenfeld unter Windows eine Zeichenfolge mit untergeordneten Zeichen haben, wird die japanische Version gegartet. Um dieses Problem zu beheben, kompilieren Sie die Anwendung entweder als Unicode, oder verwenden Sie ein vom Besitzer gezeichnetes Listenfeld.

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Erstellen eines Listen Felds](#creating-a-list-box)
-   [Listenfeld Typen und Stile](#list-box-types-and-styles)
-   [Listenfeld Funktionen](#list-box-functions)
-   [Benachrichtigungs Meldungen von Listenfeldern](#notification-messages-from-list-boxes)
-   [Nachrichten in Listenfelder](#notification-messages-from-list-boxes)
-   [Standardmäßige Fenster Nachrichtenverarbeitung](#default-window-message-processing)
-   [Vom Besitzer gezeichnete Listenfelder](#owner-drawn-list-boxes)
-   [Listenfelder ziehen](#drag-list-boxes)
    -   [Erstellen von Drag-Listenfeldern](#creating-drag-list-boxes)
    -   [Listenfeld Meldungen ziehen](#drag-list-box-messages)
    -   [Benachrichtigungs Codes für das Listenfeld ziehen](#drag-list-box-notification-codes)

## <a name="creating-a-list-box"></a>Erstellen eines Listen Felds

Die einfachste Möglichkeit, ein Listenfeld in einem Dialogfeld zu erstellen, besteht darin, es aus der Toolbox in Microsoft Visual Studio auf die Dialogfeld Ressource zu ziehen. Um ein Listenfeld dynamisch zu erstellen oder um ein Listenfeld in einem anderen Fenster als einem Dialogfeld zu erstellen, verwenden Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", wobei Sie die Fenster Klasse " [**WC \_ ListBox**](common-control-window-classes.md) " und die entsprechenden [Listenfeld Stile](list-box-styles.md)angeben.

## <a name="list-box-types-and-styles"></a>Listenfeld Typen und Stile

Es gibt zwei Arten von Listenfeldern: einfache Auswahl (Standard) und Mehrfachauswahl. In einem Listenfeld mit einfacher Auswahl kann der Benutzer jeweils nur ein Element auswählen. Im Listenfeld Mehrfachauswahl kann der Benutzer mehrere Elemente gleichzeitig auswählen. Um ein Listenfeld Mehrfachauswahl zu erstellen, geben Sie den [**lbs \_ multiplesel**](list-box-styles.md) -oder den [**lbs- \_ extendedsel**](list-box-styles.md) -Stil an.

Die Darstellung und der Vorgang eines Listen Felds werden von [Listenfeld Stilen](list-box-styles.md) und Fenster Stilen gesteuert. Diese Stile geben an, ob die Liste sortiert ist, in mehreren Spalten angeordnet ist, von der Anwendung gezeichnet wird usw. Die Dimensionen und Stile eines Listen Felds werden in der Regel in einer Dialogfeld Vorlage definiert, die in den Ressourcen einer Anwendung enthalten ist.

> [!Note]  
> Um visuelle Stile mit diesen Steuerelementen zu verwenden, muss eine Anwendung ein Manifest einschließen und muss am Anfang des Programms [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) aufzurufen. Weitere Informationen zu visuellen Stilen finden Sie unter [visuelle Stile](themes-overview.md). Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="list-box-functions"></a>Listenfeld Funktionen

Die [**dlgdirlist**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) -Funktion ersetzt den Inhalt eines Listen Felds durch die Namen von Laufwerken, Verzeichnissen und Dateien, die mit einem bestimmten Kriteriensatz übereinstimmen. Die [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) -Funktion Ruft die aktuelle Auswahl in einem Listenfeld ab, das von **dlgdirlist** initialisiert wird. Diese Funktionen ermöglichen es dem Benutzer, ein Laufwerk, ein Verzeichnis oder eine Datei aus einem Listenfeld auszuwählen, ohne den Speicherort und den Namen der Datei einzugeben.

Außerdem gibt die [**getlistboxinfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) -Funktion die Anzahl der Elemente pro Spalte in einem angegebenen Listenfeld zurück.

## <a name="notification-messages-from-list-boxes"></a>Benachrichtigungs Meldungen von Listenfeldern

Wenn ein Ereignis in einem Listenfeld auftritt, sendet das Listenfeld einen Benachrichtigungs Code in Form einer WM- [**\_ Befehls**](/windows/desktop/menurc/wm-command) Meldung an die Dialogfeld Prozedur des Besitzer Fensters. Listenfeld-Benachrichtigungs Codes werden gesendet, wenn ein Benutzer ein Listenfeld Element auswählt, doppelklickt oder abbricht. , wenn das Listenfeld den Tastaturfokus erhält oder verliert. und wenn das System nicht genügend Arbeitsspeicher für eine Listenfeld Anforderung zuordnen kann. Eine **WM- \_ Befehls** Meldung enthält den Listenfeld Bezeichner im nieder wertigen Wort des *wParam* -Parameters und den Benachrichtigungs Code im höherwertigen Wort. Der *LPARAM* -Parameter enthält das Steuerelement Fenster handle.

Eine Dialogfeld Prozedur ist nicht erforderlich, um diese Nachrichten zu verarbeiten. Diese werden von der standardmäßigen Fenster Prozedur verarbeitet.

Eine Anwendung sollte die folgenden Listenfeld-Benachrichtigungs Codes überwachen und verarbeiten.



| Benachrichtigungs Code                   | BESCHREIBUNG                                                      |
|-------------------------------------|------------------------------------------------------------------|
| [LBN- \_ dblclk](lbn-dblclk.md)       | Der Benutzer doppelklickt auf ein Element im Listenfeld.                  |
| [LBN- \_ errspace](lbn-errspace.md)   | Das Listenfeld kann nicht genügend Arbeitsspeicher zuordnen, um eine Anforderung zu erfüllen. |
| [LBN- \_ killfokus](lbn-killfocus.md) | Das Listenfeld verliert den Tastaturfokus.                           |
| [LBN \_ selcancel](lbn-selcancel.md) | Der Benutzer bricht die Auswahl eines Elements im Listenfeld ab.       |
| [LBN \_ selChange](lbn-selchange.md) | Die Auswahl in einem Listenfeld wird gerade geändert.                  |
| [LBN- \_ SetFocus](lbn-setfocus.md)   | Das Listenfeld erhält den Tastaturfokus.                        |



 

## <a name="messages-to-list-boxes"></a>Nachrichten in Listenfelder

In einer Dialogfeld Prozedur können Nachrichten an ein Listenfeld gesendet werden, um Listenfeld Elemente hinzuzufügen, zu löschen, zu überprüfen und zu ändern. Eine Dialogfeld Prozedur könnte z. b. eine [**lb- \_ AddString**](lb-addstring.md) -Nachricht an ein Listenfeld senden, um ein Element hinzuzufügen, und eine [**lb- \_ GetSEL**](lb-getsel.md) -Nachricht, um zu bestimmen, ob das Element ausgewählt ist. Andere Meldungen legen Informationen über die Größe, Darstellung und das Verhalten des Listen Felds fest und rufen diese ab. Beispielsweise wird durch die Nachricht [**lb \_ sethorizontalblock**](lb-sethorizontalextent.md) die scrollbare Breite eines Listen Felds festgelegt. Eine Dialogfeld Prozedur kann jede Nachricht mithilfe der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion oder der [**SendDlgItemMess**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) -Funktion an ein Listenfeld senden.

Auf ein Listenfeld Element wird häufig über den *Index* verwiesen, eine ganze Zahl, die die Position des Elements im Listenfeld darstellt. Der Index des ersten Elements in einem Listenfeld ist 0, der Index des zweiten Elements ist 1 usw.

In der folgenden Tabelle wird beschrieben, wie die vordefinierte Listenfeld Prozedur auf Listenfeld Meldungen antwortet.



| `Message`                                                   | Antwort                                                                                                                                                                                                                         |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LB- \_ AddFile**](lb-addfile.md)                         | Fügt eine Datei in ein von der [**dlgdirlist**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) -Funktion ausgefülltes Verzeichnislisten Feld ein und ruft den Listenfeld Index des eingefügten Elements ab.                                                                  |
| [**LB- \_ AddString**](lb-addstring.md)                     | Fügt einem Listenfeld eine Zeichenfolge hinzu und gibt den Index zurück.                                                                                                                                                                               |
| [**LB- \_ deletestring**](lb-deletestring.md)               | Entfernt eine Zeichenfolge aus einem Listenfeld und gibt die Anzahl der Zeichen folgen zurück, die in der Liste verbleiben.                                                                                                                                      |
| [**LB- \_ dir**](lb-dir.md)                                 | Fügt einem Listenfeld eine Liste von Dateinamen hinzu und gibt den Index des letzten hinzugefügten Datei namens zurück.                                                                                                                                       |
| [**LB- \_ FindString**](lb-findstring.md)                   | Gibt den Index der ersten Zeichenfolge im Listenfeld zurück, das mit einer angegebenen Zeichenfolge beginnt.                                                                                                                                       |
| [**LB- \_ FindStringExact**](lb-findstringexact.md)         | Gibt den Index der Zeichenfolge im Listenfeld zurück, das gleich einer angegebenen Zeichenfolge ist.                                                                                                                                             |
| [**LB- \_ getanchorindex**](lb-getanchorindex.md)           | Gibt den Index des Elements zurück, das von der Maus zuletzt ausgewählt wurde.                                                                                                                                                                      |
| [**LB \_ getcaretindex**](lb-getcaretindex.md)             | Gibt den Index des Elements zurück, das über das Fokus Rechteck verfügt.                                                                                                                                                                      |
| [**LB- \_ GetCount**](lb-getcount.md)                       | Gibt die Anzahl der Elemente im Listenfeld zurück.                                                                                                                                                                                     |
| [**LB- \_ getcurrsel**](lb-getcursel.md)                     | Gibt den Index des derzeit ausgewählten Elements zurück.                                                                                                                                                                                |
| [**LB- \_ gethorizontalblock**](lb-gethorizontalextent.md) | Gibt die scrollbare Breite eines Listen Felds in Pixel zurück.                                                                                                                                                                          |
| [**LB- \_ GetItemData**](lb-getitemdata.md)                 | Gibt den Wert zurück, der dem angegebenen Element zugeordnet ist.                                                                                                                                                                    |
| [**LB- \_ GetItemHeight**](lb-getitemheight.md)             | Gibt die Höhe eines Elements in einem Listenfeld in Pixel zurück.                                                                                                                                                                         |
| [**LB- \_ GetItemRect**](lb-getitemrect.md)                 | Ruft die Client Koordinaten des angegebenen Listenfeld Elements ab.                                                                                                                                                                 |
| [**LB \_ getLocale**](lb-getlocale.md)                     | Ruft das Gebiets Schema des Listen Felds ab. Das Haupt Wort enthält den Länder-/Regionscode, und das nieder wertige Wort enthält den sprach Bezeichner.                                                                              |
| [**LB- \_ GetSEL**](lb-getsel.md)                           | Gibt den Auswahl Zustand eines Listenfeld Elements zurück.                                                                                                                                                                                  |
| [**LB- \_ getselcount**](lb-getselcount.md)                 | Gibt die Anzahl ausgewählter Elemente in einem Listenfeld mit Mehrfachauswahl zurück.                                                                                                                                                           |
| [**LB- \_ getselitems**](lb-getselitems.md)                 | Erstellt ein Array der Indizes aller ausgewählten Elemente in einem Listenfeld mit Mehrfachauswahl und gibt die Gesamtanzahl der ausgewählten Elemente zurück.                                                                                           |
| [**LB- \_ gettext**](lb-gettext.md)                         | Ruft die Zeichenfolge ab, die einem angegebenen Element und der Länge der Zeichenfolge zugeordnet ist.                                                                                                                                              |
| [**LB- \_ gettextlen**](lb-gettextlen.md)                   | Gibt die Länge der Zeichenfolge in Zeichen zurück, die einem angegebenen Element zugeordnet ist.                                                                                                                                               |
| [**LB- \_ gettopindex**](lb-gettopindex.md)                 | Gibt den Index des ersten sichtbaren Elements in einem Listenfeld zurück.                                                                                                                                                                       |
| [**LB- \_ InitStorage**](lb-initstorage.md)                 | Belegt Speicher für die angegebene Anzahl von Elementen und die zugeordneten Zeichen folgen.                                                                                                                                                 |
| [**LB- \_ InsertString**](lb-insertstring.md)               | Fügt eine Zeichenfolge an einem angegebenen Index in einem Listenfeld ein.                                                                                                                                                                             |
| [**LB- \_ itemfrompoint**](lb-itemfrompoint.md)             | Ruft den NULL basierten Index des Elements ab, das dem angegebenen Punkt in einem Listenfeld am nächsten liegt.                                                                                                                                            |
| [**LB- \_ resetcontent**](lb-resetcontent.md)               | Entfernt alle Elemente aus einem Listenfeld.                                                                                                                                                                                               |
| [**LB- \_ SelectString**](lb-selectstring.md)               | Wählt die erste gefundene Zeichenfolge aus, die mit einem angegebenen Präfix übereinstimmt.                                                                                                                                                               |
| [**LB- \_ selitemrange**](lb-selitemrange.md)               | Wählt einen angegebenen Bereich von Elementen in einem Listenfeld aus.                                                                                                                                                                                |
| [**LB- \_ selitemrangeex**](lb-selitemrangeex.md)           | Wählt einen angegebenen Bereich von Elementen aus, wenn der Index des ersten Elements im Bereich kleiner als der Index des letzten Elements im Bereich ist. Bricht die Auswahl im Bereich ab, wenn der Index des ersten Elements größer als das letzte ist. |
| [**LB- \_ Zielindex**](lb-setanchorindex.md)           | Legt das Element fest, das von der Maus zuletzt für ein angegebenes Element ausgewählt wurde.                                                                                                                                                                  |
| [**LB- \_ setcaretindex**](lb-setcaretindex.md)             | Legt das Fokus Rechteck auf ein angegebenes Listenfeld Element fest.                                                                                                                                                                           |
| [**LB- \_ setcolumnwidth**](lb-setcolumnwidth.md)           | Legt die Breite aller Spalten in einem Listenfeld in Pixel fest.                                                                                                                                                                         |
| [**LB- \_ SetCount**](lb-setcount.md)                       | Legt die Anzahl der Elemente in einem Listenfeld fest.                                                                                                                                                                                          |
| [**LB- \_ setcurrsel**](lb-setcursel.md)                     | Wählt ein angegebenes Listenfeld Element aus.                                                                                                                                                                                               |
| [**LB-Abbild \_ Umfang**](lb-sethorizontalextent.md) | Legt die scrollbare Breite eines Listen Felds in Pixel fest.                                                                                                                                                                             |
| [**LB- \_ Daten**](lb-setitemdata.md)                 | Ordnet einem Listenfeld Element einen Wert zu.                                                                                                                                                                                         |
| [**LB- \_ Größe**](lb-setitemheight.md)             | Legt die Höhe eines Elements oder der Elemente in einem Listenfeld in Pixel fest.                                                                                                                                                                   |
| [**LB- \_ setlocale**](lb-setlocale.md)                     | Legt das Gebiets Schema eines Listen Felds fest und gibt den vorherigen Gebiets Schema Bezeichner zurück.                                                                                                                                                        |
| [**LB- \_ Sekunden**](lb-setsel.md)                           | Wählt ein Element in einem Listenfeld mit Mehrfachauswahl aus.                                                                                                                                                                                |
| [**LB- \_ settabstopps**](lb-settabstops.md)                 | Legt die Tabstopps auf die in einem angegebenen Array angegebenen fest.                                                                                                                                                                      |
| [**LB- \_ settopindex**](lb-settopindex.md)                 | Führt einen Bildlauf im Listenfeld durch, sodass sich das angegebene Element am oberen Rand des sichtbaren Bereichs befindet.                                                                                                                                                   |



 

## <a name="default-window-message-processing"></a>Standardmäßige Fenster Nachrichtenverarbeitung

Die Fenster Prozedur für die vordefinierte Listenfeld Fenster-Klasse führt die Standard Verarbeitung für alle Nachrichten aus, die vom Listenfeld nicht verarbeitet werden. Wenn die Listenfeld Prozedur für eine Nachricht **false** zurückgibt, prüft die vordefinierte Fenster Prozedur die Meldung und führt Standard Aktionen aus, wie in der folgenden Tabelle dargestellt.



| `Message`                                            | Standardaktion                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ -Zeichen**](/windows/desktop/inputdev/wm-char)                   | Verschiebt die Auswahl auf das erste Element, das mit dem vom Benutzer eingegebenen Zeichen beginnt. Wenn das Listenfeld den Stil "L. Besitzer [**\_ Zeichnen**](button-styles.md) " aufweist, erfolgt keine Aktion. Mehrere Zeichen, die innerhalb eines kurzen Intervalls eingegeben werden, werden als Gruppe behandelt, und das erste Element, das mit dieser Zeichenfolge beginnt, wird ausgewählt.<br/> |
| [**WM \_ Erstellen**](/windows/desktop/winmsg/wm-create)                 | Erstellt ein leeres Listenfeld.                                                                                                                                                                                                                                                                                                                                               |
| [**WM \_ zerstören**](/windows/desktop/winmsg/wm-destroy)               | Zerstört das Listenfeld und gibt alle Ressourcen frei, die es verwendet.                                                                                                                                                                                                                                                                                                              |
|                                                    | Übergibt die Nachricht an die Dialogfeld Prozedur oder den übergeordneten Fenster Prozess.                                                                                                                                                                                                                                                                                                 |
| [**WM \_ aktivieren**](/windows/desktop/winmsg/wm-enable)                 | Wenn das Steuerelement sichtbar ist, wird das Rechteck für ungültig erklärt, sodass die Zeichen folgen Grau gezeichnet werden können.                                                                                                                                                                                                                                                                                 |
| [**WM- \_ erasebkgnd**](/windows/desktop/winmsg/wm-erasebkgnd)         | Löscht den Hintergrund eines Listen Felds. Wenn das Listenfeld den Stil "L. Besitzer [**\_ Zeichnen**](button-styles.md) " aufweist, wird der Hintergrund nicht gelöscht.                                                                                                                                                                                                                   |
| [**WM \_ getdlgcode**](/windows/desktop/dlgbox/wm-getdlgcode)         | Gibt dlgc \_ wantpfeile \| dlgc \_ wantchars zurück und gibt an, dass die Standardprozedur für das Listenfeld die Pfeiltasten und die [**WM \_ char**](/windows/desktop/inputdev/wm-char) -Meldungen verarbeitet.                                                                                                                                                                                                      |
| [**WM- \_ getFont**](/windows/desktop/winmsg/wm-getfont)               | Gibt ein Handle für die aktuelle Schriftart für das Listenfeld zurück.                                                                                                                                                                                                                                                                                                                   |
| [**WM- \_ HScroll**](wm-hscroll.md)                  | Führt einen horizontalen Bildlauf im Listenfeld aus.                                                                                                                                                                                                                                                                                                                                       |
| [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown)             | Verarbeitet virtuelle Schlüssel für den Bildlauf. Der virtuelle Schlüssel ist der Index des Elements, zu dem die Einfügemarke verschoben werden soll. Die Auswahl wird nicht geändert.                                                                                                                                                                                                                                       |
| [**WM- \_ killfokus**](/windows/desktop/inputdev/wm-killfocus)         | Schaltet die Einfügemarke aus und zerstört sie. Sendet einen [LBN- \_ killfocus](lbn-killfocus.md) -Benachrichtigungs Code an den Besitzer des Listen Felds.                                                                                                                                                                                                                                        |
| [**WM \_ lbuttondblclk**](/windows/desktop/inputdev/wm-lbuttondblclk) | Verfolgt die Maus im Listenfeld Client Bereich. Dadurch kann der Benutzer eine Auswahl abbrechen, wenn die Maustaste außerhalb des Listenfeld-Client Bereichs losgelassen wird.                                                                                                                                                                                                              |
| [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown)     | Verfolgt die Maus im Listenfeld Client Bereich. Dadurch kann der Benutzer eine Auswahl abbrechen, wenn die Maustaste außerhalb des Listenfeld-Client Bereichs losgelassen wird.                                                                                                                                                                                                              |
| [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup)         | Verfolgt die Maus im Listenfeld Client Bereich. Dadurch kann der Benutzer eine Auswahl abbrechen, wenn die Maustaste außerhalb des Listenfeld-Client Bereichs losgelassen wird.                                                                                                                                                                                                              |
| [**WM- \_ mouseelmove**](/windows/desktop/inputdev/wm-mousemove)         | Verfolgt die Maus im Listenfeld Client Bereich. Dadurch kann der Benutzer eine Auswahl abbrechen, wenn die Maustaste außerhalb des Listenfeld-Client Bereichs losgelassen wird.                                                                                                                                                                                                              |
| [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint)                      | Führt einen untergeordneten Paint-Vorgang mithilfe des Listenfeld Handles für den Gerätekontext (DC) aus.                                                                                                                                                                                                                                                                           |
| [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)           | Schaltet die Einfügemarke um und sendet einen [LBN- \_ SetFocus](lbn-setfocus.md) -Benachrichtigungs Code an den Besitzer des Listen Felds.                                                                                                                                                                                                                                                        |
| [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont)               | Legt eine neue Schriftart für das Listenfeld fest.                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ -Ziel**](/windows/desktop/gdi/wm-setredraw)              | Legt das Flag zum Neuzeichnen basierend auf dem Wert von *wParam* fest oder löscht dieses.                                                                                                                                                                                                                                                                                                           |
| [**WM- \_ Größe**](/windows/desktop/winmsg/wm-size)                     | Passt die Größe des Listen Felds auf eine ganzzahlige Anzahl von Elementen an.                                                                                                                                                                                                                                                                                                                     |
| [**WM- \_ VScroll**](wm-vscroll.md)                  | Führt einen vertikalen Bildlauf im Listenfeld aus.                                                                                                                                                                                                                                                                                                                                         |



 

Die vordefinierte Listenfeld Prozedur übergibt alle anderen Nachrichten zur Standard Verarbeitung an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

## <a name="owner-drawn-list-boxes"></a>Listenfelder Owner-Drawn

Eine Anwendung kann ein vom *Besitzer gezeichnetes* Listenfeld erstellen, um Aufgaben für das Zeichnen von Listenelementen zu übernehmen. Das übergeordnete Fenster oder Dialogfeld eines von einem Besitzer gezeichneten Listen Felds (dessen *Besitzer*) empfängt [**WM \_ DrawItem**](wm-drawitem.md) -Nachrichten, wenn ein Teil des Listen Felds gezeichnet werden muss. Ein vom Besitzer gezeichnetes Listenfeld kann weitere Informationen als oder zusätzlich zu Text Zeichenfolgen auflisten.

Der Besitzer eines von einem Besitzer gezeichneten Listen Felds muss die [**WM- \_ DrawItem**](wm-drawitem.md) -Nachricht verarbeiten. Diese Meldung wird immer dann gesendet, wenn ein Teil des Listen Felds neu gezeichnet werden muss. Abhängig von den für das Listenfeld angegebenen Stilen muss der Besitzer möglicherweise andere Nachrichten verarbeiten.

Eine Anwendung kann ein vom Besitzer gezeichnetes Listenfeld erstellen, indem Sie den-Typ der lbs-Besitzer [**\_ drawfixed**](list-box-styles.md) oder [**\_ lbs**](list-box-styles.md) -Besitzer angibt. Wenn alle Listenelemente im Listenfeld die gleiche Höhe haben (z. b. Zeichen folgen oder Symbole), kann eine Anwendung das **lbs \_** -Besitzer Zeichen verwenden. Wenn Listenelemente eine unterschiedliche Höhe haben (z. b. Bitmaps mit unterschiedlicher Größe), kann eine Anwendung den **lbs \_** -Besitzer der-Klasse verwenden.

Der Besitzer eines von einem Besitzer gezeichneten Listen Felds kann eine [**WM \_ MeasureItem**](wm-measureitem.md) -Nachricht verarbeiten, um die Dimensionen von Listenelementen anzugeben. Wenn die Anwendung das Listenfeld mithilfe des lbs- [**\_ Besitzers**](list-box-styles.md) erstellt, sendet das System die **WM- \_ MeasureItem** -Nachricht nur einmal. Die Dimensionen, die vom Besitzer angegeben werden, werden für alle Listenelemente verwendet. Wenn das [**lbs \_**](list-box-styles.md) -Besitzer Zeichen verwendet wird, sendet das System eine **WM \_ MeasureItem** -Meldung für jedes Listenelement, das dem Listenfeld hinzugefügt wird. Der Besitzer kann die Höhe eines Listen Elements jederzeit mithilfe der [**lb- \_ GetItemHeight**](lb-getitemheight.md) -und [**lb \_ setitemheight**](lb-setitemheight.md) -Nachrichten bestimmen oder festlegen.

Wenn die Informationen, die in einem vom Besitzer gezeichneten Listenfeld angezeigt werden, Text enthalten, kann eine Anwendung den Text für die einzelnen Listenelemente nachverfolgen, indem Sie den [**lbs \_ hasstrings**](list-box-styles.md) -Stil angibt. Listenfelder mit dem [**lbs- \_ Sortier**](list-box-styles.md) Stil werden basierend auf diesem Text sortiert. Wenn ein Listenfeld sortiert ist, aber nicht der **lbs \_ hasstrings** -Stil ist, muss der Besitzer die [**WM \_ compareitem**](wm-compareitem.md) -Nachricht verarbeiten.

In einem vom Besitzer gezeichneten Listenfeld muss der Besitzer Listenelemente nachverfolgen, die andere Informationen als oder zusätzlich zu Text enthalten. Eine bequeme Möglichkeit hierfür ist das Speichern des Handles in den Informationen als Elementdaten mithilfe der [**lb \_**](lb-setitemdata.md) -Nachricht. Zum Freigeben von Datenobjekten, die Elementen in einem Listenfeld zugeordnet sind, kann der Besitzer die " [**WM \_ DeleteItem**](wm-deleteitem.md) "-Meldung verarbeiten.

Ein Beispiel für ein vom Besitzer gezeichnetes Listenfeld finden [Sie unter How to Create a Owner-Drawn List Box](create-an-owner-drawn-list-box.md).

## <a name="drag-list-boxes"></a>Listenfelder ziehen

Ein Drag List Box-Element ist eine besondere Art von Listenfeld, mit dem der Benutzer Elemente von einer Position auf eine andere verschieben kann. Eine Anwendung kann ein Drag-Listenfeld verwenden, um Zeichen folgen in einer bestimmten Sequenz anzuzeigen und dem Benutzer zu ermöglichen, die Reihenfolge zu ändern, indem die Elemente an die Position gezogen werden.

### <a name="creating-drag-list-boxes"></a>Erstellen von Drag-Listenfeldern

Ziehen Sie Listenfelder dieselben Fenster Stile, und verarbeiten Sie dieselben Meldungen wie Standard Listenfelder. Um ein Listenfeld mit Drag & amp; Drop zu erstellen, erstellen Sie zunächst ein Standard Listenfeld, und rufen Sie dann die Funktion [**makedraglist**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) Wenn Sie ein Listenfeld in einem Dialogfeld in ein Drag-Listenfeld konvertieren möchten, können Sie **makedraglist** bei der Verarbeitung der WM- \_ InitDialog-Nachricht aufzurufen.

### <a name="drag-list-box-messages"></a>Listenfeld Meldungen ziehen

Ein Drag List Box-Element benachrichtigt das übergeordnete Fenster von Drag-Ereignissen, indem es eine Drag List-Meldung sendet. Das übergeordnete Fenster muss die Drag List-Meldung verarbeiten.

Das Listenfeld durchziehen registriert diese Meldung, wenn die [**makedraglist**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) -Funktion aufgerufen wird. Um die Nachrichten-ID (numerischer Wert) der Drag List-Nachricht abzurufen, rufen Sie die [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion auf, und geben Sie den draglistmsgstring-Wert an.

Der *wParam* -Parameter der Drag List-Meldung ist der Steuerelement Bezeichner für das Zieh Listenfeld. Der *LPARAM* -Parameter ist die Adresse einer [**draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) -Struktur, die den Benachrichtigungs Code für das Zieh Ereignis und weitere Informationen enthält. Der Rückgabewert der Nachricht hängt von der Benachrichtigung ab.

### <a name="drag-list-box-notification-codes"></a>Benachrichtigungs Codes für das Listenfeld ziehen

Der Benachrichtigungs Code der Drag-Liste, der durch den **unotifizierungsmember** der [**draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) -Struktur identifiziert wird, der in der Drag List-Nachricht enthalten ist, kann [DL \_ BeginDrag](dl-begindrag.md), [DL \_ Drag](dl-dragging.md), [DL \_ CancelDrag](dl-canceldrag.md)oder [DL \_ Drop](dl-dropped.md)sein.

Der [DL \_ BeginDrag](dl-begindrag.md) -Benachrichtigungs Code wird gesendet, wenn sich der Cursor in einem Listenelement befindet und der Benutzer mit der linken Maustaste klickt. Das übergeordnete Fenster kann **true** zurückgeben, um den Zieh Vorgang zu starten, oder **false** , um das ziehen zu unterbinden Auf diese Weise kann das übergeordnete Fenster das ziehen für einige Listenelemente aktivieren und für andere Benutzer deaktivieren. Mithilfe der [**lbitemfrompt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) -Funktion können Sie ermitteln, welches Listenelement sich am angegebenen Speicherort befindet.

Wenn das ziehen wirksam ist, wird der Benachrichtigungs Code für die [DL- \_ Zieh](dl-dragging.md) Vorgänge gesendet, wenn der Mauszeiger bewegt wird, oder in regelmäßigen Abständen, wenn die Maus nicht bewegt wird. Das übergeordnete Fenster sollte zuerst das Listenelement unter dem Cursor mithilfe von [**lbitemfrompt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) ermitteln und dann das Einfügesymbol mithilfe der [**drawinsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) -Funktion zeichnen. Wenn Sie " **true** " für den " *bauroscroll* "-Parameter von " **lbitemfrompt**" angeben, können Sie bewirken, dass im Listenfeld ein Bildlauf um eine Zeile erfolgt, wenn der Cursor oberhalb oder unterhalb des Client Bereichs liegt Der Wert, den Sie für diese Benachrichtigung zurückgeben, gibt den Typ des Mauszeigers an, den das Drag-Listenfeld festlegen soll.

Der [DL- \_ CancelDrag](dl-canceldrag.md) -Benachrichtigungs Code wird gesendet, wenn der Benutzer einen Zieh Vorgang abbricht, indem er auf die Rechte Maustaste klickt oder die ESC-Taste drückt. Der gesendete [DL \_ ](dl-dropped.md) -Benachrichtigungs Code wird gesendet, wenn der Benutzer einen Zieh Vorgang durch Loslassen der linken Maustaste abschließt, auch wenn sich der Cursor nicht über einem Listenelement befindet. Das Zieh Listenfeld gibt die Maus Aufzeichnung vor dem Senden einer Benachrichtigung frei. Der Rückgabewert dieser beiden Benachrichtigungen wird ignoriert. Liste ziehen

 

