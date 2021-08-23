---
title: Registerkarten-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den Steuerelementtyp "Tabulator".
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den Steuerelementtyp "Tabulator"
- Benutzeroberflächenautomatisierung,Steuerelementtyp "Tabulator"
- Benutzeroberflächenautomatisierung,Struktur für Tabstopp-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den Steuerelementtyp "Tabulator"
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Steuerelementtyp "Tabulator"
- Benutzeroberflächenautomatisierung,Events für den Steuerelementtyp "Tabulator"
- Strukturstrukturen,Steuerelementtyp "Tabulator"
- Eigenschaften,Steuerelementtyp "Tabulator"
- Steuerelementmuster, Tabstopp-Steuerelementtyp
- events,Tab-Steuerelementtyp
- Unterstützung für den Steuerelementtyp "Tabulator"
- Tabulator-Steuerelementtyp
- Steuerelementtypen,Struktur für Tabstopp-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für Tabstopp-Steuerelementtyp
- Steuerelementtypen,Unterstützung für Tabulator
- Steuerelementtypen, Registerkarte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9270936c50b04cb843aa96f71f3d8c8b4a14d74d034cc27e5ccbb7f1262352fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118824869"
---
# <a name="tab-control-type"></a>Registerkarten-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **Steuerelementtyp "Tabulator".**

Ein Registerkarten-Steuerelement entspricht in etwa einem Trennblatt in einem Notizbuch den Beschriftungen in einer Hängeregistratur. Durch Verwenden eines Registerkarten-Steuerelements können in einer Anwendung mehrere Seiten für denselben Bereich in einem Fenster oder Dialogfeld definiert werden.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Steuerelementtyp "Tabulator"** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Registerkartensteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung struktur, die sich auf Registerkartensteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Steuerelementansicht</th>
<th>Inhaltsansicht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Registerkarte
<ul>
<li>TabItem (1 oder mehr)</li>
<li>ScrollBar (0 oder 1)
<ul>
<li>Button (0 oder 2)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Registerkarte
<ul>
<li>TabItem (1 oder mehr)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Registerkartensteuerelemente verfügen über untergeordnete Benutzeroberflächenautomatisierung, die auf dem [TabItem-Steuerelementtyp](uiauto-supporttabitemcontroltype.md) basieren. Beim Gruppieren von Registerkartenelementen (z. B.  in Microsoft Office-Anwendungen) kann der Steuerelementtyp Tabulator auch Gruppen-Steuerelementtypen für die gruppenierten Registerkartenelemente hosten, wie die folgende Struktur zeigt. 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Steuerelementansicht</th>
<th>Inhaltsansicht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Registerkarte
<ul>
<li>TabItem (1 oder mehr)</li>
<li>Group (beliebige Anzahl)
<ul>
<li>TabItem (beliebige Anzahl)</li>
</ul></li>
<li>ScrollBar (0 oder 1)
<ul>
<li>Button (0 oder 2)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Registerkarte
<ul>
<li>TabItem (1 oder mehr)</li>
<li>Group (beliebige Anzahl)
<ul>
<li>TabItem (beliebige Anzahl)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die eigenschaften Benutzeroberflächenautomatisierung, deren Wert oder Definition für Registerkartensteuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                                                                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Nein         | Das Registerkarten-Steuerelement verfügt nicht über klickbare Punkte.                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TAB**    |                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Registerkarten-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Registerkarten-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE       | Der Tab-Steuerelementtyp muss den Tastaturfokus empfangen können. In der Regel ruft ein Benutzeroberflächenautomatisierung-Client [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) auf einem Registerkartensteuerelement auf, und eines seiner Elemente gibt den Tastaturfokus an das Registerkartensteuerelement weiter. Bei einigen Registerkartencontainern ist es möglich, dass sie den Fokus annehmen, ohne dass der Fokus für eines ihrer Elemente festgelegt wurde. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Registerkarten-Steuerelemente haben üblicherweise eine statische Beschriftung, die durch diese Eigenschaft verfügbar gemacht wird.                                                                                                                                                                                                                                                                                        |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp "Tab"** entspricht. Der Standardwert ist "tab" für en-US oder Englisch (USA).                                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Das Registerkarten-Steuerelement erfordert selten eine **Name-Eigenschaft.**                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Siehe Hinweise. | Durch das Registerkarten-Steuerelement muss immer angeben werden, ob es horizontal oder vertikal positioniert ist.                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von allen Registerkartensteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                             | Unterstützung/Wert | Hinweise                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Erforderlich      | Alle Registerkartensteuerelemente müssen das [Steuerelementmuster Auswahl](uiauto-implementingselection.md) unterstützen.                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | TRUE          | Ein Registerkarten-Steuerelement erfordert immer, dass eine Auswahl getroffen wird.                                                                                                                  |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | FALSE         | Registerkarten-Steuerelemente sind immer Einzelauswahlcontainer.                                                                                                                   |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depends (Abhängig)       | Das [](uiauto-implementingscroll.md) Scroll-Steuerelementmuster muss unterstützt werden, wenn das Registerkartensteuerelement über Widgets verfügt, die das Scrollen durch einen Satz von Registerkartenelementen ermöglichen. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Registerkartensteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                        | Hinweise                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                      | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                  | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)   | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)           | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)       | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)     | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)               | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




