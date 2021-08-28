---
title: ProgressBar-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den ProgressBar-Steuerelementtyp.
ms.assetid: 2ea0c1f1-1a0a-4360-bdcb-8edc13cc3c31
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den ProgressBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,ProgressBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den ProgressBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den ProgressBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den ProgressBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Events für den ProgressBar-Steuerelementtyp
- Strukturstrukturen,ProgressBar-Steuerelementtyp
- properties,ProgressBar-Steuerelementtyp
- Steuerelementmuster,ProgressBar-Steuerelementtyp
- events,ProgressBar-Steuerelementtyp
- Unterstützung für den ProgressBar-Steuerelementtyp
- ProgressBar-Steuerelementtyp
- Steuerelementtypen,Struktur für ProgressBar-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für den ProgressBar-Steuerelementtyp
- Steuerelementtypen,Unterstützung für ProgressBar
- Steuerelementtypen, ProgressBar
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 5dc5dd22abcaca70ae9ce86717db6055642a21ce
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472297"
---
# <a name="progressbar-control-type"></a>ProgressBar-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **ProgressBar-Steuerelementtyp.**

Statusleisten-Steuerelemente geben den Status eines längeren Vorgangs an. Das Steuerelement besteht aus einem Rechteck, das mit dem Fortschreiten eines Vorgangs allmählich mit der Hervorhebungsfarbe des Systems ausgefüllt wird.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **ProgressBar-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Statusleisten-Steuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

- [Typische Strukturstruktur](#typical-tree-structure)
- [Relevante Eigenschaften](#relevant-properties)
- [Erforderliche Steuerelementmuster](#required-control-patterns)
- [Erforderliche Ereignisse](#required-events)
- [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf Statusleistensteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)


| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>ProgressBar</li></ul> | <ul><li>ProgressBar</li></ul> | 


Die Statusleisten-Steuerelemente enthalten keine unteren Bzw. in der Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren Wert oder Definition für Statusleisten besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)

| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert           | Hinweise                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.      | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.      | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.      | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebundenen Rechtecks angeklickt werden kann und das Element spezielle Treffertests ausführt, überschreiben Und stellen Sie einen klickbaren Punkt zur Verfügung. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ProgressBar** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**        | Das Statusleisten-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**        | Das Statusleisten-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.      | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.      | Wenn es eine statische Textbezeichnung gibt, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.      | Lokalisierte Zeichenfolge, die dem **ProgressBar-Steuerelementtyp** entspricht. Der Standardwert ist "Statusleiste" für en-US oder Englisch (USA).                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.      | Das Statusanzeige-Steuerelement ruft seinen Namen in der Regel aus einer statischen Textbezeichnung ab. Wenn keine statische Textbezeichnung vorhanden ist, muss der Anwendungsentwickler einen Wert für die Eigenschaft „Name“ verfügbar machen.                  |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von Statusleisten-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                              | Unterstützung/Wert | Hinweise                                                                                                                                      |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Depends (Abhängig)       | Statusleisten-Steuerelemente, die einen numerischen Bereich verwenden, müssen das [RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) implementieren.        |
| [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Depends (Abhängig)           | Der Wert dieser Eigenschaft ist der Mindestwert, auf den das Steuerelement festgelegt werden kann. Dieser Wert sollte kleiner als Maximum [**sein.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)                                                      |
| [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Depends (Abhängig)         | Der Wert dieser Eigenschaft ist der Höchstwert, auf den das Steuerelement festgelegt werden kann. Dieser Wert sollte größer als Minimum [**sein.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)                                                        |
| [**Smallchange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | **NaN**       | Diese Eigenschaft ist nicht erforderlich, da Statusanzeige-Steuerelemente schreibgeschützt sind.                                                                 |
| [**Largechange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NaN**       | Diese Eigenschaft ist nicht erforderlich, da Statusanzeige-Steuerelemente schreibgeschützt sind.                                                                 |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Depends (Abhängig)       | Statusanzeige-Steuerelemente, die eine Textanzeige für den Fortschritt geben, müssen das [Value-Steuerelementmuster](uiauto-implementingvalue.md) implementieren. |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | **TRUE**      | Der Wert für diese Eigenschaft ist immer **TRUE.**                                                                                            |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Siehe Hinweise.    | Durch diese Eigenschaft wird der Fortschritt eines Statusanzeige-Steuerelements als Text verfügbar.                                                                          |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die Statusleisten unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ NamePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ RangeValueValuePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)        | Wenn das Steuerelement das [RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Durch die ValueValuePropertyId-Eigenschaft**](uiauto-control-pattern-propids.md) geändertes Ereignis.                  | Wenn das Steuerelement das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützt, muss es dieses Ereignis unterstützen.             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




