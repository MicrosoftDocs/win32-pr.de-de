---
title: Informationen zu List-View Steuerelementen
description: Ein Listenansicht-Steuerelement ist ein Fenster, in dem eine Sammlung von Elementen angezeigt wird.
ms.assetid: 163f7778-690c-4166-b0c5-c7be1a03ae98
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: fe1b953bf7d7204a3afffcfa0bc5aa5af9bf94fa
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106350745"
---
# <a name="about-list-view-controls"></a>Informationen zu List-View Steuerelementen

Siehe das [Virtual ListView-Steuerelement Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw).

Ein Listenansicht-Steuerelement ist ein Fenster, in dem eine Sammlung von Elementen angezeigt wird. Listenansicht-Steuerelemente bieten verschiedene Möglichkeiten zum Anordnen und Anzeigen von Elementen und sind viel flexibler als einfache [Listenfelder](list-boxes.md). Beispielsweise können in Spalten rechts neben dem Symbol und der Bezeichnung zusätzliche Informationen zu den einzelnen Elementen angezeigt werden.

-   [Listenansicht: Stile und Ansichten](#list-view-styles-and-views)
    -   [Erweiterte List-View Stile](#extended-list-view-styles)
-   [Stil des virtuellen List-View](#virtual-list-view-style)
    -   [Erstellen eines virtuellen List-View-Steuer Elements](#creating-a-virtual-list-view-control)
    -   [Kompatibilitätsprobleme](#compatibility-issues)
    -   [Behandeln von Benachrichtigungs Codes für virtuelle List-View Steuerelemente](#handling-virtual-list-view-control-notification-codes)
    -   [Cache Verwaltung](#cache-management)
-   [Auflisten: Arbeitsbereiche anzeigen](#list-view-working-areas)
-   [Listenansicht: Bildlisten](#list-view-image-lists)
-   [Listen-Ansichts Elemente und unter Elemente](#list-view-items-and-subitems)
    -   [Listen-Ansichts Element Zustände](#list-view-item-states)
    -   [Rückruf Elemente und die Rückruf Maske](#callback-items-and-the-callback-mask)
    -   [Listen-Ansichts Element Position](#list-view-item-position)
    -   [Anordnen, Sortieren und suchen von Elementen](#arranging-sorting-and-finding-items)
-   [Listen-View-Spalten](#list-view-columns)
-   [Bild Lauf Position in der Liste anzeigen](#list-view-scroll-position)
-   [Bezeichnungs Bearbeitung für Listenansicht](#list-view-label-editing)
-   [Listen-anzeigen von Farben](#list-view-colors)
-   [Anordnen von Listenelementen nach Gruppe](#arranging-list-items-by-group)
-   [Einfügezeichen](#insertion-marks)

## <a name="list-view-styles-and-views"></a>List-View Stile und Ansichten

Listenansicht-Steuerelemente können Elemente in fünf verschiedenen Ansichten anzeigen. Der Fenster Stil des Steuer Elements gibt die Standardansicht an. Zusätzliche Fenster Stile geben die Ausrichtung von Elementen und Steuerelement spezifischen Funktionen an. In der folgenden Tabelle werden die-Sichten beschrieben.



| Ansichtsname             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Symbol Ansicht             | Wird durch den [**LVS- \_ Symbol**](list-view-window-styles.md) Fenster Stil oder durch Übergabe des **LV- \_ Ansichts \_ Symbols** mit der [**LVM- \_ Setview**](lvm-setview.md) -Nachricht angegeben. Jedes Element wird als Symbol in voller Größe und mit einer Bezeichnung darunter dargestellt. Der Benutzer kann die Elemente an eine beliebige Stelle im Fenster "Listenansicht" ziehen.                                                                                                                                                                                                                                         |
| Kleine Symbol Ansicht       | Wird durch den [**LVS \_ SmallIcon**](list-view-window-styles.md) -Fenster Stil oder durch übergeben der **LV- \_ Ansicht \_ SmallIcon** mit [**LVM \_ Setview**](lvm-setview.md)angegeben. Jedes Element wird als kleines Symbol mit der Bezeichnung auf der rechten Seite angezeigt. Der Benutzer kann die Elemente an einen beliebigen Speicherort ziehen.                                                                                                                                                                                                                                                       |
| Listenansicht             | Wird durch den [**LVS- \_ Listen**](list-view-window-styles.md) Fenster Stil oder durch übergeben der **LV- \_ Ansichts \_ Liste** mit [**LVM \_ Setview**](lvm-setview.md)angegeben. Jedes Element wird als kleines Symbol mit einer Bezeichnung auf der rechten Seite angezeigt. Elemente werden in Spalten angeordnet, und der Benutzer kann Sie nicht an eine beliebige Stelle ziehen.                                                                                                                                                                                                                               |
| Berichtsansicht (Details) | Wird durch den [**LVS- \_ Berichts**](list-view-window-styles.md) Fenster Stil oder durch Übergabe der **Details der LV- \_ Ansicht \_** mit [**LVM \_ Setview**](lvm-setview.md)angegeben. Jedes Element wird in einer eigenen Zeile angezeigt, und die Informationen werden in Spalten angeordnet. Die Spalte ganz links ist immer linksbündig und enthält das kleine Symbol und die Bezeichnung. Nachfolgende Spalten enthalten unter Elemente, wie von der Anwendung angegeben. Jede Spalte verfügt über einen-Header, es sei denn, Sie geben auch den Fenster Stil [**LVS \_ nocolumnheader**](list-view-window-styles.md) an. |
| Neben-/Untereinanderansicht             | **Version 6 und höher.** Wird durch übergeben der **LV- \_ Ansichts \_ Kachel** mit [**LVM \_ Setview**](lvm-setview.md)angegeben. Jedes Element wird als Symbol in voller Reihenfolge mit einer Bezeichnung von einer oder mehreren Zeilen daneben angezeigt.                                                                                                                                                                                                                                                                                                                                                        |



 

In den folgenden Screenshots werden Sichten verwendet, um unterschiedliche Mengen von Informationen zu jedem der sieben Haustiere anzuzeigen. Die Ansichten veranschaulichen, wie die Informationen unter Windows Vista angezeigt werden können. Die visuellen Stile für das-Steuerelement wurden mithilfe von [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme)auf das Design "Explorer" festgelegt.

Der folgende Screenshot zeigt die Detailansicht.

![Screenshot, der Informationen in fünf Spalten und sieben Zeilen anzeigt](images/lv-detailsview.png)

Der folgende Screenshot zeigt die Symbol Ansicht.

![Screenshot, der nur den Namen der einzelnen Haustiere anzeigt, und ein Symbol, das die Art angibt](images/lv-iconview.png)

Der folgende Screenshot zeigt die Listenansicht.

![Screenshot, der für jedes Haustier ein großes Symbol als nächstes als Text für den Namen, die Rasse und den Preis des Tieres anzeigt](images/lv-listview.png)

Der folgende Screenshot zeigt die Kachel Ansicht.

![Kachel Ansicht.](images/lv-tileview.png)

Sie können den Ansichtstyp ändern, nachdem Sie ein Listenansicht-Steuerelement erstellt haben. Zum Abrufen und Ändern des Fenster Stils verwenden Sie die Funktionen " [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) " und " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) ". Verwenden Sie zum Bestimmen der Fenster Stile der aktuellen Ansicht den [**LVS- \_ typemask**](list-view-window-styles.md) -Wert.

Sie können steuern, wie Elemente in einer Symbol Ansicht oder in einer kleinen Symbol Ansicht angeordnet werden, indem Sie entweder den [**LVS \_ AlignTop**](list-view-window-styles.md) (Standard) oder den [**LVS \_ alignleft**](list-view-window-styles.md) -Fenster Stil angeben.

Sie können die Ausrichtung ändern, nachdem Sie ein Listenansicht-Steuerelement erstellt haben. Verwenden Sie den [**LVS \_ alignmask**](list-view-window-styles.md) -Wert, um die aktuelle Ausrichtung zu ermitteln.

Zusätzliche Fenster Stile bieten weitere Optionen, z. b. ob ein Benutzer Bezeichnungen bearbeiten oder mehr als ein Element gleichzeitig auswählen kann. Eine komplette Liste finden Sie unter [Listenansicht-Fenster Stile](list-view-window-styles.md).

### <a name="extended-list-view-styles"></a>Erweiterte List-View Stile

Die erweiterten Listenansicht-Steuerelement Stile bieten Optionen, wie z. b. Kontrollkästchen, flatscrollleisten, Rasterlinien und Hot-Tracking. Eine komplette Liste finden Sie unter [Erweiterte List-View Stile](extended-list-view-styles.md). Sie greifen nicht auf Erweiterte Listen Ansichts Stile auf die gleiche Weise wie Standardfenster Stile zu. Sie verwenden die Funktionen " [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) " und " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) " nicht, um erweiterte Stiländerungen vorzunehmen.

Es gibt zwei Nachrichten, die erweiterte Stil Informationen, [**LVM \_ setextendedlistviewstyle**](lvm-setextendedlistviewstyle.md) und [**LVM \_ getextendedlistviewstyle**](lvm-getextendedlistviewstyle.md), festlegen und abrufen. Anstatt die Nachrichten explizit zu senden, können Sie die folgenden entsprechenden Makros verwenden: [**ListView \_ abtextendedlistviewstyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle), [**ListView \_ abtextendedlistviewstyleex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)und [**ListView \_ getextendedlistviewstyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle).

## <a name="virtual-list-view-style"></a>Stil des virtuellen List-View

Eine virtuelle Listenansicht ist ein Listenansicht-Steuerelement, das über den [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil verfügt. Dieser Stil ermöglicht dem Steuerelement das Verarbeiten von Millionen von Elementen, da der Besitzer die Last der Verwaltung von Elementdaten erhält. Dies ermöglicht es Ihnen, das Steuerelement für die virtuelle Listenansicht mit großen Datenbanken zu verwenden, in denen bestimmte Methoden des Datenzugriffs bereits vorhanden sind.

Ein virtuelles Listenansicht-Steuerelement verwaltet sehr wenig Element Informationen selbst. Mit Ausnahme der Elementauswahl und der Fokus Informationen muss der Besitzer des Steuer Elements alle Element Informationen verwalten. Andere Prozesse fordern mithilfe von [LVN \_ getdispinfo](lvn-getdispinfo.md) -Benachrichtigungs Codes Element Informationen vom Besitzer an.

Da diese Art von Listen Steuerelement für große Datasets gedacht ist, sollten Sie angeforderte Elementdaten Zwischenspeichern, um die Abruf Leistung zu verbessern. Die Listenansicht bietet einen Cache-Hinting-Mechanismus, der die Optimierung des Caches unterstützt. Der Hinweis wird in Form eines [LVN- \_ odcachehint](lvn-odcachehint.md) -Benachrichtigungs Codes implementiert.

### <a name="creating-a-virtual-list-view-control"></a>Erstellen eines virtuellen List-View-Steuer Elements

Sie erstellen virtuelle Listenansicht-Steuerelemente mithilfe der Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " und geben dabei den Stil des [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Fensters als Teil des *dwstyle* -Funktions Parameters an. Dynamisches wechseln zum und aus dem **LVS \_** -Besitzer Daten Stil wird nicht unterstützt.

Sie können den [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil in Kombination mit den meisten anderen Fenster Stilen verwenden, mit Ausnahme der Sortierungsart [**LVS \_ SortAscending**](list-view-window-styles.md) oder [**LVS \_ sortabsteigend**](list-view-window-styles.md) . Alle Virtual List-View-Steuerelemente werden standardmäßig auf den [**LVS \_ AutoArrange**](list-view-window-styles.md) -Stil festgelegt.

Damit Elemente in der Liste angezeigt werden können, müssen Sie zunächst entweder explizit oder mithilfe des ListView-Elements " [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) [**" das- \_**](lvm-setitemcount.md) Makro "*" senden.

Die folgenden Meldungen werden unter dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil nicht unterstützt: [**LVM \_ enablegroupview**](lvm-enablegroupview.md), [**LVM \_ GetItemText**](lvm-getitemtext.md), [**LVM \_ settileinfo**](lvm-settileinfo.md)und [**LVM \_ mapiddeindex**](lvm-mapidtoindex.md).

### <a name="compatibility-issues"></a>Kompatibilitätsprobleme

Alle vier der Listen Ansichts Stile – Symbol, kleines Symbol, Liste und Berichtsansicht – unterstützen den [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil. Listenansicht-Steuerelemente, die über den **LVS-Besitzer \_ Daten** Stil verfügen, speichern keine Element spezifischen Informationen. Daher sind die einzigen gültigen elementstatusflags, die Sie auf ein Element anwenden können, [**LVIS \_ ausgewählt**](list-view-item-states.md) und [**LVIS \_ fokussiert**](list-view-item-states.md). Es werden keine weiteren Zustandsinformationen gespeichert. Insbesondere verwaltet das Listenansicht-Steuerelement keine Zustands-oder Überlagerungs Bilder für jedes Element. Sie können jedoch festlegen, dass das Listenansicht-Steuerelement Ihre Anwendung für diese Images abfragt, indem es eine [**LVM- \_ SetCallbackMask**](lvm-setcallbackmask.md) -Nachricht sendet.

Die meisten Listenansicht-Steuerelement Meldungen und die zugehörigen Makros werden vollständig unterstützt. Einige Nachrichten weisen jedoch Einschränkungen auf oder werden nicht unterstützt, wenn Sie den [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil verwenden. In der folgenden Tabelle werden die betroffenen Nachrichten zusammengefasst.



| `Message`                                             | Einschränkung                                                                                                                                                                                                                                                      |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LVM \_ anordnen**](lvm-arrange.md)                 | Unterstützt nicht den **LVA- \_ snapragrid** -Stil.                                                                                                                                                                                                                 |
| [**LVM \_ DeleteAllItems**](lvm-deleteallitems.md)   | Legt die Element Anzahl auf 0 (null) fest und löscht alle internen Auswahl Variablen, löscht aber keine Elemente. Er führt einen Benachrichtigungs Rückruf aus.                                                                                                           |
| [**LVM \_ DeleteItem**](lvm-deleteitem.md)           | Wird nur für die Auswahl Integrität unterstützt. ein Element wird nicht tatsächlich gelöscht.                                                                                                                                                                                 |
| [**LVM \_ GetItemState**](lvm-getitemstate.md)       | Gibt nur den Fokus und Auswahl Zustände zurück (d. h. die Zustände, die vom Listenansicht-Steuerelement gespeichert werden).                                                                                                                                                                |
| [**LVM \_ GetNextItem**](lvm-getnextitem.md)         | Bietet keine Unterstützung für die Suchkriterien für die Listenansicht " **lvni \_ cut**", " **lvni \_ Hidden**" oder " **lvni \_**". Alle anderen Kriterien werden unterstützt.                                                                                                                     |
| [**LVM- \_ getworkareas**](lvm-getworkareas.md)       | Wird nicht unterstützt.                                                                                                                                                                                                                                               |
| [**LVM \_ InsertItem**](lvm-insertitem.md)           | Wird nur für die Auswahl Integrität unterstützt.                                                                                                                                                                                                                      |
| [**LVM \_ -Element**](lvm-setitem.md)                 | Wird nicht unterstützt. Um den Element Zustand festzulegen, verwenden Sie die [**ListView \_ SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) -Nachricht.                                                                                                                                               |
| [**LVM- \_ Anzahl von Sekunden**](lvm-setitemcount.md)       | Legt die Anzahl der Elemente fest, die sich derzeit in der Liste befinden. Wenn das Listenansicht-Steuerelement eine Benachrichtigung sendet, die Daten für ein beliebiges Element bis zum maximalen Satz anfordert, muss der Besitzer darauf vorbereitet sein, diese Daten bereitzustellen. Die Nachrichten Parameter unterstützen virtuelle Listenansicht-Steuerelemente. |
| [**LVM-" \_ abtitemposition"**](lvm-setitemposition.md) | Wird nicht unterstützt.                                                                                                                                                                                                                                               |
| [**LVM- \_ Status**](lvm-setitemstate.md)       | Ermöglicht es, dass nur die Auswahl-und Fokus Zustände für das Element geändert werden.                                                                                                                                                                                          |
| [**LVM- \_ abtitemtext**](lvm-setitemtext.md)         | Wird nicht unterstützt. Es ist Aufgabe der Anwendung, die Element Texte beizubehalten.                                                                                                                                                                            |
| [**LVM- \_ setworkareas**](lvm-setworkareas.md)       | Wird nicht unterstützt.                                                                                                                                                                                                                                               |
| [**LVM- \_ sortiitems**](lvm-sortitems.md)             | Wird nicht unterstützt. Es liegt in der Verantwortung der Anwendung, die Elemente in der gewünschten Reihenfolge darzustellen.                                                                                                                                                             |



 

### <a name="handling-virtual-list-view-control-notification-codes"></a>Behandeln von Benachrichtigungs Codes für virtuelle List-View Steuerelemente

Listenansicht-Steuerelemente mit dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil senden dieselben Benachrichtigungs Codes wie andere Listenansicht-Steuerelemente und zwei weitere: [LVN \_ odcachehint](lvn-odcachehint.md) und [LVN \_ odfinditem](lvn-odfinditem.md). Im folgenden finden Sie die häufigsten Benachrichtigungen, die das Listenansicht-Steuerelement mit dem **LVS-Besitzer \_ Daten** Stil sendet.



|                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LVN \_ getdispinfo](lvn-getdispinfo.md) | Ein virtuelles Listenansicht-Steuerelement verwaltet sehr wenig Element Informationen. Daher sendet Sie häufig den [LVN \_ getdispinfo](lvn-getdispinfo.md) -Benachrichtigungs Code, um Element Informationen anzufordern. Diese Meldung wird auf die gleiche Weise behandelt wie Rückruf Elemente in einem Standard Listen-Steuerelement. Da die Anzahl der vom Steuerelement unterstützten Elemente sehr groß sein kann, wird die Leistung durch das Zwischenspeichern von Elementdaten verbessert. Bei der Behandlung von LVN \_ getdispinfo versucht der Besitzer des Steuer Elements zunächst, angeforderte Element Informationen aus dem Cache bereitzustellen (Weitere Informationen finden Sie unter [Cache Verwaltung](#cache-management)). Wenn das angeforderte Element nicht zwischengespeichert wird, muss der Besitzer darauf vorbereitet sein, die Informationen auf andere Weise bereitzustellen. |
| [LVN \_ odcachehint](lvn-odcachehint.md) | Eine virtuelle Listenansicht sendet den [LVN- \_ odcachehint](lvn-odcachehint.md) -Benachrichtigungs Code zur Unterstützung bei der Optimierung des Caches. Der Benachrichtigungs Code stellt inklusive Indexwerte für einen Bereich von Elementen bereit, die zwischengespeichert werden sollen. Beim Empfang des Benachrichtigungs Codes muss der Besitzer darauf vorbereitet sein, den Cache mit Element Informationen für den angeforderten Bereich zu laden, damit die Informationen sofort verfügbar sind, wenn eine [LVN \_ getdispinfo](lvn-getdispinfo.md) -Nachricht gesendet wird.                                                                                                                                                                                                                                   |
| [LVN \_ odfinditem](lvn-odfinditem.md)   | Der [LVN \_ odfinditem](lvn-odfinditem.md) -Benachrichtigungs Code wird von einem Virtual List-View-Steuerelement gesendet, wenn das Steuerelement den Besitzer benötigt, um ein bestimmtes Rückruf Element zu finden. Der Benachrichtigungs Code wird gesendet, wenn das Listenansicht-Steuerelement einen schnellen Schlüssel Zugriff erhält oder wenn eine [**LVM- \_ FindItem**](lvm-finditem.md) -Nachricht empfangen wird. Suchinformationen werden in Form einer " [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) "-Struktur gesendet, die ein Member der [**nmlvfinditem**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) -Struktur ist. Der Besitzer muss darauf vorbereitet sein, nach einem Element zu suchen, das den vom Listenansicht-Steuerelement angegebenen Informationen entspricht. Der Besitzer gibt den Index des Elements zurück, wenn erfolgreich, oder-1, wenn kein übereinstimmendes Element gefunden wurde.               |



 

### <a name="cache-management"></a>Cache Verwaltung

Ein Listenansicht-Steuerelement mit dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil erzeugt eine große Anzahl von [LVN \_ getdispinfo](lvn-getdispinfo.md) -Benachrichtigungs Codes und, um die Optimierung des Caches zu unterstützen, eine [LVN- \_ odcachehint](lvn-odcachehint.md) -Nachricht. LVN \_ odcachehint-Meldungen enthalten Informationen über die empfohlenen Elemente, die im Cache enthalten sein sollen. Diese Nachrichten werden als [**WM- \_ Benachrichtigungs**](wm-notify.md) Nachrichten gesendet, wobei der *LPARAM* -Wert als Adresse einer [**nmlvcachehint**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) -Struktur fungiert.

Die [**nmlvcachehint**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) -Struktur enthält zwei ganzzahlige Member ( **ifrom** und **iTo**), die die inklusiven Endpunkte eines Bereichs von Elementen darstellen, die höchstwahrscheinlich benötigt werden. Der Besitzer muss darauf vorbereitet sein, den Cache mit den Element Informationen für die einzelnen Elemente innerhalb des empfohlenen Bereichs zu laden.

Das Listen Steuerelement benötigt häufig Element Informationen für das erste Element (Offset 0). Der [LVN \_ odcachehint](lvn-odcachehint.md) -Benachrichtigungs Code enthält möglicherweise nicht immer Element 0, er muss jedoch immer im Cache enthalten sein.

Der Zugriff auf die letzten Elemente in der Liste erfolgt häufig. Daher kann der Besitzer einen zweiten Cache beibehalten, der die Elemente am Ende der Liste enthält. Der angeforderte Bereich von [LVN \_ odcachehint](lvn-odcachehint.md) kann gegen den endcache überprüft werden, damit er automatisch verfügbar wird, anstatt jedes Mal denselben Endbereich erneut laden zu müssen.

## <a name="list-view-working-areas"></a>Arbeitsbereiche List-View

Listenansicht-Steuerelemente unterstützen Arbeitsbereiche, bei denen es sich um rechteckige virtuelle Bereiche handelt, die das Listenansicht-Steuerelement zum Anordnen der Elemente verwendet Ein Arbeitsbereich ist kein Fenster und kann keinen sichtbaren Rahmen aufweisen. Standardmäßig weist das Listenansicht-Steuerelement keine Arbeitsbereiche auf. Wenn Sie einen Arbeitsbereich erstellen, können Sie Links, oben oder rechts von den Elementen einen leeren Rahmen erstellen oder eine horizontale Schiebe Leiste anzeigen, wenn es normalerweise keine wäre.

Wenn ein Arbeitsbereich erstellt wird, werden Elemente, die sich innerhalb des Arbeitsbereichs befinden, zu Mitgliedern des Arbeitsbereichs. Wenn ein Element in einen Arbeitsbereich verschoben wird, wird das Element ebenso zu einem Member dieses Arbeitsbereichs. Wenn ein Element nicht in einem Arbeitsbereich vorhanden ist, wird es automatisch zu einem Member des ersten Arbeitsbereichs (Index 0). Wenn Sie ein neues Element in einem bestimmten Arbeitsbereich platzieren möchten, müssen Sie zuerst das Element erstellen und dann entweder die LVM-" [**\_ stitemposition**](lvm-setitemposition.md) " oder die [**LVM- \_ SETITEMPOSITION32**](lvm-setitemposition32.md) -Nachricht verwenden, um es in den gewünschten Arbeitsbereich zu verschieben.

Die folgende Abbildung ist ein Beispiel für ein Listenansicht-Steuerelement, das vier Arbeitsbereiche enthält, die jeweils in einem anderen Quadranten des Client Bereichs enthalten sind.

![Screenshot eines Listenansicht-Steuer Elements mit einem Arbeitsbereich in jedem Quadrant des Client Bereichs](images/working.jpg)

Es können mehrere Arbeitsbereiche verwendet werden, um unterschiedliche Bereiche innerhalb einer Ansicht zu erstellen. Sie können Bereiche in einer einzelnen Ansicht erstellen, die unterschiedliche Bedeutungen haben. Beispielsweise kann eine Ansicht eines Dateisystems einen Bereich für Dateien mit Lese-/Schreibzugriff und einen anderen Bereich für schreibgeschützte Dateien enthalten. Der Benutzer kann Elemente kategorisieren, indem er Sie in unterschiedlichen Arbeitsbereichen platziert. Wenn eine Datei in den schreibgeschützten Bereich verschoben wird, wird Sie automatisch schreibgeschützt.

Mehrere Arbeitsbereiche können sich überschneiden, aber alle Elemente, die sich innerhalb der Schnittmenge befinden, werden zu Mitgliedern des Bereichs mit dem unteren Index. Daher ist es am besten, diese Situation zu vermeiden. Beim Sortieren mehrerer Arbeitsbereiche werden die Elemente im Vergleich zu den anderen Elementen im gleichen Arbeitsbereich sortiert.

Die Anzahl der Arbeitsbereiche kann mit der Nachricht [**LVM \_ getnumofworkareas**](lvm-getnumberofworkareas.md) abgerufen werden. Die Arbeitsbereiche werden mit der " [**LVM \_ setworkareas**](lvm-setworkareas.md) "-Nachricht geändert und können mit der Nachricht " [**LVM \_ getworkareas**](lvm-getworkareas.md) " abgerufen werden. Beide Nachrichten übernehmen die Adresse eines Arrays von [**Rect**](/previous-versions//dd162897(v=vs.85)) -Strukturen als *LPARAM* und die Anzahl der **Rect** -Strukturen als *wParam*. Der **linke** und der **obere** Member dieser Strukturen geben die Koordinaten der oberen linken Ecke (des Ursprungs) des Arbeitsbereichs an, und der **Rechte** und **untere** Member geben die rechte untere Ecke des Arbeitsbereichs an. Alle Koordinaten befinden sich in den Client Koordinaten der Listenansicht. Die maximal zulässige Anzahl von Arbeitsbereichen wird durch den Wert für die maximale Arbeits **\_ \_ Bereiche von LV** definiert.

Das Ändern des Arbeitsbereichs hat keine Auswirkungen auf Listenansicht-Steuerelemente, die über die [**LVS- \_ Liste**](list-view-window-styles.md) oder die [**LVS- \_ Berichts**](list-view-window-styles.md) Ansicht verfügen, aber die Arbeitsbereiche bleiben erhalten, wenn der Ansichtstyp geändert wird. Mit dem [**LVS- \_ Symbol**](list-view-window-styles.md) und den [**LVS \_ SmallIcon**](list-view-window-styles.md) -Sichten kann der Arbeitsbereich geändert werden, um die Art und Weise zu ändern, in der die Elemente angezeigt werden. Wenn die Breite des Arbeitsbereichs (rechtsbündig) größer als die Client Breite des Steuer Elements ist, werden die Elemente an diese Breite umschließt, und die horizontale Schiebe Leiste wird angezeigt. Wenn die Breite des Arbeitsbereichs schmaler ist als die Breite des Client Bereichs des Steuer Elements, werden die Elemente in den Arbeitsbereich und nicht in den Client Bereich umschließt. Wenn Sie den **linken** oder **oberen** Member auf einen positiven Wert festlegen, werden die Elemente beginnend mit dem Arbeitsbereich angezeigt, und es wird ein leerer Bereich zwischen dem Rand des Steuer Elements und den Elementen erstellt. Ein leerer Bereich kann auch zwischen dem rechten Rand des Steuer Elements und den Elementen erstellt werden, indem die Breite des Arbeitsbereichs kleiner ist als die Client Breite des Steuer Elements.

## <a name="list-view-image-lists"></a>List-View Bildlisten

Standardmäßig werden von einem Listenansicht-Steuerelement keine Element Bilder angezeigt. Zum Anzeigen von Element Bildern müssen Sie Bildlisten erstellen und Sie dem Steuerelement zuordnen. Ein Listenansicht-Steuerelement kann drei Bildlisten aufweisen:

-   Eine Bildliste mit Symbolen in voller Größe, die angezeigt werden, wenn sich das Steuerelement in der Symbol Ansicht befindet.
-   Eine Bildliste, die kleine Symbole enthält, die angezeigt werden, wenn sich das Steuerelement in der kleinen Symbol Ansicht, der Listenansicht oder der Berichtsansicht befindet.
-   Eine Bildliste mit Zustands Bildern, die auf der linken Seite des Symbols in voller Größe angezeigt werden. Sie können Zustands Bilder, wie z. b. aktivierte und gelöschte Kontrollkästchen, verwenden, um Anwendungs definierte Element Zustände anzugeben. Zustands Bilder werden in der Symbol Ansicht angezeigt, in der kleinen Symbol Ansicht, in der Listenansicht und in der Berichtsansicht.

Die Symbol Listen für Volltext-und kleine Symbole können auch *Überlagerungs Bilder* enthalten, die so entworfen wurden, dass Sie transparent über die Element Symbole gezeichnet werden.

So verwenden Sie Überlagerungs Bilder in einem Listenansicht-Steuerelement:

1.  Mit der [**ImageList-Funktion " \_ SetImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) " können Sie einem Bild einen Überlagerungs Bild Index einem Bild in den Bildlisten der vollzahlige und kleinen Symbole zuweisen. Ein Überlagerungs Bild wird durch einen 1-basierten Index identifiziert.
2.  Sie können einem Element einen Überlagerungs Bild Index zuordnen, wenn Sie das [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) -oder ListView-Objekt " [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) " aufzurufen. Verwenden Sie das [**indexyoverlaymask**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) -Makro, um einen Überlagerungs Bild Index im **State** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur des Elements anzugeben. Sie müssen auch die [**LVIS \_ overlaymask**](list-view-item-states.md) -Bits im **Status Ask** -Member festlegen.

Wenn eine Status Bild Liste angegeben ist, reserviert ein Listenansicht-Steuerelement für ein Zustands Bild links neben dem Symbol des einzelnen Elements Platz.

Um einem Element ein Zustands Bild zuzuordnen, verwenden Sie das [**indexystateimagemask**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) -Makro, um einen Status Bild Index im **State** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur anzugeben. Der Index identifiziert ein Bild in der Zustands Bild Liste des Steuer Elements. Obwohl Bildlisten Indizes NULL-basiert sind, verwendet das-Steuerelement einen einzelnen-basierten Index zur Identifizierung von Zustands Bildern. Ein Status Bild Index von NULL gibt an, dass ein Element kein Status Bild hat.

Wenn ein Listenansicht-Steuerelement zerstört wird, werden standardmäßig die ihm zugewiesenen Bildlisten zerstört. Wenn jedoch ein Listenansicht-Steuerelement den LVS-Stil " [**\_ shareimagelists**](list-view-window-styles.md) " hat, ist die Anwendung für das zerstören der Bildlisten verantwortlich, wenn Sie nicht mehr verwendet werden. Sie sollten diesen Stil angeben, wenn Sie die gleichen Bildlisten mehreren Listenansicht-Steuerelementen zuweisen. Andernfalls können mehr als ein Steuerelement versuchen, dieselbe Bildliste zu zerstören.

## <a name="list-view-items-and-subitems"></a>List-View Elemente und unter Elemente

Jedes Element in einem Listenansicht-Steuerelement verfügt über ein Symbol, eine Bezeichnung, einen aktuellen Zustand und einen Anwendungs definierten Wert. Mithilfe von Listenansicht-Nachrichten können Sie Elemente hinzufügen, ändern und löschen sowie Informationen zu Elementen abrufen.

Jedes Element kann ein *oder mehrere unter* Elemente enthalten. Ein Unterelement ist eine Zeichenfolge, die in der Berichtsansicht in einer Spalte angezeigt wird, die vom Symbol und der Bezeichnung des Elements getrennt ist. Um den Text eines unter Elements anzugeben, verwenden Sie die [**LVM \_**](lvm-setitemtext.md) [**-Nachricht " \_**](lvm-setitem.md) . Alle Elemente in einem Listenansicht-Steuerelement haben die gleiche Anzahl von unter Elementen. Die Anzahl der unter Elemente wird durch die Anzahl der Spalten im Listenansicht-Steuerelement bestimmt. Wenn Sie einem Listenansicht-Steuerelement eine Spalte hinzufügen, geben Sie den zugehörigen untergeordneten Index an.

Die [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur definiert ein Listen Ansichts Element oder Unterelement. Der **iItem** -Member ist der null basierte Index des Elements. Das **iSubItem** -Element ist der einsbasierte Index eines unter Elements oder 0 (null), wenn die Strukturinformationen zu einem Element enthält. Zusätzliche Member geben Text-, Symbol-, Zustands-und Elementdaten des Elements an. *Elementdaten* ist ein von der Anwendung definierter Wert, der einem Listen Ansichts Element zugeordnet ist.

Wenn Sie ein Element zu einem Listenansicht-Steuerelement hinzufügen möchten, verwenden Sie die " [**LVM \_ InsertItem**](lvm-insertitem.md) "-Nachricht, indem Sie die Adresse einer [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur angeben. Bevor Sie mehrere Elemente hinzufügen, können Sie dem Steuerelement eine [**LVM \_**](lvm-setitemcount.md) -Nachricht senden, indem Sie die Anzahl der Elemente angeben, die das Steuerelement letztendlich enthalten soll. Diese Meldung ermöglicht dem Listenansicht-Steuerelement, seine internen Datenstrukturen nur einmal neu zuzuordnen, anstatt jedes Mal, wenn Sie ein Element hinzufügen. Sie können die Anzahl der Elemente in einem Listenansicht-Steuerelement mithilfe der [**LVM \_ GetItemCount**](lvm-getitemcount.md) -Nachricht ermitteln. Wenn Sie einem Listenansicht-Steuerelement eine große Anzahl von Elementen hinzufügen, können Sie den Prozess beschleunigen, indem Sie das Neuzeichnen deaktivieren, bevor Sie die Elemente hinzufügen, und anschließend das Neuzeichnen aktivieren, nachdem die Elemente hinzugefügt wurden. Verwenden Sie die WM-Nachricht, um das erneute zeichnen zu aktivieren und zu deaktivieren. [**\_**](/windows/desktop/gdi/wm-setredraw)

Wenn Sie die Attribute eines Listen Ansichts Elements ändern möchten, verwenden Sie die [**LVM- \_ ltitem**](lvm-setitem.md) -Nachricht, indem Sie die Adresse einer [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur angeben. Der **Mask** -Member dieser Struktur gibt die Element Attribute an, die Sie ändern möchten. Wenn Sie z. b. nur den Text eines Elements oder unter Elements ändern möchten, verwenden Sie die [**LVM \_**](lvm-setitemtext.md) -Nachricht.

Zum Abrufen von Informationen über ein Listen Ansichts Element verwenden Sie die [**LVM \_ GetItem**](lvm-getitem.md) -Nachricht, die die Adresse der einzufüllenden [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur angibt. Der **Mask** -Member dieser-Struktur gibt die Element Attribute an, die abgerufen werden sollen. Um nur den Text eines Elements oder des unter Elements abzurufen, verwenden Sie die [**LVM \_ GetItemText**](lvm-getitemtext.md) -Nachricht.

Zum Löschen eines Listen Ansichts Elements verwenden Sie die [**LVM- \_ DeleteItem**](lvm-deleteitem.md) -Nachricht. Sie können alle Elemente in einem Listenansicht-Steuerelement mithilfe der " [**LVM \_ DeleteAllItems**](lvm-deleteallitems.md) "-Nachricht löschen.

### <a name="list-view-item-states"></a>List-View Element Zustände

Der Zustand eines Elements ist ein Wert, der die Verfügbarkeit des Elements angibt, Benutzeraktionen angibt oder anderweitig den Status des Elements widerspiegelt. Ein Listenansicht-Steuerelement ändert einige Zustands Bits, z. b. wenn der Benutzer ein Element auswählt. In einer Anwendung können andere Zustands Bits geändert werden, um das Element zu deaktivieren oder auszublenden, oder um ein Überlagerungs Bild oder ein Zustands Bild anzugeben. Weitere Informationen zu Überlagerungs Bildern und Zustands Bildern finden Sie unter [List-View Image Lists](#list-view-image-lists).

Der Zustand eines Elements wird vom **State** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur angegeben. Wenn Sie den Zustand eines Elements angeben oder ändern, gibt der **statemask** -Member an, welche Zustands Bits geändert werden müssen. Sie können den Zustand eines Elements ändern, indem Sie die LVM-Nachricht " [**\_ abtitemstate**](lvm-setitemstate.md) " verwenden. Sie können den Zustand eines Elements angeben, wenn Sie es erstellen, oder wenn Sie die zugehörigen Attribute mithilfe der [**LVM \_ -Nachricht**](lvm-setitem.md) "*" ändern. Um den aktuellen Zustand eines Elements zu bestimmen, verwenden Sie die [**LVM \_ GetItemState**](lvm-getitemstate.md) -oder [**LVM \_ GetItem**](lvm-getitem.md) -Nachricht.

Um das Überlagerungs Bild eines Elements festzulegen, muss der **statemask** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur den [**LVIS \_ overlaymask**](list-view-item-states.md) -Wert enthalten, und das statusmember **muss den 1** -basierten Index des Überlagerungs Bilds mit dem [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) -Makro in die linke 8 Bits verschieben. Der Index kann NULL sein, um kein Überlagerungs Bild anzugeben.

Um das Zustands Bild eines Elements festzulegen, muss der **statemask** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur [**den LVIS-Wert \_ stateimagemask**](list-view-item-states.md) enthalten, und das statusmember muss den 1-basierten Index **des Zustands** Bilds mit dem [**indextostateimagemask**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) -Makro auf die linken 12 Bits verschieben. Der Index kann NULL sein, um kein Status Bild anzugeben.

### <a name="callback-items-and-the-callback-mask"></a>Rückrufelemente und die Rückrufmaske

Für alle Elemente speichert ein Listenansicht-Steuerelement in der Regel den Bezeichnungs Text, den Bildlisten Index der Element Symbole und einen Satz von Bitflags für den Zustand des Elements. Sie können Rückruf Elemente definieren oder die Rückruf Maske des Steuer Elements ändern, um anzugeben, dass die Anwendung und nicht das Steuerelement einige oder alle dieser Informationen speichert. Möglicherweise möchten Sie Rückrufe verwenden, wenn Ihre Anwendung einige dieser Informationen speichert.

Ein *Rückruf Element* in einem Listenansicht-Steuerelement ist ein Element, für das die Anwendung den Text-oder Symbol Index speichert, oder beides. Sie können Rückruf Elemente definieren, wenn Sie die [**LVM- \_ InsertItem**](lvm-insertitem.md) -Nachricht senden, um dem Listenansicht-Steuerelement ein Element hinzuzufügen. Wenn die Anwendung den Text für das Element oder das Unterelement speichert, legen Sie den **pszText** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur des Elements auf **LPSTR \_ textcallback** fest. Wenn die Anwendung den Symbol Index für ein Element speichert, legen Sie den **iImage** -Member der **lvitem** -Struktur des Elements auf " **\_ imagecallback**" fest.

Bei der *Rückruf Maske* eines Listenansicht-Steuer Elements handelt es sich um einen Satz von Bitflags, die die Element Zustände angeben, für die die Anwendung und nicht das Steuerelement die aktuellen Daten speichert. Die Rückruf Maske gilt für alle Elemente des Steuer Elements, im Gegensatz zur Rückruf Element Bezeichnung, die für ein bestimmtes Element gilt. Die Rückruf Maske ist standardmäßig 0 (null), was bedeutet, dass das Listenansicht-Steuerelement alle Element Zustandsinformationen speichert. Nachdem Sie ein Listenansicht-Steuerelement erstellt und seine Elemente initialisiert haben, können Sie die [**LVM- \_ SetCallbackMask**](lvm-setcallbackmask.md) -Nachricht senden, um die Rückruf Maske zu ändern. Um die aktuelle Rückruf Maske abzurufen, senden Sie die [**LVM \_ GetCallbackMask**](lvm-getcallbackmask.md) -Nachricht.

Wenn ein Listenansicht-Steuerelement ein Listen Ansichts Element anzeigen oder sortieren muss, für das die Anwendung Rückruf Informationen speichert, sendet das Steuerelement den [LVN \_ getdispinfo](lvn-getdispinfo.md) -Benachrichtigungs Code an das übergeordnete Fenster des Steuer Elements. Diese Meldung gibt eine [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur an, die den Typ der erforderlichen Informationen enthält und das Element oder Unterelement identifiziert, das abgerufen werden soll. Das übergeordnete Fenster muss LVN \_ getdispinfo verarbeiten, um die angeforderten Daten bereitzustellen.

Wenn das Listenansicht-Steuerelement eine Änderung in den Rückruf Informationen eines Elements erkennt, z. b. eine Änderung der Text-, Symbol-oder Zustandsinformationen, sendet das Steuerelement einen [LVN \_ setdispinfo](lvn-setdispinfo.md) -Benachrichtigungs Code, um Sie über die Änderung zu benachrichtigen.

Wenn Sie die Attribute oder Zustands Bits eines Rückruf Elements ändern, verwenden Sie die [**LVM- \_ Update**](lvm-update.md) Nachricht, um das Steuerelement zu zwingen, das Element neu zu zeichnen. Diese Meldung bewirkt auch, dass das Steuerelement seine Elemente anordnet, wenn es den [**LVS \_ AutoArrange**](list-view-window-styles.md) -Stil hat. Sie können die [**LVM \_ RedrawItems**](lvm-redrawitems.md) -Nachricht verwenden, um einen Bereich von Elementen neu zu zeichnen, indem Sie die entsprechenden Teile des Client Bereichs des Listenansicht-Steuer Elements für ungültig erklären.

Durch die effektive Verwendung von Rückruf Elementen und der Rückruf Maske können Sie sicherstellen, dass jedes Element Attribut an nur einem Ort beibehalten wird. Dies kann die Anwendung vereinfachen, aber der einzige Speicherplatz ist der Speicher, der andernfalls zum Speichern von Element Bezeichnungen und untergeordneten Text benötigt wird.

### <a name="list-view-item-position"></a>Position des List-View Elements

Jedes Listen Ansichts Element hat eine Position und Größe, die Sie mithilfe von Nachrichten abrufen und festlegen können. Sie können auch bestimmen, welches Element ggf. an einer bestimmten Position liegt. Die Position von Listen Ansichts Elementen wird in *Ansichts Koordinaten* angegeben, bei denen es sich um Client Koordinaten handelt, die von der Scrollposition abgeglichen werden.

Um die Position eines Elements abzurufen und festzulegen, verwenden Sie die [**LVM- \_ getitemposition**](lvm-getitemposition.md) -und [**LVM \_ setitemposition**](lvm-setitemposition.md) -Meldungen. **LVM \_ "Getitemposition** " funktioniert für alle Sichten, " **LVM \_** -" "" ist jedoch nur für Symbol Ansichten und kleine Symbole geeignet.

Mithilfe der Nachricht [**LVM \_ HitTest**](lvm-hittest.md) können Sie feststellen, welches Element ggf. an einem bestimmten Speicherort vorhanden ist.

Zum Abrufen des umgebenden Rechtecks für ein Listenelement oder nur für das Symbol oder die Bezeichnung verwenden Sie die [**LVM- \_ GetItemRect**](lvm-getitemrect.md) -Nachricht.

### <a name="arranging-sorting-and-finding-items"></a>Anordnen, Sortieren und suchen von Elementen

Mithilfe von Listenansicht-Nachrichten können Sie Elemente anordnen und Sortieren und nach Elementen auf der Grundlage ihrer Attribute oder Positionen suchen. Anordnen von Elementen zum Ausrichten an einem Raster, aber die Indizes der Elemente werden nicht geändert. Beim Sortieren wird die Reihenfolge der Elemente (und ihre entsprechenden Indizes) geändert und entsprechend neu positioniert. Sie können Elemente nur in Symbol Ansichten und kleinen Symbolen anordnen, aber Sie können Elemente in einer beliebigen Ansicht Sortieren. Um Elemente zu suchen, senden Sie Listen Ansichts Meldungen, die einen Element Speicherort oder eine Element Eigenschaft angeben.

Verwenden Sie zum Anordnen von Elementen die [**LVM- \_ Anordnungs**](lvm-arrange.md) Nachricht. Sie können sicherstellen, dass Elemente zu allen Zeitpunkten angeordnet werden, indem Sie den LVS-Fenster Stil für [**\_ Automatische Anordnung**](list-view-window-styles.md) angeben.

Verwenden Sie zum Sortieren von Elementen die LVM-Meldung " [**\_ seltems**](lvm-sortitems.md) ". Wenn Sie mit dieser Meldung sortieren, geben Sie eine Anwendungs definierte Rückruffunktion an, die vom Listenansicht-Steuerelement aufgerufen wird, um die relative Reihenfolge von zwei Elementen zu vergleichen. Das-Steuerelement übergibt die Elementdaten, die den einzelnen beiden Elementen zugeordnet sind, an die Vergleichsfunktion. Die Elementdaten sind der Wert, der im **LPARAM** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur des Elements angegeben wurde, als Sie in die Liste eingefügt wurde. Durch die Angabe der entsprechenden Elementdaten und die Bereitstellung einer geeigneten Vergleichsfunktion können Sie Elemente anhand ihrer Bezeichnung, eines beliebigen unter Elements oder einer beliebigen anderen Eigenschaft sortieren. Beachten Sie, dass das Sortieren von Elementen die entsprechenden unter Elemente nicht neu anordnen kann. Wenn Elemente neu angeordnet werden, werden die entsprechenden unter Elemente mit Ihnen übertragen. Das heißt, ganze Zeilen werden zusammengehalten. Wenn Sie die Spalten getrennt voneinander sortieren und die unter Elemente von ihren Elementen trennen möchten, müssen Sie die Spalten nach dem Sortieren mit [**LVM \_**](lvm-setitem.md)-Element neu generieren.

Sie können sicherstellen, dass ein Listenansicht-Steuerelement immer sortiert wird, indem Sie den [**LVS \_ SortAscending**](list-view-window-styles.md) -oder [**LVS \_ sortabsteig**](list-view-window-styles.md) enden Fenster Stil angeben. Steuerelemente mit diesen Stilen verwenden den Beschriftungs Text der Elemente, um Sie in aufsteigender oder absteigender Reihenfolge zu sortieren. Sie können keine Vergleichsfunktion angeben, wenn Sie diese Fenster Stile verwenden. Wenn ein Listenansicht-Steuerelement einen dieser Stile hat, schlägt eine [**LVM- \_ InsertItem**](lvm-insertitem.md) -Nachricht fehl, wenn Sie versuchen, ein Element einzufügen, das **LPSTR \_ textcallback** als **pszText** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur hat.

Sie können ein Listen Ansichts Element mit bestimmten Eigenschaften suchen, indem Sie die [**LVM \_ FindItem**](lvm-finditem.md) -Nachricht verwenden. Sie können ein Listen Ansichts Element suchen, das sich in einem angegebenen Zustand befindet und über eine angegebene Beziehung zu einem angegebenen Element verfügt, indem Sie die [**LVM \_ GetNextItem**](lvm-getnextitem.md) -Nachricht verwenden. Sie können z. b. das nächste ausgewählte Element rechts neben einem angegebenen Element abrufen.

## <a name="list-view-columns"></a>List-View Spalten

Spalten steuern die Art und Weise, in der Elemente und deren unter Elemente in der Berichtsansicht angezeigt werden. Jede Spalte hat einen Titel und eine Breite und ist einem bestimmten Unterelement zugeordnet. Unterelement Zero ist das Symbol und die Bezeichnung des Elements. Die Attribute einer Spalte werden durch eine [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) -Struktur definiert.

Verwenden Sie zum Hinzufügen einer Spalte zu einem Listenansicht-Steuerelement die [**LVM- \_ InsertColumn**](lvm-insertcolumn.md) -Nachricht. Um eine Spalte zu löschen, verwenden Sie die " [**LVM \_ deleteColumn**](lvm-deletecolumn.md) "-Nachricht.

> [!Note]  
> Das Löschen der Spalte NULL eines Listenansicht-Steuer Elements wird nur in ComCtl32.dll Version 6 und höher unterstützt. Version 5 unterstützt auch das Löschen von Spalten NULL, aber erst nach der Verwendung von [**ccm \_ setVersion**](ccm-setversion.md) , um die Version auf 5 oder höher festzulegen. Versionen vor Version 5 unterstützen das Löschen von Spalten NULL nicht.

 

Sie können die Eigenschaften einer vorhandenen Spalte abrufen und ändern, indem Sie die [**LVM \_ GetColumn**](lvm-getcolumn.md) -und [**LVM \_ SetColumn**](lvm-setcolumn.md) -Meldungen verwenden. Um die Breite einer Spalte abzurufen oder zu ändern, verwenden Sie die LVM-Nachrichten " [**\_ getColumnWidth**](lvm-getcolumnwidth.md) " und " [**LVM \_ setcolumnwidth**](lvm-setcolumnwidth.md) ".

Die Spaltenüberschriften werden in der Berichtsansicht angezeigt, es sei denn, der [**LVS \_ nocolumnheader**](list-view-window-styles.md) -Fenster Stil ist angegeben. Der Benutzer kann auf eine Spaltenüberschrift klicken, wodurch ein [**LVN- \_ ColumnClick**](lvn-columnclick.md) -Benachrichtigungs Code an das übergeordnete Fenster gesendet wird. In der Regel sortiert das übergeordnete Fenster das Listenansicht-Steuerelement nach der angegebenen Spalte, wenn dieser Klick auftritt. Der Benutzer kann auch die Spalten Handbücher zwischen den Headern ziehen, um die Spalten zu verkleinern.

Listenansicht-Steuerelemente können Bilder neben Spalten Titeln anzeigen. Um dieses Feature zu implementieren, geben Sie den Wert des **lvcf- \_ Bilds** an, und weisen Sie den Index des Bilds dem **iImage** -Member in der Struktur " [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) " zu

Listenansicht-Steuerelemente können die Reihenfolge festlegen, in der Spalten angezeigt werden. Um dieses Feature zu implementieren, geben Sie den " **lvcf"- \_ Reihen** folgen Wert an, und weisen Sie die Spaltenreihenfolge dem **iorder** -Member in [**der Struktur "**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) Die Spaltenreihenfolge ist NULL basiert und befindet sich in der Reihenfolge von links nach rechts. Beispielsweise gibt 0 (null) die Spalte ganz links an.

## <a name="list-view-scroll-position"></a>List-View Scrollposition

Wenn der Stil des [**LVS- \_ NoScroll**](list-view-window-styles.md) -Fensters nicht angegeben wird, kann ein Listenansicht-Steuerelement gescrollt werden, um mehr Elemente anzuzeigen, als in den Client Bereich des Steuer Elements passen. Sie können die Scrollposition eines Listenansicht-Steuer Elements und zugehörige Informationen abrufen, einen Bildlauf in einem Listenansicht-Steuerelement durch einen angegebenen Betrag durchführen oder einen Bildlauf durch ein Listenansicht-Steuerelement durchführen, sodass ein angegebenes Listenelement

In der Symbol Ansicht oder in der kleinen Symbol Ansicht wird die aktuelle Bild Lauf Position durch den *Ursprung der Sicht* definiert. Der Ansichts Ursprung ist der Satz von Koordinaten, der relativ zum sichtbaren Bereich des Listenansicht-Steuer Elements ist, das den Ansichts Koordinaten (0,0) entspricht. Um den aktuellen Ansichts Ursprung abzurufen, verwenden Sie die [**LVM \_ getorigin**](lvm-getorigin.md) -Nachricht. Diese Meldung sollte nur in der Symbol Ansicht oder in der kleinen Symbol Ansicht verwendet werden. Es wird ein Fehler in der Listen-oder Berichtsansicht zurückgegeben.

In der Listen-oder Berichtsansicht wird die aktuelle Bild Lauf Position durch den *obersten Index* definiert. Der oberste Index ist der Index des ersten sichtbaren Elements im Listenansicht-Steuerelement. Verwenden Sie die [**\_ gettopindex**](lvm-gettopindex.md) -Nachricht LVM, um den aktuellen obersten Index abzurufen. Diese Meldung gibt ein gültiges Ergebnis nur in der Listen-oder Berichtsansicht zurück. in der Symbol Ansicht oder in der kleinen Symbol Ansicht wird NULL zurückgegeben.

Sie können die [**LVM \_ GetViewRect**](lvm-getviewrect.md) -Nachricht verwenden, um das umgebende Rechteck aller Elemente in einem Listenansicht-Steuerelement relativ zum sichtbaren Bereich des Steuer Elements abzurufen.

Die [**LVM \_ getseetperpage**](lvm-getcountperpage.md) -Meldung gibt die Anzahl der Elemente zurück, die auf eine Seite des Listenansicht-Steuer Elements passen. Diese Meldung gibt ein gültiges Ergebnis nur in der Listen-und Berichtsansicht zurück. in Symbol Ansichten und kleinen Symbolen wird die Gesamtzahl der Elemente zurückgegeben.

Um einen Bildlauf in einem Listenansicht-Steuerelement zu einem bestimmten Betrag durchführen zu können, verwenden Sie die [**LVM \_**](lvm-scroll.md) - Mithilfe der [**LVM \_ EnsureVisible**](lvm-ensurevisible.md) -Nachricht können Sie ggf. einen Bildlauf durch das Listenansicht-Steuerelement durchführen, um sicherzustellen, dass ein bestimmtes Element sichtbar ist.

## <a name="list-view-label-editing"></a>Bearbeitung der List-View Bezeichnung

Ein Listenansicht-Steuerelement mit dem [**LVS \_ EditLabels**](list-view-window-styles.md) -Fenster Stil ermöglicht es einem Benutzer, Element Bezeichnungen an Ort und Stelle zu bearbeiten. Der Benutzer beginnt mit der Bearbeitung, indem er auf die Bezeichnung eines Elements klickt, das den Fokus besitzt. Alternativ kann eine Anwendung mithilfe der [**LVM- \_ EditLabel**](lvm-editlabel.md) -Nachricht automatisch mit der Bearbeitung beginnen. Das Listenansicht-Steuerelement benachrichtigt das übergeordnete Fenster, wenn die Bearbeitung beginnt und abgebrochen oder abgeschlossen wird. Wenn die Bearbeitung abgeschlossen ist, ist das übergeordnete Fenster für das Aktualisieren der Element Bezeichnung zuständig, falls dies erforderlich ist.

Wenn die Bezeichnungs Bearbeitung beginnt, wird ein [Bearbeitungs Steuer](edit-controls.md) Element erstellt, positioniert und initialisiert. Bevor es angezeigt wird, sendet das Listenansicht-Steuerelement seinen übergeordneten Fenster einen [LVN \_ beginlabeledit](lvn-beginlabeledit.md) -Benachrichtigungs Code. Wenn Sie den Bearbeitungsprozess der Bezeichnung ändern müssen, können Sie einen Handler für diese Benachrichtigung implementieren.

Eine Verwendung für einen [LVN \_ beginlabeledit](lvn-beginlabeledit.md) -Benachrichtigungs Handler besteht darin, zu steuern, welche Bezeichnungen der Benutzer bearbeiten kann. Um die Bezeichnungs Bearbeitung zu verhindern, geben Sie einen Wert ungleich NULL zurück. Zum Anpassen der Bezeichnungs Bearbeitung muss der Benachrichtigungs Handler ein Handle für das Bearbeitungs Steuerelement abrufen, indem er eine [**LVM \_ geteditcontrol**](lvm-geteditcontrol.md) -Nachricht an das Listenansicht-Steuerelement sendet. Sobald Sie über dieses Handle verfügen, können Sie das Bearbeitungs Steuerelement anpassen, indem Sie die üblichen EM \_ xxx-Meldungen senden. Um z. b. die Menge an Text einzuschränken, die ein Benutzer eingeben kann, senden Sie dem Bearbeitungs Steuerelement eine [**EM- \_ Begrenzungs Text**](em-limittext.md) Nachricht. Sie können den Standardtext des Bearbeitungs Steuer Elements mit [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)ändern. Sie können sogar das Bearbeitungs Steuerelement unterteilen, um ungültige Zeichen abzufangen und zu verwerfen.

Wenn die Bezeichnungs Bearbeitung abgebrochen oder abgeschlossen wird, sendet ein Listenansicht-Steuerelement das übergeordnete Fenster an den [LVN \_ endlabeledit](lvn-endlabeledit.md) -Benachrichtigungs Code. Der *LPARAM* -Parameter ist die Adresse einer [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur. Das **Element Element** dieser Struktur ist eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, deren **iItem** -Member das Element identifiziert. Wenn die Bearbeitung abgebrochen wird, ist der **pszText** -Member der **lvitem** -Struktur **null**. Andernfalls ist **pszText** die Adresse des bearbeiteten Texts. Das übergeordnete Fenster ist für die Aktualisierung der Element Bezeichnung zuständig, wenn die neue Bezeichnung beibehalten werden soll.

## <a name="list-view-colors"></a>List-View Farben

Eine Anwendung kann drei Farben für ein Listenansicht-Steuerelement abrufen und festlegen.



| Color                   | Zum Abrufen und Festlegen von Farben verwendete Nachrichten                                                             |
|-------------------------|------------------------------------------------------------------------------------------------------|
| Textfarbe              | [**LVM \_ gettextcolor**](lvm-gettextcolor.md), [ **LVM \_ SetTextColor**](lvm-settextcolor.md)         |
| Farbe des Text Hintergrunds   | [**LVM \_ gettextbkcolor**](lvm-gettextbkcolor.md), [ **LVM \_ settextbkcolor**](lvm-settextbkcolor.md) |
| Hintergrundfarbe des Fensters | [**LVM \_ GetBkColor**](lvm-getbkcolor.md), [ **LVM \_ SetBkColor**](lvm-setbkcolor.md)                 |



 

Um die Darstellung eines Listenansicht-Steuer Elements deutlich zu gestalten, verwenden Sie [nm \_ customdraw (Listenansicht)](nm-customdraw-list-view.md) oder visuelle Stile (siehe [visuelle Stile](themes-overview.md) und [Aktivieren von visuellen Stilen](cookbook-overview.md)).

## <a name="arranging-list-items-by-group"></a>Anordnen von Listenelementen nach Gruppe

Die Gruppierungsfunktionen des Listenansicht-Steuer Elements ermöglichen es Ihnen, logisch verwandte Sätze von Elementen visuell zu gruppieren. Gruppen können basierend auf Element Eigenschaften, Attributen oder anderen Merkmalen erstellt werden. Diese Gruppen werden in der Regel durch einen horizontalen Header, der den Namen der Gruppe enthält, auf dem Bildschirm getrennt. Der folgende Screenshot zeigt gruppierte Elemente.

![Screenshot eines Listenansicht-Steuer Elements mit Hunden in einer Gruppe und Katzen in einer anderen Gruppe](images/lv-groups.png)

Sie verwenden die Struktur " [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ", um Informationen über eine Gruppe, z. b. Kopf-und Fußzeilen Text, den aktuellen Status der Gruppe usw., zu speichern. Die Gruppierungs-API enthält Nachrichten, die es Ihnen ermöglichen, Gruppen und Gruppenelemente durch Hinzufügen von Elementen zu Gruppen, Hinzufügen von Gruppen zu Sichten, Sortieren von Gruppenelementen und Abfragen von Gruppen für die Elementgröße und andere Informationen zu verwalten. Sie können z. b. Anzeige Parameter für jede Gruppe mithilfe der [**ListView-Makros \_ setgroupmetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupmetrics) und [**ListView \_ getgroupmetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupmetrics) festlegen und abrufen.

Die Gruppierung ist in allen Sichten außer der Listenansicht verfügbar. Es ist für Steuerelemente, die über den [**LVS \_**](list-view-window-styles.md) -Besitzer Daten Stil verfügen, nicht verfügbar.

Weitere Informationen finden Sie unter [Verwenden von List-View](using-list-view-controls.md)-Steuerelementen.

## <a name="insertion-marks"></a>Einfügezeichen

Einfügemarkierungen zeigen Benutzer an, in denen gezogene Elemente abgelegt werden. Einfügemarkierungen werden derzeit angezeigt, wenn der Benutzer ein Element in das **Startmenü** oder die Schnellstartleiste zieht. Die Einfügemarke funktioniert auch für Listen, die auf AutoArrange festgelegt sind. Wenn ein Benutzer ein Element an eine Stelle zwischen zwei anderen Elementen zieht, gibt die Einfügemarke die erwartete neue Position des Elements an. Der folgende Screenshot zeigt eine Einfügemarke.

![Screenshot, der eine Einfügemarke anzeigt, wenn eine Datei zwischen zwei anderen in einem Listenansicht-Steuerelement gezogen wird](images/insertmark.png)

Die Einfügemarke-API-Elemente ermöglichen das Platzieren von Einfügemarkierungen durch Bereitstellen von Nachrichten und Flags, die die Treffer Erkennung durchführen, die die Position und Darstellung der Einfügemarke nach Element angeben, und diese Abfrage nach Informationen zur aktuellen Größe und Darstellung der Einfügemarke

## <a name="see-also"></a>Siehe auch

* [Virtual ListView-Steuerelement Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)
