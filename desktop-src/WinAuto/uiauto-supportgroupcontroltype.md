---
title: Gruppensteuersteuertyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den Steuerelementtyp "Gruppe".
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den Steuerelementtyp "Gruppe"
- Benutzeroberflächenautomatisierung,Steuerelementtyp "Gruppe"
- Benutzeroberflächenautomatisierung,Struktur für den Steuerelementtyp "Gruppe"
- Benutzeroberflächenautomatisierung,Eigenschaften für den Steuerelementtyp "Gruppe"
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Steuerelementtyp "Gruppe"
- Benutzeroberflächenautomatisierung,Ereignisse für den Steuerelementtyp "Gruppe"
- Strukturstrukturen,Gruppensteuertyp
- Eigenschaften,Gruppensteuertyp
- Steuerelementmuster, Gruppensteuertyp
- events,Group control type
- Unterstützung für den Steuerelementtyp "Gruppe"
- Gruppe-Steuerelementtyp
- Steuerelementtypen,Struktur für Steuerelementtyp "Gruppe"
- Steuerelementtypen,Steuerelementmuster für den Steuerelementtyp "Gruppe"
- Steuerelementtypen,Unterstützung für Gruppe
- Steuerelementtypen, Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe0cee05f7132a35c8dd3f998ae9af5a89ac2a71
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477746"
---
# <a name="group-control-type"></a>Gruppensteuersteuertyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **Steuerelementtyp "Gruppe".**

Ein Gruppensteuerpunkt stellt einen Knoten innerhalb einer Hierarchie dar. Der **Steuerelementtyp** Gruppe erstellt eine Trennung in der Benutzeroberflächenautomatisierung, sodass elemente, die zusammen gruppiert werden, eine logische Division innerhalb der Benutzeroberflächenautomatisierung haben.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Steuerelementtyp Gruppe** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Gruppensteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung struktur, die sich auf Gruppensteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Group<ul><li>Beliebig viele Steuerelemente</li></ul></li></ul> | <ul><li>Group<ul><li>Beliebig viele Steuerelemente</li></ul></li></ul> | 




 

Gruppensteuerelemente enthalten in der Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen, die sich darunter in der Unterstruktur finden, einschließlich der [Steuerelementtypen ListItem,](uiauto-supportlistitemcontroltype.md) [TreeItem](uiauto-supporttreeitemcontroltype.md)und [DataItem.](uiauto-supportdataitemcontroltype.md) Da es sich bei einem Gruppensteuer steuerelement um einen generischen Container handelt, ist es möglich, dass sich jede Art von Steuerelement unter dem Gruppensteuersystem in der Struktur befindet.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, deren Wert oder Definition für die Gruppensteuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebundenen Rechtecks angeklickt werden kann und das Element spezielle Treffertests ausführt, überschreiben Und stellen Sie einen klickbaren Punkt zur Verfügung. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Gruppe**  |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Gruppensteuer steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Gruppensteuer steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Gruppensteuerelemente sind in der Regel selbstbezeichnend. In diesen Fällen wird NULL **zurückgegeben.** Wenn die Gruppe über eine statische Textbezeichnung verfügt, geben Sie die Bezeichnung als Wert der **LabeledBy-Eigenschaft** zurück.                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp Gruppe** entspricht. Der Standardwert ist "group" für en-US oder Englisch (USA).                                                                     |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Das Gruppensteuerelement ruft seinen Namen in der Regel aus dem Text ab, mit dem das Steuerelement beschriftet ist.                                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die für den Steuerelementtyp Gruppe **unterstützt** werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Gruppensteuerelemente, die zum Ein- oder Ausblenden von Informationen verwendet werden können, müssen das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) unterstützen. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die von Gruppensteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                                | Hinweise                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                              |                                                                                                                                                  |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement das [Steuerelementmustermuster ExpandCollapse](uiauto-implementingexpandcollapse.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                              | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.                         |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                          | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.                       |
| [**UIA \_ ToggleToggleStatePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)                                 | Wenn das Steuerelement das [Umschalten-Steuerelementmuster](uiauto-implementingtoggle.md) unterstützt, muss es dieses Ereignis unterstützen.                                 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




