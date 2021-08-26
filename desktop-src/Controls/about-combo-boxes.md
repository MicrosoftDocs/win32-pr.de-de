---
title: Informationen zu Kombinationsfeldern
description: In diesem Abschnitt werden die verschiedenen Arten von Kombinationsfeldern erläutert.
ms.assetid: 76410a87-aa0e-4da9-9e78-c80ac485e3cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497bc6fc7e9254feb58ef95051ba1278e135ff241d3af93781f611373d2d096c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922514"
---
# <a name="about-combo-boxes"></a>Informationen zu Kombinationsfeldern

Ein Kombinationsfeld kombiniert ein Bearbeitungsfeld oder statischen Text und eine Liste.

Dieses Thema enthält folgende Abschnitte:

-   [Kombinationsfeldtypen und -stile](#combo-box-types-and-styles)
-   [Kombinationsfeldliste](#combo-box-list)
    -   [Aktuelle Auswahl](#current-selection)
    -   [Dropdownlisten](#drop-down-lists)
    -   [Inhalt auflisten](#list-contents)
-   [Bearbeiten von Steuerelementauswahlfeldern](#edit-control-selection-fields)
-   [Vom Besitzer gezeichnete Kombinationsfelder](#owner-drawn-combo-boxes)
-   [Kombinationsfelder mit Unterklassen](#subclassed-combo-boxes)

## <a name="combo-box-types-and-styles"></a>Kombinationsfeldtypen und -stile

Ein Kombinationsfeld besteht aus einer Liste und einem Auswahlfeld. Die Liste enthält die Optionen, die ein Benutzer auswählen kann, und das Auswahlfeld zeigt die aktuelle Auswahl an. Wenn das Auswahlfeld ein Bearbeitungssteuerfeld ist, kann der Benutzer Informationen eingeben, die nicht in der Liste verfügbar sind. Andernfalls kann der Benutzer nur Elemente in der Liste auswählen.

Die Bibliothek für allgemeine Steuerelemente enthält drei Hauptstile von Kombinationsfelden, wie in der folgenden Tabelle gezeigt.



| Kombinationsfeldtyp             | Stilkonst constant                                                 | BESCHREIBUNG                                                                                  |
|----------------------------|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Einfach                     | [**CBS \_ SIMPLE**](combo-box-styles.md)             | Zeigt die Liste jederzeit an und zeigt das ausgewählte Element in einem Bearbeitungssteuerelement an.              |
| Drop-down                  | [**\_CBS-DROPDOWNLISTE**](combo-box-styles.md)         | Zeigt die Liste an, wenn auf das Symbol geklickt wird, und zeigt das ausgewählte Element in einem Bearbeitungssteuerelement an.  |
| Dropdownliste (Dropdownliste) | [**\_CBS-DROPDOWNLISTE**](combo-box-styles.md) | Zeigt die Liste an, wenn auf das Symbol geklickt wird, und zeigt das ausgewählte Element in einem statischen Steuerelement an. |



 

Die folgenden Screenshots zeigen jeweils die drei Arten von Kombinationsfelden, wie sie möglicherweise in Windows Vista angezeigt werden. Im ersten Screenshot hat der Benutzer ein Element im einfachen Kombinationsfeld ausgewählt. Der Benutzer kann auch einen neuen Wert in das Bearbeitungsfeld dieses Steuerelements eingeben. Die Größe der Liste wurde im ressourcen Microsoft Visual Studio-Editor geändert und ist nur groß genug, um zwei Elemente aufnehmen zu können.

![Screenshot, der ein in einem einfachen Kombinationsfeld ausgewähltes Element zeigt](images/simplecombo.png)

Im zweiten Screenshot hat der Benutzer neuen Text in das Bearbeitungssteuerfeld des Dropdown-Kombinationsfelds eingefügt. Der Benutzer könnte auch ein vorhandenes Element ausgewählt haben. Das Listenfeld wird erweitert, um so viele Elemente wie möglich aufnehmen zu können.

![Screenshot mit Text, der in ein Dropdown-Kombinationsfeld eingefügt wurde](images/dropdown.png)

Im dritten Screenshot hat der Benutzer das Dropdownlisten-Kombinationsfeld geöffnet. Das Listenfeld wird erweitert, um so viele Elemente wie möglich aufnehmen zu können. Der Benutzer kann keinen neuen Text eingeben.

![Screenshot, der ein in einem Dropdownlisten-Kombinationsfeld ausgewähltes Element zeigt](images/droplist.png)

Es gibt auch eine Reihe von Kombinationsfeldstilen, die bestimmte Eigenschaften definieren. Kombinationsfeldstile definieren bestimmte Eigenschaften eines Kombinationsfelds. Sie können Stile kombinieren. Einige Stile gelten jedoch nur für bestimmte Kombinationsfeldtypen. Eine Tabelle mit Kombinationsfeldstilen finden Sie unter [Kombinationsfeldstile.](combo-box-styles.md)

> [!Note]  
> Um visuelle Stile mit Kombinationsfeldern zu verwenden, muss eine Anwendung ein Manifest enthalten und [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) am Anfang des Programms aufrufen. Informationen zu visuellen Stilen finden Sie unter [Visuelle Stile.](themes-overview.md) Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="combo-box-list"></a>Kombinationsfeldliste

Die Liste ist der Teil eines Kombinationsfelds, in dem die Elemente angezeigt werden, die ein Benutzer auswählen kann. In der Regel initialisiert eine Anwendung den Inhalt der Liste, wenn sie ein Kombinationsfeld erstellt. Jedes vom Benutzer ausgewählte Listenelement ist die *aktuelle Auswahl.* Mehrere Elemente können nicht ausgewählt werden. In einfachen Kombinationsfeldern und Dropdownfeldern kann der Benutzer in das Auswahlfeld eingeben, anstatt ein Listenelement auszuwählen. In diesen Fällen gibt es keine aktuelle Auswahl, und es liegt in der Verantwortung der Anwendung, das Element der Liste hinzuzufügen und es zur aktuellen Auswahl zu machen, falls dies sinnvoll ist.

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Aktuelle Auswahl](#current-selection)
-   [Dropdownlisten](#drop-down-lists)
-   [Inhalt auflisten](#list-contents)

### <a name="current-selection"></a>Aktuelle Auswahl

Die aktuelle Auswahl ist ein Listenelement, das der Benutzer ausgewählt hat. Der ausgewählte Text wird im Auswahlfeld des Kombinationsfelds angezeigt. Im Fall eines einfachen Kombinationsfelds oder Dropdown-Kombinationsfelds ist die aktuelle Auswahl jedoch nur eine Form möglicher Benutzereingaben in einem Kombinationsfeld. Der Benutzer kann auch Text in das Auswahlfeld eingeben.

Die aktuelle Auswahl wird durch den nullbasierten Index des ausgewählten Listenelements identifiziert. Eine Anwendung kann sie jederzeit festlegen und abrufen. Das übergeordnete Fenster oder die Dialogfeldprozedur erhält eine Benachrichtigung, wenn der Benutzer die aktuelle Auswahl für ein Kombinationsfeld ändert. Das übergeordnete Fenster oder Dialogfeld wird nicht benachrichtigt, wenn die Anwendung die Auswahl ändert.

Wenn ein Kombinationsfeld erstellt wird, gibt es keine aktuelle Auswahl. Dies gilt auch für ein einfaches Oder-Dropdown-Kombinationsfeld, wenn der Benutzer den Inhalt des Auswahlfelds bearbeitet hat. Zum Festlegen der aktuellen Auswahl sendet eine Anwendung die [**CB \_ SETCURSEL-Nachricht**](cb-setcursel.md) an das Kombinationsfeld. Eine Anwendung kann auch die [**CB \_ SELECTSTRING-Nachricht**](cb-selectstring.md) verwenden, um die aktuelle Auswahl auf ein Listenelement festzulegen, dessen Zeichenfolge mit einer angegebenen Zeichenfolge beginnt. Um die aktuelle Auswahl zu bestimmen, sendet eine Anwendung die [**CB \_ GETCURSEL-Nachricht**](cb-getcursel.md) an das Kombinationsfeld. Wenn keine aktuelle Auswahl vorkommt, gibt diese Meldung CB \_ ERR zurück.

Wenn der Benutzer die aktuelle Auswahl in einem Kombinationsfeld ändert, empfängt das übergeordnete Fenster oder die Dialogfeldprozedur eine [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) mit dem [CBN SELCHANGE-Benachrichtigungscode \_](cbn-selchange.md) im hohen Wort des *wParam-Parameters.* Dieser Benachrichtigungscode wird nicht gesendet, wenn die aktuelle Auswahl mithilfe der [**CB \_ SETCURSEL-Meldung festgelegt**](cb-setcursel.md) wird.

Ein Dropdown-Kombinationsfeld oder Dropdownlistenfeld sendet den [CBN CLOSEUP-Benachrichtigungscode \_ ](cbn-closeup.md) an das übergeordnete Fenster oder die Dialogfeldprozedur, wenn die Dropdownliste geschlossen wird. Wenn der Benutzer die aktuelle Auswahl geändert hat, sendet das Kombinationsfeld auch den [CBN SELCHANGE-Benachrichtigungscode, \_ ](cbn-selchange.md) wenn die Dropdownliste geschlossen wird. Um bei jeder Auswahl eines Listenelements durch den Benutzer einen bestimmten Prozess auszuführen, können Sie entweder den CBN \_ SELCHANGE- oder CBN \_ CLOSEUP-Benachrichtigungscode verarbeiten. In der Regel warten Sie auf den CBN \_ CLOSEUP-Benachrichtigungscode, bevor Sie eine Änderung der aktuellen Auswahl verarbeiten. Dies kann besonders wichtig sein, wenn ein beträchtlicher Verarbeitungsaufwand erforderlich ist.

Eine Anwendung kann auch die Benachrichtigungscodes [CBN \_ SELENDOK](cbn-selendok.md) und [CBN \_ SELENDCANCEL](cbn-selendcancel.md) verarbeiten. Das System sendet CBN SELENDOK, wenn der Benutzer ein Listenelement auswählt oder ein Element auswählt und \_ dann die Liste schließt. Dies gibt an, dass der Benutzer fertig ist und dass die Auswahl verarbeitet werden soll. CBN SELENDCANCEL wird gesendet, wenn der Benutzer ein Element auswählt, aber dann ein anderes Steuerelement auswählt, ESC drückt, während die Dropdownliste geöffnet ist, oder das Dialogfeld \_ schließt. Dies gibt an, dass die Auswahl des Benutzers ignoriert werden soll. CBN \_ SELENDOK wird vor jeder [CBN \_ SELCHANGE-Nachricht](cbn-selchange.md) gesendet.

In einem einfachen Kombinationsfeld sendet das System den [CBN DBLCLK-Benachrichtigungscode, \_ ](cbn-dblclk.md) wenn der Benutzer auf ein Listenelement doppelklickt. In einem Dropdown-Kombinationsfeld oder einer Dropdownliste blendet ein einzelner Klick die Liste aus, sodass es nicht möglich ist, auf ein Element zu doppelklicken.

### <a name="drop-down-lists"></a>Dropdownlisten

Bestimmte Benachrichtigungen und Nachrichten gelten nur für Kombinationsfelder, die Dropdownlisten enthalten. Wenn eine Dropdownliste geöffnet oder geschlossen ist, empfängt das übergeordnete Fenster eines Kombinationsfelds eine Benachrichtigung in Form einer [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command) Wenn die Liste geöffnet wird, ist das obere Wort *von wParam* [CBN \_ DROPDOWN.](cbn-dropdown.md) Wenn die Liste geschlossen wird, ist dies [CBN \_ CLOSEUP.](cbn-closeup.md)

Eine Anwendung kann die Liste eines Dropdown-Kombinationsfelds oder Dropdownlistenfelds mithilfe der [**CB \_ SHOWDROPDOWN-Meldung**](cb-showdropdown.md) öffnen. Sie kann mithilfe der CB [**\_ GETDROPPEDSTATE-Nachricht**](cb-getdroppedstate.md) bestimmen, ob die Liste geöffnet ist, und die Koordinaten einer Dropdownliste mithilfe der [**CB \_ GETDROPPEDCONTROLRECT-Nachricht**](cb-getdroppedcontrolrect.md) bestimmen. Eine Anwendung kann auch die Breite einer Dropdownliste mithilfe der [**CB \_ SETDROPPEDWIDTH-Nachricht**](cb-setdroppedwidth.md) erhöhen.

### <a name="list-contents"></a>Inhalt auflisten

Wenn eine Anwendung ein Kombinationsfeld erstellt, initialisiert sie das Kombinationsfeld in der Regel, indem ein oder mehrere Elemente zur Liste hinzugefügt werden. Später kann eine Anwendung Listenelemente hinzufügen oder löschen, die Liste erneut initialisieren oder Elementinformationen daraus abrufen.

Eine Anwendung fügt einem Kombinationsfeld Listenelemente hinzu, indem die [**CB \_ ADDSTRING-Nachricht**](cb-addstring.md) an dieses gesendet wird. Das angegebene Element wird am Ende der Liste oder in einem sortierten Kombinationsfeld an der richtigen sortierten Position basierend auf der Zeichenfolge des Elements hinzugefügt. In einem nicht abgebrochenen Kombinationsfeld kann eine Anwendung die [**CB \_ INSERTSTRING-Nachricht**](cb-insertstring.md) verwenden, um ein Element an einer bestimmten Position einzufügen. Nach dem Hinzufügen wird ein Listenelement durch seine Position identifiziert.

Mithilfe der [**CB \_ FINDSTRING-**](cb-findstring.md) oder [**CB \_ FINDSTRINGEXACT-Nachricht**](cb-findstringexact.md) kann eine Anwendung die Position eines Listenelements bestimmen. **CB \_ FINDSTRING** sucht nach einem Element, dessen Zeichenfolge mit der angegebenen Zeichenfolge beginnt. **CB \_ FINDSTRINGEXACT** sucht ein Element, dessen Zeichenfolge genau mit der Zeichenfolge übereinstimmt. Bei keiner der Nachrichten wird die Groß-/Kleinschreibung beachtet.

Eine Anwendung kann ein Listenelement mithilfe der [**CB \_ DELETESTRING-Nachricht**](cb-deletestring.md) entfernen. Wenn eine Anwendung die Kombinationsfeldliste erneut initialisieren muss, kann sie zunächst ihren gesamten Inhalt mithilfe der [**CB \_ RESETCONTENT-Nachricht**](cb-resetcontent.md) löschen. Wenn der Liste mehrere Elemente hinzugefügt werden, nachdem bereits ein Kombinationsfeld angezeigt wurde, kann eine Anwendung das neu gezeichnete Flag löschen, um zu verhindern, dass das Kombinationsfeld neu gezeichnet wird, nachdem jedes Element hinzugefügt wurde. Weitere Informationen zum Neuzeichnen finden Sie in der Beschreibung der [**WM \_ SETREDRAW-Meldung.**](/windows/desktop/gdi/wm-setredraw)

Um die einem Listenelement zugeordnete Zeichenfolge abzurufen, kann eine Anwendung die [**CB \_ GETLBTEXT-Nachricht**](cb-getlbtext.md) verwenden. Die Zeichenfolge des Elements wird in den von der Anwendung angegebenen Puffer kopiert. Um sicherzustellen, dass der Puffer groß genug ist, um die Zeichenfolge zu empfangen, kann die Anwendung zuerst die [**CB \_ GETLBTEXTLEN-Nachricht**](cb-getlbtextlen.md) verwenden, um die Länge der Zeichenfolge zu bestimmen. Um die Anzahl der Listenelemente in einem Kombinationsfeld abzurufen, kann eine Anwendung die [**CB \_ GETCOUNT-Nachricht**](cb-getcount.md) verwenden.

## <a name="edit-control-selection-fields"></a>Bearbeiten von Steuerelementauswahlfeldern

Eine Anwendung kann den Inhalt des Auswahlfelds abrufen oder festlegen und die Bearbeitungsauswahl bestimmen oder festlegen. Die Anwendung kann auch die Textmenge begrenzen, die ein Benutzer in das Auswahlfeld eingeben kann. Wenn sich der Inhalt des Auswahlfelds ändert, sendet das System Benachrichtigungsmeldungen an das übergeordnete Fenster oder die Übergeordnete Dialogfeldprozedur.

Um den Inhalt des Auswahlfelds abzurufen, kann eine Anwendung die [**WM \_ GETTEXT-Nachricht**](/windows/desktop/winmsg/wm-gettext) an das Kombinationsfeld senden. Um den Inhalt des Auswahlfelds eines einfachen oder Dropdown-Kombinationsfelds festzulegen, kann eine Anwendung die [**WM \_ SETTEXT-Nachricht**](/windows/desktop/winmsg/wm-settext) an das Kombinationsfeld senden.

Die Bearbeitungsauswahl ist ggf. der Bereich des ausgewählten Texts im Auswahlfeld eines einfachen Oder Dropdown-Kombinationsfelds. Eine Anwendung kann die Anfangs- und Endzeichenposition der aktuellen Auswahl mithilfe der [**CB \_ GETEDITSEL-Nachricht**](cb-geteditsel.md) bestimmen. Sie kann auch Zeichen in der Bearbeitungsauswahl auswählen, indem die [**CB \_ SETEDITSEL-Nachricht**](cb-seteditsel.md) verwendet wird.

Anfänglich wird die Textmenge, die der Benutzer in das Auswahlfeld eingeben kann, durch die Größe des Auswahlfelds beschränkt. Wenn das Kombinationsfeld jedoch den [**CBS \_ AUTOHSCROLL-Stil**](combo-box-styles.md) auf hat, kann der Text über die Größe des Auswahlfelds hinaus fortgesetzt werden. Eine Anwendung kann die [**CB \_ LIMITTEXT-Nachricht**](cb-limittext.md) verwenden, um die Textmenge einzuschränken, die ein Benutzer in das Auswahlfeld eingeben kann, unabhängig davon, ob das Steuerelement über den **CBS \_ AUTOHSCROLL-Stil** verfügt.

Wenn der Benutzer den Inhalt des Auswahlfelds bearbeitet, empfängt die übergeordnete Fenster- oder Dialogfeldprozedur Benachrichtigungsmeldungen. Zuerst wird der [CBN EDITUPDATE-Benachrichtigungscode \_ ](cbn-editupdate.md) gesendet, der angibt, dass der Text im Auswahlfeld bearbeitet wurde. Nachdem der geänderte Text angezeigt wurde, sendet das System [CBN \_ EDITCHANGE](cbn-editchange.md). Wenn sich der Inhalt des Auswahlfelds als Ergebnis der Auswahl eines Listenelements ändert, werden diese Nachrichten nicht gesendet.

## <a name="owner-drawn-combo-boxes"></a>Owner-Drawn Kombinationsfelder

Eine Anwendung kann ein vom Besitzer gezeichnetes Kombinationsfeld erstellen, um die Verantwortung für das Zeichnen von Listenelementen zu übernehmen. Das übergeordnete Fenster eines vom Besitzer gezeichneten Kombinationsfelds (dessen Besitzer) empfängt [**WM \_ DRAWITEM-Meldungen,**](wm-drawitem.md) wenn ein Teil des Kombinationsfelds gezeichnet werden muss. Ein vom Besitzer gezeichnetes Kombinationsfeld kann andere Informationen als oder zusätzlich zu Textzeichenfolgen auflisten. Vom Besitzer gezeichnete Kombinationsfelder können einen beliebigen Typ aufweisen. Das Bearbeitungssteuerelement in einem einfachen oder Dropdown-Kombinationsfeld kann jedoch nur Text anzeigen, während der Besitzer das Auswahlfeld in einem Dropdownlistenfeld zeichnet.

Der Besitzer eines vom Besitzer gezeichneten Kombinationsfelds muss die [**WM \_ DRAWITEM-Nachricht**](wm-drawitem.md) verarbeiten. Diese Meldung wird immer dann gesendet, wenn ein Teil des Kombinationsfelds neu gezeichnet werden muss. Abhängig von den für das Kombinationsfeld angegebenen Formatvorlagen muss der Besitzer möglicherweise andere Nachrichten verarbeiten.

Eine Anwendung kann ein vom Besitzer gezeichnetes Kombinationsfeld erstellen, indem sie den [**Stil CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) oder [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) angibt. Wenn alle Listenelemente im Kombinationsfeld die gleiche Höhe aufweisen, z. B. Zeichenfolgen oder Symbole, kann eine Anwendung den **CBS \_ OWNERDRAWFIXED-Stil** verwenden. Wenn Listenelemente unterschiedliche Höhe haben, z. B. Bitmaps unterschiedlicher Größe, kann eine Anwendung den **CBS \_ OWNERDRAWVARIABLE-Stil** verwenden.

Der Besitzer eines vom Besitzer gezeichneten Kombinationsfelds kann eine [**WM \_ MEASUREITEM-Nachricht**](wm-measureitem.md) verarbeiten, um die Dimensionen von Listenelementen im Kombinationsfeld anzugeben. Wenn die Anwendung das Kombinationsfeld mithilfe des [**CBS \_ OWNERDRAWFIXED-Stils**](combo-box-styles.md) erstellt, sendet das System die **WM \_ MEASUREITEM-Nachricht** nur einmal. Die vom Besitzer angegebenen Dimensionen werden für alle Listenelemente verwendet. Wenn der [**CBS \_ OWNERDRAWVARIABLE-Stil**](combo-box-styles.md) verwendet wird, sendet das System eine **WM \_ MEASUREITEM-Meldung** für jedes Listenelement, das dem Kombinationsfeld hinzugefügt wurde. Der Besitzer kann die Höhe eines Listenelements jederzeit mithilfe der [**NACHRICHTEN CB \_ GETITEMHEIGHT**](cb-getitemheight.md) bzw. [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md) bestimmen oder festlegen.

Wenn die in einem vom Besitzer gezeichneten Kombinationsfeld angezeigten Informationen Text enthalten, kann eine Anwendung den Text für jedes Listenelement nachverfolgen, indem sie das [**FORMAT CBS \_ HASSTRINGS**](combo-box-styles.md) angibt. Kombinationsfelder mit dem [**CBS \_ SORT-Format**](combo-box-styles.md) werden basierend auf diesem Text sortiert. Wenn ein Kombinationsfeld sortiert ist und nicht im **CBS \_ HASSTRINGS-Format,** muss der Besitzer die [**WM \_ COMPAREITEM-Nachricht**](wm-compareitem.md) verarbeiten.

In einem vom Besitzer gezeichneten Kombinationsfeld muss der Besitzer Listenelemente nachverfolgen, die andere Informationen als oder zusätzlich zu Text enthalten. Eine praktische Möglichkeit besteht darin, das Handle für die Informationen als Elementdaten zu speichern. Zum Freigeben von Datenobjekten, die Elementen in einem Kombinationsfeld zugeordnet sind, kann der Besitzer die [**WM \_ DELETEITEM-Nachricht**](wm-deleteitem.md) verarbeiten.

## <a name="subclassed-combo-boxes"></a>Unterklassen-Kombinationsfelder

Unterklassen sind Prozeduren, die es einer Anwendung ermöglichen, Nachrichten abzufangen und zu verarbeiten, die an ein Fenster gesendet oder gesendet werden. Durch die Verwendung von Unterklassen kann eine Anwendung ihre eigene Verarbeitung für bestimmte Nachrichten ersetzen, während die meisten Nachrichtenverarbeitungen der klassendefinierten Fensterprozedur überlassen werden.

Wenn das Betriebssystem ein Fenster erstellt, speichert es Informationen darüber in einer internen Datenstruktur, die einen Zeiger auf die Fensterprozedur enthält. Um eine Unterklasse für ein Fenster zu erstellen, ruft eine Anwendung die [**SetClassLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) auf, um den Zeiger auf diese Prozedur durch einen Zeiger auf eine anwendungsdefinierte Unterklassenprozedur zu ersetzen. Danach werden alle Nachrichten an das Fenster an die Unterklassenprozedur gesendet. Diese Prozedur verwendet dann die [**CallWindowProc-Funktion,**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) um nicht verarbeitete Nachrichten an die ursprüngliche Fensterprozedur zu übergeben. Eine Beschreibung der Nachrichtenverarbeitung, die von der Combobox-Klassenfensterprozedur ausgeführt wird, finden Sie unter [Default Combo Box Behavior](combo-box-features.md).

Wenn sich das Kombinationsfeld außerhalb eines Dialogfelds befindet, kann eine Anwendung die TAB-, EINGABE- und ESC-Schlüssel nur verarbeiten, wenn eine Unterklassenprozedur verwendet wird. Wenn ein einfaches Oder Dropdown-Kombinationsfeld den Eingabefokus empfängt, legt es den Fokus sofort auf das untergeordnete Bearbeitungssteuerelement fest. Daher muss eine Anwendung das Bearbeitungssteuerelement untergliedern, um Tastatureingaben für ein einfaches Oder Dropdown-Kombinationsfeld abzufangen. Ein Beispiel hierfür finden Sie unter [Unterklassen eines Kombinationsfelds.](using-combo-boxes.md)

Wenn eine Unterklassenprozedur die [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) verarbeitet, muss sie die [**BeginPaint-Funktion**](/windows/desktop/api/winuser/nf-winuser-beginpaint) verwenden, um das Zeichnen vorzubereiten. Vor dem Aufrufen der [**EndPaint-Funktion**](/windows/desktop/api/winuser/nf-winuser-endpaint) übergibt sie das Gerätekontexthandle (DC) als *wParam-Parameter* für die Fensterprozedur. Wenn **EndPaint** zuerst aufgerufen wird, führt die Klassenfensterprozedur kein Zeichnen durch, da **EndPaint** das gesamte Fenster überprüft.

Eine Technik im Zusammenhang mit Unterklassen ist die Oberklasse. Eine Übergeordnete Klasse ähnelt jeder anderen Klasse, außer dass ihre Fensterprozedur [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) nicht aufruft, um nicht verarbeitete Nachrichten zu verarbeiten. Stattdessen werden nicht verarbeitete Nachrichten an die Fensterprozedur für die übergeordnete Fensterklasse übergeben. Befolgen Sie die Richtlinien in [Fensterprozessuren,](/windows/desktop/winmsg/window-procedures) um Probleme zu vermeiden, die bei Unterklassen und Übergeordneten Klassen auftreten können.

 

 