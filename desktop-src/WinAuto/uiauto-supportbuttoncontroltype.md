---
title: Schaltflächen-Steuerelementtyp
description: Dieses Thema enthält Informationen zur Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den Schaltflächen-Steuerelementtyp.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung des Steuerelementtyps "Schaltfläche"
- Benutzeroberflächenautomatisierung,Schaltflächen-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für Schaltflächen-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für Den Schaltflächen-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für Den Schaltflächen-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für Den Schaltflächen-Steuerelementtyp
- Strukturstrukturen, Schaltflächen-Steuerelementtyp
- properties,Button-Steuerelementtyp
- Steuerelementmuster, Schaltflächen-Steuerelementtyp
- Ereignisse, Schaltflächen-Steuerelementtyp
- Unterstützung für den Schaltflächen-Steuerelementtyp
- Button-Steuerelementtyp
- Steuerelementtypen,Struktur für Schaltflächen-Steuerelementtyp
- Steuerelementtypen, Steuerelementmuster für Den Schaltflächen-Steuerelementtyp
- Steuerelementtypen,Unterstützung für Schaltfläche
- Steuerelementtypen, Schaltfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c080018e0fcaf8cd196204f80c61041d03fc1589
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478036"
---
# <a name="button-control-type"></a>Schaltflächen-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **Schaltflächen-Steuerelementtyp.**

Eine Schaltfläche ist ein Objekt, das ein Benutzer dazu verwendet, eine Aktion auszuführen, z. B. die Schaltflächen OK und Abbrechen in einem Dialogfeld. Das Schaltflächen-Steuerelement ist hinsichtlich des Verfügbarmachens ein einfaches Steuerelement, weil es einem einzelnen Befehl zugeordnet ist, den der Benutzer ausführen möchte.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Schaltflächen-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Schaltflächensteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf Schaltflächensteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Schaltfläche<ul><li>Bild (beliebige Anzahl)</li><li>Text (beliebige Anzahl)</li></ul></li></ul> | <ul><li>Schaltfläche</li></ul> | 




 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für die Steuerelemente, die den **Steuerelementtyp Button** implementieren (z. B. Schaltflächensteuerelemente), besonders relevant sind. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Ein Schaltflächensteuerelement unterstützt in der Regel eine Zugriffstaste, damit der Endbenutzer die aktion, die durch die Schaltfläche dargestellt wird, schnell über die Tastatur ausführen kann.                                             |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umschließenden Rechtecks klickbar ist und das Element spezielle Treffertests durchführt, überschreibt und stellt einen klickbaren Punkt bereit. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Schaltfläche** |                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Der Hilfetext sollte angeben, was das Endergebnis der Aktivierung der Schaltfläche sein wird. Dies ist in der Regel die gleiche Art von Informationen, die über eine QuickInfo angezeigt werden.                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Schaltflächensteuerelement muss immer inhalt sein.                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Schaltflächen-Steuerelement muss immer ein -Steuerelement sein.                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | Schaltflächen-Steuerelemente werden durch ihren Inhalt selbstbeschriftet.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp Button entspricht.** Der Standardwert ist "button" für en-US oder Englisch (USA).                                                                   |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Name des Schaltflächensteuerelements ist der Text, der zur Bezeichnung verwendet wird. Jedes Mal, wenn ein Bild zum Bezeichnen einer Schaltfläche verwendet wird, muss alternativer Text für die **Name-Eigenschaft** der Schaltfläche angegeben werden.                        |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Schaltflächensteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                  | Unterstützung/Wert | Hinweise                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Siehe Hinweise.    | Wenn eine Schaltfläche als untergeordnetes Element einer unterteilten Schaltfläche gehostet wird, kann die untergeordnete Schaltfläche das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) anstelle des [Invoke-](uiauto-implementinginvoke.md) oder [Toggle-Steuerelementmusters](uiauto-implementingtoggle.md) unterstützen. Das ExpandCollapse-Steuerelementmuster kann zum Öffnen oder Schließen eines Menüs oder einer anderen Unterstruktur verwendet werden, die dem Schaltflächenelement zugeordnet ist. |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Siehe Hinweise.    | Alle Schaltflächen sollten [](uiauto-implementinginvoke.md) das Invoke-Steuerelementmuster oder das [Toggle-Steuerelementmuster](uiauto-implementingtoggle.md) unterstützen, aber nicht beides. Das Invoke-Steuerelementmuster muss unterstützt werden, wenn die Schaltfläche auf Anforderung des Benutzers einen Befehl ausführt. Dieser Befehl ist einem einzelnen Vorgang zugeordnet, etwa Ausschneiden, Kopieren, Einfügen oder Löschen.                                                              |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Siehe Hinweise.    | Alle Schaltflächen sollten [](uiauto-implementinginvoke.md) das Invoke-Steuerelementmuster oder das [Toggle-Steuerelementmuster](uiauto-implementingtoggle.md) unterstützen, aber nicht beides. Das Umschalt-Steuerelementmuster muss unterstützt werden, wenn die Schaltfläche eine Reihe von bis zu drei Zuständen durchlaufen kann. In der Regel ist dies als Ein-/Ausschalter für bestimmte Features zu sehen.                                                                        |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Schaltflächensteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                     | Wenn das Steuerelement [](uiauto-implementinginvoke.md) das Invoke-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Das NamePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Das ToggleToggleStatePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)    | Wenn das Steuerelement das [Umschalten-Steuerelementmuster](uiauto-implementingtoggle.md) unterstützt, muss es dieses Ereignis unterstützen.           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




