---
title: Slider-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Schieberegler-Steuerelement Typen.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für den Schieberegler
- Benutzeroberflächenautomatisierungs-, Slider-Steuerelement
- Benutzeroberflächenautomatisierungs-Struktur für Schieberegler-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Slider-Steuerelement
- UI-Automatisierung, Steuerelement Muster für den Schieberegler-Steuerelement
- UI-Automatisierung, Ereignisse für den Schieberegler-Steuerelement
- Baumstrukturen, Schieberegler-Steuerelement Typen
- Eigenschaften, Schieberegler-Steuerelement Typen
- Steuerelement Muster, Schieberegler-Steuerelement Typen
- Ereignisse, Schieberegler-Steuerelement Typen
- Unterstützung für den Slider-Steuerelement
- Schiebereglersteuerungstyp
- Steuerelement Typen, Baumstruktur für den Schieberegler-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Schieberegler-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Schieberegler
- Steuerelement Typen, Schieberegler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be8e82dfc8f011363086745368ed1693c45a6aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947845"
---
# <a name="slider-control-type"></a>Slider-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Schieberegler** -Steuerelement Typen.

Ein Schieberegler-Steuerelement ist ein zusammengesetztes Steuerelement mit Schaltflächen, mit denen ein Benutzer einen numerischen Bereich festlegen oder einen Satz von Elementen auswählen kann.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Schieberegler** -Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Schieberegler-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Schieberegler-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Schieberegler
<ul>
<li>Schaltfläche (2 oder 4)</li>
<li>Thumb (1)</li>
<li>Listenelement (beliebige Anzahl)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Schieberegler
<ul>
<li>Listenelement (beliebige Anzahl)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Schieberegler-Steuerelemente besonders relevant ist Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                   |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                       |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Die Mehrzahl der Schieberegler-Steuerelemente müssen den [**UIA \_ E \_ noclickablepoint**](uiauto-error-codes.md) -Fehler zurückgeben, da das gesamte umgebende Rechteck des Schieberegler-Steuer Elements durch untergeordnete Steuerelemente belegt wird. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Schieberegler** | Dieser Wert ist für alle Frameworks gleich.                                                                                                                                                                                     |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Schieberegler-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                           |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Schieberegler-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                           |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen. Die untergeordneten Elemente (Schaltflächen und Thumb) eines Schieberegler-Steuer Elements sollten niemals den Fokus haben. Der Fokus sollte immer auf dem Schieberegler-Steuerelement selbst bleiben.       |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn dem Steuerelement eine statische Text Bezeichnung zugeordnet ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen. Wenn das Text Steuerelement eine Unterkomponente eines anderen Steuer Elements ist, wird keine **LabeledBy** -Eigenschaft festgelegt.   |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge für den Steuerungstyp des **Schiebereglers** . Der Standardwert ist "Slider" für en-US oder Englisch (USA).                                                                                             |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Name des Schieberegler-Steuer Elements wird in der Regel aus einer statischen Text Bezeichnung generiert. Wenn keine statische Text Bezeichnung vorhanden ist, muss der Anwendungsentwickler einen Eigenschafts Wert für den **Namen** zuweisen.                              |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von allen Slider-Steuerelementen unterstützt Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                          | Unterstützung/Wert | Notizen                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Depends (Abhängig)       | Ein Schieberegler muss das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützen, wenn der Inhalt auf einen Wert in einem numerischen Bereich festgelegt werden kann.                                                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | Depends (Abhängig)       | Ein Schieberegler sollte das [Auswahl](uiauto-implementingselection.md) Steuerelement Muster unterstützen, wenn der Inhalt einen Wert unter einem diskreten Satz von Optionen darstellt. Wenn das Selection-Steuerelementmuster unterstützt wird, muss die entsprechende Auswahl als ein oder mehrere untergeordnete Listenelemente des Schiebereglers verfügbar gemacht werden. |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | Depends (Abhängig)       | Ein Schieberegler muss das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützen, wenn der Inhalt einen Wert unter einem diskreten Satz von Optionen darstellt.                                                                                                                                                     |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die Schieberegler-Steuerelemente zur Unterstützung Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Rangevaluevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.        | Wenn das Steuerelement das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA- \_ Auswahl \_ invalidatedeventid**](uiauto-event-ids.md)                                       | Wenn das Steuerelement das [Selection](uiauto-implementingselection.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.     |
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

 

 




