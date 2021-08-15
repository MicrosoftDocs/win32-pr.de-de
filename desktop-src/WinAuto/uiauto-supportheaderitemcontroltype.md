---
title: HeaderItem-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den HeaderItem-Steuerelementtyp.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für headerItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,HeaderItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für headerItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für headerItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für headerItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für headerItem-Steuerelementtyp
- Strukturstrukturen, HeaderItem-Steuerelementtyp
- properties,HeaderItem-Steuerelementtyp
- Steuerelementmuster,HeaderItem-Steuerelementtyp
- events,HeaderItem-Steuerelementtyp
- Unterstützung für headerItem-Steuerelementtyp
- HeaderItem-Steuerelementtyp
- Steuerelementtypen, Struktur für HeaderItem-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für HeaderItem-Steuerelementtyp
- Steuerelementtypen,Unterstützung für HeaderItem
- Steuerelementtypen,HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6bbcd6d86e7401c3fa98d162e3aa273613dfd3a32705da891fc89d1f4ea003f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098210"
---
# <a name="headeritem-control-type"></a>HeaderItem-Steuerelementtyp

Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den **HeaderItem-Steuerelementtyp.**

Der **HeaderItem-Steuerelementtyp** stellt eine visuelle Bezeichnung für eine Zeile oder Spalte mit Informationen bereit.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **HeaderItem-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Headerelementsteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf Headerelementsteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).



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
<li>HeaderItem</li>
</ul></td>
<td>(Nicht vorhanden)</td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für den **HeaderItem-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert          | Hinweise                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.     | Der Wert dieser Eigenschaft muss für alle Peerelemente in der Rohansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.     | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.     | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umschließenden Rechtecks klickbar ist und das Element spezielle Treffertests durchführt, überschreibt und stellt einen klickbaren Punkt bereit. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **HeaderItem** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE          | Das Headerelement-Steuerelement ist nicht in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE           | Das Headerelement-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.     | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Siehe Hinweise      | Diese Eigenschaft stellt Informationen für Sortierreihenfolgen nach Headerelement bereit.                                                                                                                               |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL           | Headerelementsteuerelemente verfügen nicht über eine statische Textbezeichnung.                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.     | Lokalisierte Zeichenfolge, die dem **HeaderItem-Steuerelementtyp entspricht.** Der Standardwert ist "header item" für en-US oder Englisch (USA).                                                          |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.     | Das Headerelement-Steuerelement ist immer selbstbezeichnend.                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Headerelementsteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support | Notizen                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | Depends (Abhängig) | Implementieren [](uiauto-implementinginvoke.md) Sie das Invoke-Steuerelementmuster, wenn auf das Headerelement-Steuerelement geklickt werden kann, um die Daten zu sortieren. |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depends (Abhängig) | Implementieren [](uiauto-implementingtransform.md) Sie das Transformationssteuerelementmuster, wenn die Größe des Headerelementsteuerelements geändert werden kann.            |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Headerelementsteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                     | Wenn das Steuerelement [](uiauto-implementinginvoke.md) das Invoke-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




