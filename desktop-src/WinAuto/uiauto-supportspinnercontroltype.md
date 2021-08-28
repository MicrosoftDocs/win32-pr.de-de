---
title: Spinner-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den Spinner-Steuerelementtyp.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung des Spinner-Steuerelementtyps
- Benutzeroberflächenautomatisierung,Spinner-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für Spinner-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für Spinner-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für Spinner-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den Spinner-Steuerelementtyp
- Strukturstrukturen, Spinner-Steuerelementtyp
- Eigenschaften, Spinner-Steuerelementtyp
- Steuerelementmuster, Spinner-Steuerelementtyp
- Ereignisse, Spinner-Steuerelementtyp
- Unterstützung für den Spinner-Steuerelementtyp
- Spinner-Steuerelementtyp
- Steuerelementtypen, Struktur für Spinner-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für Spinner-Steuerelementtyp
- Steuerelementtypen,Unterstützung für Spinner
- Steuerelementtypen, Spinner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1472fe400c189b6e5a1e894e1097395e8521e757
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478536"
---
# <a name="spinner-control-type"></a>Spinner-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft  Benutzeroberflächenautomatisierung Unterstützung für den Spinner-Steuerelementtyp.

Spinner-Steuerelemente werden dazu verwendet, um aus einem Bereich von Elementen oder Zahlen auszuwählen.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Spinner-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Spinnersteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die spinner-Steuerelemente betreffen, wenn sie die **RangeValue-** und **Selection-Steuerelementmuster** unterstützen, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).

**RangeValue-Steuerelementmuster**




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Spinner<ul><li>Bearbeitung (0 oder 1)</li><li>Schaltfläche (2)</li></ul></li></ul> | <ul><li>Spinner</li></ul> | 




 

**Selection-Steuerelementmuster**




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Spinner<ul><li>Bearbeitung (0 oder 1)</li><li>Schaltfläche (2)</li><li>Listenelement (beliebige Anzahl)</li></ul></li></ul> | <ul><li>Spinner<ul><li>ListItem (beliebige Anzahl)</li></ul></li></ul> | 




 

Um sicherzustellen, dass die beiden Schaltflächen in der Unterstruktur der Steuerelementansicht durch automatisierte Testtools unterschieden werden können, weisen Sie den Wert **ScrollAmount \_ SmallIncrement** oder [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) der **AutomationId-Eigenschaft** entsprechend zu. Bei einigen Implementierungen kann das zugeordnete Bearbeitungssteuerelement ein Peer des Spinnersteuerelements sein.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für Spinnersteuerelemente besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert       | Hinweise                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.  | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.  | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.  | Der durch Klicken aktivierbare Punkt des Spinner-Steuerelements übergibt den Fokus an den Bearbeitungsbereich des Steuerelements.                                                                                                                                                                                                                                      |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Spinner** | Dieser Wert ist für alle Frameworks gleich.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Das Spinner-Steuerelement muss immer ein Inhaltselement sein.                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Das Spinnersteuerelement muss immer ein -Steuerelement sein.                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.  | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen. Ein Spinnersteuerelement nimmt den Fokus nur selten in den Fokus, aber wenn es dies tut, sollte der Fokus auf dem Drehfeldsteuerelement selbst und nicht auf den untergeordneten Schaltflächen bleiben. Der Benutzer sollte in der Lage sein, alle Scrollaktionen mithilfe der NACH-OBEN- und NACH-UNTEN-TASTE auszuführen. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.  | Spinner-Steuerelemente verfügen über eine statische Textbezeichnung.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.  | Lokalisierte Zeichenfolge, die dem **Spinner-Steuerelementtyp** entspricht. Der Standardwert ist "spinner" für en-US oder Englisch (USA).                                                                                                                                                                                       |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.  | Das Spinner-Steuerelement ruft seinen Namen in der Regel aus einer statischen Textbezeichnung ab.                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Spinnersteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                         | Unterstützung/Wert | Hinweise                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | Depends (Abhängig)       | Spinner-Steuerelemente, die einen numerischen Bereich umfassen, können das [RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) unterstützen.               |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | Depends (Abhängig)       | Spinner-Steuerelemente, die über eine Liste von elementen verfügen, die ausgewählt werden sollen, müssen das [Selection-Steuerelementmuster](uiauto-implementingselection.md) unterstützen. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | FALSE         | Spinner-Steuerelemente sind immer Einfachauswahlcontainer.                                                                                  |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | Depends (Abhängig)       | Spinner-Steuerelemente, die sich über eine Reihe von Optionen oder Zahlen erstrecken, können das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützen.    |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die spinner-Steuerelemente unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ RangeValueValuePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)        | Wenn das Steuerelement das [RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Ereignis \_ zur Änderung der InvalidatedEventId-Eigenschaft.**](uiauto-event-ids.md)               | Wenn das Steuerelement das [Selection-Steuerelementmuster](uiauto-implementingselection.md) unterstützt, muss es dieses Ereignis unterstützen.     |
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

 

 




