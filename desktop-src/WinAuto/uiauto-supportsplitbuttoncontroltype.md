---
title: SplitButton-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den SplitButton-Steuerelementtyp.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den SplitButton-Steuerelementtyp
- Benutzeroberflächenautomatisierung,SplitButton-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den SplitButton-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den SplitButton-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den SplitButton-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den SplitButton-Steuerelementtyp
- Strukturstrukturen, SplitButton-Steuerelementtyp
- Properties, SplitButton-Steuerelementtyp
- Steuerelementmuster, SplitButton-Steuerelementtyp
- Ereignisse, SplitButton-Steuerelementtyp
- Unterstützung für den SplitButton-Steuerelementtyp
- SplitButton-Steuerelementtyp
- Steuerelementtypen, Struktur für SplitButton-Steuerelementtyp
- Steuerelementtypen, Steuerelementmuster für den SplitButton-Steuerelementtyp
- Steuerelementtypen,Unterstützung für SplitButton
- Steuerelementtypen, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb04f75a075fdd10b1cf31db01d09c6a9d9fd9a5d78c7c0499d9196a9ff8a956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825227"
---
# <a name="splitbutton-control-type"></a>SplitButton-Steuerelementtyp

Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den **SplitButton-Steuerelementtyp.**

Das Steuerelement für geteilte Schaltflächen ermöglicht das Ausführen einer Aktion für ein Steuerelement und das Erweitern des Steuerelements, um eine Liste anderer möglicher Aktionen anzuzeigen, die ausgeführt werden können.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **SplitButton-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Steuerelemente für geteilte Schaltflächen, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Beispiel für splitButton-Steuerelementtyp](#splitbutton-control-type-example)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf Steuerelemente für geteilte Schaltflächen bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).



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
<li>SplitButton
<ul>
<li>Bild (0 oder 1)</li>
<li>Text (0 oder 1)</li>
<li>Button (1 oder 2)
<ul>
<li>Menü (0 oder 1; wird als untergeordnetes Element einer Unterschaltfläche angezeigt, die das ExpandCollapse-Muster unterstützt)
<ul>
<li>MenuItem (1:n)</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>SplitButton
<ul>
<li>Button (1 oder 2)
<ul>
<li>MenuItem (1:n)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für den **SplitButton-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert           | Hinweise                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.      | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.      | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.      | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umschließenden Rechtecks klickbar ist und das Element spezielle Treffertests durchführt, überschreibt und stellt einen klickbaren Punkt bereit. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **SplitButton** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                        |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise.      | Der Hilfetext kann das Ergebnis der Aktivierung der unterteilten Schaltfläche angeben. Hierbei handelt es sich in der Regel um dieselben Informationen, die durch ein QuickInfo angezeigt werden.                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | Das Steuerelement für eine unterteilte Schaltfläche enthält Informationen für den Endbenutzer.                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | Das Steuerelement für eine unterteilte Schaltfläche ist für den Endbenutzer sichtbar.                                                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.      | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | Steuerelemente für unterteilte Schaltflächen verfügen nicht über eine statische Textbezeichnung.                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.      | Lokalisierte Zeichenfolge, die dem **SplitButton-Steuerelementtyp** entspricht. Der Standardwert ist "split button" für en-US oder Englisch (USA).                                                        |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.      | Der Text, der zum Bezeichnen der geteilten Schaltfläche verwendet wird. Wenn ein Bild verwendet wird, um eine geteilte Schaltfläche zu bezeichnen, muss alternativer Text für die Name-Eigenschaft der geteilten Schaltfläche angegeben werden.                              |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Steuerelementen für geteilte Schaltflächen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support  | Notizen                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Erforderlich | Da geteilte Schaltflächen immer die Möglichkeit haben, eine Liste von Optionen zu erweitern, müssen sie das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) unterstützen.                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Erforderlich | Da geteilte Schaltflächen immer einer Standardaktion zugeordnet sind, die der [**IInvokeProvider::Invoke-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) zugeordnet ist, müssen sie das [Invoke-Steuerelementmuster](uiauto-implementinginvoke.md) unterstützen. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die steuerelemente für geteilte Schaltflächen unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                                | Hinweise                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                              |                                                                                                                            |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md) |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                              | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                          | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a>Beispiel für den SplitButton-Steuerelementtyp

Die folgende Abbildung veranschaulicht ein Steuerelement, das den **SplitButton-Steuerelementtyp** implementiert.

![Screenshot: Beispiel für ein SplitButton-Steuerelement](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Benutzeroberflächenautomatisierung Struktur – Steuerelementansicht</th>
<th>Benutzeroberflächenautomatisierung Struktur – Inhaltsansicht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>&quot;SplitButton-Name &quot; (Invoke, ExpandCollapse)
<ul>
<li>Schaltfläche &quot; "Mehr" &quot; (Option) (Aufrufen)
<ul>
<li>Menü
<ul>
<li>MenuItem</li>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>&quot;SplitButton-Name &quot; (Invoke, ExpandCollapse)
<ul>
<li>Schaltfläche &quot; "Mehr" &quot; (Option) (Aufrufen)
<ul>
<li>Menü
<ul>
<li>MenuItem</li>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




