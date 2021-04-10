---
title: Typ des semanticzoom-Steuer Elements
description: Dieses Thema enthält Informationen zur Benutzeroberflächenautomatisierungs-Unterstützung für den semanticzoom-Steuerelement.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Benutzeroberflächenautomatisierungs-Unterstützung für semanticzoom-Steuerelement Typen
- Benutzeroberflächenautomatisierungs-Steuerelement (semanticzoom)
- UI-Automatisierung, Baumstruktur für semanticzoom-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für semanticzoom-Steuerelement Typen
- UI-Automatisierung, Steuerelement Muster für semanticzoom-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für semanticzoom-Steuerelement Typen
- Struktur Strukturen, semanticzoom-Steuerelement Typen
- Eigenschaften, semanticzoom-Steuerelement Typen
- Steuerelement Muster, semanticzoom-Steuerelement Typen
- Ereignisse, semanticzoom-Steuerelement Typen
- Unterstützung für semanticzoom-Steuerelement Typen
- Typ des semanticzoom-Steuer Elements
- Steuerelement Typen, Baumstruktur für semanticzoom-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für semanticzoom-Steuerelement Typen
- Steuerelement Typen, Unterstützung für semanticzoom
- Steuerelement Typen, semanticzoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4712aa4f10489081b1b5d0f69fed849080bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101682"
---
# <a name="semanticzoom-control-type"></a>Typ des semanticzoom-Steuer Elements

Dieses Thema enthält Informationen zur Benutzeroberflächenautomatisierungs-Unterstützung für den **semanticzoom** -Steuerelement.

Der semantische Zoom ist eine Technik, die in Windows 8 eingeführt wurde, um große Mengen verwandter Daten oder Inhalte in einer einzelnen Ansicht, z. b. ein Foto Album, eine APP-Liste oder ein Adressbuch, darzustellen und zu navigieren. Der semantische Zoom verwendet zwei verschiedene Modi für die Klassifizierung und Darstellung der Inhalte. Der Low-Level *(oder vergrößern*)-Modus zeigt Elemente in einer flachen, "gesamten" Struktur an; und der Modus für hohe Ebene (oder *Zoom*) zeigt Elemente in Gruppen an, sodass der Benutzer schnell navigieren und den Inhalt durchsuchen kann. Beispielsweise kann das Zoomen einer Liste von Städten zu einer Liste von Bundesstaaten wechseln, die diese Städte enthalten. Das Zoomen einer Liste von Programmen kann zu einer Liste logischer Programm Gruppen wechseln.

Weitere Informationen zum semantischen Zoom, der speziell für Windows Store-Apps verwendet wird, finden Sie unter [Richtlinien für den semantischen Zoom](/windows/uwp/controls-and-patterns/semantic-zoom).

Das Verwendungs Modell des **semanticzoom** -Steuerelement Typs ist insofern ungewöhnlich, als es vor allem für den programmgesteuerten Zugriff vorhanden ist. Microsoft UI Automation-Clients können das semantische Zoom Steuerelement überwachen und bearbeiten, um den Zoomzustand der Liste zu steuern. Benutzer, die keine Hilfstechnologie verwenden, würden das semantische Zoom Steuerelement normalerweise direkt über Touchgesten oder Tastenkombinationen bearbeiten.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **semanticzoom** -Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle semantischen Zoom Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster und-Eigenschaften](#required-control-patterns-and-properties)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für den **semanticzoom** -Steuerelement Typen sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>List
<ul>
<li>SemanticZoom
<ul>
<li>ListItem (beliebige Anzahl)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>List
<ul>
<li>ListItem (beliebige Anzahl)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Oder:



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
<li>SemanticZoom
<ul>
<li>List
<ul>
<li>ListItem (beliebige Anzahl)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>List
<ul>
<li>ListItem (beliebige Anzahl)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Steuerelemente, die den Steuerelement **semanticzoom** implementieren, besonders relevant sind. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Benutzeroberflächenautomatisierungs-Eigenschaft</th>
<th>Wert</th>
<th>Notizen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></td>
<td>Siehe Hinweise.</td>
<td>Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.</td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></td>
<td>Siehe Hinweise.</td>
<td>Das äußere Rechteck, das das gesamte Steuerelement enthält.</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></td>
<td>Siehe Hinweise.</td>
<td>Wenn das Listen Steuerelement über einen klickbaren Punkt verfügt (ein Punkt, auf den geklickt werden kann, damit die Liste den Fokus erhält), muss dieser Punkt durch diese Eigenschaft verfügbar gemacht werden. Wenn der Wert der <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> -Eigenschaft <strong>true</strong>ist, führt der Versuch, diese Eigenschaft abzurufen, zu <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> Fehler.</td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></td>
<td><strong>SemanticZoom</strong></td>

</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></td>
<td>TRUE</td>

</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></td>
<td>TRUE</td>

</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></td>
<td>false</td>

</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></td>
<td>Siehe Hinweise.</td>
<td>Wenn eine statische Text Bezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></td>
<td>Siehe Hinweise.</td>
<td>Eine lokalisierte Zeichenfolge, die dem Typ des <strong>semanticzoom</strong> -Steuer Elements entspricht. Der Standardwert ist der &quot; semantische Zoom &quot; für en-US oder Englisch (USA).
<blockquote>
[!Note]<br />
Einige Frameworks verkettet dies als &quot; semanticzoom &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></td>
<td>Siehe Hinweise.</td>
<td>Eine leere Zeichenfolge ist zulässig, oder es kann ein hilfreicher Name bereitgestellt werden, solange Sie nicht den Begriff Semantik Zoom enthält, wodurch die Kombination aus Steuerungstyp und-Name verwirrend wäre.</td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a>Erforderliche Steuerelement Muster und-Eigenschaften

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Semantik Zoom Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                  | Unterstützung/Wert | Notizen                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Depends (Abhängig)       | Semantik Zoom Steuerelemente unterstützen das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster, um die Aktivierung oder Deaktivierung des Zoom zuzulassen. Objekt [**Status \_ Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) entspricht dem flachen, dem gesamten up-Zustand und dem Wert von " [**degglestate" \_ in**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) entspricht der Ansicht "hoch", "Zoomansicht". |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Semantik Zoom Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.    |                                                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Wenn eine Benutzeroberfläche über eine sichtbare Schaltfläche verfügt, um das semantische Zoom Steuerelement Verhalten umzuschalten, sollte diese Schaltfläche keinen **semanticzoom** -Steuer ungstyp aufweisen. Dies ist kontraintuitiv, aber der **semanticzoom** -Steuer ungstyp kennzeichnet den Container des Zoom Inhalts, nicht eine Schaltfläche, die den Zoom steuert. (Eine solche Schaltfläche könnte einfach als [Button](uiauto-supportbuttoncontroltype.md) -Steuerelement mit dem [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster dargestellt werden.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

