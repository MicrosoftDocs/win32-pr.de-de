---
title: CheckBox-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den CheckBox-Steuerelementtyp.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den CheckBox-Steuerelementtyp
- Benutzeroberflächenautomatisierung,CheckBox-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den CheckBox-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den CheckBox-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den CheckBox-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den CheckBox-Steuerelementtyp
- Strukturstrukturen, CheckBox-Steuerelementtyp
- Properties, CheckBox-Steuerelementtyp
- Steuerelementmuster, CheckBox-Steuerelementtyp
- Ereignisse, CheckBox-Steuerelementtyp
- Unterstützung für den CheckBox-Steuerelementtyp
- CheckBox-Steuerelementtyp
- Steuerelementtypen, Struktur für den CheckBox-Steuerelementtyp
- Steuerelementtypen, Steuerelementmuster für den CheckBox-Steuerelementtyp
- Steuerelementtypen,Unterstützung für CheckBox
- Steuerelementtypen,CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec20bc259095c41bd1bdc4c3d4e5953be2e883d2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467807"
---
# <a name="checkbox-control-type"></a>CheckBox-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung  Unterstützung für den CheckBox-Steuerelementtyp.

Ein Kontrollkästchen ist ein Objekt, mit dem ein Zustand gekennzeichnet wird und das Benutzer dazu verwenden können, diesen Zustand zu durchlaufen. Kontrollkästchen bieten dem Benutzer eine binäre Option [(Ja/Nein) oder (Ein/Aus)] oder eine tertiäre Option (Ein, Aus, Unbestimmt).

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **CheckBox-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Kontrollkästchen-Steuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Defaultaction](#defaultaction)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf Kontrollkästchen-Steuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>CheckBox</li></ul> | <ul><li>CheckBox</li></ul> | 




 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für den **CheckBox-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Hinweise                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                                                                                                       |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                           |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umschließenden Rechtecks klickbar ist und das Element spezielle Treffertests durchführt, überschreibt und stellt einen klickbaren Punkt bereit.                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **CheckBox** |                                                                                                                                                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Der Wert dieser Eigenschaft muss immer **TRUE** sein. Dies bedeutet, dass das Kontrollkästchen-Steuerelement immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur enthalten sein muss.                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Der Wert dieser Eigenschaft muss immer **TRUE** sein. Dies bedeutet, dass das Kontrollkästchen-Steuerelement immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten sein muss.                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null         | Kontrollkästchen-Steuerelemente sind selbstbeschriftet.                                                                                                                                                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem **CheckBox-Steuerelementtyp** entspricht. Der Standardwert ist "Kontrollkästchen" für en-US oder Englisch (USA).                                                                                                                                            |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Der Wert der [**IUIAutomationElement::CurrentName-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (oder [**CachedName)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)des Kontrollkästchensteuerelements ist der Text, der neben dem Feld angezeigt wird, das den Umschaltzustand beibehält. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Kontrollkästchen-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                  | Unterstützung/Wert | Hinweise                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Erforderlich      | Kontrollkästchen unterstützen das Umschalten-Steuerelementmuster, damit das Kontrollkästchen programmgesteuert durch seine internen Zustände durchlaufen werden kann. [](uiauto-implementingtoggle.md) |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Kontrollkästchensteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Das ToggleToggleStatePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)    |                                                                                                                            |



 

## <a name="defaultaction"></a>Defaultaction

Die Standardaktion für ein Kontrollkästchen besteht darin, einem Optionsfeld den Fokus zu geben und dessen aktuellen Status umzuschalten. Wie bereits erwähnt, stellen Kontrollkästchen entweder eine binäre Entscheidung (Ja/Nein oder Ein/Aus) für den Benutzer oder eine tertiäre (Ein, Aus, Unbestimmte) vor. Ist das Kontrollkästchen binär, bewirkt die Standardaktion, dass aus dem Zustand „Ein“ in den Zustand „Aus“ oder aus dem Zustand „Aus“ in den Zustand „Ein“ geschaltet wird. In einem tertiären Kontrollkästchen durchzyklen die Standardaktion die Zustände des Kontrollkästchens in der gleichen Reihenfolge, in der der Benutzer aufeinanderfolgende Mausklicks an das Steuerelement gesendet hätte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




