---
title: Headersteuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den Header-Steuerelementtyp.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für Header-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Header-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für Header-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für Header-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für Header-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für Header-Steuerelementtyp
- Strukturstrukturen, Headersteuerelementtyp
- Properties, Header-Steuerelementtyp
- Steuerelementmuster, Headersteuerelementtyp
- Ereignisse, Headersteuerelementtyp
- Unterstützung für header-Steuerelementtyp
- Header-Seuerelementtyp
- Steuerelementtypen, Struktur für Header-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für Header-Steuerelementtyp
- Steuerelementtypen,Unterstützung für Header
- Steuerelementtypen,Header
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472a0d7185fa3c2b2dc1dc7593afd106008890bb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482510"
---
# <a name="header-control-type"></a>Headersteuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **Header-Steuerelementtyp.**

Ein Headersteuerelement stellt einen visuellen Container für Beschriftungen von Zeilen oder Spalten bereit, die Informationen enthalten.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Header-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Headersteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die header-Steuerelemente betrifft, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Header<ul><li>HeaderItem (1 oder mehr)</li></ul></li></ul> | (Nicht vorhanden) | 




 

Headersteuerelemente verfügen in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur immer über mindestens ein untergeordnetes Steuerelement.

Headersteuerelemente weisen in der Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur 0 untergeordnete Elemente auf.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für Headersteuerelemente besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert                                                            | Hinweise                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.                                                       | Der Wert dieser Eigenschaft muss für alle Steuerelemente in einer Anwendung eindeutig sein.                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.                                                       | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.                                                       | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umschließenden Rechtecks klickbar ist und das Element spezielle Treffertests durchführt, überschreibt und stellt einen klickbaren Punkt bereit. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Header**                                                       |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE                                                            | Das Headersteuerelement ist nicht in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE                                                             | Das Headersteuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.                                                       | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL                                                             | Headersteuerelemente haben keine statische Bezeichnung.                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.                                                       | Der Standardwert ist "header" für en-US oder Englisch (USA).                                                                                                                                  |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.                                                       | Das Headersteuerelement benötigt einen Namen, wenn mehrere Zeilen- oder Spaltenüberschriften vorhanden sind. Dadurch werden die Informationen für den Header (Überschrift) gekennzeichnet.                                              |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | **OrientationType \_ Horizontal** oder **OrientationType \_ Vertical** | Der Wert dieser Eigenschaft macht die Position des Headersteuerelements verfügbar– unabhängig davon, ob es sich um einen Zeilenheader (**OrientationType \_ Horizontal**) oder einen Spaltenheader (**OrientationType \_ Vertical**) handelt.                 |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die für Headersteuerelemente unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support | Notizen                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depends (Abhängig) | Implementieren [](uiauto-implementingtransform.md) Sie das Transformationssteuerelementmuster, wenn die Größe des Headersteuerelements geändert werden kann. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Headersteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
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

 

 




