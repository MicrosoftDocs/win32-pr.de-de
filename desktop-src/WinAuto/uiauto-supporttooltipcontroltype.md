---
title: QuickInfo-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den ToolTip-Steuerelementtyp. QuickInfo-Steuerelemente sind Popupfenster, die Text enthalten.
ms.assetid: 810f85a9-4d3b-4ceb-bd2c-bf70e8712ae2
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den ToolTip-Steuerelementtyp
- Benutzeroberflächenautomatisierung,ToolTip-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den ToolTip-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den ToolTip-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den QuickInfo-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Events für den ToolTip-Steuerelementtyp
- Strukturstrukturen,ToolTip-Steuerelementtyp
- Properties,ToolTip-Steuerelementtyp
- Steuerelementmuster,ToolTip-Steuerelementtyp
- Events,ToolTip-Steuerelementtyp
- Unterstützung für den ToolTip-Steuerelementtyp
- ToolTip-Steuerelementtyp
- Steuerelementtypen,Struktur für ToolTip-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für den ToolTip-Steuerelementtyp
- Steuerelementtypen,Unterstützung für QuickInfo
- Steuerelementtypen, QuickInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a627114afcdeeb9b6e156572476462fa7ecde75a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472856"
---
# <a name="tooltip-control-type"></a>QuickInfo-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **ToolTip-Steuerelementtyp.** QuickInfo-Steuerelemente sind Popupfenster, die Text enthalten.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **QuickInfo-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle QuickInfo-Steuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf QuickInfo-Steuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>ToolTip<ul><li>Text (beliebige Anzahl)</li><li>Bild (beliebige Anzahl)</li></ul></li></ul> | <ul><li>ToolTip</li></ul> | 




 

QuickInfo-Steuerelemente werden nur in der Inhaltsansicht der Benutzeroberflächenautomatisierung angezeigt, wenn sie den Tastaturfokus erhalten können. Andernfalls sind alle Informationen der QuickInfo über die [**IUIAutomationElement::CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) -Eigenschaft (oder [**CachedHelpText)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)für das Element verfügbar, auf das die QuickInfo verweist.

QuickInfos sollten unter dem Steuerelement angezeigt werden, auf das ihre Informationen verweisen. Clients müssen auf [**die \_ UIA-ToolTipOpenedEventId**](uiauto-event-ids.md) lauschen, um sicherzustellen, dass sie konsistent Informationen erhalten, die in QuickInfos enthalten sind.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren Wert oder Definition für den **ToolTip-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert       | Hinweise                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.  | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                                                                                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.  | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.  | Der klickbare Punkt sollte der Teil der QuickInfo sein, der das Steuerelement verlässt. Einige QuickInfos verfügen nicht über diese Funktion und haben keinen klickbaren Punkt.                                                                                                                                                                                                  |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ToolTip** |                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | Depends (Abhängig)     | Wenn das QuickInfo-Steuerelement den Tastaturfokus erhalten kann, muss es in der Inhaltsansicht der Struktur angezeigt werden. Wenn es sich nur um Text handelt, ist es als [**IUIAutomationElement::CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) -Eigenschaft (oder [**CachedHelpText)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)des Steuerelements verfügbar, das sie ausgelöst hat. |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | True        | Das QuickInfo-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.  | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | QuickInfo-Steuerelemente sind immer durch ihren Inhalt selbstbeschriftet.                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.  | Lokalisierte Zeichenfolge für den Steuerelementtyp „ToolTip“. Der Standardwert ist "QuickInfo" für en-US oder Englisch (USA).                                                                                                                                                                                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.  | Der Name des QuickInfo-Steuerelements ist der Text, der in der QuickInfo angezeigt wird.                                                                                                                                                                                                                                                                              |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von QuickInfo-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                   | Support | Notizen                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Depends (Abhängig) | Für eine bessere Barrierefreiheit kann ein QuickInfo-Steuerelement das [Text-Steuerelementmuster](uiauto-implementingtextandtextrange.md) unterstützen, obwohl es nicht erforderlich ist. Das Text-Steuerelementmuster ist nützlich, wenn der Text viele Formate und Attribute hat (z. B., Farbe, Fettdruck und Kursivdruck). |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) | Depends (Abhängig) | QuickInfos, die durch Klicken auf ein Benutzeroberflächenelement geschlossen werden können, müssen das [Fenster-Steuerelementmuster](uiauto-implementingwindow.md) unterstützen, damit sie automatisch geschlossen werden können.                                                                                                                 |



 

## <a name="required-events"></a>Erforderliche Ereignisse

QuickInfo-Steuerelemente müssen das [**\_ UIA-ToolTipOpenedEventId-Ereignis**](uiauto-event-ids.md) ausgelöst werden, wenn sie auf dem Bildschirm angezeigt werden. Das Ereignis enthält einen Verweis auf das Benutzeroberflächenautomatisierung der QuickInfo selbst.

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die von QuickInfo-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                            | Hinweise                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                               |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)          |                                                                                                                            |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                          | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                      | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Das NamePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                    |                                                                                                                            |
| [**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)                                                          | Wenn das Steuerelement [](uiauto-implementingtextandtextrange.md) das Text-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ ToolTipClosedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**\_ \_ UIA-FensterFensterClosedEventId**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [Window-Steuerelementmuster](uiauto-implementingwindow.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**\_ \_ UIA-FensterOpenedEventId**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [Window-Steuerelementmuster](uiauto-implementingwindow.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ WindowWindowVisualStatePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement das [Window-Steuerelementmuster](uiauto-implementingwindow.md) unterstützt, muss es dieses Ereignis unterstützen.           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




