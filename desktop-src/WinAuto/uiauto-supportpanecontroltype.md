---
title: Bereichssteuerungstyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den Steuerelementtyp Bereich.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den Steuerelementtyp "Bereich"
- Benutzeroberflächenautomatisierung,Steuerelementtyp "Bereich"
- Benutzeroberflächenautomatisierung,Struktur für Bereich-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den Steuerelementtyp "Bereich"
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Steuerelementtyp "Bereich"
- Benutzeroberflächenautomatisierung,Events für den Steuerelementtyp "Bereich"
- Strukturstrukturen,Steuerelementtyp "Bereich"
- Eigenschaften,Steuerelementtyp "Bereich"
- Steuerelementmuster, Steuerelementtyp "Bereich"
- events,Pane-Steuerelementtyp
- Unterstützung für den Steuerelementtyp "Bereich"
- Pane-Steuerelementtyp
- Steuerelementtypen,Struktur für Bereich-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für den Steuerelementtyp "Bereich"
- Steuerelementtypen,Unterstützung für Bereich
- Steuerelementtypen, Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e4a7225869c0752e65aece7e4eca00a416614315c8d5af810bdeb57d29aae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825526"
---
# <a name="pane-control-type"></a>Bereichssteuerungstyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den **Steuerelementtyp Bereich.**

Der **Steuerelementtyp** Bereich ist für potenziell bildlauffähige Bereiche mit unterschiedlichen Inhalten. Es wird verwendet, um ein Objekt in einem Frame oder Dokumentfenster zu darstellen. Benutzer können zwischen Bereichssteuerelementen und innerhalb des Inhalts des aktuellen Bereichs navigieren. Bereichssteuerelemente stellen eine Gruppierungsebene dar, die niedriger als Fenster oder Dokumente, aber über einzelnen Steuerelementen ist. Der Benutzer kann je nach Kontext durch Drücken von TAB, F6 oder STRG+TAB zwischen den Bereichen navigieren.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Steuerelementtyp Bereich** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Bereichssteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Beispiel für Pane-Steuerelementtyp](#pane-control-type-example)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung struktur, die sich auf Bereichssteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)



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
<li>Bereich</li>
</ul></td>
<td><ul>
<li>Bereich</li>
</ul></td>
</tr>
</tbody>
</table>



 

Ein Bereichssteuerfeld wird immer in den Steuerelement- und Inhaltsansichten angezeigt. Machen Sie ein Layoutobjekt weder im Steuerelement noch in der Inhaltsansicht als Bereich verfügbar, wenn das Objekt nur für die visuelle Darstellung verwendet wird.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren Wert oder Definition für Bereichssteuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn eine bestimmte Tastenkombination den Fokus auf den Bereich erhält, sollten diese Informationen über diese Eigenschaft verfügbar gemacht werden.                                                                                                                                                                                                      |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Struktur der Benutzeroberflächenautomatisierung sein.                                                                                                                                                                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Diese Eigenschaft macht einen durch Klicken aktivierbaren Punkt des Bereichssteuerelements verfügbar, durch den der Bereich den Fokus erhält, wenn auf den Punkt geklickt wird.                                                                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Bereich**   |                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Der Hilfetext für Bereichssteuerelemente sollte den Zweck des Frames und seine Zusammenhang mit anderen Frames erläutern. Eine Beschreibung ist erforderlich, wenn der Zweck und die Beziehung der Frames aus dem Wert der [**\_ UIA-Eigenschaft NamePropertyId nicht eindeutig**](uiauto-automation-element-propids.md) sind. |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Bereichssteuerfeld ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Bereichssteuerfeld ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                             |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Bereichssteuerelemente haben in der Regel keine statische Bezeichnung. Ist eine statische Beschriftung vorhanden, muss sie über diese Eigenschaft verfügbar gemacht werden.                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp Bereich** entspricht. Der Standardwert ist "pane" für en-US oder English (USA).                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Wert für diese Eigenschaft muss immer ein eindeutiger, präziser und aussagekräftiger Titel sein.                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von Bereichssteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support | Notizen                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Depends (Abhängig) | Implementieren [](uiauto-implementingdock.md) Sie das Dock-Steuerelementmuster, wenn das Bereichssteuerfeld angedockt werden kann.                                                                                          |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depends (Abhängig) | Implementieren [](uiauto-implementingscroll.md) Sie das Bildlauf-Steuerelementmuster, wenn für das Bereichssteuerfeld ein Bildlauf möglich ist.                                                                                    |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depends (Abhängig) | Implementieren Sie das [Steuerelementmuster Transformieren,](uiauto-implementingtransform.md) wenn das Bereichssteuerelement auf dem Bildschirm verschoben, geändert oder gedreht werden kann.                                              |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Nie   | Wenn das Element das [Window-Steuerelementmuster](uiauto-implementingwindow.md) implementieren muss, sollte das Steuerelement auf dem [Steuerelementtyp Fenster](uiauto-supportwindowcontroltype.md) basieren. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die bereichssteuerelemente unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                        | Hinweise                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                  | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)   | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)           | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)       | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)     | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)               | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a>Beispiel für Pane-Steuerelementtyp

Die folgende Abbildung zeigt ein Steuerelement, das den **Steuerelementtyp Bereich** implementiert.

![Screenshot: Beispiel für ein Bereichssteuerelement](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Benutzeroberflächenautomatisierung-Struktur – Steuerelementansicht</th>
<th>Benutzeroberflächenautomatisierung-Struktur – Inhaltsansicht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Bereich
<ul>
<li>Struktur (Scroll-Muster)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
</ul></li>
<li>Bereich
<ul>
<li>Bearbeiten (Scrollmuster)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Bereich
<ul>
<li>Struktur (Scroll-Muster)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
<li>Bereich
<ul>
<li>Bearbeiten (Scrollmuster)</li>
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

 

 




