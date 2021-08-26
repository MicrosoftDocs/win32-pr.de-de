---
title: Trennzeichen-Steuerelementtyp
description: Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den Separator-Steuerelementtyp.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für Trennzeichen-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Trennzeichen-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für Trennzeichen-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für Trennzeichen-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Trennzeichen-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für Den Trennzeichen-Steuerelementtyp
- Strukturstrukturen, Trennzeichen-Steuerelementtyp
- Properties, Separator-Steuerelementtyp
- Steuerelementmuster, Trennzeichen-Steuerelementtyp
- Ereignisse, Trennzeichen-Steuerelementtyp
- Unterstützung für den Trennzeichen-Steuerelementtyp
- Trennzeichensteuerelementtyp
- Steuerelementtypen, Struktur für Trennzeichen-Steuerelementtyp
- Steuerelementtypen, Steuerelementmuster für Den Trennzeichen-Steuerelementtyp
- Steuerelementtypen,Unterstützung für Trennzeichen
- Steuerelementtypen, Trennzeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0685f21565a6252febfadad115c8edf10990995c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477716"
---
# <a name="separator-control-type"></a>Trennzeichen-Steuerelementtyp

Dieses Thema enthält Informationen zur Unterstützung von  Microsoft Benutzeroberflächenautomatisierung für den Trennzeichen-Steuerelementtyp.

Mithilfe von Separator-Steuerelementen wird ein Bereich visuell in zwei Abschnitte unterteilt. Ein Separator-Steuerelement kann z. B. eine Leiste sein, die zwei Bereiche in einem Fenster definiert. Wenn die Trennlinie verschoben werden kann, sollte das Steuerelement als Steuerelementtyp „Thumb“ verfügbar gemacht werden.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Separator-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Trennzeichensteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

In der folgenden Tabelle sind ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur dargestellt, die sich auf Trennzeichensteuerelemente bezieht, und es wird beschrieben, was in den einzelnen Ansichten enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Trennzeichen</li></ul> | <ul><li>Der <strong>Trennzeichen-Steuerelementtyp</strong> verfügt nie über Inhalt.</li></ul> | 




 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für Trennzeichensteuerelemente besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert         | Hinweise                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.    | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.    | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.    | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umschließenden Rechtecks klickbar ist und das Element spezielle Treffertests durchführt, überschreibt und stellt einen klickbaren Punkt bereit. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Trennzeichen** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE         | Das Separator-Steuerelement ist nie ein Inhaltselement.                                                                                                                                                              |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | Das Separator-Steuerelement muss immer ein Steuerelement sein.                                                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.    | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Das Separator-Steuerelement hat keine statische Bezeichnung.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.    | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp Separator** entspricht. Der Standardwert ist "Trennzeichen" für en-US oder Englisch (USA).                                                             |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | ""            | Für das Trennzeichen-Steuerelement ist keine **Name-Eigenschaft** erforderlich.                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

Das Separator-Steuerelement ist nicht erforderlich, um Steuerelementmuster zu unterstützen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die Trennzeichensteuerelemente unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




