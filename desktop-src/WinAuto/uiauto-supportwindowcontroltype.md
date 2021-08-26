---
title: Fenster-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den Steuerelementtyp "Fenster".
ms.assetid: 521fb514-e083-48b3-b4a0-52c530154740
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den Steuerelementtyp "Fenster"
- Benutzeroberflächenautomatisierung,Fenster-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für Fenster-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den Steuerelementtyp "Fenster"
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Steuerelementtyp "Fenster"
- Benutzeroberflächenautomatisierung,Ereignisse für den Steuerelementtyp "Fenster"
- Strukturstrukturen,Fenster-Steuerelementtyp
- Eigenschaften,Fenster-Steuerelementtyp
- Steuerelementmuster, Fenster-Steuerelementtyp
- events,Window-Steuerelementtyp
- Unterstützung für den Steuerelementtyp "Fenster"
- Window-Steuerelementtyp
- Steuerelementtypen,Struktur für Window-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für Den Fenster-Steuerelementtyp
- Steuerelementtypen,Unterstützung für Window
- Steuerelementtypen, Fenster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59486f12545c0dbe6b38e20e29f6df5397cbca21
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466417"
---
# <a name="window-control-type"></a>Fenster-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den **Steuerelementtyp "Fenster".**

Das Window-Steuerelement besteht aus dem Fensterrahmen, der untergeordnete Objekte wie Titelleiste, Client sowie andere Objekte enthält.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Steuerelementtyp Window** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Fenstersteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung struktur, die sich auf Fenstersteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Fenster</li></ul> | <ul><li>Fenster</li></ul> | 




 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die eigenschaften Benutzeroberflächenautomatisierung, deren Wert oder Definition für Fenstersteuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                            |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Das Fenster-Steuerelement muss über einen klickbaren Punkt verfügen, der bewirkt, dass das Fenster ausgewählt oder deaktiviert wird.                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Fenster** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                           |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Fenster-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Fenster-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                               |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | Fenstersteuerelemente verfügen nicht über eine statische Fensterbezeichnung.                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp Window** entspricht. Der Standardwert ist "window" für en-US oder English (USA).                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Das Fenstersteuerelement enthält immer ein primäres Fensterelement, das sich darauf bezieht, was der Benutzer als semantischsten Bezeichner für das Element zuordnen würde. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von Fenstersteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                        | Unterstützung/Wert | Hinweise                                                                                                                                                                        |
|---------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Bedingt   | Das [](uiauto-implementingdock.md) Dock-Steuerelementmuster muss unterstützt werden, wenn das Fenster angedockt werden kann.                                                                       |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Erforderlich      | Mit [dem Steuerelementmuster](uiauto-implementingtransform.md) Transformieren kann das Fenster auf dem Bildschirm verschoben, seine Größe geändert oder gedreht werden. (Gilt nicht für Windows Store-Apps.) |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Erforderlich      | Das [Fenster-Steuerelementmuster](uiauto-implementingwindow.md) ermöglicht bestimmte Vorgänge für das Fenster.                                                                      |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die **von Window-Steuerelementen** unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                        | Hinweise                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                                                                                                           |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                                           |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                      |                                                                                                                                                                                                                           |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                      | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.                                                                                                  |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                  | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.                                                                                                |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                                           |
| [**UIA \_ Das NamePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                                |                                                                                                                                                                                                                           |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)   | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ ScrollHorizontalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)           | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ ScrollVerticallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)       | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)     | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ ScrollVerticalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)               | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                                           |
| [**\_ \_ UIA-FensterFensterClosedEventId**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**\_ \_ UIA-FensterOpenedEventId**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**UIA \_ WindowWindowVisualStatePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)             | Wenn das Steuerelement die [**WindowVisualState-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-get_cachedwindowvisualstate) des [Window-Steuerelementmusters](uiauto-implementingwindow.md) unterstützt, muss dieses Ereignis unterstützt werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




