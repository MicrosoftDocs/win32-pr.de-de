---
title: Tabellensteuersteuertyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den Tabellensteuertyp.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den Tabellensteuertyp
- Benutzeroberflächenautomatisierung,Table-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für Den Tabellen-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den Steuerelementtyp "Tabelle"
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Steuerelementtyp "Table"
- Benutzeroberflächenautomatisierung,Ereignisse für den Steuerelementtyp "Tabelle"
- Strukturstrukturen,Tabellensteuertyp
- properties,Table-Steuerelementtyp
- Steuerelementmuster, Tabellensteuertyp
- events,Table-Steuerelementtyp
- Unterstützung für den Tabellensteuertyp
- Table-Steuerelementtyp
- Steuerelementtypen,Struktur für Den Tabellen-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für Den Tabellen-Steuerelementtyp
- Steuerelementtypen,Unterstützung für Table
- Steuerelementtypen, Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0badb06cfc449140162663625f3fa7282f9c1589
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470077"
---
# <a name="table-control-type"></a>Tabellensteuersteuertyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den **Tabellensteuertyp.**

Tabellensteuerelemente enthalten Zeilen und Spalten mit Text und optional Zeilen- und Spaltenüberschriften.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Table-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Tabellensteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung, die sich auf Tabellensteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Tabelle<ul><li>Text (0 oder 1)</li><li>Header (0 oder mehr)</li><li>Verschiedene Steuerelemente (0 oder mehr)</li></ul></li></ul> | <ul><li>Tabelle<ul><li>Text (1 oder mehr)</li><li>Verschiedene Steuerelemente (0 oder mehr)</li></ul></li></ul> | 




 

Wenn ein Tabellensteuer steuerelement Zeilen- oder Spaltenüberschriften enthält, müssen sie in der Steuerelementansicht der Benutzeroberflächenautomatisierung werden. Die Inhaltsansicht muss diese Informationen nicht verfügbar machen, da auf sie mithilfe von [**IUIAutomationTablePattern zugegriffen werden kann.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern)

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren Wert oder Definition für Tabellensteuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebundenen Rechtecks angeklickt werden kann und das Element spezielle Treffertests ausführt, überschreiben Und stellen Sie einen klickbaren Punkt zur Verfügung.                              |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Tabelle**  |                                                                                                                                                                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                   | Siehe Hinweise. | Wenn die Tabelle von anderen Benutzeroberflächenelementen (z. B. von einem Textelement, das die Beschreibung für die Tabelle enthält) mit Anmerkungen versehen ist, sollte die „DescribedBy“-Eigenschaft einen Verweis auf das Automatisierungselement des Textsteuerelements verfügbar machen.           |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Weitere Informationen zum Zweck der Tabelle sollten über diese Eigenschaft verfügbar gemacht werden, wenn sie nicht ausreichend durch die [**Eigenschaft UIA \_ NamePropertyId erläutert**](uiauto-automation-element-propids.md) wird.      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Tabellensteuer steuerelement muss immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung werden.                                                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Tabellensteuer steuerelement muss immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung werden.                                                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn eine statische Textbezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf das Automatisierungselement des Steuerelements verfügbar machen.                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Table-Steuerelementtyp** entspricht. Der Standardwert ist "table" für en-US oder Englisch (USA).                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Das Tabellensteuerfeld ruft in der Regel den Wert für seinen Namen aus einer statischen Textbezeichnung ab. Wenn keine statische Textbezeichnung vorhanden ist, muss das Element eine Name-Eigenschaft zuweisen, die immer verfügbar sein muss, um den Zweck der Tabelle zu erläutern. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von allen Tabellensteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support                     | Notizen                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Erforderlich                    | Da das Tabellensteuerfeld Elemente enthält, die in einem Raster angezeigt werden, unterstützt es immer das [Grid-Steuerelementmuster.](uiauto-implementinggrid.md)                                                                                                                                                    |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Erforderlich mit untergeordneten Objekten | Die inneren Objekte einer Tabelle sollten sowohl das [GridItem-](uiauto-implementinggriditem.md) als auch [das TableItem-Steuerelementmuster](uiauto-implementingtableitem.md) unterstützen. Die Tabelle selbst muss das GridItem- oder TableItem-Steuerelementmuster nur unterstützen, wenn die Tabelle Teil einer anderen Tabelle ist.  |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Erforderlich                    | Dem Tabellensteuer steuerelement können immer Header zugeordnet sein.                                                                                                                                                                                                                       |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Erforderlich mit untergeordneten Objekten | Die inneren Objekte einer Tabelle sollten sowohl das [GridItem-](uiauto-implementinggriditem.md) als auch [das TableItem-Steuerelementmuster](uiauto-implementingtableitem.md) unterstützen. Die Tabelle selbst muss das GridItem- oder TableItem-Steuerelementmuster nicht unterstützen, es sei denn, die Tabelle ist Teil einer anderen Tabelle. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die Tabellensteuerelemente unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




