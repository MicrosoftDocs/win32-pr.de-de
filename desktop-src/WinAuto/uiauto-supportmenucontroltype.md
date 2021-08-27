---
title: Typ des Menüsteuerelements
description: Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den Steuerelementtyp Menü.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung des Steuerelementtyps "Menü"
- Benutzeroberflächenautomatisierung,Steuerelementtyp "Menü"
- Benutzeroberflächenautomatisierung,Struktur für Menüsteuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für Den Menü-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für Den Menü-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den Steuerelementtyp "Menü"
- Strukturstrukturen, Menüsteuerelementtyp
- Eigenschaften,Menüsteuerelementtyp
- Steuerelementmuster, Menüsteuerelementtyp
- Ereignisse, Menüsteuerelementtyp
- Unterstützung für den Steuerelementtyp "Menü"
- Menü-Steuerelementtyp
- Steuerelementtypen,Struktur für Menüsteuerelementtyp
- Steuerelementtypen, Steuerelementmuster für den Steuerelementtyp "Menü"
- Steuerelementtypen,Unterstützung für Menü
- Steuerelementtypen,Menü
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d86d5aad29519bca4e9cfe03da4b6f0e9ccaeb9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468077"
---
# <a name="menu-control-type"></a>Typ des Menüsteuerelements

Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den **Steuerelementtyp Menü.**

Ein Menüsteuerelement ermöglicht die hierarchische Organisation von Elementen, die Befehlen und Ereignishandlern zugeordnet sind. In einer typischen Microsoft Windows-Anwendung enthält eine Menüleiste mehrere Menüschaltflächen (z. B. **Datei,** **Bearbeiten** und **Fenster),** und jede Menüschaltfläche zeigt ein Menü an. Ein Menü enthält eine Sammlung von Menüelementen (z. B. **Neu**, **Öffnen** und **Schließen**), die erweitert werden können, um weitere Menüelemente anzuzeigen, oder auf die geklickt werden kann, um eine bestimmte Aktion auszuführen.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Steuerelementtyp Menu** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Menüsteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf Menüsteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Menü<ul><li>MenuItem (1 oder viele)</li></ul><ul><li>Andere Steuerelemente (0 oder viele)</li></ul></li></ul> | <ul><li>Menü<ul><li>MenuItem (1 oder viele)</li></ul><ul><li>Andere Steuerelemente (0 oder viele)</li></ul></li></ul> | 




 

Menüsteuerelemente werden immer in der Steuerelementansicht und in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur angezeigt. Menüsteuerelemente sollten unter dem Steuerelement angezeigt werden, auf das ihre Informationen verweisen. Benutzeroberflächenautomatisierung Clients können auf [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) lauschen, um sicherzustellen, dass sie konsistent Informationen abrufen, die von Menüsteuerelementen übermittelt werden. Kontextmenü-Steuerelemente sind ein besonderer Fall. Sie können als untergeordnete Elemente des Desktops oder eines Anwendungsfensters der obersten Ebene angezeigt werden.

Ein Menüsteuerelement kann andere Steuerelemente, z. B. Bearbeitungssteuerelemente und Kombinationsfelder, in seiner Struktur enthalten. Diese zusätzlichen Steuerelemente entsprechen den "anderen Steuerelementen", die in der vorherigen Tabelle in den Steuerelement- und Inhaltsansichten aufgeführt sind.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für den **Steuerelementtyp Menü** besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                      | Wert      | Hinweise                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)           | **Menü**   |                                                                                                                                                                         |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md) | TRUE       | Das Menüsteuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md) | TRUE       | Das Menüsteuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)               | NULL       | Für ein typisches Menüsteuerelement wird keine Bezeichnung erwartet.                                                                                                                    |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Für das Menüsteuerelement muss keine **Name-Eigenschaft** festgelegt werden, oder es kann den gleichen Namen wie das zugeordnete Steuerelement aufweisen, z. B. ein Menüelement, das das Untermenü geöffnet hat. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

Für den Menu-Steuerelementtyp gibt es keine erforderlichen Steuerelementmuster.

## <a name="required-events"></a>Erforderliche Ereignisse

Menüsteuerelemente müssen das [**UIA \_ MenuOpenedEventId-Ereignis**](uiauto-event-ids.md) auslösen, wenn sie auf dem Bildschirm angezeigt werden. Das **UIA \_ MenuOpenedEventId-Ereignis** enthält den Text des Steuerelements. Das [**UIA \_ MenuClosedEventId-Ereignis**](uiauto-event-ids.md) muss ausgelöst werden, wenn ein Menü vom Bildschirm verschwindet.

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Menüsteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**\_UIA-MenüClosedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**\_UIA-MenüOpenedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




