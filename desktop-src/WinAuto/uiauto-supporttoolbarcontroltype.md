---
title: ToolBar-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den ToolBar-Steuerelementtyp. Symbolleisten-Steuerelemente ermöglichen Endbenutzern das Aktivieren von Befehlen und Tools, die in einer Anwendung enthalten sind.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den ToolBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,ToolBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den ToolBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den ToolBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den ToolBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den ToolBar-Steuerelementtyp
- Strukturstrukturen,ToolBar-Steuerelementtyp
- Properties,ToolBar-Steuerelementtyp
- Steuerelementmuster, ToolBar-Steuerelementtyp
- events,ToolBar-Steuerelementtyp
- Unterstützung für den ToolBar-Steuerelementtyp
- ToolBar-Steuerelementtyp
- Steuerelementtypen,Struktur für ToolBar-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für den ToolBar-Steuerelementtyp
- Steuerelementtypen,Unterstützung für ToolBar
- Steuerelementtypen, ToolBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194c9aabaa684370b99d23d91c979ff3410305b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471156"
---
# <a name="toolbar-control-type"></a>ToolBar-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den **ToolBar-Steuerelementtyp.** Symbolleisten-Steuerelemente ermöglichen Endbenutzern das Aktivieren von Befehlen und Tools, die in einer Anwendung enthalten sind.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **ToolBar-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Symbolleistensteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf Symbolleistensteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>ToolBar<ul><li>Verschiedene Steuerelemente (0 oder mehr)</li></ul></li></ul> | <ul><li>ToolBar<ul><li>Verschiedene Steuerelemente (0 oder mehr)</li></ul></li></ul> | 




 

Ein Symbolleisten-Steuerelement kann einen beliebigen Steuerelementtyp in seiner Unterstruktur enthalten. Am häufigsten enthalten sie Schaltflächen, Kombinationsfelder und unterteilte Schaltflächen.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren Wert oder Definition für den **ToolBar-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert       | Hinweise                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.  | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.  | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.  | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebundenen Rechtecks angeklickt werden kann und das Element spezielle Treffertests ausführt, überschreiben Und stellen Sie einen klickbaren Punkt zur Verfügung.       |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Symbolleiste** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Das Symbolleisten-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Das Symbolleisten-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.  | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Ein Symbolleisten-Steuerelement hat nie eine Bezeichnung.                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.  | Lokalisierte Zeichenfolge, die dem **ToolBar-Steuerelementtyp** entspricht. Der Standardwert ist "Toolleiste" für en-US oder Englisch (USA).                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Depends (Abhängig)     | Das Symbolleisten-Steuerelement benötigt nur dann einen Namen, wenn in einer Anwendung mehr als ein Name verwendet wird. Wenn mehr als ein Name vorhanden ist, muss jeder einen unterscheidenden Namen haben (z. B. "Formatierung" oder "Lining"). |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von Symbolleisten-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Depends (Abhängig) | Wenn die Symbolleiste an verschiedene Teile des Bildschirms angedockt werden kann, muss sie das [Dock-Steuerelementmuster](uiauto-implementingdock.md) unterstützen.                       |
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Wenn die Symbolleiste erweitert und reduziert werden kann, um weitere Elemente anzuzeigen, muss sie das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) unterstützen. |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Depends (Abhängig) | Wenn die Größe der Symbolleiste geändert, gedreht oder verschoben werden kann, muss sie das [Transformationssteuermuster](uiauto-implementingtransform.md) unterstützen.                          |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die von Symbolleisten-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                                | Hinweise                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                              | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.         |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                          | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




