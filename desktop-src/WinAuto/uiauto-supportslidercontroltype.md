---
title: Schieberegler-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den Schieberegler-Steuerelementtyp.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den Schieberegler-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Slider-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für Schieberegler-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den Schieberegler-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Schieberegler-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für Schieberegler-Steuerelementtyp
- Strukturstrukturen,Schieberegler-Steuerelementtyp
- Eigenschaften,Schieberegler-Steuerelementtyp
- Steuerelementmuster, Schieberegler-Steuerelementtyp
- events,Slider-Steuerelementtyp
- Unterstützung für den Schieberegler-Steuerelementtyp
- Schiebereglersteuerungstyp
- Steuerelementtypen,Struktur für Schieberegler-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für Schieberegler-Steuerelementtyp
- Steuerelementtypen,Unterstützung für Schieberegler
- Steuerelementtypen, Schieberegler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354217323ba4c3c59e416f7b9c36661d8ffe8a77
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472876"
---
# <a name="slider-control-type"></a>Schieberegler-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung unterstützung für den **Schieberegler-Steuerelementtyp.**

Ein Schieberegler-Steuerelement ist ein zusammengesetztes Steuerelement mit Schaltflächen, mit denen ein Benutzer einen numerischen Bereich festlegen oder aus einer Gruppe von Elementen auswählen kann.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Schieberegler-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Schiebereglersteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf Schiebereglersteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Schieberegler<ul><li>Schaltfläche (2 oder 4)</li><li>Thumb (1)</li><li>Listenelement (beliebige Anzahl)</li></ul></li></ul> | <ul><li>Schieberegler<ul><li>Listenelement (beliebige Anzahl)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren Wert oder Definition für Schiebereglersteuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Die meisten Schieberegler-Steuerelemente müssen den [**UIA \_ E \_ NOCLICKABLEPOINT-Fehler**](uiauto-error-codes.md) zurückgeben, da das gesamte umgebundene Rechteck des Schieberegler-Steuerelements von untergeordneten Steuerelementen belegt wird. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Schieberegler** | Dieser Wert ist für alle Frameworks gleich.                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Schieberegler-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Schieberegler-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen. Die unteren (Schaltflächen und Thumb) eines Schieberegler-Steuerelements sollten nie den Fokus haben. Der Fokus sollte immer auf dem Schieberegler-Steuerelement selbst bleiben.       |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn dem Steuerelement eine statische Textbezeichnung zugeordnet ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen. Wenn das Textsteuerfeld eine Unterkomponenten eines anderen Steuerelements ist, ist keine **LabeledBy-Eigenschaft** festgelegt.   |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Schieberegler-Steuerelementtyp** entspricht. Der Standardwert ist "Schieberegler" für en-US oder Englisch (USA).                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Name des Schieberegler-Steuerelements wird in der Regel aus einer statischen Textbezeichnung generiert. Wenn es keine statische Textbezeichnung gibt,  muss der Anwendungsentwickler einen Eigenschaftswert für Name zuweisen.                              |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von allen Schieberegler-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                          | Unterstützung/Wert | Hinweise                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Depends (Abhängig)       | Ein Schieberegler sollte das [RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) unterstützen, wenn der Inhalt auf einen Wert innerhalb eines numerischen Bereichs festgelegt werden kann.                                                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | Depends (Abhängig)       | Ein Schieberegler sollte das [Selection-Steuerelementmuster](uiauto-implementingselection.md) unterstützen, wenn der Inhalt einen Wert aus einem diskreten Satz von Optionen darstellt. Wenn das Selection-Steuerelementmuster unterstützt wird, muss die entsprechende Auswahl als ein oder mehrere untergeordnete Listenelemente des Schiebereglers verfügbar gemacht werden. |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | Depends (Abhängig)       | Ein Schieberegler sollte das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützen, wenn der Inhalt einen Wert aus einem diskreten Satz von Optionen darstellt.                                                                                                                                                     |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die Schiebereglersteuerelemente unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ RangeValueValuePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)        | Wenn das Steuerelement das [RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)                                       | Wenn das Steuerelement das [Selection-Steuerelementmuster](uiauto-implementingselection.md) unterstützt, muss es dieses Ereignis unterstützen.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Durch die ValueValuePropertyId-Eigenschaft**](uiauto-control-pattern-propids.md) geändertes Ereignis.                  | Wenn das Steuerelement das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützt, muss es dieses Ereignis unterstützen.             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




