---
title: Table-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Tabellen Steuerungstyp.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für Tabellen Steuerelement
- Benutzeroberflächenautomatisierungs, Tabellen Steuerungstyp
- UI-Automatisierung, Baumstruktur für den Tabellen Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Tabellen Steuerungstyp
- UI-Automatisierung, Steuerelement Muster für den Tabellen Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Ereignisse für den Tabellen Steuerungstyp
- Baumstrukturen, Tabellen Steuerelement-Typ
- Eigenschaften, Tabellen Steuerelement-Typ
- Steuerelement Muster, Tabellen Steuerelement-Typ
- Ereignisse, Tabellen Steuerelement-Typ
- Unterstützung für den Tabellen Steuerungstyp
- Table-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für den Tabellen Steuerelement-Typ
- Steuerelement Typen, Steuerelement Muster für den Tabellen Steuerelement-Typ
- Steuerelement Typen, Unterstützung für Tabelle
- Steuerelement Typen, Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4ee709bd16156a62882aeee014b4744dab2214
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515926"
---
# <a name="table-control-type"></a>Table-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Tabellen** Steuerungstyp.

Tabellen Steuerelemente enthalten Zeilen und Spalten mit Text und, optional, Zeilen-und Spaltenüberschriften.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Tabellen** Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Table-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung für die Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Table-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Tabelle
<ul>
<li>Text (0 oder 1)</li>
<li>Header (0 oder mehr)</li>
<li>Verschiedene Steuerelemente (0 oder mehr)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Tabelle
<ul>
<li>Text (1 oder mehr)</li>
<li>Verschiedene Steuerelemente (0 oder mehr)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Wenn ein Tabellen Steuerelement über Zeilen-oder Spaltenheader verfügt, müssen diese in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur verfügbar gemacht werden. Die Inhaltsansicht muss diese Informationen nicht verfügbar machen, da Sie mithilfe von [**iuiautomationtablepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern)darauf zugreifen können.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Table-Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                      |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                          |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.                              |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Table**  |                                                                                                                                                                                                                                   |
| [**UIA \_ describedbypropertyid**](uiauto-automation-element-propids.md)                   | Siehe Hinweise. | Wenn die Tabelle von anderen Benutzeroberflächenelementen (z. B. von einem Textelement, das die Beschreibung für die Tabelle enthält) mit Anmerkungen versehen ist, sollte die „DescribedBy“-Eigenschaft einen Verweis auf das Automatisierungselement des Textsteuerelements verfügbar machen.           |
| [**UIA \_ helptextpropertyid**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Weitere Details zum Zweck der Tabelle sollten über diese Eigenschaft verfügbar gemacht werden, wenn Sie von der Eigenschaft [**UIA \_ namepropertyid**](uiauto-automation-element-propids.md) nicht ausreichend erläutert wird.      |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Table-Steuerelement muss immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt werden.                                                                                                                                               |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Table-Steuerelement muss immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt werden.                                                                                                                                               |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                         |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn eine statische Textbezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf das Automatisierungselement des Steuerelements verfügbar machen.                                                                                                                |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Tabellen** Steuerelement-Typ entspricht. Der Standardwert ist "Table" für en-US oder Englisch (USA).                                                                                                  |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Das Table-Steuerelement ruft in der Regel den Wert für seinen Namen aus einer statischen Text Bezeichnung ab. Wenn keine statische Text Bezeichnung vorhanden ist, muss das Element eine Name-Eigenschaft zuweisen, die immer verfügbar sein muss, um den Zweck der Tabelle zu erläutern. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Tabellen Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support                     | Notizen                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Erforderlich                    | Da das Table-Steuerelement Elemente enthält, die in einem Raster dargestellt sind, unterstützt es immer das [Raster](uiauto-implementinggrid.md) -Steuerelement Muster.                                                                                                                                                    |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Erforderlich für untergeordnete Objekte | Die inneren Objekte einer Tabelle sollten sowohl das [GridItem](uiauto-implementinggriditem.md) -Steuerelement als auch das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster unterstützen. Die Tabelle selbst muss das GridItem-oder TableItem-Steuerelement Muster nicht unterstützen, es sei denn, die Tabelle ist Teil einer anderen Tabelle.  |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Erforderlich                    | Das Table-Steuerelement kann immer über Header verfügen, die dem Inhalt zugeordnet sind.                                                                                                                                                                                                                       |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Erforderlich für untergeordnete Objekte | Die inneren Objekte einer Tabelle sollten sowohl das [GridItem](uiauto-implementinggriditem.md) -Steuerelement als auch das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster unterstützen. Die Tabelle selbst muss das GridItem- oder TableItem-Steuerelementmuster nicht unterstützen, es sei denn, die Tabelle ist Teil einer anderen Tabelle. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Tabellen Steuerelementen Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




