---
title: ProgressBar-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den ProgressBar-Steuerelement-Typ.
ms.assetid: 2ea0c1f1-1a0a-4360-bdcb-8edc13cc3c31
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für den ProgressBar-Steuerelement
- Benutzeroberflächenautomatisierungs-, ProgressBar-Steuerelement
- Benutzeroberflächenautomatisierungs-, Baumstruktur für ProgressBar-Steuerelement
- UI-Automatisierung, Eigenschaften für den ProgressBar-Steuerelement-Typ
- Benutzeroberflächenautomatisierungs-Steuerelement Muster für den ProgressBar-Steuerelement
- UI-Automatisierung, Ereignisse für den ProgressBar-Steuerelement-Typ
- Struktur Strukturen, ProgressBar-Steuerelement Typen
- Eigenschaften, ProgressBar-Steuerelement Typen
- Steuerelement Muster, ProgressBar-Steuerelement Typen
- Ereignisse, ProgressBar-Steuerelement Typen
- Unterstützung des ProgressBar-Steuerelement Typs
- ProgressBar-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für den ProgressBar-Steuerelement-Typ
- Steuerelement Typen, Steuerelement Muster für den ProgressBar-Steuerelement Typen
- Steuerelement Typen, Unterstützung für ProgressBar
- Steuerelement Typen, ProgressBar
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 98be22a4a3d3b99e113d3c0d1402f2c45ee25550
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "104101150"
---
# <a name="progressbar-control-type"></a>ProgressBar-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **ProgressBar** -Steuerelement-Typ.

Statusanzeige-Steuerelemente zeigen den Fortschritt eines langwierigen Vorgangs an. Das Steuerelement besteht aus einem Rechteck, das mit dem Fortschreiten eines Vorgangs allmählich mit der Hervorhebungsfarbe des Systems ausgefüllt wird.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **ProgressBar** -Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Statusanzeige-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung für die Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

- [Typische Baumstruktur](#typical-tree-structure)
- [Relevante Eigenschaften](#relevant-properties)
- [Erforderliche Steuerelement Muster](#required-control-patterns)
- [Erforderliche Ereignisse](#required-events)
- [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Statusanzeige-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).

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
<li>ProgressBar</li>
</ul></td>
<td><ul>
<li>ProgressBar</li>
</ul></td>
</tr>
</tbody>
</table>

Die Statusanzeige-Steuerelemente haben keine untergeordneten Elemente in der Steuerelement-oder Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Werte oder Definitionen für Status leisten besonders relevant sind. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).

| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert           | Notizen                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.      | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.      | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.      | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **ProgressBar** |                                                                                                                                                                                                      |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**        | Das Statusanzeige-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                           |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**        | Das Statusanzeige-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                           |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.      | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.      | Wenn eine statische Text Bezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.                                                                                                              |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.      | Lokalisierte Zeichenfolge für den Steuerelement-Typ " **ProgressBar** ". Der Standardwert ist "Statusanzeige" für en-US oder Englisch (USA).                                                        |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.      | Das Statusanzeige-Steuerelement ruft seinen Namen in der Regel aus einer statischen Textbezeichnung ab. Wenn keine statische Textbezeichnung vorhanden ist, muss der Anwendungsentwickler einen Wert für die Eigenschaft „Name“ verfügbar machen.                  |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von Statusanzeige-Steuerelementen unterstützt Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                              | Unterstützung/Wert | Notizen                                                                                                                                      |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Depends (Abhängig)       | Statusanzeige-Steuerelemente, die einen numerischen Bereich annehmen, müssen das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster implementieren.        |
| [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Depends (Abhängig)           | Der Wert dieser Eigenschaft ist der Minimalwert, auf den das Steuerelement festgelegt werden kann. Dieser Wert muss kleiner als der [**maximal**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)Wert sein.                                                      |
| [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Depends (Abhängig)         | Der Wert dieser Eigenschaft ist der Höchstwert, auf den das Steuerelement festgelegt werden kann. Dieser Wert muss größer als der [**minimale**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)Wert sein.                                                        |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | **NaN**       | Diese Eigenschaft ist nicht erforderlich, da Statusanzeige-Steuerelemente schreibgeschützt sind.                                                                 |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NaN**       | Diese Eigenschaft ist nicht erforderlich, da Statusanzeige-Steuerelemente schreibgeschützt sind.                                                                 |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Depends (Abhängig)       | Statusanzeige-Steuerelemente, die eine Text Angabe des Fortschritts enthalten, müssen das [value](uiauto-implementingvalue.md) -Steuerelement Muster implementieren. |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | **TRUE**      | Der Wert für diese Eigenschaft ist immer " **true**".                                                                                            |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Siehe Hinweise.    | Durch diese Eigenschaft wird der Fortschritt eines Statusanzeige-Steuerelements als Text verfügbar.                                                                          |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Status leisten erforderlich Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                           |                                                                                                                            |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Rangevaluevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.        | Wenn das Steuerelement das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                  | Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




