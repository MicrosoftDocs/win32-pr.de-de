---
title: Register Steuerungstyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Tab-Steuerelement-Typ.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für Tab-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Register Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Struktur für Register Steuerungstyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für Register Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Register Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Ereignisse für Register Steuerelement-Typ
- Struktur Strukturen, Registerkarten-Steuerelement Typen
- Eigenschaften, Register Steuerelement-Typ
- Steuerelement Muster, Register Steuerelement-Typ
- Ereignisse, Registerkarten-Steuerelement Typen
- Unterstützung für Tab-Steuerelement Typen
- Tabulator-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Register Steuerungstyp
- Steuerelement Typen, Steuerelement Muster für Registerkarten-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Registerkarte
- Steuerelement Typen, Registerkarte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769a03617830c33fce4a8f64c594010b2120785b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947844"
---
# <a name="tab-control-type"></a>Register Steuerungstyp

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Tab** -Steuerelement-Typ.

Ein Registerkarten-Steuerelement entspricht in etwa einem Trennblatt in einem Notizbuch den Beschriftungen in einer Hängeregistratur. Durch Verwenden eines Registerkarten-Steuerelements können in einer Anwendung mehrere Seiten für denselben Bereich in einem Fenster oder Dialogfeld definiert werden.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Tab** -Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Registerkarten-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Registerkarten-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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



 

Registerkarten-Steuerelemente verfügen über untergeordnete Benutzeroberflächenautomatisierungs-Elemente, die auf dem [TabItem](uiauto-supporttabitemcontroltype.md) - Wenn Registerkarten Elemente gruppiert sind (z. b. wie in Microsoft Office Anwendungen), kann der **Register** Steuerelementtyp auch **Gruppen** Steuerelement Typen für die gruppierten Registerkarten Elemente hosten, wie in der folgenden Baumstruktur dargestellt.



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

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Register Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                                                                                                                  |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Nein         | Das Registerkarten-Steuerelement enthält keine durch Klicken aktivierbaren Punkte.                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **TAB**    |                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Registerkarten-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Registerkarten-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | TRUE       | Der Tab-Steuerelementtyp muss den Tastaturfokus empfangen können. In der Regel Ruft ein Benutzeroberflächenautomatisierungs-Client [**iuiautomationelement:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) auf einem Registerkarten-Steuerelement auf, und eines seiner Elemente führt den Tastaturfokus an das Registerkarten-Steuerelement weiter. Bei einigen Registerkartencontainern ist es möglich, dass sie den Fokus annehmen, ohne dass der Fokus für eines ihrer Elemente festgelegt wurde. |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Registerkarten-Steuerelemente haben üblicherweise eine statische Beschriftung, die durch diese Eigenschaft verfügbar gemacht wird.                                                                                                                                                                                                                                                                                        |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Register** Steuerungstyp entspricht. Der Standardwert ist "Tab" für en-US oder Englisch (USA).                                                                                                                                                                                                                                                  |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Das Registerkarten-Steuerelement erfordert selten eine **Name** -Eigenschaft.                                                                                                                                                                                                                                                                                                                          |
| [**UIA- \_ orientationpropertyid**](uiauto-automation-element-propids.md)                   | Siehe Hinweise. | Durch das Registerkarten-Steuerelement muss immer angeben werden, ob es horizontal oder vertikal positioniert ist.                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Register Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                             | Unterstützung/Wert | Notizen                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Erforderlich      | Alle Registerkarten-Steuerelemente müssen das [Auswahl](uiauto-implementingselection.md) Steuerelement Muster unterstützen.                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | TRUE          | Ein Registerkarten-Steuerelement erfordert immer, dass eine Auswahl getroffen wird.                                                                                                                  |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | false         | Registerkarten-Steuerelemente sind immer Einzelauswahlcontainer.                                                                                                                   |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depends (Abhängig)       | Das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster muss unterstützt werden, wenn das Registerkarten-Steuerelement Widgets enthält, mit denen ein Satz von Registerkarten Elementen durchlaufen werden kann. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die Registerkarten-Steuerelemente zur Unterstützung Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                        | Notizen                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                      |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                      | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                  | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.   | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.           | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.       | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.     | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.               | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




