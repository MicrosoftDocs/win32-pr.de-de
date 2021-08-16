---
title: Informationen zu List-View-Steuerelementen
description: Ein Listenansichtssteuerelement ist ein Fenster, in dem eine Auflistung von Elementen angezeigt wird.
ms.assetid: 163f7778-690c-4166-b0c5-c7be1a03ae98
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8f97059e607595aa944631c739ef38490ce7287879b77c9f9c8dda9c06103dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958493"
---
# <a name="about-list-view-controls"></a>Informationen zu List-View-Steuerelementen

Weitere Informationen finden Sie im Beispiel für das [Steuerelement Virtual listview](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw).

Ein Listenansichtssteuerelement ist ein Fenster, in dem eine Auflistung von Elementen angezeigt wird. Listenansichtssteuerelemente bieten mehrere Möglichkeiten zum Anordnen und Anzeigen von Elementen und sind viel flexibler als einfache [Listenfelder.](list-boxes.md) Beispielsweise können zusätzliche Informationen zu jedem Element in Spalten rechts neben dem Symbol und der Bezeichnung angezeigt werden.

-   [Listenansichtsstile und -ansichten](#list-view-styles-and-views)
    -   [Erweiterte List-View Stile](#extended-list-view-styles)
-   [Virtual List-View Style](#virtual-list-view-style)
    -   [Erstellen eines virtuellen List-View-Steuerelements](#creating-a-virtual-list-view-control)
    -   [Kompatibilitätsprobleme](#compatibility-issues)
    -   [Behandeln von Benachrichtigungscodes für virtuelle List-View-Steuerelement](#handling-virtual-list-view-control-notification-codes)
    -   [Cacheverwaltung](#cache-management)
-   [Listenansicht von Arbeitsbereichen](#list-view-working-areas)
-   [Listenansichtsbildlisten](#list-view-image-lists)
-   [Listenansichtselemente und Unterelemente](#list-view-items-and-subitems)
    -   [Listenansichtselementzustände](#list-view-item-states)
    -   [Rückrufelemente und die Rückrufmaske](#callback-items-and-the-callback-mask)
    -   [Position des Listenansichtselements](#list-view-item-position)
    -   [Anordnen, Sortieren und Suchen von Elementen](#arranging-sorting-and-finding-items)
-   [Listenansichtsspalten](#list-view-columns)
-   [Scrollposition der Listenansicht](#list-view-scroll-position)
-   [Bearbeiten von Listenansichtsbezeichnungen](#list-view-label-editing)
-   [Listenansichtsfarben](#list-view-colors)
-   [Anordnen von Listenelementen nach Gruppe](#arranging-list-items-by-group)
-   [Einfügemarke](#insertion-marks)

## <a name="list-view-styles-and-views"></a>List-View Stile und Ansichten

Listenansichtssteuerelemente können Elemente in fünf verschiedenen Ansichten anzeigen. Der Fensterstil des Steuerelements gibt die Standardansicht an. Zusätzliche Fensterstile geben die Ausrichtung von Elementen und steuerelementspezifischen Features an. In der folgenden Tabelle werden die Ansichten beschrieben.



| Ansichtsname             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Symbolansicht             | Angegeben durch das [**LVS \_ ICON-Fensterformat**](list-view-window-styles.md) oder durch Übergeben des **LV \_ \_ VIEW-SYMBOLS** mit der [**LVM \_ SETVIEW-Meldung.**](lvm-setview.md) Jedes Element wird als Symbol in voller Größe und mit einer Bezeichnung darunter dargestellt. Der Benutzer kann die Elemente an eine beliebige Position im Listenansichtsfenster ziehen.                                                                                                                                                                                                                                         |
| Kleine Symbolansicht       | Wird durch den [**LVS \_ SMALLICON-Fensterstil**](list-view-window-styles.md) oder durch Übergeben von **LV VIEW \_ \_ SMALLICON** mit [**LVM \_ SETVIEW**](lvm-setview.md)angegeben. Jedes Element wird als kleines Symbol mit der Bezeichnung rechts davon angezeigt. Der Benutzer kann die Elemente an eine beliebige Position ziehen.                                                                                                                                                                                                                                                       |
| Listenansicht             | Wird durch das [**LVS \_ LIST-Fensterformat**](list-view-window-styles.md) oder durch Übergeben von **LV VIEW \_ \_ LIST** mit [**LVM \_ SETVIEW angegeben.**](lvm-setview.md) Jedes Element wird als kleines Symbol mit einer Bezeichnung rechts davon angezeigt. Elemente werden in Spalten angeordnet, und der Benutzer kann sie nicht an eine beliebige Position ziehen.                                                                                                                                                                                                                               |
| Berichtsansicht (Details) | Wird durch das [**LVS \_ REPORT-Fensterformat**](list-view-window-styles.md) oder durch Übergeben von **LV VIEW \_ \_ DETAILS** mit [**LVM \_ SETVIEW**](lvm-setview.md)angegeben. Jedes Element wird in einer eigenen Zeile angezeigt, wobei Informationen in Spalten angeordnet sind. Die äußerste linke Spalte ist immer linksbündig ausgerichtet und enthält das kleine Symbol und die Bezeichnung. Nachfolgende Spalten enthalten Unteritems, wie von der Anwendung angegeben. Jede Spalte verfügt über einen Header, es sei denn, Sie geben auch den [**LVS \_ NOCOLUMNHEADER-Fensterstil**](list-view-window-styles.md) an. |
| Neben-/Untereinanderansicht             | **Version 6 und höher.** Wird durch Übergeben von **LV \_ VIEW \_ TILE** mit [**LVM \_ SETVIEW**](lvm-setview.md)angegeben. Jedes Element wird als Symbol in voller Größe mit einer Bezeichnung von einer oder mehreren Zeilen daneben angezeigt.                                                                                                                                                                                                                                                                                                                                                        |



 

In den folgenden Screenshots werden Ansichten verwendet, um verschiedene Mengen von Informationen zu jedem von sieben Haustieren anzuzeigen. Die Ansichten veranschaulichen, wie die Informationen auf Windows Vista angezeigt werden können. Die visuellen Stile für das Steuerelement wurden mithilfe von [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme)auf das Design "Explorer" festgelegt.

Der folgende Screenshot zeigt die Detailansicht.

![Screenshot mit Informationen in fünf Spalten und sieben Zeilen](images/lv-detailsview.png)

Der folgende Screenshot zeigt die Symbolansicht.

![Screenshot, der nur den Namen jedes Haustiers und ein Symbol zeigt, das die Art angibt](images/lv-iconview.png)

Der folgende Screenshot zeigt die Listenansicht.

![Screenshot, der für jedes Haustier ein großes Symbol neben dem Text des Namens, der Brut und des Preises des Haustiers zeigt](images/lv-listview.png)

Der folgende Screenshot zeigt die Kachelansicht.

![Kachelansicht.](images/lv-tileview.png)

Sie können den Ansichtstyp ändern, nachdem Sie ein Listenansicht-Steuerelement erstellt haben. Verwenden Sie zum Abrufen und Ändern des Fensterstils die Funktionen [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) und [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) Verwenden Sie den [**LVS \_ TYPEMASK-Wert,**](list-view-window-styles.md) um die Fensterstile der aktuellen Ansicht zu bestimmen.

Sie können die Anordnung von Elementen in der Symbolansicht oder in der kleinen Symbolansicht steuern, indem Sie entweder das [**LVS \_ ALIGNTOP-Fenster**](list-view-window-styles.md) (Standard) oder das [**LVS \_ ALIGNLEFT-Fensterformat**](list-view-window-styles.md) angeben.

Sie können die Ausrichtung ändern, nachdem Sie ein Listenansicht-Steuerelement erstellt haben. Um die aktuelle Ausrichtung zu bestimmen, verwenden Sie den [**LVS \_ ALIGNMASK-Wert.**](list-view-window-styles.md)

Zusätzliche Fensterstile bieten weitere Optionen, z. B. ob ein Benutzer Bezeichnungen bearbeiten oder mehrere Elemente gleichzeitig auswählen kann. Eine vollständige Liste finden Sie unter [Listenansichtsfensterstile.](list-view-window-styles.md)

### <a name="extended-list-view-styles"></a>Erweiterte List-View Stile

Die erweiterten Listenansicht-Steuerelementstile bieten Optionen wie Kontrollkästchen, flache Scrollleisten, Rasterlinien und hot-tracking. Eine vollständige Liste finden Sie unter [Erweiterte List-View Stile.](extended-list-view-styles.md) Sie greifen nicht auf die gleiche Weise auf erweiterte Listenansichtsstile zu wie auf Standardfensterstile. Sie verwenden die Funktionen [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) und [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) nicht, um erweiterte Stiländerungen vorzunehmen.

Es gibt zwei Meldungen, die Erweiterte Stilinformationen festlegen und abrufen: [**LVM \_ SETEXTENDEDLISTVIEWSTYLE**](lvm-setextendedlistviewstyle.md) und [**LVM \_ GETEXTENDEDLISTVIEWSTYLE.**](lvm-getextendedlistviewstyle.md) Anstatt die Nachrichten explizit zu senden, können Sie die folgenden entsprechenden Makros verwenden: [**ListView \_ SetExtendedListViewStyle,**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)und [**ListView \_ GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle).

## <a name="virtual-list-view-style"></a>Virtual List-View Style

Eine virtuelle Listenansicht ist ein Listenansichtssteuerelement mit dem [**LVS \_ OWNERDATA-Stil.**](list-view-window-styles.md) Dieser Stil ermöglicht es dem Steuerelement, Millionen von Elementen zu verarbeiten, da der Besitzer die Last der Verwaltung von Elementdaten erhält. Dadurch können Sie das virtuelle Listenansichtssteuerelement mit großen Informationsdatenbanken verwenden, in denen bereits bestimmte Methoden für den Datenzugriff vorhanden sind.

Ein virtuelles Listenansichtssteuerelement verwaltet nur sehr wenige Elementinformationen selbst. Mit Ausnahme der Elementauswahl- und Fokusinformationen muss der Besitzer des Steuerelements alle Elementinformationen verwalten. Andere Prozesse fordern Elementinformationen vom Besitzer mithilfe von [LVN \_ GETDISPINFO-Benachrichtigungscodes](lvn-getdispinfo.md) an.

Da diese Art von Listensteuerelement für große Datensätze vorgesehen ist, wird empfohlen, angeforderte Elementdaten zwischenzuspeichern, um die Abrufleistung zu verbessern. Die Listenansicht bietet einen Cachehinweismechanismus, der bei der Optimierung des Caches hilft. Der Hinweis wird in Form eines [LVN \_ ODCACHEHINT-Benachrichtigungscodes](lvn-odcachehint.md) implementiert.

### <a name="creating-a-virtual-list-view-control"></a>Erstellen eines virtuellen List-View-Steuerelements

Sie erstellen virtuelle Listenansichtssteuerelemente mithilfe der [**CreateWindow-**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) und geben den [**LVS \_ OWNERDATA-Fensterstil**](list-view-window-styles.md) als Teil des *dwStyle-Funktionsparameters* an. Dynamisches Wechseln zum und vom **LVS \_ OWNERDATA-Stil** wird nicht unterstützt.

Sie können den [**LVS \_ OWNERDATA-Stil**](list-view-window-styles.md) in Kombination mit den meisten anderen Fensterstilen verwenden, mit Ausnahme des [**LVS \_ SORTASCENDING-**](list-view-window-styles.md) oder [**LVS \_ SORTDESCENDING-Stils.**](list-view-window-styles.md) Alle virtuellen Listenansichtssteuerelemente werden standardmäßig im [**LVS \_ AUTOARRANGE-Stil**](list-view-window-styles.md) verwendet.

Damit Elemente in der Liste angezeigt werden können, müssen Sie zuerst die [**LVM \_ SETITEMCOUNT-Nachricht**](lvm-setitemcount.md) senden, entweder explizit oder mithilfe des [**ListView \_ SetItemCountEx-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex)

Die folgenden Meldungen werden im [**LVS \_ OWNERDATA-Stil**](list-view-window-styles.md) nicht unterstützt: [**LVM \_ ENABLEGROUPVIEW,**](lvm-enablegroupview.md) [**LVM \_ GETITEMTEXT,**](lvm-getitemtext.md) [**LVM \_ SETTILEINFO**](lvm-settileinfo.md)und [**LVM \_ MAPIDTOINDEX**](lvm-mapidtoindex.md).

### <a name="compatibility-issues"></a>Kompatibilitätsprobleme

Alle vier Listenansichtsstile –Symbol, kleines Symbol, Liste und Berichtsansicht – unterstützen den [**LVS \_ OWNERDATA-Stil.**](list-view-window-styles.md) Listenansichtssteuerelemente, die den **LVS \_ OWNERDATA-Stil** haben, speichern keine elementspezifischen Informationen. Daher sind [**LVIS \_ SELECTED**](list-view-item-states.md) und LVIS FOCUSED die einzigen gültigen Elementzustandsflags, die Sie auf ein [**Element anwenden \_ können.**](list-view-item-states.md) Es werden keine anderen Zustandsinformationen gespeichert. Insbesondere behält das Listenansicht-Steuerelement nicht den Zustand oder Überlagerungsbilder für jedes Element bei. Sie können jedoch das Listenansicht-Steuerelement ihre Anwendung nach diesen Bildern abfragen lassen, indem Sie ihr eine [**LVM \_ SETCALLBACKMASK-Nachricht**](lvm-setcallbackmask.md) senden.

Die meisten Listenansicht-Steuerelementmeldungen und die zugehörigen Makros werden vollständig unterstützt. Einige Meldungen haben jedoch Einschränkungen oder werden nicht unterstützt, wenn Sie den [**LVS \_ OWNERDATA-Stil**](list-view-window-styles.md) verwenden. In der folgenden Tabelle sind die betroffenen Meldungen zusammengefasst.



| `Message`                                             | Einschränkung                                                                                                                                                                                                                                                      |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LVM \_ ARRANGE**](lvm-arrange.md)                 | Unterstützt nicht das **\_ LVA-SNAPTOGRID-Format.**                                                                                                                                                                                                                 |
| [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md)   | Legt die Elementanzahl auf 0 (null) fest und löscht alle internen Auswahlvariablen, löscht jedoch keine Elemente. Er gibt einen Benachrichtigungsrückruf aus.                                                                                                           |
| [**LVM \_ DELETEITEM**](lvm-deleteitem.md)           | Wird nur für die Auswahlintegrität unterstützt und löscht kein Element.                                                                                                                                                                                 |
| [**LVM \_ GETITEMSTATE**](lvm-getitemstate.md)       | Gibt nur Fokus- und Auswahlzustände zurück (d. h. die vom Listenansicht-Steuerelement gespeicherten Zustände).                                                                                                                                                                |
| [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md)         | Unterstützt nicht die Suchkriterien **LVNI \_ CUT,** **LVNI \_ HIDDEN** oder **LVNI \_ DROPHILITED.** Alle anderen Kriterien werden unterstützt.                                                                                                                     |
| [**LVM \_ GETWORKAREAS**](lvm-getworkareas.md)       | Wird nicht unterstützt.                                                                                                                                                                                                                                               |
| [**LVM \_ INSERTITEM**](lvm-insertitem.md)           | Wird nur für die Auswahlintegrität unterstützt.                                                                                                                                                                                                                      |
| [**LVM \_ SETITEM**](lvm-setitem.md)                 | Wird nicht unterstützt. Verwenden Sie zum Festlegen des Elementstatus die [**ListView \_ SetItemState-Meldung.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate)                                                                                                                                               |
| [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md)       | Legt die Anzahl der Elemente fest, die derzeit in der Liste enthalten sind. Wenn das Listenansichtssteuerelement eine Benachrichtigung sendet, die Daten für ein Element bis zum maximal festgelegten Wert anfing, muss der Besitzer darauf vorbereitet sein, diese Daten zu liefern. Die Meldungsparameter unterstützen virtuelle Listenansichtssteuerelemente. |
| [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) | Wird nicht unterstützt.                                                                                                                                                                                                                                               |
| [**LVM \_ SETITEMSTATE**](lvm-setitemstate.md)       | Ermöglicht nur das Ändern der Auswahl- und Fokuszustände für das Element.                                                                                                                                                                                          |
| [**LVM \_ SETITEMTEXT**](lvm-setitemtext.md)         | Wird nicht unterstützt. Es liegt in der Verantwortung der Anwendung, die Elementtexte zu verwalten.                                                                                                                                                                            |
| [**LVM \_ SETWORKAREAS**](lvm-setworkareas.md)       | Wird nicht unterstützt.                                                                                                                                                                                                                                               |
| [**LVM \_ SORTITEMS**](lvm-sortitems.md)             | Wird nicht unterstützt. Es liegt in der Verantwortung der Anwendung, die Elemente in der gewünschten Reihenfolge zu präsentieren.                                                                                                                                                             |



 

### <a name="handling-virtual-list-view-control-notification-codes"></a>Behandeln von Benachrichtigungscodes List-View virtuellen Steuerelementen

Listenansichtssteuerelemente im [**LVS \_ OWNERDATA-Format**](list-view-window-styles.md) senden die gleichen Benachrichtigungscodes wie andere Listenansichtssteuerelemente und zwei zusätzliche Steuerelemente: [LVN \_ ODCACHEHINT](lvn-odcachehint.md) und [LVN \_ ODFINDITEM](lvn-odfinditem.md). Im Folgenden finden Sie die gängigsten Benachrichtigungen, die vom Listenansicht-Steuerelement mit **dem LVS \_ OWNERDATA-Stil** gesendet werden.



|      Benachrichtigung                    |     Beschreibung                         |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LVN \_ GETDISPINFO](lvn-getdispinfo.md) | Ein virtuelles Listenansicht-Steuerelement verwaltet nur sehr wenige Elementinformationen. Daher wird häufig der [LVN \_ GETDISPINFO-Benachrichtigungscode](lvn-getdispinfo.md) zum Anfordern von Elementinformationen sendet. Diese Nachricht wird auf die gleiche Weise wie Rückrufelemente in einem Standardlisten-Steuerelement behandelt. Da die Anzahl der vom Steuerelement unterstützten Elemente sehr groß sein kann, verbessert das Zwischenspeichern von Elementdaten die Leistung. Bei der Verarbeitung von LVN GETDISPINFO versucht der Besitzer des Steuerelements zunächst, angeforderte Elementinformationen aus dem Cache zu liefern (weitere Informationen finden Sie \_ unter [Cacheverwaltung](#cache-management)). Wenn das angeforderte Element nicht zwischengespeichert wird, muss der Besitzer darauf vorbereitet sein, die Informationen auf andere Art und Art zur Verfügung zu stellen. |
| [LVN \_ ODCACHEHINT](lvn-odcachehint.md) | Eine virtuelle Listenansicht sendet den [LVN \_ ODCACHEHINT-Benachrichtigungscode,](lvn-odcachehint.md) um die Optimierung des Caches zu unterstützen. Der Benachrichtigungscode stellt inklusive Indexwerte für einen Bereich von Elementen zur Auswahl, die zwischengespeichert werden sollen. Beim Empfang des Benachrichtigungscodes muss der Besitzer darauf vorbereitet sein, den Cache mit Elementinformationen für den angeforderten Bereich zu laden, damit die Informationen sofort verfügbar sind, wenn eine [LVN \_ GETDISPINFO-Nachricht gesendet](lvn-getdispinfo.md) wird.                                                                                                                                                                                                                                   |
| [LVN \_ ODFINDITEM](lvn-odfinditem.md)   | Der [LVN \_ ODFINDITEM-Benachrichtigungscode](lvn-odfinditem.md) wird von einem virtuellen Listenansichtssteuerelement gesendet, wenn das Steuerelement den Besitzer benötigt, um ein bestimmtes Rückrufelement zu finden. Der Benachrichtigungscode wird gesendet, wenn das Listenansicht-Steuerelement schnellen Schlüsselzugriff erhält oder wenn es eine [**LVM \_ FINDITEM-Nachricht empfängt.**](lvm-finditem.md) Suchinformationen werden in Form einer [**LVFINDINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) gesendet, die ein Element der [**NMLVFINDITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) ist. Der Besitzer muss darauf vorbereitet sein, nach einem Element zu suchen, das den vom Listenansicht-Steuerelement angegebenen Informationen entspricht. Der Besitzer gibt den Index des Elements zurück, wenn erfolgreich, oder -1, wenn kein übereinstimmendes Element gefunden wird.               |



 

### <a name="cache-management"></a>Cacheverwaltung

Ein Listenansicht-Steuerelement mit dem [**LVS \_ OWNERDATA-Stil**](list-view-window-styles.md) erzeugt eine große Anzahl von [LVN \_ GETDISPINFO-Benachrichtigungscodes](lvn-getdispinfo.md) und, um die Optimierung des Caches zu unterstützen, eine [LVN \_ ODCACHEHINT-Nachricht.](lvn-odcachehint.md) LVN \_ ODCACHEHINT-Nachrichten enthalten Informationen zu den empfohlenen Elementen, die in den Cache enthalten sein sollen. Diese Nachrichten werden als [**WM \_ NOTIFY-Nachrichten**](wm-notify.md) gesendet, und der *lParam-Wert* wird als Adresse einer [**NMLVCACHEHINT-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) verwendet.

Die [**NMLVCACHEHINT-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) enthält zwei ganzzahlige Member, **iFrom** und **iTo,** die die inklusiven Endpunkte eines Bereichs von Elementen darstellen, die höchstwahrscheinlich benötigt werden. Der Besitzer muss darauf vorbereitet sein, den Cache mit den Elementinformationen für jedes Element innerhalb des empfohlenen Bereichs zu laden.

Das Listensteuerelement benötigt häufig Elementinformationen für das erste Element (Offset 0). Der [LVN \_ ODCACHEHINT-Benachrichtigungscode](lvn-odcachehint.md) enthält möglicherweise nicht immer Element 0, muss aber immer im Cache enthalten sein.

Auf die letzten Elemente in der Liste wird häufig zugegriffen. Daher kann der Besitzer einen zweiten Cache behalten, der die Elemente am Ende der Liste enthält. Der angeforderte Bereich von [LVN \_ ODCACHEHINT](lvn-odcachehint.md) kann mit dem Endcache überprüft werden, um ihn automatisch verfügbar zu machen, anstatt jedes Mal den gleichen Endbereich neu zu laden.

## <a name="list-view-working-areas"></a>List-View von Arbeitsbereichen

Listenansichtssteuerelemente unterstützen Arbeitsbereiche, bei denen es sich um rechteckige virtuelle Bereiche handelt, die das Listenansicht-Steuerelement zum Anordnen seiner Elemente verwendet. Ein Arbeitsbereich ist kein Fenster und kann keinen sichtbaren Rahmen haben. Standardmäßig verfügt das Listenansicht-Steuerelement über keine Arbeitsbereiche. Wenn Sie einen Arbeitsbereich erstellen, können Sie links, oben oder rechts der Elemente einen leeren Rahmen erstellen oder bewirken, dass eine horizontale Scrollleiste angezeigt wird, wenn es normalerweise keinen gibt.

Wenn ein Arbeitsbereich erstellt wird, werden Elemente, die sich innerhalb des Arbeitsbereichs befindet, Zu Mitgliedern des Arbeitsbereichs. Wenn ein Element in einen Arbeitsbereich verschoben wird, wird das Element entsprechend zu einem Element dieses Arbeitsbereichs. Wenn ein Element nicht in einem Bestimmten Bereich liegt, wird es automatisch mitglied des ersten (Index 0)-Arbeitsbereichs. Um ein neues Element in einem bestimmten Arbeitsbereich zu platzieren, müssen Sie zuerst das Element erstellen und dann entweder [**die LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) oder die [**LVM \_ SETITEMPOSITION32-Nachricht**](lvm-setitemposition32.md) verwenden, um es in den gewünschten Arbeitsbereich zu verschieben.

Die folgende Abbildung ist ein Beispiel für ein Listenansicht-Steuerelement, das vier Arbeitsbereiche enthält, die sich jeweils in einem anderen Quadranten des Clientbereichs befinden.

![Screenshot eines Listenansicht-Steuerelements mit einem Arbeitsbereich in jedem Quadranten des Clientbereichs](images/working.jpg)

Mehrere Arbeitsbereiche können verwendet werden, um unterschiedliche Bereiche innerhalb einer Ansicht zu erstellen. Sie können Bereiche in einer einzelnen Ansicht erstellen, die unterschiedliche Bedeutungen haben. Beispielsweise kann eine Ansicht eines Dateisystems einen Bereich für Lese-/Schreibdateien und einen anderen Bereich für schreibgeschützte Dateien enthalten. Der Benutzer kann Elemente kategorisieren, indem er sie in verschiedenen Arbeitsbereichen platziert. Wenn eine Datei in den schreibgeschützten Bereich verschoben wird, wird sie automatisch schreibgeschützt.

Mehrere Arbeitsbereiche können sich überschneiden, aber alle Elemente, die innerhalb der Schnittmenge liegen, werden Elemente des Bereichs mit dem unteren Index. Daher ist es am besten, diese Situation zu vermeiden. Beim Sortieren mehrerer Arbeitsbereiche werden die Elemente im Vergleich zu den anderen Elementen im gleichen Arbeitsbereich sortiert.

Die Anzahl der Arbeitsbereiche kann mit der [**LVM \_ GETNUMBEROFWORKAREAS-Meldung abgerufen**](lvm-getnumberofworkareas.md) werden. Die Arbeitsbereiche werden mit der [**LVM \_ SETWORKAREAS-Nachricht**](lvm-setworkareas.md) geändert und können mit der [**LVM \_ GETWORKAREAS-Nachricht abgerufen**](lvm-getworkareas.md) werden. Beide Nachrichten nehmen die Adresse eines Arrays von [**RECT-Strukturen**](/previous-versions//dd162897(v=vs.85)) als *lParam* und die Anzahl der **RECT-Strukturen** als *wParam an.* Die **linken** und **oberen** Elemente dieser Strukturen geben die Koordinaten der oberen linken Ecke (den Ursprung) des Arbeitsbereichs an, und die **rechten** und **unteren** Elemente geben die untere rechte Ecke des Arbeitsbereichs an. Alle Koordinaten befinden sich in Clientkoordinaten der Listenansicht. Die maximal zulässige Anzahl von Arbeitsbereichen wird durch den **LV \_ MAX \_ WORKAREAS-Wert** definiert.

Das Ändern des Arbeitsbereichs hat keine Auswirkungen auf Listenansichtssteuerelemente, die über die Ansicht [**LVS \_ LIST**](list-view-window-styles.md) oder [**LVS \_ REPORT**](list-view-window-styles.md) verfügen. Die Arbeitsbereiche werden jedoch beibehalten, wenn der Ansichtstyp geändert wird. Mit dem [**\_ LVS-SYMBOL**](list-view-window-styles.md) und den [**LVS \_ SMALLICON-Ansichten**](list-view-window-styles.md) kann der Arbeitsbereich geändert werden, um die Anzeige der Elemente zu ändern. Wenn die Breite des Arbeitsbereichs (rechts – links) größer als die Clientbreite des Steuerelements ist, werden die Elemente bei dieser Breite umschlossen, und die horizontale Bildlaufleiste wird angezeigt. Wenn die Breite des Arbeitsbereichs kleiner als die Breite des Clientbereichs des Steuerelements ist, werden die Elemente innerhalb des Arbeitsbereichs und nicht im Clientbereich umschlossen. Das Festlegen des **linken** oder **oberen** Elements auf einen positiven Wert bewirkt, dass die Elemente ab dem Arbeitsbereich angezeigt werden, wodurch ein leerer Bereich zwischen dem Rand des Steuerelements und den Elementen entsteht. Zwischen dem rechten Rand des Steuerelements und den Elementen kann auch ein leerer Bereich erstellt werden, indem die Breite des Arbeitsbereichs kleiner als die Clientbreite des Steuerelements wird.

## <a name="list-view-image-lists"></a>List-View Bildlisten

Standardmäßig zeigt ein Listenansichtssteuerelement keine Elementbilder an. Um Elementbilder anzuzeigen, müssen Sie Bildlisten erstellen und sie dem Steuerelement zuordnen. Ein Listenansicht-Steuerelement kann drei Bildlisten enthalten:

-   Eine Bildliste mit Symbolen in voller Größe, die angezeigt werden, wenn sich das Steuerelement in der Symbolansicht befindet.
-   Eine Bildliste, die kleine Symbole enthält, die angezeigt werden, wenn sich das Steuerelement in einer kleinen Symbolansicht, Listenansicht oder Berichtsansicht befindet.
-   Eine Bildliste, die Zustandsbilder enthält, die links neben dem Symbol mit voller Größe oder klein angezeigt werden. Sie können Zustandsbilder wie aktivierte und gelöschte Kontrollkästchen verwenden, um anwendungsdefinierte Elementzustände anzugeben. Zustandsbilder werden in der Symbolansicht, in der kleinen Symbolansicht, in der Listenansicht und in der Berichtsansicht angezeigt.

Die Bildlisten mit voller Größe und kleinen Symbolen können auch *Überlagerungsbilder* enthalten, die transparent über die Elementsymbole gezeichnet werden sollen.

So verwenden Sie Überlagerungsbilder in einem Listenansicht-Steuerelement:

1.  Rufen Sie die [**ImageList \_ SetOverlayImage-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) auf, um einem Bild in den Bildlisten mit voller Größe und kleinen Symbolen einen Overlaybildindex zuzuweisen. Ein Überlagerungsbild wird durch einen einsbasierten Index identifiziert.
2.  Sie können einem Element einen Overlaybildindex zuordnen, wenn Sie das [**ListView \_ InsertItem-**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) oder [**ListView \_ SetItem-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) aufrufen. Verwenden Sie das [**INDEXTOOVERLAYMASK-Makro,**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) um einen Überlagerungsbildindex im **Zustandsmember** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) des Elements anzugeben. Sie müssen auch die [**LVIS \_ OVERLAYMASK-Bits**](list-view-item-states.md) im **stateMask-Member** festlegen.

Wenn eine Zustandsbildliste angegeben wird, reserviert ein Listenansicht-Steuerelement links neben dem Symbol jedes Elements Platz für ein Zustandsbild.

Verwenden Sie zum Zuordnen eines Zustandsbilds zu einem Element das [**Makro INDEXTOSTATEIMAGEMASK,**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) um einen Zustandsbildindex im **Zustandsmember** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) anzugeben. Der Index identifiziert ein Bild in der Zustandsbildliste des Steuerelements. Obwohl Bildlistenindizes nullbasiert sind, verwendet das Steuerelement einsbasierte Indizes, um Zustandsbilder zu identifizieren. Ein Zustandsbildindex von 0 (null) gibt an, dass ein Element über kein Zustandsbild verfügt.

Wenn ein Listenansichtssteuerelement zerstört wird, werden standardmäßig die ihm zugewiesenen Bildlisten zerstört. Wenn ein Listenansichtssteuerelement jedoch über den [**LVS \_ SHAREIMAGELISTS-Fensterstil**](list-view-window-styles.md) verfügt, ist die Anwendung dafür verantwortlich, die Bildlisten zu zerstören, wenn sie nicht mehr verwendet werden. Sie sollten diesen Stil angeben, wenn Sie mehreren Listenansichtssteuerelementen die gleichen Bildlisten zuweisen. Andernfalls können mehrere -Steuerelement versuchen, dieselbe Bildliste zu zerstören.

## <a name="list-view-items-and-subitems"></a>List-View Elemente und Unterelemente

Jedes Element in einem Listenansichts-Steuerelement verfügt über ein Symbol, eine Bezeichnung, einen aktuellen Zustand und einen anwendungsdefinierte Wert. Mithilfe von Listenansichtsmeldungen können Sie Elemente hinzufügen, ändern und löschen sowie Informationen zu Elementen abrufen.

Jedes Element kann über mindestens ein *Unterelement verfügen.* Ein Unterelement ist eine Zeichenfolge, die in der Berichtsansicht getrennt vom Symbol und der Bezeichnung des Elements in einer Spalte angezeigt wird. Um den Text eines Unteritems anzugeben, verwenden Sie die [**LVM \_ SETITEMTEXT-**](lvm-setitemtext.md) oder [**LVM \_ SETITEM-Nachricht.**](lvm-setitem.md) Alle Elemente in einem Listenansichtssteuerelement verfügen über die gleiche Anzahl von Unterelementen. Die Anzahl der Unteritems wird durch die Anzahl der Spalten im Listenansichtssteuerelement bestimmt. Wenn Sie einem Listenansichtssteuerelement eine Spalte hinzufügen, geben Sie den zugehörigen Unterelementindex an.

Die [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) definiert ein Listenansichtselement oder Unterelement. Das **iItem-Element** ist der nullbasierte Index des Elements. Der **iSubItem-Member** ist der einsbasierte Index eines Unterelements oder 0 (null), wenn die Struktur Informationen zu einem Element enthält. Zusätzliche Elemente geben den Text, das Symbol, den Zustand und die Elementdaten des Elements an. *Elementdaten* sind ein anwendungsdefinierter Wert, der einem Listenansichtselement zugeordnet ist.

Um einem Listenansichtssteuerelement ein Element hinzuzufügen, verwenden Sie die [**LVM \_ INSERTITEM-Nachricht,**](lvm-insertitem.md) und geben Sie die Adresse einer [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) an. Bevor Sie mehrere Elemente hinzufügen, können Sie dem Steuerelement eine [**LVM \_ SETITEMCOUNT-Nachricht**](lvm-setitemcount.md) senden und die Anzahl der Elemente angeben, die das Steuerelement letztendlich enthalten soll. Diese Meldung ermöglicht es dem Listenansichtssteuerelement, seine internen Datenstrukturen nur einmal und nicht jedes Mal neu zu verteilen, wenn Sie ein Element hinzufügen. Sie können die Anzahl der Elemente in einem Listenansichtssteuerelement mithilfe der [**LVM \_ GETITEMCOUNT-Nachricht**](lvm-getitemcount.md) ermitteln. Wenn Sie einem Listenansichtssteuerelement eine große Anzahl von Elementen hinzufügen, können Sie den Prozess beschleunigen, indem Sie das Neurahen vor dem Hinzufügen der Elemente deaktivieren und dann das Neuzeichnen aktivieren, nachdem die Elemente hinzugefügt wurden. Verwenden Sie die [**WM \_ SETREDRAW-Meldung,**](/windows/desktop/gdi/wm-setredraw) um die Neuzeichnung zu aktivieren und zu deaktivieren.

Verwenden Sie zum Ändern der Attribute eines Listenansichtselements die [**LVM \_ SETITEM-Nachricht,**](lvm-setitem.md) und geben Sie die Adresse einer [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) an. Der **Maskenmember** dieser Struktur gibt die Elementattribute an, die Sie ändern möchten. Verwenden Sie beispielsweise die [**LVM \_ SETITEMTEXT-Nachricht,**](lvm-setitemtext.md) um nur den Text eines Elements oder Unterelements zu ändern.

Verwenden Sie zum Abrufen von Informationen zu einem Listenansichtselement die [**LVM \_ GETITEM-Nachricht,**](lvm-getitem.md) und geben Sie die Adresse der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) an, die ausgefüllt werden soll. Der **Maskenmember** dieser Struktur gibt die abzurufenden Elementattribute an. Verwenden Sie die [**LVM \_ GETITEMTEXT-Nachricht,**](lvm-getitemtext.md) um nur den Text eines Elements oder Unterelements abzurufen.

Um ein Listenansichtselement zu löschen, verwenden Sie die [**LVM \_ DELETEITEM-Meldung.**](lvm-deleteitem.md) Sie können alle Elemente in einem Listenansichtssteuerelement löschen, indem Sie die [**LVM \_ DELETEALLITEMS-Meldung**](lvm-deleteallitems.md) verwenden.

### <a name="list-view-item-states"></a>List-View Elementzustände

Der Zustand eines Elements ist ein Wert, der die Verfügbarkeit des Elements angibt, Benutzeraktionen angibt oder den Status des Elements anderweitig widerspiegelt. Ein Listenansichtssteuerelement ändert einige Zustandsbits, z. B. wenn der Benutzer ein Element auswählt. Eine Anwendung kann andere Zustandsbits ändern, um das Element zu deaktivieren oder auszublenden oder ein Überlagerungsbild oder Zustandsbild anzugeben. Weitere Informationen zu Überlagerungsbildern und Zustandsbildern finden Sie unter [Listenansichtsbildlisten.](#list-view-image-lists)

Der Zustand eines Elements wird vom **Zustandsmember** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) angegeben. Wenn Sie den Zustand eines Elements angeben oder ändern, gibt der **stateMask-Member** an, welche Zustandsbits Sie ändern müssen. Sie können den Zustand eines Elements ändern, indem Sie die [**LVM \_ SETITEMSTATE-Nachricht**](lvm-setitemstate.md) verwenden. Sie können den Zustand eines Elements angeben, wenn Sie es erstellen oder wenn Sie dessen Attribute ändern, indem Sie die [**LVM \_ SETITEM-Nachricht**](lvm-setitem.md) verwenden. Um den aktuellen Zustand eines Elements zu bestimmen, verwenden Sie die [**LVM \_ GETITEMSTATE-**](lvm-getitemstate.md) oder [**LVM \_ GETITEM-Nachricht.**](lvm-getitem.md)

Um das Überlagerungsbild eines Elements festzulegen, muss der **stateMask-Member** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) den [**LVIS \_ OVERLAYMASK-Wert**](list-view-item-states.md) enthalten, und der **Zustandsmember** muss den 1-basierten Index des Überlagerungsbilds enthalten, das mithilfe des [**INDEXTOOVERLAYMASK-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) nach links verschoben wurde. Der Index kann 0 (null) sein, um kein Überlagerungsbild anzugeben.

Um das Zustandsbild eines Elements festzulegen, muss der **stateMask-Member** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) den [**LVIS \_ STATEIMAGEMASK-Wert**](list-view-item-states.md) enthalten, und der **Zustandsmember** muss den 1-basierten Index des Zustandsbilds enthalten, das mithilfe des [**INDEXTOSTATEIMAGEMASK-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) um 12 Bit nach links verschoben wurde. Der Index kann 0 (null) sein, um kein Zustandsbild anzugeben.

### <a name="callback-items-and-the-callback-mask"></a>Rückrufelemente und die Rückrufmaske

Für jedes seiner Elemente speichert ein Listenansichtssteuerelement in der Regel den Bezeichnungstext, den Bildlistenindex der Symbole des Elements und eine Reihe von Bitflags für den Zustand des Elements. Sie können Rückrufelemente definieren oder die Rückrufmaske des Steuerelements ändern, um anzugeben, dass die Anwendung anstelle des Steuerelements einige oder alle dieser Informationen speichert. Möglicherweise möchten Sie Rückrufe verwenden, wenn Ihre Anwendung einige dieser Informationen speichert.

Ein *Rückrufelement* in einem Listenansichtssteuerelement ist ein Element, für das die Anwendung den Text- oder Symbolindex oder beides speichert. Sie können Rückrufelemente definieren, wenn Sie die [**LVM \_ INSERTITEM-Nachricht**](lvm-insertitem.md) senden, um dem Listenansicht-Steuerelement ein Element hinzuzufügen. Wenn die Anwendung den Text für das Element oder Unterelement speichert, legen Sie den **pszText-Member** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) des Elements auf **LPSTR \_ TEXTCALLBACK** fest. Wenn die Anwendung den Symbolindex für ein Element speichert, legen Sie den **iImage-Member** der **LVITEM-Struktur** des Elements auf **I \_ IMAGECALLBACK** fest.

Die *Rückrufmaske* eines Listenansichtssteuerelements ist ein Satz von Bitflags, die die Elementzustände angeben, für die die Anwendung anstelle des Steuerelements die aktuellen Daten speichert. Die Rückrufmaske gilt im Gegensatz zur Rückrufelementbezeichnung, die für ein bestimmtes Element gilt, für alle Elemente des Steuerelements. Die Rückrufmaske ist standardmäßig 0 (null), was bedeutet, dass das Listenansichts-Steuerelement alle Elementzustandsinformationen speichert. Nachdem Sie ein Listenansichtssteuerelement erstellt und dessen Elemente initialisiert haben, können Sie die [**LVM \_ SETCALLBACKMASK-Nachricht**](lvm-setcallbackmask.md) senden, um die Rückrufmaske zu ändern. Um die aktuelle Rückrufmaske abzurufen, senden Sie die [**LVM \_ GETCALLBACKMASK-Nachricht.**](lvm-getcallbackmask.md)

Wenn ein Listenansichtssteuerelement ein Listenansichtselement anzeigen oder sortieren muss, für das die Anwendung Rückrufinformationen speichert, sendet das Steuerelement den [LVN \_ GETDISPINFO-Benachrichtigungscode](lvn-getdispinfo.md) an das übergeordnete Fenster des Steuerelements. Diese Meldung gibt eine [**NMLVDISPINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) an, die den erforderlichen Informationstyp enthält und das abzurufende Element oder Unterelement identifiziert. Das übergeordnete Fenster muss LVN \_ GETDISPINFO verarbeiten, um die angeforderten Daten bereitzustellen.

Wenn das Listenansichtssteuerelement eine Änderung an den Rückrufinformationen eines Elements erkennt, z. B. eine Änderung der Text-, Symbol- oder Statusinformationen, sendet das Steuerelement einen [LVN SETDISPINFO-Benachrichtigungscode, \_ ](lvn-setdispinfo.md) um Sie über die Änderung zu benachrichtigen.

Wenn Sie die Attribute oder Zustandsbits eines Rückrufelements ändern, verwenden Sie die [**LVM \_ UPDATE-Meldung,**](lvm-update.md) um zu erzwingen, dass das Steuerelement das Element neu malt. Diese Meldung bewirkt auch, dass das Steuerelement seine Elemente anordnt, wenn es über den [**LVS \_ AUTOARRANGE-Stil**](list-view-window-styles.md) verfügt. Sie können die [**LVM \_ REDRAWITEMS-Nachricht**](lvm-redrawitems.md) verwenden, um einen Bereich von Elementen neu zu zeichnen, indem Sie die entsprechenden Teile des Clientbereichs des Listenansichtssteuerelements ungültig machen.

Durch die effektive Verwendung von Rückrufelementen und der Rückrufmaske können Sie sicherstellen, dass jedes Elementattribut nur an einem Ort verwaltet wird. Dies kann Ihre Anwendung vereinfachen, aber der einzige gespeicherte Speicherplatz ist der Arbeitsspeicher, der andernfalls zum Speichern von Elementbezeichnungen und Unterelementtext erforderlich wäre.

### <a name="list-view-item-position"></a>List-View Elementposition

Jedes Listenansichtselement verfügt über eine Position und Größe, die Sie mithilfe von Nachrichten abrufen und festlegen können. Sie können auch bestimmen, welches Element sich an einer angegebenen Position befindet, sofern vorhanden. Die Position von Listenansichtselementen wird in *Ansichtskoordinaten* angegeben, bei denen es sich um Clientkoordinaten handelt, die durch die Bildlaufposition versetzt werden.

Verwenden Sie zum Abrufen und Festlegen der Position eines Elements [**die LVM \_ GETITEMPOSITION-**](lvm-getitemposition.md) und [**LVM \_ SETITEMPOSITION-Meldungen.**](lvm-setitemposition.md) **LVM \_ GETITEMPOSITION** funktioniert für alle Ansichten, **ABER LVM \_ SETITEMPOSITION** funktioniert nur für Symbolansichten und kleine Symbolansichten.

Mithilfe der [**\_ LVM-HITTEST-Nachricht**](lvm-hittest.md) können Sie ermitteln, welches Element sich an einem bestimmten Speicherort befindet.

Verwenden Sie die [**LVM \_ GETITEMRECT-Meldung,**](lvm-getitemrect.md) um das umgebundene Rechteck für ein Listenelement oder nur für dessen Symbol oder Bezeichnung abzurufen.

### <a name="arranging-sorting-and-finding-items"></a>Anordnen, Sortieren und Suchen von Elementen

Sie können Listenansichtsmeldungen verwenden, um Elemente zu sortieren und basierend auf ihren Attributen oder Positionen nach Elementen zu suchen. Durch das Anordnen von Neupositionierungselementen, die an einem Raster ausgerichtet sind, ändern sich die Indizes der Elemente nicht. Beim Sortieren wird die Sequenz der Elemente (und die entsprechenden Indizes) geändert und anschließend entsprechend neu positioniert. Sie können Elemente nur in Symbol- und kleinen Symbolansichten anordnen, aber Sie können Elemente in jeder Ansicht sortieren. Um Elemente zu suchen, senden Sie Listenansichtsnachrichten, die einen Elementspeicherort oder eine Eigenschaft angeben.

Verwenden Sie zum Anordnen von Elementen die [**LVM \_ ARRANGE-Nachricht.**](lvm-arrange.md) Sie können sicherstellen, dass Elemente jederzeit angeordnet sind, indem Sie den [**LVS \_ AUTOARRANGE-Fensterstil**](list-view-window-styles.md) angeben.

Verwenden Sie zum Sortieren von Elementen die [**LVM \_ SORTITEMS-Meldung.**](lvm-sortitems.md) Wenn Sie mit dieser Meldung sortieren, geben Sie eine anwendungsdefinierte Rückruffunktion an, die das Listenansichtssteuerelemente aufruft, um die relative Reihenfolge zweier Elemente zu vergleichen. Das -Steuerelement übergibt die Elementdaten, die jedem der beiden Elemente zugeordnet sind, an die Vergleichsfunktion. Die Elementdaten sind der Wert, der beim Einfügen in die Liste im **lParam-Element** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) des Elements angegeben wurde. Indem Sie die entsprechenden Elementdaten angeben und eine entsprechende Vergleichsfunktion angeben, können Sie Elemente nach ihrer Bezeichnung, nach jedem Unterelement oder nach einer anderen Eigenschaft sortieren. Beachten Sie, dass beim Sortieren von Elementen die entsprechenden Unterelemente nicht neu angeordnet werden. Wenn Elemente neu angeordnet werden, werden die entsprechenden Unterelemente mit ihnen ausgeführt. Das heißt, ganze Zeilen werden zusammengehalten. Um die Spalten getrennt voneinander zu sortieren und die Unterelemente von ihren Elementen zu trennen, müssen Sie die Spalten nach dem Sortieren mit [**LVM \_ SETITEM neu generieren.**](lvm-setitem.md)

Sie können sicherstellen, dass ein Listenansicht-Steuerelement immer sortiert wird, indem Sie den [**LVS \_ SORTASCENDING-**](list-view-window-styles.md) oder [**LVS \_ SORTDESCENDING-Fensterstil**](list-view-window-styles.md) angeben. Steuerelemente mit diesen Stilen verwenden den Bezeichnungstext der Elemente, um sie in aufsteigender oder absteigender Reihenfolge zu sortieren. Wenn Sie diese Fensterstile verwenden, können Sie keine Vergleichsfunktion verwenden. Wenn ein Listenansichtssteuerelement über einen dieser Stile verfügt, kann eine [**LVM \_ INSERTITEM-Meldung**](lvm-insertitem.md) nicht angezeigt werden, wenn Sie versuchen, ein Element mit **LPSTR \_ TEXTCALLBACK** als **pszText-Member** seiner [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) hinzuzufügen.

Sie können ein Listenansichtselement mit bestimmten Eigenschaften finden, indem Sie die [**LVM \_ FINDITEM-Meldung**](lvm-finditem.md) verwenden. Mithilfe der [**LVM \_ GETNEXTITEM-Nachricht**](lvm-getnextitem.md) finden Sie ein Listenansichtselement, das sich in einem angegebenen Zustand befindet und über eine angegebene Beziehung zu einem bestimmten Element verfügt. Beispielsweise können Sie das nächste ausgewählte Element rechts neben einem angegebenen Element abrufen.

## <a name="list-view-columns"></a>List-View Spalten

Spalten steuern, wie Elemente und ihre Unterelemente in der Berichtsansicht angezeigt werden. Jede Spalte hat einen Titel und eine Breite und ist einem bestimmten Unterem zugeordnet. Unterelement 0 (null) ist das Symbol und die Bezeichnung des Elements. Die Attribute einer Spalte werden durch eine [**LVCOLUMN-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) definiert.

Um einem Listenansicht-Steuerelement eine Spalte hinzuzufügen, verwenden Sie die [**LVM \_ INSERTCOLUMN-Meldung.**](lvm-insertcolumn.md) Um eine Spalte zu löschen, verwenden Sie die [**LVM \_ DELETECOLUMN-Meldung.**](lvm-deletecolumn.md)

> [!Note]  
> Das Löschen der Spalte 0 eines Listenansicht-Steuerelements wird nur in ComCtl32.dll Version 6 und höher unterstützt. Version 5 unterstützt auch das Löschen der Spalte 0 , jedoch erst, nachdem Sie [**CCM \_ SETVERSION zum**](ccm-setversion.md) Festlegen der Version auf 5 oder höher verwendet haben. Versionen vor Version 5 unterstützen das Löschen der Spalte 0 nicht.

 

Sie können die Eigenschaften einer vorhandenen Spalte mithilfe der [**LVM \_ GETCOLUMN-**](lvm-getcolumn.md) und [**LVM \_ SETCOLUMN-Meldungen**](lvm-setcolumn.md) abrufen und ändern. Verwenden Sie zum Abrufen oder Ändern der Breite einer Spalte [**die MELDUNGEN LVM \_ GETCOLUMNWIDTH**](lvm-getcolumnwidth.md) und [**LVM \_ SETCOLUMNWIDTH.**](lvm-setcolumnwidth.md)

Sofern nicht [**der LVS \_ NOCOLUMNHEADER-Fensterstil**](list-view-window-styles.md) angegeben ist, werden Spaltenüberschriften in der Berichtsansicht angezeigt. Der Benutzer kann auf eine Spaltenüberschrift klicken, wodurch ein [**LVN COLUMNCLICK-Benachrichtigungscode \_**](lvn-columnclick.md) an das übergeordnete Fenster gesendet wird. In der Regel sortiert das übergeordnete Fenster das Listenansicht-Steuerelement nach der angegebenen Spalte, wenn dieser Klick erfolgt. Der Benutzer kann auch die Spaltenführungslinien zwischen den Headern ziehen, um die Spaltengröße zu ändern.

Listenansichtssteuerelemente können Bilder neben Spaltentiteln anzeigen. Um dieses Feature zu implementieren, geben Sie den **LVCF \_ IMAGE-Wert** an, und weisen Sie den Index des Bilds dem **iImage-Member** in der [**LVCOLUMN-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) zu.

Listenansichtssteuerelemente können die Reihenfolge festlegen, in der Spalten angezeigt werden. Um dieses Feature zu implementieren, geben Sie den **LVCF \_ ORDER-Wert** an, und weisen Sie die Spalten reihenfolge dem **iOrder-Member** in der [**LVCOLUMN-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) zu. Die Spalten reihenfolge ist nullbasierte und befindet sich in der Reihenfolge von links nach rechts. Beispielsweise gibt 0 (null) die spalte ganz links an.

## <a name="list-view-scroll-position"></a>List-View Scrollposition

Wenn der [**LVS \_ NOSCROLL-Fensterstil**](list-view-window-styles.md) nicht angegeben ist, kann ein Listenansicht-Steuerelement gescrollt werden, um mehr Elemente anzuzeigen, als in den Clientbereich des Steuerelements passen. Sie können die Bildlaufposition eines Listenansichtssteuerelements und zugehörige Informationen abrufen, ein Listenansichtssteuerelement um einen angegebenen Wert scrollen oder ein Listenansichtssteuerelement scrollen, damit ein angegebenes Listenelement sichtbar ist.

In der Symbolansicht oder kleinen Symbolansicht wird die aktuelle Bildlaufposition durch den Ursprung *der Ansicht definiert.* Der Ansichtsersprung ist der Satz von Koordinaten relativ zum sichtbaren Bereich des Listenansicht-Steuerelements, die den Ansichtskoordinaten (0, 0) entsprechen. Verwenden Sie die [**LVM \_ GETORIGIN-Nachricht,**](lvm-getorigin.md) um den aktuellen Ansichtsersprung abzurufen. Diese Meldung sollte nur in der Symbol- oder kleinen Symbolansicht verwendet werden. Es wird ein Fehler in der Listen- oder Berichtsansicht zurückgegeben.

In der Listen- oder Berichtsansicht wird die aktuelle Bildlaufposition durch den obersten *Index definiert.* Der oberste Index ist der Index des ersten sichtbaren Elements im Listenansicht-Steuerelement. Um den aktuellen obersten Index abzurufen, verwenden Sie die [**LVM \_ GETTOPINDEX-Nachricht.**](lvm-gettopindex.md) Diese Meldung gibt ein gültiges Ergebnis nur in der Listen- oder Berichtsansicht zurück. es gibt 0 (null) in der Symbol- oder kleinen Symbolansicht zurück.

Sie können die [**LVM \_ GETVIEWRECT-Nachricht**](lvm-getviewrect.md) verwenden, um das umgebundene Rechteck aller Elemente in einem Listenansicht-Steuerelement relativ zum sichtbaren Bereich des Steuerelements abzurufen.

Die [**LVM \_ GETCOUNTPERPAGE-Nachricht**](lvm-getcountperpage.md) gibt die Anzahl der Elemente zurück, die in eine Seite des Listenansicht-Steuerelements passen. Diese Meldung gibt nur in Listen- und Berichtsansichten ein gültiges Ergebnis zurück. in Symbolansichten und kleinen Symbolansichten wird die Gesamtzahl der Elemente zurückgegeben.

Verwenden Sie die LVM SCROLL-Meldung, um ein Listenansicht-Steuerelement um einen [**bestimmten \_ Wert zu**](lvm-scroll.md) scrollen. Mithilfe [**der LVM \_ ENSUREVISIBLE-Meldung**](lvm-ensurevisible.md) können Sie im Listenansichtssteuerelement bei Bedarf einen Bildlauf durchführen, um sicherzustellen, dass ein angegebenes Element sichtbar ist.

## <a name="list-view-label-editing"></a>List-View Bezeichnungsbearbeitung

Ein Listenansicht-Steuerelement, das über den [**LVS \_ EDITLABELS-Fensterstil**](list-view-window-styles.md) verfügt, ermöglicht es einem Benutzer, Elementbezeichnungen zu bearbeiten. Der Benutzer beginnt mit der Bearbeitung, indem er auf die Bezeichnung eines Elements klickt, das den Fokus besitzt. Alternativ kann eine Anwendung mit der automatischen Bearbeitung beginnen, indem die [**LVM \_ EDITLABEL-Nachricht verwendet**](lvm-editlabel.md) wird. Das Listenansicht-Steuerelement benachrichtigt das übergeordnete Fenster, wenn die Bearbeitung beginnt und wenn es abgebrochen oder abgeschlossen wird. Wenn die Bearbeitung abgeschlossen ist, ist das übergeordnete Fenster für die Aktualisierung der Bezeichnung des Elements verantwortlich, falls dies erforderlich ist.

Wenn die Bearbeitung von Bezeichnungen beginnt, wird ein [Bearbeitungssteuerzeichen](edit-controls.md) erstellt, positioniert und initialisiert. Bevor es angezeigt wird, sendet das Listenansicht-Steuerelement dem übergeordneten Fenster einen [LVN \_ BEGINLABELEDIT-Benachrichtigungscode.](lvn-beginlabeledit.md) Wenn Sie den Bearbeitungsprozess für Bezeichnungen ändern müssen, können Sie einen Handler für diese Benachrichtigung implementieren.

Eine Verwendung für einen [LVN \_ BEGINLABELEDIT-Benachrichtigungshandler](lvn-beginlabeledit.md) besteht in der Steuerung, welche Bezeichnungen der Benutzer bearbeiten kann. Um die Bearbeitung von Bezeichnungen zu verhindern, geben Sie einen Wert ungleich 0 (null) zurück. Um die Bezeichnungsbearbeitung anzupassen, muss der Benachrichtigungshandler ein Handle für das Bearbeitungssteuerzeichen abrufen, indem eine [**LVM \_ GETEDITCONTROL-Nachricht**](lvm-geteditcontrol.md) an das Listenansicht-Steuerelement gesendet wird. Sobald Sie über dieses Handle verfügen, können Sie das Bearbeitungssteuerzeichen anpassen, indem Sie die üblichen EM \_ XXX-Nachrichten senden. Um beispielsweise die Textmenge zu begrenzen, die ein Benutzer eingeben kann, senden Sie dem Bearbeitungssteuerfeld eine [**EM \_ LIMITTEXT-Nachricht.**](em-limittext.md) Sie können den Standardtext des Bearbeitungssteuerfelds mit [**SetWindowText ändern.**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) Sie können sogar eine Unterklasse des Bearbeitungssteuerzeichens erstellen, um ungültige Zeichen abzufangen und zu verwerfen.

Wenn die Bearbeitung von Bezeichnungen abgebrochen oder abgeschlossen wird, sendet ein Listenansicht-Steuerelement dem übergeordneten Fenster einen [LVN \_ ENDLABELEDIT-Benachrichtigungscode.](lvn-endlabeledit.md) Der *lParam-Parameter* ist die Adresse einer [**NMLVDISPINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) Das **Elementelement** dieser -Struktur ist eine [**LVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvitema) **deren iItem-Member** das Element identifiziert. Wenn die Bearbeitung abgebrochen wird, ist **das pszText-Member** der **LVITEM-Struktur** **NULL.** **andernfalls ist pszText** die Adresse des bearbeiteten Texts. Das übergeordnete Fenster ist für das Aktualisieren der Bezeichnung des Elements verantwortlich, wenn die neue Bezeichnung erhalten bleiben soll.

## <a name="list-view-colors"></a>List-View Farben

Eine Anwendung kann drei Farben für ein Listenansicht-Steuerelement abrufen und festlegen.



| Color                   | Zum Abrufen und Festlegen von Farben verwendete Meldungen                                                             |
|-------------------------|------------------------------------------------------------------------------------------------------|
| Textfarbe              | [**LVM \_ GETTEXTCOLOR**](lvm-gettextcolor.md), [ **LVM \_ SETTEXTCOLOR**](lvm-settextcolor.md)         |
| Hintergrundfarbe für Text   | [**LVM \_ GETTEXTBKCOLOR**](lvm-gettextbkcolor.md), [ **LVM \_ SETTEXTBKCOLOR**](lvm-settextbkcolor.md) |
| Hintergrundfarbe des Fensters | [**LVM \_ GETBKCOLOR**](lvm-getbkcolor.md), [ **LVM \_ SETBKCOLOR**](lvm-setbkcolor.md)                 |



 

Um die Darstellung eines Listenansicht-Steuerelements erheblich anzupassen, verwenden Sie [NM \_ CUSTOMDRAW (Listenansicht)](nm-customdraw-list-view.md) oder visuelle Stile (siehe [Visuelle Stile](themes-overview.md) und Aktivieren von visuellen [Stilen](cookbook-overview.md)).

## <a name="arranging-list-items-by-group"></a>Anordnen von Listenelementen nach Gruppe

Mit den Gruppierungsfeatures des Listenansicht-Steuerelements können Sie logisch verknüpfte Sätze von Elementen visuell gruppieren. Gruppen können basierend auf Elementeigenschaften, Attributen oder anderen Merkmalen erstellt werden. Diese Gruppen werden in der Regel auf dem Bildschirm durch einen horizontalen Header getrennt, der den Namen der Gruppe enthält. Der folgende Screenshot zeigt gruppierte Elemente.

![Screenshot eines Listenansicht-Steuerelements mit Hunden in einer Gruppe und Katzen in einer anderen Gruppe](images/lv-groups.png)

Sie verwenden die [**LVGROUP-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) um Informationen zu einer Gruppe zu speichern, z. B. den Kopf- und Fußzeilentext, den aktuellen Status der Gruppe und so weiter. Die Gruppierungs-API enthält Nachrichten, mit denen Sie Gruppen und Gruppenelemente verwalten können, indem Sie Gruppen Elemente hinzufügen, Ansichten Gruppen hinzufügen, Gruppenelemente sortieren und Gruppen nach Elementgröße und anderen Informationen abfragen. Beispielsweise können Sie anzeigeparameter für jede Gruppe mithilfe der [**Makros ListView \_ SetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupmetrics) und [**ListView \_ GetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupmetrics) festlegen und abrufen.

Die Gruppierung ist in allen Ansichten mit Ausnahme der Listenansicht verfügbar. Es ist nicht für Steuerelemente verfügbar, die den [**LVS \_ OWNERDATA-Stil**](list-view-window-styles.md) haben.

Weitere Informationen finden Sie unter [Verwenden von List-View Steuerelementen.](using-list-view-controls.md)

## <a name="insertion-marks"></a>Einfügemarken

Einfügemarken zeigen Benutzern an, wo gezogene Elemente platziert werden. Einfügemarken werden derzeit angezeigt, wenn der Benutzer ein Element in das **Startmenü** oder die Schnellstart zieht. Die Einfügemarke funktioniert auch für Listen, die auf autoarrange festgelegt sind. Wenn ein Benutzer ein Element an eine Stelle zwischen zwei anderen Elementen zieht, gibt die Einfügemarke die erwartete neue Position des Elements an. Der folgende Screenshot zeigt eine Einfügemarke.

![Screenshot: Einfügemarke beim Ziehen einer Datei zwischen zwei anderen Dateien in einem Listenansicht-Steuerelement](images/insertmark.png)

Die Einfügemarke-API-Elemente ermöglichen die Platzierung von Einfügemarken, indem Meldungen und Flags bereitgestellt werden, die die Treffererkennung ausführen, die Position und Darstellung der Einfügemarke nach Element angeben und informationen zur aktuellen Größe und Darstellung der Einfügemarke abfragen.

## <a name="see-also"></a>Weitere Informationen

* [Beispiel für ein Steuerelement für die virtuelle Listenansicht](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)
