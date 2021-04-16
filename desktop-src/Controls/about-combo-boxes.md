---
title: Informationen zu Kombinations Feldern
description: In diesem Abschnitt werden die unterschiedlichen Arten von Kombinations Feldern erläutert.
ms.assetid: 76410a87-aa0e-4da9-9e78-c80ac485e3cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344596a3c0aa772568956344aaddcc053b534993
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104558367"
---
# <a name="about-combo-boxes"></a>Informationen zu Kombinations Feldern

Ein Kombinations Feld kombiniert ein Bearbeitungsfeld oder einen statischen Text und eine Liste.

Dieses Thema enthält folgende Abschnitte:

-   [Kombinations Feld Typen und Stile](#combo-box-types-and-styles)
-   [Kombinations Feld Liste](#combo-box-list)
    -   [Aktuelle Auswahl](#current-selection)
    -   [Dropdown Listen](#drop-down-lists)
    -   [Inhalt auflisten](#list-contents)
-   [Steuerelement Auswahlfelder bearbeiten](#edit-control-selection-fields)
-   [Vom Besitzer gezeichnete Kombinations Felder](#owner-drawn-combo-boxes)
-   [Untergeordnete Kombinations Felder](#subclassed-combo-boxes)

## <a name="combo-box-types-and-styles"></a>Kombinations Feld Typen und Stile

Ein Kombinations Feld besteht aus einer Liste und einem Auswahlfeld. Die Liste enthält die Optionen, die ein Benutzer auswählen kann, und im Feldauswahl wird die aktuelle Auswahl angezeigt. Wenn das Auswahlfeld ein Bearbeitungs Steuerelement ist, kann der Benutzerinformationen eingeben, die in der Liste nicht verfügbar sind. Andernfalls kann der Benutzer nur Elemente in der Liste auswählen.

Die Bibliothek für allgemeine Steuerelemente umfasst drei Haupt Formate von Kombinations Feldern, wie in der folgenden Tabelle dargestellt.



| Typ des Kombinations Felds             | Stil Konstante                                                 | BESCHREIBUNG                                                                                  |
|----------------------------|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Einfach                     | [**CBS \_ Simple**](combo-box-styles.md)             | Zeigt die Liste jederzeit an und zeigt das ausgewählte Element in einem Bearbeitungs Steuerelement an.              |
| Drop-down                  | [**CBS- \_ Dropdown**](combo-box-styles.md)         | Zeigt die Liste an, wenn auf das Symbol geklickt wird, und zeigt das ausgewählte Element in einem Bearbeitungs Steuerelement an.  |
| Dropdown Liste (Dropdown Liste) | [**CBS- \_ Dropdown Liste**](combo-box-styles.md) | Zeigt die Liste an, wenn auf das Symbol geklickt wird, und zeigt das ausgewählte Element in einem statischen Steuerelement an. |



 

Die folgenden Screenshots zeigen die drei Arten von Kombinations Feldern, die in Windows Vista angezeigt werden können. Im ersten Screenshot hat der Benutzer ein Element im einfachen Kombinations Feld ausgewählt. Der Benutzer kann auch einen neuen Wert in das Bearbeitungsfeld dieses Steuer Elements eingeben. Die Größe der Liste wurde im Microsoft Visual Studio Ressourcen-Editor angepasst und ist nur groß genug, um zwei Elemente aufzunehmen.

![Screenshot, der ein in einem einfachen Kombinations Feld ausgewähltes Element anzeigt](images/simplecombo.png)

Im zweiten Screenshot hat der Benutzer im Dropdown-Kombinations Feld neuen Text in das Bearbeitungs Steuerelement eingegeben. Der Benutzer könnte auch ein vorhandenes Element auswählen. Das Listenfeld wird erweitert, um so viele Elemente wie möglich aufzunehmen.

![Screenshot mit Text, der in ein Dropdown-Kombinations Feld eingegeben wird](images/dropdown.png)

Im dritten Screenshot hat der Benutzer das Kombinations Feld für die Dropdown Liste geöffnet. Das Listenfeld wird erweitert, um so viele Elemente wie möglich aufzunehmen. Der Benutzer kann keinen neuen Text eingeben.

![Screenshot mit einem Element, das in einem Kombinations Feld der Dropdown Liste ausgewählt ist](images/droplist.png)

Es gibt auch eine Reihe von Kombinations Feld Stilen, die bestimmte Eigenschaften definieren. Kombinations Feld Stile definieren bestimmte Eigenschaften eines Kombinations Felds. Sie können Stile kombinieren. einige Stile gelten jedoch nur für bestimmte Kombinations Feld Typen. Eine Tabelle mit Kombinations Feld Formaten finden Sie unter Kombinations [Feld-Stile](combo-box-styles.md).

> [!Note]  
> Um visuelle Stile mit Kombinations Feldern zu verwenden, muss eine Anwendung ein Manifest enthalten, und es muss am Anfang des Programms [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) aufgerufen werden. Weitere Informationen zu visuellen Stilen finden Sie unter [visuelle Stile](themes-overview.md). Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="combo-box-list"></a>Kombinations Feld Liste

Die Liste ist der Teil eines Kombinations Felds, in dem die Elemente angezeigt werden, die ein Benutzer auswählen kann. In der Regel Initialisiert eine Anwendung den Inhalt der Liste, wenn ein Kombinations Feld erstellt wird. Jedes vom Benutzer ausgewählte Listenelement ist die *aktuelle Auswahl*. Es können nicht mehrere Elemente ausgewählt werden. In einfachen und Dropdown-Kombinations Feldern kann der Benutzer das Auswahlfeld eingeben, anstatt ein Listenelement auszuwählen. In diesen Fällen gibt es keine aktuelle Auswahl, und die Anwendung ist dafür verantwortlich, das Element der Liste hinzuzufügen und Sie zur aktuellen Auswahl zu machen, wenn dies angebracht ist.

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Aktuelle Auswahl](#current-selection)
-   [Dropdown Listen](#drop-down-lists)
-   [Inhalt auflisten](#list-contents)

### <a name="current-selection"></a>Aktuelle Auswahl

Die aktuelle Auswahl ist ein Listenelement, das der Benutzer ausgewählt hat. der ausgewählte Text wird im Auswahlfeld des Kombinations Felds angezeigt. Bei einem einfachen Kombinations Feld oder einem Dropdown-Kombinations Feld ist die aktuelle Auswahl jedoch nur eine Form der möglichen Benutzereingabe in einem Kombinations Feld. Der Benutzer kann auch Text in das Auswahlfeld eingeben.

Die aktuelle Auswahl wird durch den NULL basierten Index des ausgewählten Listen Elements identifiziert. Eine Anwendung kann Sie jederzeit festlegen und abrufen. Das übergeordnete Fenster oder die Dialogfeld Prozedur empfängt eine Benachrichtigung, wenn der Benutzer die aktuelle Auswahl für ein Kombinations Feld ändert. Das übergeordnete Fenster oder Dialogfeld wird nicht benachrichtigt, wenn die Anwendung die Auswahl ändert.

Wenn ein Kombinations Feld erstellt wird, gibt es keine aktuelle Auswahl. Dies gilt auch für ein einfaches oder Dropdown-Kombinations Feld, wenn der Benutzer den Inhalt des Auswahl Felds bearbeitet hat. Um die aktuelle Auswahl festzulegen, sendet eine Anwendung die [**CB- \_ setcurrsel**](cb-setcursel.md) -Nachricht an das Kombinations Feld. Eine Anwendung kann auch die [**CB- \_ SelectString**](cb-selectstring.md) -Nachricht verwenden, um die aktuelle Auswahl auf ein Listenelement festzulegen, dessen Zeichenfolge mit einer angegebenen Zeichenfolge beginnt. Um die aktuelle Auswahl zu bestimmen, sendet eine Anwendung die [**CB \_ getcurrsel**](cb-getcursel.md) -Nachricht an das Kombinations Feld. Wenn keine aktuelle Auswahl vorhanden ist, gibt diese Meldung CB \_ Err zurück.

Wenn der Benutzer die aktuelle Auswahl in einem Kombinations Feld ändert, empfängt das übergeordnete Fenster oder die Dialogfeld Prozedur eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung mit dem [CBN \_ selChange](cbn-selchange.md) -Benachrichtigungs Code im höherwertigen Wort des *wParam* -Parameters. Dieser Benachrichtigungs Code wird nicht gesendet, wenn die aktuelle Auswahl mithilfe der [**CB- \_ setcurrsel**](cb-setcursel.md) -Nachricht festgelegt wird.

Ein Dropdown-Kombinations Feld oder ein Dropdown-Listenfeld sendet den [CBN- \_ closeup](cbn-closeup.md) -Benachrichtigungs Code an das übergeordnete Fenster oder die Dialogfeld Prozedur, wenn die Dropdown Liste geschlossen wird. Wenn der Benutzer die aktuelle Auswahl geändert hat, sendet das Kombinations Feld auch den [CBN \_ selChange](cbn-selchange.md) -Benachrichtigungs Code, wenn die Dropdown Liste geschlossen wird. Um einen bestimmten Prozess jedes Mal auszuführen, wenn der Benutzer ein Listenelement auswählt, können Sie entweder den \_ Benachrichtigungs Code CBN selChange oder CBN \_ closeup verarbeiten. In der Regel warten Sie \_ vor dem Verarbeiten einer Änderung in der aktuellen Auswahl den Benachrichtigungs Code für die CBN-Schließung. Dies kann besonders wichtig sein, wenn eine beträchtliche Menge an Verarbeitung erforderlich ist.

Eine Anwendung kann auch die Benachrichtigungs Codes " [CBN \_ selendok](cbn-selendok.md) " und " [CBN \_ selendcancel](cbn-selendcancel.md) " verarbeiten. Das System sendet CBN \_ selendok, wenn der Benutzer ein Listenelement auswählt, oder wählt ein Element aus und schließt dann die Liste. Dies gibt an, dass der Benutzer beendet wurde und dass die Auswahl verarbeitet werden sollte. CBN \_ selendcancel wird gesendet, wenn der Benutzer ein Element auswählt, dann aber ein anderes Steuerelement auswählt, ESC drückt, während die Dropdown Liste geöffnet ist, oder das Dialogfeld schließt. Dies gibt an, dass die Auswahl des Benutzers ignoriert werden soll. CBN- \_ selendok wird vor jeder [CBN- \_ selChange](cbn-selchange.md) -Nachricht gesendet.

In einem einfachen Kombinations Feld sendet das System den [CBN- \_ dblclk](cbn-dblclk.md) -Benachrichtigungs Code, wenn der Benutzer auf ein Listenelement doppelklickt. Wenn Sie in einem Dropdown-Kombinations Feld oder in einer Dropdown Liste die Liste ausblenden, ist es nicht möglich, auf ein Element zu doppelklicken.

### <a name="drop-down-lists"></a>Dropdown Listen

Bestimmte Benachrichtigungen und Nachrichten gelten nur für Kombinations Felder mit Dropdown Listen. Wenn eine Dropdown Liste geöffnet oder geschlossen ist, empfängt das übergeordnete Fenster eines Kombinations Felds eine Benachrichtigung in Form einer [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung. Wenn die Liste geöffnet wird, ist das hochwertige Wort von *wParam* die [CBN- \_ Dropdown](cbn-dropdown.md)Liste. Wenn die Liste geschlossen wird, ist Sie [CBN- \_ closeup](cbn-closeup.md).

Eine Anwendung kann die Liste mit einem Dropdown-Kombinations Feld oder einem Dropdown-Listenfeld öffnen, indem Sie die [**CB- \_ ShowDropDown**](cb-showdropdown.md) -Meldung verwendet. Mithilfe der [**CB \_ getdroppedstate**](cb-getdroppedstate.md) -Nachricht kann ermittelt werden, ob die Liste geöffnet ist, und die Koordinaten einer Dropdown Liste können mithilfe der [**CB \_ getdroppedcontrolrect**](cb-getdroppedcontrolrect.md) -Nachricht bestimmt werden. Eine Anwendung kann die Breite einer Dropdown Liste auch erhöhen, indem Sie die [**CB- \_ setdroppeer-DTH**](cb-setdroppedwidth.md) -Nachricht verwendet.

### <a name="list-contents"></a>Inhalt auflisten

Wenn eine Anwendung ein Kombinations Feld erstellt, wird das Kombinations Feld in der Regel initialisiert, indem ein oder mehrere Elemente zur Liste hinzugefügt werden. Später kann eine Anwendung Listenelemente hinzufügen oder löschen, die Liste erneut initialisieren oder Element Informationen daraus abrufen.

Eine Anwendung fügt einem Kombinations Feld Listenelemente hinzu, indem die [**CB \_ AddString**](cb-addstring.md) -Nachricht an Sie gesendet wird. Das angegebene Element wird am Ende der Liste oder in einem sortierten Kombinations Feld in der richtigen sortierten Position basierend auf der Element Zeichenfolge hinzugefügt. In einem unsortierten Kombinations Feld kann eine Anwendung die [**CB \_ InsertString**](cb-insertstring.md) -Nachricht verwenden, um ein Element an einer bestimmten Position einzufügen. Nach dem hinzufügen wird ein Listenelement durch seine Position identifiziert.

Mithilfe der [**CB- \_ FindString**](cb-findstring.md) -oder [**CB \_ FindStringExact**](cb-findstringexact.md) -Nachricht kann eine Anwendung die Position eines Listen Elements bestimmen. **CB \_ FindString** findet ein Element, dessen Zeichenfolge mit der angegebenen Zeichenfolge beginnt. **CB \_ FindStringExact** findet ein Element, dessen Zeichenfolge exakt mit der Zeichenfolge übereinstimmt. Bei beiden Meldungen wird die Groß-/Kleinschreibung

Eine Anwendung kann ein Listenelement mithilfe der [**CB \_ deletestring**](cb-deletestring.md) -Nachricht entfernen. Wenn eine Anwendung die Kombinations Feld Liste erneut initialisieren muss, kann Sie zuerst den gesamten Inhalt mithilfe der [**CB \_ resetcontent**](cb-resetcontent.md) -Nachricht löschen. Wenn der Liste mehrere Elemente hinzugefügt werden, nachdem bereits ein Kombinations Feld angezeigt wurde, kann eine Anwendung das Flag neu zeichnen löschen, um zu verhindern, dass das Kombinations Feld neu gezeichnet wird, nachdem jedes Element hinzugefügt wurde. Weitere Informationen zum erneuten Zeichnen finden Sie in der Beschreibung der [**WM- \_**](/windows/desktop/gdi/wm-setredraw) Nachricht.

Zum Abrufen der Zeichenfolge, die einem Listenelement zugeordnet ist, kann eine Anwendung die [**CB \_ getlbtext**](cb-getlbtext.md) -Nachricht verwenden. Die Zeichenfolge des Elements wird in den Puffer kopiert, der von der Anwendung angegeben wird. Um sicherzustellen, dass der Puffer groß genug ist, um die Zeichenfolge zu empfangen, kann die Anwendung zuerst die [**CB \_ getlbtextlen**](cb-getlbtextlen.md) -Nachricht verwenden, um die Länge der Zeichenfolge zu bestimmen. Um die Anzahl der Listenelemente in einem Kombinations Feld zu erhalten, kann eine Anwendung die [**CB \_ GetCount**](cb-getcount.md) -Nachricht verwenden.

## <a name="edit-control-selection-fields"></a>Steuerelement Auswahlfelder bearbeiten

Eine Anwendung kann den Inhalt des Auswahl Felds abrufen oder festlegen und die Bearbeitungs Auswahl bestimmen oder festlegen. Die Anwendung kann auch die Menge an Text begrenzen, die ein Benutzer in das Auswahlfeld eingeben kann. Wenn sich der Inhalt des Auswahl Felds ändert, sendet das System Benachrichtigungs Meldungen an das übergeordnete Fenster oder die Dialogfeld Prozedur.

Um den Inhalt des Auswahl Felds abzurufen, kann eine Anwendung die WM- [**\_ gettext**](/windows/desktop/winmsg/wm-gettext) -Nachricht an das Kombinations Feld senden. Um den Inhalt des Auswahl Felds eines einfachen oder Dropdown-Kombinations Felds festzulegen, kann eine Anwendung die WM- [**\_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht an das Kombinations Feld senden.

Die Auswahl bearbeiten ist der Bereich des ausgewählten Texts (sofern vorhanden) im Auswahlfeld eines einfachen oder Dropdown-Kombinations Felds. Eine Anwendung kann die Position des Anfangs-und Endzeichens der aktuellen Auswahl mithilfe der [**CB \_ geteditsel**](cb-geteditsel.md) -Nachricht ermitteln. Mithilfe der CB-Nachricht " [**\_ logsditsel**](cb-seteditsel.md) " können auch Zeichen in der Bearbeitungs Auswahl ausgewählt werden.

Anfänglich wird der Text, den der Benutzer in das Auswahlfeld eingeben kann, durch die Größe des Auswahl Felds beschränkt. Wenn das Kombinations Feld jedoch den [**\_ autohscroll**](combo-box-styles.md) -Stil "CBS" aufweist, kann der Text weiterhin über die Größe des Auswahl Felds hinausgehen. Eine Anwendung kann die [**CB- \_ Begrenzungs Text**](cb-limittext.md) Nachricht verwenden, um die Menge an Text einzuschränken, die ein Benutzer in das Auswahlfeld eingeben kann, unabhängig davon, ob das Steuerelement den " **CBS \_ autohscroll** "-Stil hat.

Wenn der Benutzer den Inhalt des Auswahl Felds bearbeitet, empfängt das übergeordnete Fenster oder die Dialogfeld Prozedur Benachrichtigungs Meldungen. Der [CBN- \_ editupdate](cbn-editupdate.md) -Benachrichtigungs Code wird zuerst gesendet und zeigt an, dass der Text im Auswahlfeld bearbeitet wurde. Nachdem der geänderte Text angezeigt wird, sendet das System [CBN \_ EditChange](cbn-editchange.md). Wenn das Auswahlfeld Inhalt geändert wird, wenn ein Listenelement ausgewählt wird, werden diese Nachrichten nicht gesendet.

## <a name="owner-drawn-combo-boxes"></a>Kombinations Felder Owner-Drawn

Eine Anwendung kann ein vom Besitzer gezeichnetes Kombinations Feld erstellen, um Aufgaben für das Zeichnen von Listenelementen zu übernehmen. Das übergeordnete Fenster eines von einem Besitzer gezeichneten Kombinations Felds (dessen Besitzer) empfängt [**WM \_ DrawItem**](wm-drawitem.md) -Nachrichten, wenn ein Teil des Kombinations Felds gezeichnet werden muss. Ein vom Besitzer gezeichnetes Kombinations Feld kann weitere Informationen als oder zusätzlich zu Text Zeichenfolgen auflisten. Vom Besitzer gezeichnete Kombinations Felder können von einem beliebigen Typ sein. Allerdings kann das Bearbeitungs Steuerelement in einem einfachen oder Dropdown-Kombinations Feld nur Text anzeigen, während der Besitzer das Auswahlfeld in einem Dropdown-Listenfeld zeichnet.

Der Besitzer eines von einem Besitzer gezeichneten Kombinations Felds muss die [**WM- \_ DrawItem**](wm-drawitem.md) -Nachricht verarbeiten. Diese Meldung wird immer dann gesendet, wenn ein Teil des Kombinations Felds neu gezeichnet werden muss. Der Besitzer muss möglicherweise andere Nachrichten verarbeiten, abhängig von den für das Kombinations Feld angegebenen Stilen.

Eine Anwendung kann ein vom Besitzer gezeichnetes Kombinations Feld erstellen, indem das CBS-Besitzer-oder [**CBS \_**](combo-box-styles.md) -Besitzer-Format angegeben wird. [**\_**](combo-box-styles.md) Wenn alle Listenelemente im Kombinations Feld die gleiche Höhe haben (z. b. Zeichen folgen oder Symbole), kann eine Anwendung den **CBS \_** -Besitzer "Besitzer" verwenden. Wenn Listenelemente unterschiedlich hoch sind, wie z. b. Bitmaps mit unterschiedlicher Größe, kann eine Anwendung den CBS-Besitzer der Art "Besitzer" verwenden. **\_**

Der Besitzer eines von einem Besitzer gezeichneten Kombinations Felds kann eine [**WM \_ MeasureItem**](wm-measureitem.md) -Nachricht verarbeiten, um die Dimensionen von Listenelementen im Kombinations Feld anzugeben. Wenn die Anwendung das Kombinations Feld mithilfe des CBS- [**\_ Besitzers**](combo-box-styles.md) "Besitzer" erstellt, sendet das System die " **WM \_ MeasureItem** "-Meldung nur einmal. Die vom Besitzer angegebenen Dimensionen werden für alle Listenelemente verwendet. Wenn der [**" \_ CBS**](combo-box-styles.md) -Besitzer"-Stil verwendet wird, sendet das System eine **WM \_ MeasureItem** -Meldung für jedes Listenelement, das dem Kombinations Feld hinzugefügt wird. Der Besitzer kann die Höhe eines Listen Elements jederzeit mithilfe der [**CB- \_ GetItemHeight**](cb-getitemheight.md) -und [**CB \_ setitemheight**](cb-setitemheight.md) -Nachrichten bestimmen oder festlegen.

Wenn die in einem von einem Besitzer gezeichneten Kombinations Feld angezeigten Informationen Text enthalten, kann eine Anwendung den Text für jedes Listenelement durch Angabe des [**CBS \_ hasstrings**](combo-box-styles.md) -Stils nachverfolgen. Kombinations Felder mit dem [**CBS- \_ Sortier**](combo-box-styles.md) Stil werden basierend auf diesem Text sortiert. Wenn ein Kombinations Feld und nicht der **CBS \_ hasstrings** -Stil sortiert ist, muss der Besitzer die [**WM \_ compareitem**](wm-compareitem.md) -Nachricht verarbeiten.

In einem vom Besitzer gezeichneten Kombinations Feld muss der Besitzer Listenelemente nachverfolgen, die andere Informationen als oder zusätzlich zu Text enthalten. Eine bequeme Möglichkeit hierfür ist, das Handle in den Informationen als Elementdaten zu speichern. Zum Freigeben von Datenobjekten, die Elementen in einem Kombinations Feld zugeordnet sind, kann der Besitzer die " [**WM \_ DeleteItem**](wm-deleteitem.md) "-Meldung verarbeiten.

## <a name="subclassed-combo-boxes"></a>Untergeordnete Kombinations Felder

Unterklassen sind Verfahren, mit denen eine Anwendung Nachrichten abfangen und verarbeiten kann, die an ein Fenster gesendet oder gesendet werden. Durch die Verwendung von Unterklassen kann eine Anwendung ihre eigene Verarbeitung für bestimmte Nachrichten ersetzen, während die meiste Nachrichtenverarbeitung an die Klassen definierte Fenster Prozedur überlassen wird.

Wenn das Betriebssystem ein Fenster erstellt, speichert es Informationen dazu in einer internen Datenstruktur, die einen Zeiger auf die Fenster Prozedur enthält. Zur Unterklasse eines Fensters Ruft eine Anwendung die [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) -Funktion auf, um den Zeiger auf diese Prozedur durch einen Zeiger auf eine Anwendungs definierte Unterklassen Prozedur zu ersetzen. Anschließend werden alle Nachrichten an das Fenster an die Unterklassen Prozedur gesendet. Diese Prozedur verwendet dann die [**callwindowproc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) -Funktion, um nicht verarbeitete Nachrichten an die ursprüngliche Fenster Prozedur zu übergeben. Eine Beschreibung der von der ComboBox-Klassen Fenster Prozedur ausgeführten Nachrichtenverarbeitung finden Sie unter [Standardverhalten](combo-box-features.md)für Kombinations Felder.

Wenn sich das Kombinations Feld außerhalb eines Dialog Felds befindet, kann eine Anwendung die Tab-, Enter-und ESC-Taste nicht verarbeiten, es sei denn, es wird eine Unterklassen Prozedur verwendet. Wenn ein einfaches oder Dropdown-Kombinations Feld den Eingabefokus erhält, wird der Fokus sofort auf das untergeordnete Bearbeitungs Steuerelement festgelegt. Daher muss eine Anwendung das Bearbeitungs Steuerelement unterteilen, um Tastatureingaben für ein einfaches oder Dropdown-Kombinations Feld abzufangen. Ein Beispiel hierfür finden Sie [unter Unterklassen für ein Kombinations Feld](using-combo-boxes.md).

Wenn eine Unterklassen Prozedur die WM-Zeichnungs Nachricht verarbeitet, muss Sie die [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) -Funktion verwenden, um das [**\_ Zeichnen**](/windows/desktop/gdi/wm-paint) vorzubereiten. Vor dem Aufrufen der [**endpaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) -Funktion übergibt Sie das Handle des Geräte Kontexts (DC) als *wParam* -Parameter für die Fenster Prozedur. Wenn **endpaint** zuerst aufgerufen wird, wird die Prozedur für das Klassen Fenster nicht gezeichnet, da **endpaint** das gesamte Fenster überprüft.

Eine Technik, die sich auf die Unterklassen bezieht, ist eine übergeordnete Klasse. Eine übergeordnete Klasse ähnelt jeder anderen Klasse, mit der Ausnahme, dass die Fenster Prozedur [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) nicht zum Verarbeiten nicht verarbeiteter Nachrichten aufruft. Stattdessen übergibt sie nicht verarbeitete Nachrichten an die Fenster Prozedur für die übergeordnete Fenster Klasse. Befolgen Sie die Richtlinien in [Windows-Prozeduren](/windows/desktop/winmsg/window-procedures) , um Probleme zu vermeiden, die bei Unterklassen und Superklassen auftreten können.

 

 