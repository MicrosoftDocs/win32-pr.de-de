---
title: DataGrid-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den DataGrid-Steuerelement Typen.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung des DataGrid-Steuerelement Typs
- UI-Automatisierung, DataGrid-Steuerelement Typen
- UI-Automatisierung, Baumstruktur für DataGrid-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für den DataGrid-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für DataGrid-Steuerelement Typen
- UI-Automatisierung, Ereignisse für den DataGrid-Steuerelement Typen
- Struktur Strukturen, DataGrid-Steuerelement Typen
- Eigenschaften, DataGrid-Steuerelement Typen
- Steuerelement Muster, DataGrid-Steuerelement Typen
- Ereignisse, DataGrid-Steuerelement Typen
- Unterstützung des DataGrid-Steuerelement Typs
- DataGrid-Steuerelement Typen
- Steuerelement Typen, Baumstruktur für DataGrid-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den DataGrid-Steuerelement Typen
- Steuerelement Typen, Unterstützung für DataGrid
- Steuerelement Typen, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947651"
---
# <a name="datagrid-control-type"></a>DataGrid-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **DataGrid-** Steuerelement Typen.

Mit dem **DataGrid-** Steuer Elementtyp kann ein Benutzer problemlos mit Elementen arbeiten, die in Spalten oder Zeilen dargestellten Daten-oder Automatisierungselemente enthalten. Datenraster-Steuerelemente enthalten Zeilen mit Elementen und Spalten mit Informationen über diese Elemente. Ein Listenansicht-Steuerelement in Windows Vista Explorer ist ein Beispiel, das den **DataGrid-** Steuerelement Typen unterstützt.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **DataGrid-** Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Datenraster-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Beispiel für den DataGrid-Steuerelement Typen](#datagrid-control-type-example)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Datenraster-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Steuerelementansicht</th>
<th>Inhaltsansicht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>DataGrid
<ul>
<li>Header (0, 1 oder 2)
<ul>
<li>HeaderItem (Anzahl von Spalten oder Zeilen)</li>
</ul></li>
<li>DataItem (0 oder mehr; kann in einer Hierarchie strukturiert werden)</li>
</ul></li>
</ul></td>
<td><ul>
<li>DataGrid
<ul>
<li>DataItem (0 oder mehr; kann in einer Hierarchie strukturiert werden)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **DataGrid-** Steuerelement-Typ besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Notizen                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                                                 |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                     |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.                                                                                                         |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **DataGrid** |                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Der Wert dieser Eigenschaft muss immer " **true**" sein. Dies bedeutet, dass das Datenraster-Steuerelement immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur vorliegen muss.                                                                                                                                                      |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Der Wert dieser Eigenschaft muss immer " **true**" sein. Dies bedeutet, dass das Datenraster-Steuerelement immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten sein muss.                                                                                                                                                |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                    |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.   | Wenn eine statische Text Bezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.                                                                                                                                                                                                                      |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem **DataGrid-** Steuerelement Typ entspricht. Der Standardwert ist "Data Grid" für en-US oder Englisch (USA).                                                                                                                                                                      |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Das Datenraster-Steuerelement ruft in der Regel den Wert für seine **Name** -Eigenschaft aus einer statischen Text Bezeichnung ab. Wenn keine statische Text Bezeichnung vorhanden ist, muss ein Anwendungsentwickler einen Wert für die **Name** -Eigenschaft zuweisen. Der Wert der **Name** -Eigenschaft darf nie der Text Inhalt des Bearbeitungs Steuer Elements sein. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Datenraster Steuerelementen unterstützt werden müssen Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support  | Notizen                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Erforderlich | Das Datenraster-Steuerelement selbst unterstützt immer das [Raster](uiauto-implementinggrid.md) -Steuerelement Muster, da die darin enthaltenen Elemente über Metadaten verfügen, die in einem Raster angeordnet sind. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depends (Abhängig)  | Die Möglichkeit, im Datenraster zu scrollen, hängt vom Inhalt und davon ab, ob Scrollleisten vorhanden sind.                                                                                       |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depends (Abhängig)  | Die Möglichkeit, das Datenraster auszuwählen, hängt vom Inhalt ab.                                                                                                                           |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Depends (Abhängig)  | Ein Datenraster-Steuerelement mit einem-Header sollte das [Table](uiauto-implementingtable.md) -Steuerelement Muster unterstützen.                                                                   |



 

Datenelemente im Datenrastercontainer unterstützen mindestens Folgendes:

-   [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster (wenn das Datenraster ausgewählt werden kann)
-   [ScrollItem](uiauto-implementingscrollitem.md) -Steuerelement Muster (wenn das Datenraster scrollfähig ist)
-   [GridItem](uiauto-implementinggriditem.md) -Steuerelement Muster
-   [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster (wenn das Datenraster über einen Header verfügt)

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Datenraster-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                        | Notizen                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                      |                                                                                                                                                          |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                      | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.                                 |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                  | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.                               |
| [**UIA \_ layoutinvalidatedeventid**](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| [**UIA \_ Multipleviewcurrentviewpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die CurrentView-Eigenschaft des [MultipleView](uiauto-implementingmultipleview.md) -Steuerelement Musters unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.   | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.           | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.     | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.       | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.               | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA- \_ Auswahl \_ invalidatedeventid**](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a>Beispiel für den DataGrid-Steuerelement Typen

Die folgende Abbildung veranschaulicht ein Listenansicht-Steuerelement, das den **DataGrid-** Steuerelement Typ implementiert.

![Screenshot des Listenansicht-Steuer Elements mit DataGrid-Steuerelement Typen](images/datagridxmpl.jpg)

Die Steuerelement Ansicht und die Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur, die sich auf das Listenansicht-Steuerelement bezieht, werden unten angezeigt. Die Steuerelementmuster für jedes Automatisierungselement sind in Klammern aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Benutzeroberflächenautomatisierungs-Struktur-Steuerelement Ansicht</th>
<th>Benutzeroberflächenautomatisierungs-Struktur-Inhaltsansicht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DataGrid (Sortieren, Tabelle, Auswahl, Raster)
<ul>
<li>Header
<ul>
<li>Header Item &quot; Name &quot; (aufrufen)</li>
<li>Datum des headertem- &quot; Datums &quot; (aufrufen)</li>
<li>Header Item &quot; size &quot; (aufrufen)</li>
</ul></li>
<li>Group &quot; &quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)
<ul>
<li>DataItem- &quot; Konten Receivable.doc&quot; (SelectionItem, Aufruf, TableItem *, GridItem*)</li>
<li>DataItem- &quot; Konten Payable.doc&quot; (SelectionItem, Aufruf, TableItem *, GridItem*)</li>
</ul></li>
</ul></td>
<td>DataGrid (Table, Grid, Selection)
<ul>
<li>Group &quot; &quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)
<ul>
<li>DataItem- &quot; Konten Receivable.doc&quot; (SelectionItem, Aufruf, TableItem *, GridItem*)</li>
<li>DataItem- &quot; Konten Payable.doc&quot; (SelectionItem, Aufruf, TableItem *, GridItem*)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

\*Das vorangehende Beispiel zeigt ein Datenraster, das mehrere Ebenen von Steuerelementen enthält. Das **Gruppen** Steuerelement ("kontoso") enthält zwei **DataItem** -Steuerelemente ("Accounts Receivable.doc" und "Accounts Payable.doc"). Ein **DataGrid-** / **GridItem** -Paar ist unabhängig von einem Paar auf einer anderen Ebene. Die **DataItem** -Steuerelemente unter einer **Gruppe** können auch als [ListItem](uiauto-supportlistitemcontroltype.md) -Steuer Elementtyp verfügbar gemacht werden, sodass Sie deutlicher als auswählbare Objekte und nicht als einfache Datenelemente dargestellt werden können. Dieses Beispiel enthält nicht die Unterelemente der gruppierten Datenelemente. Ein weiteres Beispiel für mehrere Ebenen von Steuerelementen finden Sie unter [DataItem](uiauto-supportdataitemcontroltype.md) -Steuerelement Typen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




