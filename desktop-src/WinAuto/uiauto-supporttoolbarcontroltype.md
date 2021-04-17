---
title: ToolBar-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuerelement-Steuerelement-Typ Symbolleisten-Steuerelemente ermöglichen Endbenutzern das Aktivieren von Befehlen und Tools, die in einer Anwendung enthalten sind.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für Steuerelement Typen
- UI-Automatisierung, Symbolleisten-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Struktur für Symbolleisten-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für Symbolleisten-Steuerelement
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den ToolBar-Steuerelement
- Benutzeroberflächenautomatisierungs, Ereignisse für ToolBar-Steuerelement Typen
- Struktur Strukturen, Symbolleisten-Steuerelement Typen
- Eigenschaften, Symbolleisten-Steuerelement Typen
- Steuerelement Muster, Symbolleisten-Steuerelement Typen
- Ereignisse, Symbolleisten-Steuerelement Typen
- Unterstützung für Symbolleisten-Steuerelement
- ToolBar-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Symbolleisten-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für ToolBar-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Symbolleiste
- Steuerelement Typen, Symbolleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327c187a86ace6f02b93082675c345eae4d4edf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388688"
---
# <a name="toolbar-control-type"></a>ToolBar-Steuerelement Typen

Dieses Thema enthält **Informationen zur Unterstützung der Microsoft** -Benutzeroberflächen Automatisierung für den Steuerelement-Steuerelement-Typ Symbolleisten-Steuerelemente ermöglichen Endbenutzern das Aktivieren von Befehlen und Tools, die in einer Anwendung enthalten sind.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse **für den Steuer** Element-Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Symbolleisten-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für ToolBar-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>ToolBar
<ul>
<li>Verschiedene Steuerelemente (0 oder mehr)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ToolBar
<ul>
<li>Verschiedene Steuerelemente (0 oder mehr)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Ein ToolBar-Steuerelement kann jede Art von Steuerelement in seiner Unterstruktur enthalten. Am häufigsten enthalten sie Schaltflächen, Kombinationsfelder und unterteilte Schaltflächen.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition **für den Steuer** Element-Steuerelement Typ besonders relevant ist Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert       | Notizen                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.  | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                               |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.  | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                   |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.  | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.       |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Suchfeld** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                              |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE        | Das Symbolleisten-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                      |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE        | Das Symbolleisten-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                      |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.  | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                  |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL        | Ein Symbolleisten-Steuerelement hat nie eine Bezeichnung.                                                                                                                                                                       |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.  | Lokalisierte Zeichenfolge für den Steuerelement-Typ der **Symbolleiste** . Der Standardwert ist "Symbolleiste" für en-US oder Englisch (USA).                                                                      |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Depends (Abhängig)     | Das Symbolleisten-Steuerelement benötigt keinen Namen, es sei denn, in einer Anwendung wird mehr als ein Name verwendet. Wenn mehr als ein Wert vorhanden ist, muss jeder über einen eindeutigen Namen verfügen (z. b. "Formatierung" oder "Gliederung"). |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von Toolbar-Steuerelementen unterstützt Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Depends (Abhängig) | Wenn die Symbolleiste an verschiedenen Teilen des Bildschirms angedockt werden kann, muss Sie das [Dock](uiauto-implementingdock.md) -Steuerelement Muster unterstützen.                       |
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Wenn die Symbolleiste erweitert und reduziert werden kann, um weitere Elemente anzuzeigen, muss Sie das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützen. |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Depends (Abhängig) | Wenn die Größe der Symbolleiste geändert, gedreht oder verschoben werden kann, muss Sie das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster unterstützen.                          |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Symbolleisten-Steuerelementen unterstützt Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                                | Notizen                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                              |                                                                                                                                  |
| [**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                              | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.         |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                          | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




