---
title: Registerkarten-Steuerelementtyp
description: Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den Steuerelementtyp Tabulator.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung des Steuerelementtyps "Registerkarte"
- Benutzeroberflächenautomatisierung,Registerkarten-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für Tabstopp-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den Registerkarten-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Registerkarten-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den Registerkarten-Steuerelementtyp
- Strukturstrukturen, Registerkartensteuerelementtyp
- Eigenschaften, Registerkarten-Steuerelementtyp
- Steuerelementmuster, Registerkartensteuerelementtyp
- Ereignisse, Registerkarten-Steuerelementtyp
- Unterstützung für den Steuerelementtyp "Registerkarte"
- Tabulator-Steuerelementtyp
- Steuerelementtypen, Struktur für Tabstopp-Steuerelementtyp
- Steuerelementtypen, Steuerelementmuster für den Steuerelementtyp "Tab"
- Steuerelementtypen,Unterstützung für Tabstopps
- Steuerelementtypen, Registerkarte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a83263db87a68e258598ea46ca903af2ddb39c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482496"
---
# <a name="tab-control-type"></a>Registerkarten-Steuerelementtyp

Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den **Steuerelementtyp "Registerkarte".**

Ein Registerkarten-Steuerelement entspricht in etwa einem Trennblatt in einem Notizbuch den Beschriftungen in einer Hängeregistratur. Durch Verwenden eines Registerkarten-Steuerelements können in einer Anwendung mehrere Seiten für denselben Bereich in einem Fenster oder Dialogfeld definiert werden.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den Registerkarten-Steuerelementtyp definiert.  Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Registerkartensteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf Registerkartensteuerelemente bezieht, und beschreibt, was in den einzelnen Ansichten enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Registerkarte<ul><li>TabItem (1 oder mehr)</li><li>ScrollBar (0 oder 1)<ul><li>Button (0 oder 2)</li></ul></li></ul></li></ul> | <ul><li>Registerkarte<ul><li>TabItem (1 oder mehr)</li></ul></li></ul> | 




 

Registerkartensteuerelemente verfügen über untergeordnete Benutzeroberflächenautomatisierung Elemente, die auf dem [TabItem-Steuerelementtyp](uiauto-supporttabitemcontroltype.md) basieren. Wenn Registerkartenelemente gruppiert werden (z. B. wie in Microsoft Office Anwendungen), kann der **Steuerelementtyp Tabstopp** auch **Gruppen-Steuerelementtypen** für die gruppierten Registerkartenelemente hosten, wie die folgende Struktur zeigt.




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Registerkarte<ul><li>TabItem (1 oder mehr)</li><li>Group (beliebige Anzahl)<ul><li>TabItem (beliebige Anzahl)</li></ul></li><li>ScrollBar (0 oder 1)<ul><li>Button (0 oder 2)</li></ul></li></ul></li></ul> | <ul><li>Registerkarte<ul><li>TabItem (1 oder mehr)</li><li>Group (beliebige Anzahl)<ul><li>TabItem (beliebige Anzahl)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für Registerkartensteuerelemente besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                                                                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Nein         | Das Registerkartensteuerelement verfügt nicht über klickbare Punkte.                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Registerkarte**    |                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Registerkartensteuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Registerkartensteuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE       | Der Tab-Steuerelementtyp muss den Tastaturfokus empfangen können. In der Regel ruft ein Benutzeroberflächenautomatisierung Client [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) auf einem Registerkartensteuerelement auf, und eines seiner Elemente leitet den Tastaturfokus an das Registerkartensteuerelement weiter. Bei einigen Registerkartencontainern ist es möglich, dass sie den Fokus annehmen, ohne dass der Fokus für eines ihrer Elemente festgelegt wurde. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Registerkarten-Steuerelemente haben üblicherweise eine statische Beschriftung, die durch diese Eigenschaft verfügbar gemacht wird.                                                                                                                                                                                                                                                                                        |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp Tabulator** entspricht. Der Standardwert ist "tab" für en-US oder Englisch (USA).                                                                                                                                                                                                                                                  |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Das Registerkartensteuerelement erfordert selten eine **Name-Eigenschaft.**                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Siehe Hinweise. | Durch das Registerkarten-Steuerelement muss immer angeben werden, ob es horizontal oder vertikal positioniert ist.                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Registerkartensteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                             | Unterstützung/Wert | Hinweise                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Erforderlich      | Alle Registerkartensteuerelemente müssen das [Selection-Steuerelementmuster](uiauto-implementingselection.md) unterstützen.                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | TRUE          | Ein Registerkarten-Steuerelement erfordert immer, dass eine Auswahl getroffen wird.                                                                                                                  |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | FALSE         | Registerkarten-Steuerelemente sind immer Einzelauswahlcontainer.                                                                                                                   |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depends (Abhängig)       | Das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) muss unterstützt werden, wenn das Registerkarten-Steuerelement über Widgets verfügt, mit denen ein Satz von Registerkartenelementen durchscrollt werden kann. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die Registerkartensteuerelemente unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                        | Hinweise                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                      | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                  | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)   | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalViewSizePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)           | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticallyScrollablePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)       | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)     | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalViewSizePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)               | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




