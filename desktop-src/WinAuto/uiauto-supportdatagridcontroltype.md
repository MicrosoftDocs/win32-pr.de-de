---
title: DataGrid-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den DataGrid-Steuerelementtyp.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den DataGrid-Steuerelementtyp
- Benutzeroberflächenautomatisierung,DataGrid-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den DataGrid-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den DataGrid-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den DataGrid-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den DataGrid-Steuerelementtyp
- Strukturstrukturen, DataGrid-Steuerelementtyp
- Properties, DataGrid-Steuerelementtyp
- Steuerelementmuster, DataGrid-Steuerelementtyp
- Ereignisse, DataGrid-Steuerelementtyp
- Unterstützung für den DataGrid-Steuerelementtyp
- DataGrid-Steuerelementtyp
- Steuerelementtypen, Struktur für den DataGrid-Steuerelementtyp
- Steuerelementtypen, Steuerelementmuster für den DataGrid-Steuerelementtyp
- Steuerelementtypen,Unterstützung für DataGrid
- Steuerelementtypen,DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa37093402fc3c4c195b4b68ecc74652af2d6a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475596"
---
# <a name="datagrid-control-type"></a>DataGrid-Steuerelementtyp

Dieses Thema enthält Informationen zur Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den **DataGrid-Steuerelementtyp.**

Mit dem **DataGrid-Steuerelementtyp** kann ein Benutzer problemlos mit Elementen arbeiten, die Daten oder Automatisierungselemente enthalten, die in Spalten oder Zeilen dargestellt werden. Datenraster-Steuerelemente enthalten Zeilen mit Elementen und Spalten mit Informationen über diese Elemente. Ein Listenansicht-Steuerelement in Windows Vista-Explorer ist ein Beispiel, das den **DataGrid-Steuerelementtyp** unterstützt.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **DataGrid-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Datenrastersteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [DataGrid-Steuerelementtyp – Beispiel](#datagrid-control-type-example)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die datenraster-Steuerelemente betrifft, und beschreibt, was in den einzelnen Ansichten enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>DataGrid<ul><li>Header (0, 1 oder 2)<ul><li>HeaderItem (Anzahl von Spalten oder Zeilen)</li></ul></li><li>DataItem (0 oder mehr; kann in einer Hierarchie strukturiert werden)</li></ul></li></ul> | <ul><li>DataGrid<ul><li>DataItem (0 oder mehr; kann in einer Hierarchie strukturiert werden)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für den **DataGrid-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Hinweise                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umschließenden Rechtecks klickbar ist und das Element spezielle Treffertests durchführt, überschreibt und stellt einen klickbaren Punkt bereit.                                                                                                         |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataGrid** |                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Der Wert dieser Eigenschaft muss immer **TRUE** sein. Dies bedeutet, dass sich das Datenrastersteuerelement immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur befindet.                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Der Wert dieser Eigenschaft muss immer **TRUE sein.** Dies bedeutet, dass das Datenrastersteuerelement immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten sein muss.                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.   | Wenn eine statische Textbezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem **DataGrid-Steuerelementtyp** entspricht. Der Standardwert ist "data grid" für en-US oder Englisch (USA).                                                                                                                                                                      |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Das Datenraster-Steuerelement ruft in der Regel den Wert für seine **Name-Eigenschaft** aus einer statischen Textbezeichnung ab. Wenn keine statische Textbezeichnung vorhanden ist, muss ein Anwendungsentwickler einen Wert für die **Name-Eigenschaft** zuweisen. Der Wert der **Name-Eigenschaft** darf nie der Textinhalt des Bearbeitungssteuerelements sein. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Datenrastersteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support  | Notizen                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Erforderlich | Das Datenraster-Steuerelement selbst unterstützt immer das [Grid-Steuerelementmuster,](uiauto-implementinggrid.md) da die darin enthaltenen Elemente Metadaten enthalten, die in einem Raster angeordnet sind. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depends (Abhängig)  | Die Möglichkeit, im Datenraster zu scrollen, hängt vom Inhalt und davon ab, ob Scrollleisten vorhanden sind.                                                                                       |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depends (Abhängig)  | Die Möglichkeit, das Datenraster auszuwählen, hängt vom Inhalt ab.                                                                                                                           |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Depends (Abhängig)  | Ein Datenraster-Steuerelement, das über einen -Header verfügt, sollte das [Tabellensteuermuster](uiauto-implementingtable.md) unterstützen.                                                                   |



 

Datenelemente im Datenrastercontainer unterstützen mindestens Folgendes:

-   [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) (wenn das Datenraster auswählbar ist)
-   [ScrollItem-Steuerelementmuster](uiauto-implementingscrollitem.md) (wenn das Datenraster scrollbar ist)
-   [GridItem-Steuerelementmuster](uiauto-implementinggriditem.md)
-   [TableItem-Steuerelementmuster](uiauto-implementingtableitem.md) (wenn das Datenraster über einen Header verfügt)

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von Datenrastersteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                        | Hinweise                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                      |                                                                                                                                                          |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                      | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.                                 |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                  | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.                               |
| [**\_UIA-LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| [**UIA \_ MultipleViewCurrentViewPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)             | Wenn das Steuerelement die CurrentView-Eigenschaft des [MultipleView-Steuerelementmusters](uiauto-implementingmultipleview.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)   | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA \_ ScrollHorizontalViewSizePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)           | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)     | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA \_ ScrollVerticallyScrollablePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)       | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA \_ ScrollVerticalViewSizePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)               | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                         |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a>Beispiel für den DataGrid-Steuerelementtyp

Die folgende Abbildung veranschaulicht ein Listenansicht-Steuerelement, das den **DataGrid-Steuerelementtyp** implementiert.

![Screenshot des Listenansicht-Steuerelements mit dem Datagrid-Steuerelementtyp](images/datagridxmpl.jpg)

Die Steuerelementansicht und die Inhaltsansicht der Benutzeroberflächenautomatisierung, die sich auf das Listenansicht-Steuerelement bezieht, werden unten angezeigt. Die Steuerelementmuster für jedes Automatisierungselement sind in Klammern aufgeführt.




| Benutzeroberflächenautomatisierung Struktur – Steuerelementansicht | Benutzeroberflächenautomatisierung Struktur – Inhaltsansicht | 
|-----------------------------------|-----------------------------------|
| DataGrid (Sortieren, Tabelle, Auswahl, Raster)<ul><li>Header<ul><li>HeaderItem „Name“ (Invoke)</li><li>HeaderItem „Änderungsdatum“ (Invoke)</li><li>HeaderItem „Größe“ (Invoke)</li></ul></li><li>Gruppe "Contoso" (TableItem, GridItem, SelectionItem,*Table, Grid*)<ul><li>DataItem "Accounts Receivable.doc" (SelectionItem, Invoke, TableItem,*GridItem*)</li><li>DataItem "Accounts Payable.doc" (SelectionItem, Invoke, TableItem,*GridItem*)</li></ul></li></ul> | DataGrid (Table, Grid, Selection)<ul><li>Gruppe "Contoso" (TableItem, GridItem, SelectionItem,*Table, Grid*)<ul><li>DataItem "Accounts Receivable.doc" (SelectionItem, Invoke, TableItem,*GridItem*)</li><li>DataItem "Accounts Payable.doc" (SelectionItem, Invoke, TableItem,*GridItem*)</li></ul></li></ul> | 




 

\*Das vorherige Beispiel zeigt ein Datenraster, das mehrere Ebenen von Steuerelementen enthält. Das **Steuerelement** Gruppe ("Contoso") enthält zwei **DataItem-Steuerelemente** ("Accounts Receivable.doc" und "Accounts Payable.doc"). Ein **DataGrid** / **GridItem-Paar** ist unabhängig von einem Paar auf einer anderen Ebene. Die **DataItem-Steuerelemente** unter einer Gruppe können auch als  [ListItem-Steuerelementtyp](uiauto-supportlistitemcontroltype.md) verfügbar gemacht werden, sodass sie besser als auswählbare Objekte und nicht als einfache Datenelemente dargestellt werden können. Dieses Beispiel enthält nicht die Unterelemente der gruppierten Datenelemente. Ein weiteres Beispiel für mehrere Ebenen von Steuerelementen finden Sie unter [DataItem-Steuerelementtyp.](uiauto-supportdataitemcontroltype.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




