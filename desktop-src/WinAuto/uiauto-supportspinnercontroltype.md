---
title: Spinner-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Spinner-Steuerelement.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Benutzeroberflächenautomatisierungs-Unterstützung für Spinner-Steuerelement
- Benutzeroberflächenautomatisierungs-Steuerelement Typen
- Benutzeroberflächenautomatisierungs-Struktur für Spinner-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für Spinner-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Spinner-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für Spinner-Steuerelement Typen
- Baumstrukturen, Spinner-Steuerelement Typen
- Eigenschaften, Typ des Spinner-Steuer Elements
- Steuerelement Muster, Spinner-Steuerelement Typen
- Ereignisse, Spinner-Steuerelement Typen
- Unterstützung für Spinner-Steuerelement Typen
- Spinner-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Spinner-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Spinner-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Spinner
- Steuerelement Typen, Spinner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712701"
---
# <a name="spinner-control-type"></a>Spinner-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Spinner** -Steuerelement.

Spinner-Steuerelemente werden dazu verwendet, um aus einem Bereich von Elementen oder Zahlen auszuwählen.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Spinner** -Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Spinner-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur dargestellt, die sich auf Spinner-Steuerelemente bezieht, wenn Sie das **RangeValue** -Steuerelement und das **Selection** -Steuerelement Muster unterstützen Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).

**RangeValue-Steuerelement Muster**



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
<li>Spinner
<ul>
<li>Bearbeitung (0 oder 1)</li>
<li>Schaltfläche (2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Spinner</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Selection-Steuerelementmuster**



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
<li>Spinner
<ul>
<li>Bearbeitung (0 oder 1)</li>
<li>Schaltfläche (2)</li>
<li>Listenelement (beliebige Anzahl)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Spinner
<ul>
<li>ListItem (beliebige Anzahl)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Um sicherzustellen, dass die beiden Schaltflächen in der Teilstruktur der Steuerelement Ansicht von automatisierten Testtools unterschieden werden können, weisen Sie der **AutomationId** -Eigenschaft nach Bedarf den Wert **ScrollAmount \_ SmallIncrement** oder [**ScrollAmount \_ smalldekrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) zu. Bei einigen Implementierungen ist das zugeordnete Bearbeitungs Steuerelement möglicherweise ein Peer des Spinner-Steuer Elements.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Spinner-Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert       | Notizen                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.  | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                                                               |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.  | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                   |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.  | Der durch Klicken aktivierbare Punkt des Spinner-Steuerelements übergibt den Fokus an den Bearbeitungsbereich des Steuerelements.                                                                                                                                                                                                                                      |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Spinner** | Dieser Wert ist für alle Frameworks gleich.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE        | Das Spinner-Steuerelement muss immer ein Inhaltselement sein.                                                                                                                                                                                                                                                                                |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE        | Das Spinner-Steuerelement muss immer ein Steuerelement sein.                                                                                                                                                                                                                                                                              |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.  | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen. Ein Spinner-Steuerelement nimmt nur selten den Fokus, aber wenn dies der Fall ist, sollte der Fokus auf dem Spinner-Steuerelement selbst bleiben, nicht auf den untergeordneten Schaltflächen. Der Benutzer sollte in der Lage sein, alle scrollaktionen mithilfe der nach-oben-und nach-unten-Taste auszuführen. |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.  | Spinner-Steuerelemente verfügen über eine statische Textbezeichnung.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.  | Lokalisierte Zeichenfolge, die dem **Spinner** -Steuerelement Typ entspricht. Der Standardwert ist "Spinner" für en-US oder Englisch (USA).                                                                                                                                                                                       |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.  | Das Spinner-Steuerelement ruft seinen Namen in der Regel aus einer statischen Textbezeichnung ab.                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Spinner-Steuerelementen unterstützt Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                         | Unterstützung/Wert | Notizen                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | Depends (Abhängig)       | Spinner-Steuerelemente, die einen numerischen Bereich umfassen, können das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützen.               |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | Depends (Abhängig)       | Spinner-Steuerelemente, die eine Liste der auszuwählenden Elemente aufweisen, müssen das [Auswahl](uiauto-implementingselection.md) Steuerelement Muster unterstützen. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | false         | Spinner-Steuerelemente sind immer Einfachauswahlcontainer.                                                                                  |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | Depends (Abhängig)       | Spinner-Steuerelemente, die einen Satz von Optionen oder Zahlen umfassen, können das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützen.    |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Spinner-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Rangevaluevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.        | Wenn das Steuerelement das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Auswahl für die Eigenschaft " \_ invalidatedeventid**](uiauto-event-ids.md) " für "Changed".               | Wenn das Steuerelement das [Selection](uiauto-implementingselection.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.     |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                  | Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




