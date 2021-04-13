---
title: Gruppen Steuerungstyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Gruppen Steuerelement-Typ.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für den Steuerelement
- Benutzeroberflächenautomatisierungs, Gruppen Steuerelement-Typ
- Benutzeroberflächen Automatisierung, Struktur für Gruppen Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Gruppen Steuerungstyp
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den Gruppen Steuerungstyp
- Benutzeroberflächenautomatisierungs, Ereignisse für den Gruppen Steuerungstyp
- Struktur Strukturen, Gruppen Steuerelement Typen
- Eigenschaften, Gruppen Steuerelement-Typ
- Steuerelement Muster, Gruppen Steuerelement-Typ
- Ereignisse, Gruppen Steuerelement Typen
- Unterstützung für den Gruppen Steuerungstyp
- Gruppe-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Gruppen Steuerelement-Typ
- Steuerelement Typen, Steuerelement Muster für den Gruppen Steuerungstyp
- Steuerelement Typen, Unterstützung für Gruppe
- Steuerelement Typen, Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b630d0ef736d937e4f024c8131adc4c843b6e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388246"
---
# <a name="group-control-type"></a>Gruppen Steuerungstyp

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Gruppen** Steuerelement-Typ.

Ein Gruppen Steuerelement stellt einen Knoten innerhalb einer Hierarchie dar. Der Steuer Elementtyp " **Group** " erstellt eine Trennung in der Benutzeroberflächenautomatisierungs-Struktur, sodass Elemente, die gruppiert werden, eine logische Division innerhalb der Benutzeroberflächenautomatisierungs-Struktur aufweisen

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Gruppen** Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Gruppen Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen und

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Gruppen Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Gruppieren
<ul>
<li>Beliebig viele Steuerelemente</li>
</ul></li>
</ul></td>
<td><ul>
<li>Gruppieren
<ul>
<li>Beliebig viele Steuerelemente</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Gruppen Steuerelemente enthalten in der Regel Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen, die sich in der Teilstruktur darunter befinden, einschließlich der Steuerelement Typen [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)und [DataItem](uiauto-supportdataitemcontroltype.md) . Da es sich bei einem Gruppen Steuerelement um einen generischen Container handelt, ist es möglich, dass jeder Typ von Steuerelement unter dem Gruppen Steuerelement in der Struktur ist.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Gruppen Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Gruppieren**  |                                                                                                                                                                                                      |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Gruppen Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                  |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Gruppen Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                  |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Gruppensteuerelemente sind in der Regel selbstbezeichnend. In diesen Fällen wird **null** zurückgegeben. Wenn die Gruppe über eine statische Text Bezeichnung verfügt, geben Sie die Bezeichnung als Wert der Eigenschaft " **LabeledBy** " zurück.                      |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die **dem Steuerelement** des Steuer Elements entspricht. Der Standardwert ist "Group" für en-US oder Englisch (USA).                                                                     |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Das Gruppensteuerelement ruft seinen Namen in der Regel aus dem Text ab, mit dem das Steuerelement beschriftet ist.                                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die für den **Gruppen** Steuerelement-Typ unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Gruppen Steuerelemente, die zum Anzeigen oder Ausblenden von Informationen verwendet werden können, müssen das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützen. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Gruppen Steuerelementen unterstützt werden. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                                | Notizen                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                              |                                                                                                                                                  |
| [**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster-Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                              | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.                         |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                          | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.                       |
| [**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                                 | Wenn das Steuerelement das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                 |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




