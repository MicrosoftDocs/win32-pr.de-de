---
title: Informationen zu Register Steuerelementen
description: Ein Registerkarten-Steuerelement entspricht in etwa einem Trennblatt in einem Notizbuch den Beschriftungen in einer Hängeregistratur. Durch Verwenden eines Registerkarten-Steuerelements können in einer Anwendung mehrere Seiten für denselben Bereich in einem Fenster oder Dialogfeld definiert werden.
ms.assetid: 55ed2863-7f8d-43ce-a0f9-6f6d41e3f947
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c45ac7caa05c73e1dcf22a8e6f0eb4d031ca079
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102422"
---
# <a name="about-tab-controls"></a>Informationen zu Register Steuerelementen

Ein Registerkarten-Steuerelement entspricht in etwa einem Trennblatt in einem Notizbuch den Beschriftungen in einer Hängeregistratur. Durch Verwenden eines Registerkarten-Steuerelements können in einer Anwendung mehrere Seiten für denselben Bereich in einem Fenster oder Dialogfeld definiert werden. Jede Seite besteht aus einem bestimmten Informationstyp oder einer Gruppe von Steuerelementen, die von der Anwendung angezeigt werden, wenn der Benutzer die entsprechende Registerkarte auswählt.

Der folgende Screenshot zeigt ein einfaches Registerkarten-Steuerelement, das Tabstopps für Wochentage enthält. Die Registerkarte "Dienstag" wurde ausgewählt.

![Screenshot eines Eigenschaften Blatts mit fünf Registerkarten, eine für jeden Tag der Woche](images/tab-simple.png)

Das Thema enthält folgende Abschnitte:

-   [Erstellen von Register Steuerelementen](#creating-tab-controls)
-   [Register Steuerelement Stile](#tab-control-styles)
-   [Registerkarten und Registerkarten Attribute](#tabs-and-tab-attributes)
-   [Anzeigebereich](#display-area)
-   [Registerkarten Auswahl](#tab-selection)
-   [Registerkarten-Steuerelement Bildlisten](#tab-control-image-lists)
-   [Tabulator Größe und-Position](#tab-size-and-position)
-   [Vom Besitzer gezeichnete Registerkarten](#owner-drawn-tabs)
-   [Quick Infos für die Tab-Taste](#tab-control-tooltips)
-   [Standard-Steuerelement Verarbeitung von Registerkarten](#default-tab-control-message-processing)

## <a name="creating-tab-controls"></a>Erstellen von Register Steuerelementen

Sie können ein Registerkarten-Steuerelement erstellen, indem Sie die [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) -Funktion aufrufen und die Fenster Klasse " [**WC \_ TabControl**](common-control-window-classes.md) " angeben. Diese Fenster Klasse wird registriert, wenn die dll der allgemeinen Steuerelemente geladen wird. Um sicherzustellen, dass die dll geladen wird, verwenden Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion.

In Microsoft Visual Studio können Sie mithilfe der Toolbox ein Registerkarten-Steuerelement erstellen.

Sie senden Nachrichten an ein Registerkarten-Steuerelement zum Hinzufügen von Registerkarten und beeinflussen die Darstellung und das Verhalten des Steuer Elements. Jede Nachricht verfügt über ein entsprechendes Makro, das Sie verwenden können, anstatt die Nachricht explizit zu senden. Sie können eine einzelne Registerkarte in einem Registerkarten-Steuerelement nicht deaktivieren. Sie können ein Registerkarten-Steuerelement in einem Eigenschaften Blatt jedoch deaktivieren, indem Sie die entsprechende Seite deaktivieren.

## <a name="tab-control-styles"></a>Register Steuerelement Stile

Wenn das Steuerelement erstellt wird, können Sie bestimmte Merkmale auf Register Steuerelemente anwenden, indem Sie Registerkarten-Steuerelement Stile angeben. Beispielsweise können Sie die Ausrichtung und die allgemeine Darstellung der Registerkarten in einem Registerkarten-Steuerelement angeben.

Sie können bewirken, dass die Registerkarten wie Schaltflächen aussehen, indem Sie den [**TCS- \_ Schalt**](tab-control-styles.md) Flächen Stil angeben. Registerkarten in dieser Art von Registerkarten-Steuerelement sollten dieselbe Funktion wie Schaltflächen-Steuerelemente erfüllen. Das heißt, wenn Sie auf eine Registerkarte klicken, sollten Sie einen Befehl ausführen, anstatt eine Seite anzuzeigen. Da der Anzeigebereich in einem Schaltflächen-Registerkarten-Steuerelement normalerweise nicht verwendet wird, wird kein Rahmen um den Rahmen herum gezeichnet.

Sie können bewirken, dass eine Registerkarte den Eingabefokus erhält, wenn Sie durch Angabe des [**TCS \_ focusonbuttondown**](tab-control-styles.md) -Stils darauf klicken. Dieser Stil wird in der Regel nur mit dem Stil der [**TCS- \_ Schalt**](tab-control-styles.md) Flächen verwendet. Sie können angeben, dass eine Registerkarte keinen Eingabefokus erhält, wenn Sie mit dem TCS-Fokus auf das Format " [**TCS \_**](tab-control-styles.md) " geklickt wird.

Standardmäßig zeigt ein Registerkarten-Steuerelement nur eine Zeile mit Registerkarten an. Wenn nicht alle Registerkarten gleichzeitig angezeigt werden können, zeigt das Registerkarten-Steuerelement ein auf-ab-Steuerelement an, sodass der Benutzer zusätzliche Registerkarten in die Ansicht scrollen kann. Sie können bewirken, dass ein Registerkarten-Steuerelement ggf. mehrere Zeilen von Registerkarten anzeigt, indem Sie den [**\_ mehrzeiligen TCS**](tab-control-styles.md) -Stil angeben. Bei diesem Stil können alle Registerkarten gleichzeitig angezeigt werden. Die Registerkarten werden in jeder Zeile linksbündig ausgerichtet, es sei denn, Sie geben den [**TCS-Stil \_ rightrecht Recht**](tab-control-styles.md) . In diesem Fall wird die Breite der einzelnen Registerkarten angehoben, sodass jede Zeile von Registerkarten die gesamte Breite des Registerkarten-Steuer Elements füllt.

Ein Registerkarten-Steuerelement passt jede Registerkarte automatisch an Ihr Symbol, falls vorhanden, und ihre Bezeichnung an. Um allen Registerkarten die gleiche Breite zuzuweisen, können Sie den [**TCS- \_ FixedWidth**](tab-control-styles.md) -Stil angeben. Das-Steuerelement passt alle Tabstopps an die breiteste Bezeichnung an, oder Sie können eine bestimmte Breite und Höhe mithilfe der TCM-Nachricht " [**\_ stemsize**](tcm-setitemsize.md) " zuweisen. In jeder Registerkarte Zentriert das Steuerelement das Symbol und die Bezeichnung, wobei das Symbol links neben der Bezeichnung platziert wird. Sie können das Symbol auf der linken Seite erzwingen, wobei die Bezeichnung zentriert ist, indem Sie den [**TCS \_ forceienleft**](tab-control-styles.md) -Stil angeben. Sie können das Symbol und die Bezeichnung mit dem [**TCS \_ forcelabelleft**](tab-control-styles.md) -Stil linksbündig ausrichten. Der **TCS- \_ FixedWidth** -Stil kann nicht mit dem [**TCS \_ rightrecht**](tab-control-styles.md) -Stil verwendet werden.

Sie können angeben, dass das übergeordnete Fenster die Registerkarten im-Steuerelement unter Verwendung des [**TCS- \_ Besitzers**](tab-control-styles.md) für das Besitzer Zeichen zeichnet. Weitere Informationen finden Sie unter vom [Besitzer gezeichnete Registerkarten](#owner-drawn-tabs).

Sie können angeben, dass ein Registerkarten-Steuerelement mit dem [**TCS- \_ Tooltips**](tab-control-styles.md) -Stil ein QuickInfo-Steuerelement erstellt. Weitere Informationen hierzu finden Sie unter Quick Infos für Registerkarten- [Steuer](#tab-control-tooltips)Elemente.

## <a name="tabs-and-tab-attributes"></a>Registerkarten und Registerkarten Attribute

Jede Registerkarte in einem Registerkarten-Steuerelement besteht aus einem Symbol, einer Bezeichnung und Anwendungs definierten Daten. Diese Informationen werden durch eine [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur angegeben. Sie können einem Registerkarten-Steuerelement Registerkarten hinzufügen, die Anzahl der Registerkarten abrufen, den Inhalt einer Registerkarte abrufen und festlegen und Registerkarten löschen. Registerkarten werden durch ihren Null basierten Index identifiziert.

Um Registerkarten einem Registerkarten-Steuerelement hinzuzufügen, verwenden Sie die [**TCM \_ InsertItem**](tcm-insertitem.md) -Nachricht, die die Position des Elements und die Adresse einer [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur angibt. Sie können den Inhalt einer vorhandenen Registerkarte mit den Nachrichten [**TCM \_ GetItem**](tcm-getitem.md) und [**TCM \_ SetItem**](tcm-setitem.md) abrufen und festlegen. Für jede Registerkarte können Sie ein Symbol, eine Bezeichnung oder beides angeben. Sie können auch Anwendungs definierte Daten angeben, die der Registerkarte zugeordnet werden sollen.

Sie können die aktuelle Anzahl der Registerkarten mithilfe der Nachricht [**TCM \_ GetItemCount**](tcm-getitemcount.md) abrufen, eine Registerkarte mithilfe der [**TCM \_ DeleteItem**](tcm-deleteitem.md) -Nachricht löschen und alle Registerkarten in einem Registerkarten-Steuerelement mithilfe der [**TCM \_ DeleteAllItems**](tcm-deleteallitems.md) -Nachricht löschen.

Sie können den einzelnen Registerkarten Anwendungs definierte Daten zuordnen. Beispielsweise können Sie Informationen zu jeder Seite mit der entsprechenden Registerkarte Speichern. Standardmäßig ordnet ein Registerkarten-Steuerelement für Anwendungs definierte Daten vier zusätzliche Bytes pro Registerkarte zu. Sie können die Anzahl zusätzlicher Bytes pro Registerkarte ändern, indem Sie [**die \_ Nachricht TCM**](tcm-setitemextra.md) . Diese Meldung kann nur verwendet werden, wenn das Registerkarten-Steuerelement leer ist.

Die Anwendungs definierten Daten werden vom **LPARAM** -Member der [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur angegeben. Wenn Sie mehr als 4 Bytes von Anwendungs definierten Daten verwenden, müssen Sie eine eigene Struktur definieren und anstelle von **TCITEM** verwenden. Sie können Anwendungs definierte Daten auf die gleiche Weise abrufen und festlegen, wie Sie andere Informationen über eine Registerkarte abrufen und festlegen – mithilfe der Nachrichten [**TCM \_ GetItem**](tcm-getitem.md) und [**TCM \_ SetItem**](tcm-setitem.md) .

Der erste Member der Struktur muss eine [**tcitemheader**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) -Struktur sein, und die restlichen Elemente müssen Anwendungs definierte Daten angeben. **Tcitemheader** ist mit [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)identisch, mit dem Unterschied, dass er nicht über den **LPARAM** -Member verfügt. Der Unterschied zwischen der Größe ihrer Struktur und der Größe von **tcitemheader** sollte der Anzahl zusätzlicher Bytes pro Registerkarte entsprechen.

## <a name="display-area"></a>Anzeigebereich

Der Anzeigebereich eines Registerkarten-Steuer Elements ist der Bereich, in dem eine Anwendung die aktuelle Seite anzeigt. In der Regel erstellt eine Anwendung ein untergeordnetes Fenster oder Dialogfeld, das die Fenstergröße und-Position so festlegt, dass Sie in den Anzeigebereich passt. Mithilfe des Fenster Rechtecks für ein Registerkarten-Steuerelement können Sie das umgebende Rechteck des Anzeige Bereichs mithilfe der [**TCM \_**](tcm-adjustrect.md) -Nachricht mit dem Status "TCM" berechnen.

Manchmal muss der Anzeigebereich eine bestimmte Größe haben – z. b. die Größe eines untergeordneten Dialog Felds untergeordneter Elemente. Bei Angabe des umgebenden Rechtecks für den Anzeigebereich können Sie [**TCM \_**](tcm-adjustrect.md) -Element verwenden, um das entsprechende Fenster Rechteck für das Registerkarten-Steuerelement zu berechnen.

## <a name="tab-selection"></a>Registerkarten Auswahl

Wenn der Benutzer eine Registerkarte auswählt, sendet ein Registerkarten-Steuerelement seine übergeordneten Fenster Benachrichtigungs Codes in Form von WM-Benachrichtigungs Meldungen. [**\_**](wm-notify.md) Der [TCN \_ selchanging](tcn-selchanging.md) -Benachrichtigungs Code wird gesendet, bevor die Auswahl geändert wird, und der [TCN \_ selChange](tcn-selchange.md) -Benachrichtigungs Code wird gesendet, nachdem die Auswahl geändert wurde.

Sie können [TCN \_ selchanging](tcn-selchanging.md) verarbeiten, um den Status der ausgehenden Seite zu speichern. Sie können **true** zurückgeben, um zu verhindern, dass sich die Auswahl ändert. Beispielsweise möchten Sie möglicherweise nicht von einem untergeordneten Dialogfeld wechseln, in dem ein Steuerelement über eine ungültige Einstellung verfügt.

Sie müssen [TCN \_ selChange](tcn-selchange.md) verarbeiten, um die eingehende Seite im Anzeigebereich anzuzeigen. Dies könnte lediglich dazu führen, dass die in einem untergeordneten Fenster angezeigten Informationen geändert werden. Häufig besteht jede Seite aus einem untergeordneten Fenster oder Dialogfeld. In diesem Fall kann eine Anwendung diese Benachrichtigung durch das zerstören oder Ausblenden des ausgehenden untergeordneten Fensters oder Dialog Felds und durch Erstellen oder zeigen des eingehenden untergeordneten Fensters oder Dialog Felds verarbeiten.

Sie können die aktuelle Auswahl mit den Nachrichten [**TCM \_ getcurrsel**](tcm-getcursel.md) und [**TCM \_ setcurrsel**](tcm-setcursel.md) abrufen und festlegen.

## <a name="tab-control-image-lists"></a>Registerkarten-Steuerelement Bildlisten

Jeder Registerkarte kann ein Symbol zugeordnet sein, das durch einen Index in der Bildliste für das Registerkarten-Steuerelement angegeben wird. Wenn ein Registerkarten-Steuerelement erstellt wird, ist keine Bildliste zugeordnet. Eine Anwendung kann mithilfe der [**ImageList-Funktion \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) eine Bildliste erstellen und Sie dann mithilfe der [**TCM \_ SetImageList**](tcm-setimagelist.md) -Nachricht einem Registerkarten-Steuerelement zuweisen.

Sie können der Bildliste eines Registerkarten-Steuer Elements Bilder hinzufügen, genauso wie bei jeder anderen Bildliste. Allerdings sollte eine Anwendung Images mithilfe der [**TCM \_ removeimage**](tcm-removeimage.md) -Nachricht anstelle der [**ImageList \_ Remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) -Funktion entfernen. Diese Meldung stellt sicher, dass jede Registerkarte dem gleichen Bild wie zuvor zugeordnet bleibt.

Durch das zerstören eines Registerkarten-Steuer Elements wird eine zugeordnete Bildliste nicht zerstört. Sie müssen die Bildliste separat zerstören. Dies ist hilfreich, wenn Sie mehrere Registerkarten-Steuerelemente dieselbe Bildliste zuweisen möchten.

Um das Handle für die Bildliste abzurufen, die derzeit einem Registerkarten-Steuerelement zugeordnet ist, können Sie die [**TCM \_ GetImageList**](tcm-getimagelist.md) -Nachricht verwenden.

## <a name="tab-size-and-position"></a>Tabulator Größe und-Position

Jede Registerkarte in einem Registerkarten-Steuerelement hat eine Größe und Position. Sie können die Größe der Registerkarten festlegen, das umgebende Rechteck einer Registerkarte abrufen oder ermitteln, welche Registerkarte sich an einer bestimmten Position befindet.

Für Registerkarten-Steuerelemente mit fester Breite und vom Besitzer gezeichneter Registerkarten können Sie die exakte Breite und Höhe von Registerkarten mithilfe der Nachricht [**TCM \_ setitemsize**](tcm-setitemsize.md) festlegen. In anderen Registerkarten-Steuerelementen wird die Größe jeder Registerkarte basierend auf dem Symbol und der Bezeichnung für die Registerkarte berechnet. Das Registerkarten-Steuerelement enthält Platz für einen Rahmen und einen zusätzlichen Rand. Sie können die Breite des Rand mithilfe der [**TCM- \_ setPadding**](tcm-setpadding.md) -Nachricht festlegen.

Sie können das aktuelle umgebende Rechteck für eine Registerkarte mithilfe der [**TCM \_ GetItemRect**](tcm-getitemrect.md) -Nachricht ermitteln. Mithilfe der Nachricht [**TCM \_ HitTest**](tcm-hittest.md) können Sie feststellen, welche Registerkarte, falls vorhanden, sich an einem angegebenen Speicherort befindet.

In einem Registerkarten-Steuerelement mit dem [**\_ mehrzeiligen TCS**](tab-control-styles.md) -Stil können Sie die aktuelle Anzahl der Zeilen von Registerkarten mithilfe der Nachricht [**TCM \_ GetRowCount**](tcm-getrowcount.md) ermitteln.

## <a name="owner-drawn-tabs"></a>Registerkarten Owner-Drawn

Wenn ein Registerkarten-Steuerelement über das [**TCS-Objekt \_**](tab-control-styles.md) "Besitzer" verfügt, muss das übergeordnete Fenster Tabstopps zeichnen, indem die [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht verarbeitet wird. Das Registerkarten-Steuerelement sendet diese Meldung immer dann, wenn eine Registerkarte gezeichnet werden muss. Der *LPARAM* -Parameter gibt die Adresse einer [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur an, die den Index der Registerkarte, das umgebende Rechteck und den Gerätekontext (DC) enthält, in dem gezeichnet werden soll.

Standardmäßig enthält der **ItemData** -Member von [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) den Wert des **LPARAM** -Members der [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur. Wenn Sie jedoch die Menge der Anwendungs definierten Daten pro Registerkarte ändern, enthält **ItemData** stattdessen die Adresse der Daten. Mithilfe der Nachricht [**TCM \_ setitemextra**](tcm-setitemextra.md) können Sie die Menge der Anwendungs definierten Daten pro Registerkarte ändern.

Um die Größe der Elemente in einem Registerkarten-Steuerelement anzugeben, muss das übergeordnete Fenster die " [**WM \_ MeasureItem**](wm-measureitem.md) "-Meldung verarbeiten. Da alle Registerkarten in einem vom Besitzer gezeichneten Registerkarten-Steuerelement dieselbe Größe haben, wird diese Meldung nur einmal gesendet. Es gibt keinen Registerkarten-Steuerelement Stil für vom Besitzer gezeichnete Registerkarten mit unterschiedlicher Größe. Sie können auch die Breite und Höhe von Registerkarten mithilfe der Nachricht [**TCM \_ setitemsize**](tcm-setitemsize.md) festlegen.

## <a name="tab-control-tooltips"></a>Quick Infos für die Tab-Taste

Sie können ein QuickInfo-Steuerelement verwenden, um eine kurze Beschreibung der einzelnen Registerkarten in einem Registerkarten-Steuerelement anzugeben. Ein Registerkarten-Steuerelement mit dem [**TCS- \_ Tooltips**](tab-control-styles.md) -Stil erstellt bei der Erstellung ein QuickInfo-Steuerelement und zerstört das QuickInfo-Steuerelement, wenn es zerstört wird. Sie können auch ein QuickInfo-Steuerelement erstellen und es einem Registerkarten-Steuerelement zuweisen.

Wenn Sie ein QuickInfo-Steuerelement mit einem Registerkarten-Steuerelement verwenden, muss das übergeordnete Fenster den [TTN \_ getdispinfo](ttn-getdispinfo.md) -Benachrichtigungs Code verarbeiten, um eine Beschreibung der einzelnen Registerkarten auf Anforderung bereitzustellen

Wenn Sie dasselbe QuickInfo-Steuerelement mit mehreren Registerkarten-Steuerelementen verwenden möchten, erstellen Sie das QuickInfo-Steuerelement selbst, und weisen Sie es dem Registerkarten-Steuerelement mithilfe der [**TCM- \_ SetToolTips**](tcm-settooltips.md) Sie können das Handle für das aktuelle QuickInfo-Steuerelement eines Register Steuer Elements abrufen, indem Sie die [**TCM \_ gettooltips**](tcm-gettooltips.md) -Meldung verwenden. Wenn Sie ein eigenes QuickInfo-Steuerelement erstellen, sollten Sie den [**TCS- \_ Tooltips**](tab-control-styles.md) -Stil nicht verwenden.

## <a name="default-tab-control-message-processing"></a>Standard-Steuerelement Verarbeitung von Registerkarten

In diesem Abschnitt wird die von einem Registerkarten-Steuerelement ausgeführte Nachrichtenverarbeitung beschrieben. Für Registerkarten-Steuerelemente spezifische Meldungen werden in anderen Abschnitten dieser Dokumentation erläutert.



| `Message`                                                  | Verarbeitung wird ausgeführt                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM- \_ capturechanged**](/windows/desktop/inputdev/wm-capturechanged) | Hat nichts, wenn das Registerkarten-Steuerelement die Maus Aufzeichnung selbst freigegeben hat. Wenn ein anderes Fenster die Maus erfasst und eine Schaltfläche gedrückt gehalten wird, gibt der Befehl die Schaltfläche frei.                                                                                                                                                                                                                                                                                                                |
| [**WM \_ Erstellen**](/windows/desktop/winmsg/wm-create)                 | Ordnet eine interne Datenstruktur zu und initialisiert sie. Das Steuerelement erstellt ein QuickInfo-Steuerelement, wenn der [**TCS- \_ Tooltips**](tab-control-styles.md) -Stil angegeben wird.                                                                                                                                                                                                                                                                                                    |
| [**WM \_ zerstören**](/windows/desktop/winmsg/wm-destroy)               | Gibt Ressourcen frei, die während der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Verarbeitung zugewiesen                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ getdlgcode**](/windows/desktop/dlgbox/wm-getdlgcode)         | Gibt eine Kombination der dlgc \_ -wantpfeile-und dlgc- \_ wantchars-Werte zurück.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM- \_ getFont**](/windows/desktop/winmsg/wm-getfont)               | Gibt das Handle für die Schriftart zurück, die für Bezeichnungen verwendet wird.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown)               | Verarbeitet die Richtungs Tasten und ändert ggf. die Auswahl.                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**WM- \_ killfokus**](/windows/desktop/inputdev/wm-killfocus)           | Erklärt die Registerkarte mit dem Fokus für ungültig, sodass Sie neu gezeichnet wird, um einen nicht fokussierten Zustand widerzuspiegeln.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown)       | Leitet die Nachricht ggf. an das ToolTip-Steuerelement weiter und ändert die Auswahl, wenn der Benutzer auf eine Registerkarte klickt. Wenn der Benutzer auf eine Schaltfläche klickt, zeichnet das Steuerelement die Schaltfläche neu, um ein abgesenktes aussehen zu erzielen, und erfasst die Maus. Wenn der Benutzer entweder auf eine Registerkarte oder auf eine Schaltfläche klickt und der [**TCS \_ focusonbuttondown**](tab-control-styles.md) -Stil angegeben ist, legt das Steuerelement den Fokus auf sich selbst fest.                                                     |
| [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup)           | Gibt die Maus frei, wenn eine Schaltfläche gedrückt wurde. Wenn sich der Cursor über der Schaltfläche befindet und gedrückt gehalten wird, ändert das Steuerelement die Auswahl entsprechend und zeichnet die Schaltfläche neu.                                                                                                                                                                                                                                                                                                         |
| [**WM- \_ mouseelmove**](/windows/desktop/inputdev/wm-mousemove)           | Leitet die Meldung ggf. an das QuickInfo-Steuerelement weiter. Wenn der [**TCS \_**](tab-control-styles.md) -Schaltflächen Stil angegeben ist und die Maustaste nach dem Klicken gedrückt gehalten wird, wird das Steuerelement möglicherweise auch die betroffene Schaltfläche neu zeichnen, um es zu einem erhöhten oder abgesenkten aussehen zu machen.                                                                                                                                                                                            |
| [**WM- \_ Benachrichtigung**](wm-notify.md)                          | Leitet vom QuickInfo-Steuerelement gesendete Benachrichtigungs Codes weiter.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint)                            | Zeichnet einen Rahmen um den Anzeigebereich (es sei denn, der [**TCS- \_ Schalt**](tab-control-styles.md) Flächen Stil ist angegeben) und zeichnet alle Registerkarten, die das ungültige Rechteck überschneiden. Für jede Registerkarte zeichnet Sie den Hauptteil der Registerkarte (oder sendet eine [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht an das übergeordnete Fenster) und zeichnet dann einen Rahmen um die Registerkarte. Wenn der *wParam* -Parameter ungleich NULL ist, geht das Steuerelement davon aus, dass es sich bei dem Wert um einen HDC handelt und zeichnet sich durch den Gerätekontext aus. |
| [**WM- \_ rbuttondown**](/windows/desktop/inputdev/wm-rbuttondown)       | Sendet einen [nm- \_ rclick](nm-rclick-tab.md) -Benachrichtigungs Code an das übergeordnete Fenster.                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)             | Erklärt die Registerkarte mit dem Fokus für ungültig, sodass Sie neu gezeichnet wird, um einen Fokus Zustand widerzuspiegeln.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont)               | Legt die Schriftart fest, die für Bezeichnungen verwendet wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ -Ziel**](/windows/desktop/gdi/wm-setredraw)                    | Legt den Zustand eines internen Flags fest, das bestimmt, ob das Steuerelement neu gezeichnet wird, wenn Elemente eingefügt und gelöscht werden, wenn die Schriftart geändert wird usw.                                                                                                                                                                                                                                                                                                                      |
| [**WM- \_ Größe**](/windows/desktop/winmsg/wm-size)                     | Berechnet die Positionen von Registerkarten neu und kann einen Teil des Registerkarten-Steuer Elements für ungültig erklären, um das Neuzeichnen einiger oder aller Registerkarten zu erzwingen.                                                                                                                                                                                                                                                                                                                                                             |



 

 

 