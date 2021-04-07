---
title: SplitButton-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den SplitButton-Steuer Elementtyp.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für den Steuer Elementtyp "SplitButton
- Benutzeroberflächenautomatisierungs, SplitButton-Steuer Elementtyp
- UI-Automatisierung, Baumstruktur für den SplitButton-Steuer Elementtyp
- UI-Automatisierung, Eigenschaften für den SplitButton-Steuer Elementtyp
- UI-Automatisierung, Steuerelement Muster für den SplitButton-Steuer Elementtyp
- UI-Automatisierung, Ereignisse für den SplitButton-Steuer Elementtyp
- Struktur Strukturen, SplitButton-Steuer Elementtyp
- Eigenschaften, SplitButton-Steuer Elementtyp
- Steuerelement Muster, SplitButton-Steuer Elementtyp
- Ereignisse, SplitButton-Steuer Elementtyp
- Unterstützung für den SplitButton-Steuer Elementtyp
- SplitButton-Steuer Elementtyp
- Steuerelement Typen, Baumstruktur für den SplitButton-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den SplitButton-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für SplitButton
- Steuerelement Typen, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712696"
---
# <a name="splitbutton-control-type"></a>SplitButton-Steuer Elementtyp

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **SplitButton** -Steuer Elementtyp.

Das Steuerelement unterteilte Schaltflächen ermöglicht das Ausführen einer Aktion für ein Steuerelement und das Erweitern des Steuer Elements, um eine Liste mit anderen möglichen Aktionen anzuzeigen, die ausgeführt werden können.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **SplitButton** -Steuer Elementtyp definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Steuerelemente für unterteilte Schaltflächen, in denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Beispiel für den SplitButton-Steuer Elementtyp](#splitbutton-control-type-example)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für unterteilte Schaltflächen-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Menu (0 oder 1; wird als untergeordnetes Element einer untergeordneten Schaltfläche angezeigt, die das ExpandCollapse-Muster unterstützt)
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

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **SplitButton** -Steuer Elementtyp besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert           | Notizen                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.      | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.      | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.      | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **SplitButton** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                        |
| [**UIA \_ helptextpropertyid**](uiauto-automation-element-propids.md)                         | Siehe Hinweise.      | Der Hilfetext kann das Ergebnis der Aktivierung der unterteilten Schaltfläche angeben. Hierbei handelt es sich in der Regel um dieselben Informationen, die durch ein QuickInfo angezeigt werden.                                                   |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE            | Das Steuerelement für eine unterteilte Schaltfläche enthält Informationen für den Endbenutzer.                                                                                                                                      |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE            | Das Steuerelement für eine unterteilte Schaltfläche ist für den Endbenutzer sichtbar.                                                                                                                                                 |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.      | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL            | Steuerelemente für unterteilte Schaltflächen verfügen nicht über eine statische Textbezeichnung.                                                                                                                                               |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.      | Lokalisierte Zeichenfolge, die dem **SplitButton** -Steuer Elementtyp entspricht. Der Standardwert ist "unterteilte Schaltfläche" für en-US oder Englisch (USA).                                                        |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.      | Der Text, der zum bezeichnen der Trenn Schaltfläche verwendet wird. Wenn ein Bild zum Bezeichnen einer unterteilten Schaltfläche verwendet wird, muss für die Eigenschaft Name der unterteilten Schaltfläche alternativer Text angegeben werden.                              |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle sind die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgeführt Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support  | Notizen                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Erforderlich | Da unterteilte Schaltflächen immer in der Lage sind, eine Liste von Optionen zu erweitern, müssen Sie das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützen.                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Erforderlich | Da Trenn Schaltflächen immer über eine Standardaktion verfügen, die der [**IInvokeProvider:: Aufrufen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) -Methode zugeordnet ist, müssen Sie [das Steuerelement](uiauto-implementinginvoke.md) -Steuerelement Muster unterstützen. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die unterteilte Schaltflächen-Steuerelemente für die Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                                | Notizen                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                              |                                                                                                                            |
| [**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ aufrufen \_ invokedebug-ID**](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                              | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                          | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a>Beispiel für den SplitButton-Steuer Elementtyp

Die folgende Abbildung veranschaulicht ein Steuerelement, das den **SplitButton** -Steuer Elementtyp implementiert.

![Screenshot mit einem Beispiel für ein SplitButton-Steuerelement](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Benutzeroberflächenautomatisierungs-Struktur – Steuerelement Ansicht</th>
<th>Benutzeroberflächenautomatisierungs-Struktur – Inhaltsansicht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>SplitButton- &quot; Name &quot; (aufrufen, ExpandCollapse)
<ul>
<li>Schaltfläche " &quot; Weitere Optionen" &quot; (aufrufen)
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
<li>SplitButton- &quot; Name &quot; (aufrufen, ExpandCollapse)
<ul>
<li>Schaltfläche " &quot; Weitere Optionen" &quot; (aufrufen)
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

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




