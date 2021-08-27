---
title: TitleBar-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den TitleBar-Steuerelementtyp. Ein Titelleisten-Steuerelement stellt einen Titel oder eine Beschriftungsleiste in einem Fenster dar.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den TitleBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,TitleBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den TitleBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den TitleBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den TitleBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Events für den TitleBar-Steuerelementtyp
- Strukturstrukturen,TitleBar-Steuerelementtyp
- properties,TitleBar-Steuerelementtyp
- Steuerelementmuster, TitleBar-Steuerelementtyp
- events,TitleBar-Steuerelementtyp
- Unterstützung für den TitleBar-Steuerelementtyp
- TitleBar-Steuerelementtyp
- Steuerelementtypen,Struktur für TitleBar-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für den TitleBar-Steuerelementtyp
- Steuerelementtypen,Unterstützung für TitleBar
- Steuerelementtypen, TitleBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e3d3ed0c4a3abc995afab7aec4aa89d02542e2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473356"
---
# <a name="titlebar-control-type"></a>TitleBar-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **TitleBar-Steuerelementtyp.** Ein Titelleisten-Steuerelement stellt einen Titel oder eine Beschriftungsleiste in einem Fenster dar.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **TitleBar-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Titelleisten-Steuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf Titelleistensteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>TitleBar<ul><li>Menü (0 oder 1)</li><li>Schaltfläche (beliebige Anzahl)</li></ul></li></ul> | (Nicht zutreffend; das Titelleisten-Steuerelement hat keinen Inhalt)) | 




 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die eigenschaften Benutzeroberflächenautomatisierung, deren Wert oder Definition für den **TitleBar-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Hinweise                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Der von dieser Eigenschaft verfügbar gemachte Wert muss sämtliche darin enthaltenen Steuerelemente umfassen.                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebundenen Rechtecks angeklickt werden kann und das Element spezielle Treffertests ausführt, überschreiben Und stellen Sie einen klickbaren Punkt zur Verfügung. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Titlebar** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE        | Das Titelleisten-Steuerelement ist nie in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Das Titelleisten-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | FALSE        | Ein Titelleisten-Steuerelement hat nie den Tastaturfokus.                                                                                                                                                        |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depends (Abhängig)      | Ein Titelleisten-Steuerelement gibt einen Wert zurück, je nachdem, ob er auf dem Bildschirm sichtbar ist.                                                                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.   | Ein Titelleisten-Steuerelement verfügt in der Regel nicht über eine Bezeichnung.                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge für den Steuerelementtyp „TitleBar“. Der Standardwert ist "Titelleiste" für en-US oder Englisch (USA).                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | ""           | Eine Titelleiste ist kein Inhalt. Die Textinformationen werden durch den Namen des übergeordneten Fensters verfügbar gemacht.                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

Der **TitleBar-Steuerelementtyp** ist nicht erforderlich, um Steuerelementmuster zu unterstützen. Seine Funktionalität wird über [](uiauto-implementingwindow.md) das Fenster-Steuerelementmuster des [Steuerelementtyps Fenster](uiauto-supportwindowcontroltype.md) verfügbar gemacht.

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von Titelleisten-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




