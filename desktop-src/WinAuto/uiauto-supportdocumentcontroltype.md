---
title: Dokumentsteuersteuertyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den Dokument-Steuerelementtyp.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den Steuerelementtyp "Dokument"
- Benutzeroberflächenautomatisierung,Dokumentsteuertyp
- Benutzeroberflächenautomatisierung,Struktur für Dokument-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den Steuerelementtyp "Dokument"
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Steuerelementtyp "Dokument"
- Benutzeroberflächenautomatisierung,Events für den Steuerelementtyp "Dokument"
- Strukturstrukturen,Dokumentsteuertyp
- eigenschaften,Dokumentsteuertyp
- Steuerelementmuster, Dokumentsteuertyp
- events,Document-Steuerelementtyp
- Unterstützung für den Dokumentsteuersteuertyp
- Document-Steuerelementtyp
- Steuerelementtypen,Struktur für Dokumentsteuertyp
- Steuerelementtypen,Steuerelementmuster für Dokumentsteuertyp
- Steuerelementtypen,Unterstützung für Dokument
- Steuerelementtypen,Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0dffa06939ce3a35570d22334b75f5c60360800dedc080d92dafc1c5a40a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899500"
---
# <a name="document-control-type"></a>Dokumentsteuersteuertyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den **Dokument-Steuerelementtyp.**

Mithilfe von Dokumentsteuerelementen kann ein Benutzer mehrere Seiten Text anzeigen und bearbeiten. Im Gegensatz zu Bearbeitungssteuerelementen, die nur eine einfache Zeile mit unformatiertem Text unterstützen, können Dokumentsteuerelemente Text hosten, der mit vielen Stilen und Formaten formatiert ist.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Steuerelementtyp Dokument** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Dokumentsteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung struktur, die dokumentsteuerelemente betrifft, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur der Benutzeroberflächenautomatisierung finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)



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
<li>Dokument
<ul>
<li>Varies</li>
</ul></li>
</ul></td>
<td><ul>
<li>Dokument
<ul>
<li>Varies</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren Wert oder Definition für Dokumentsteuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Hinweise                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Struktur der Benutzeroberflächenautomatisierung sein.                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Das Dokument hat einen klickbaren Punkt, über den veranlasst werden kann, dass das Dokument oder eines seiner Elemente im Dokumentcontainer den Fokus erhält.                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Dokument** |                                                                                                                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Das Dokumentsteuer steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Das Dokumentsteuer steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss die Bezeichnung des Dokumentsteuerelements sein. In der Regel wird der Titel des Dokuments verwendet.                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp Dokument** entspricht. Der Standardwert ist "document" für en-US oder Englisch (USA).            |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Das Dokumentsteuer steuerelement ruft seinen Namen in der Regel aus dem Dateinamen ab, aus dem es geladen wird. Dieser wird häufig im Titel eines umgebenden Fensters oder Rahmens angezeigt. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von Dokumentsteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                  | Unterstützung/Wert | Hinweise                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | Depends (Abhängig)       | Das Dokumentsteuerelement kann einen Bereich umfassen, der größer ist als der Bereich des Viewports. Das Steuerelement sollte das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützen, wenn der Inhalt scrollbar ist.                                                                                                                              |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Erforderlich      | Alle Dokumentsteuerelemente müssen das [Text-Steuerelementmuster](uiauto-implementingtextandtextrange.md) unterstützen.                                                                                                                                                                                                                |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Depends (Abhängig)       | Während Benutzeroberflächenautomatisierung-Clients [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) verwenden können, um Textinformationen zu einem Dokument zu erhalten, benötigen sie das Value-Steuerelementmuster, um den inneren Wert festlegen zu können. [](uiauto-implementingvalue.md) Ein einfacher Texteintrag ist nur über das Value-Steuerelementmuster möglich. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die Dokumentsteuerelemente unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                        | Hinweise                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                      | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                  | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)   | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)           | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)       | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)     | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)               | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            | Wenn das Steuerelement das [Selection-Steuerelementmuster](uiauto-implementingselection.md) unterstützt, muss es dieses Ereignis unterstützen.     |
| [**UIA \_ Text \_ TextSelectionChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| [**UIA \_ ValueValuePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)                                       | Wenn das Steuerelement das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützt, muss es dieses Ereignis unterstützen.             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




