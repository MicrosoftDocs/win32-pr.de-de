---
title: MenuBar-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den MenuBar-Steuerelementtyp.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den MenuBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,MenuBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den MenuBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den MenuBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den MenuBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Events für den MenuBar-Steuerelementtyp
- Strukturstrukturen,MenuBar-Steuerelementtyp
- Properties,MenuBar-Steuerelementtyp
- Steuerelementmuster, MenuBar-Steuerelementtyp
- events,MenuBar-Steuerelementtyp
- Unterstützung für den MenuBar-Steuerelementtyp
- MenuBar-Steuerelementtyp
- Steuerelementtypen,Struktur für MenuBar-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für MenuBar-Steuerelementtyp
- Steuerelementtypen,Unterstützung für MenuBar
- Steuerelementtypen, MenuBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558a734d69a9197b3e0a8d6c5655405074878bca
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468157"
---
# <a name="menubar-control-type"></a>MenuBar-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **MenuBar-Steuerelementtyp.**

Menüleisten-Steuerelemente sind ein Beispiel für Steuerelemente, die den **MenuBar-Steuerelementtyp** implementieren. Menüleisten geben dem Benutzer die Möglichkeit, Befehle und Optionen zu aktivieren, die in einer Anwendung enthalten sind.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **MenuBar-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Menüleisten-Steuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf Menüleisten-Steuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>MenuBar<ul><li>MenuItem (1 oder mehr)</li><li>Andere Steuerelemente (0 oder viele)</li></ul></li></ul> | <ul><li>Nicht zutreffend<ul><li>MenuItem (1 oder mehr)</li><li>Andere Steuerelemente (0 oder viele)</li></ul></li></ul> | 




 

Ein Menüleisten-Steuerelement wird immer in der Steuerelementansicht, aber nicht in der Inhaltsansicht angezeigt, da es dem Endbenutzer normalerweise keine aussagekräftigen Informationen vermittelt (es sei denn, die Anwendung enthält mehr als eine Menüleiste).

Benutzeroberflächenautomatisierung clients können auf das [**UIA \_ MenuModeStartEventId-Ereignis**](uiauto-event-ids.md) lauschen, um sicherzustellen, dass sie konsistent benachrichtigt werden, wenn die Benutzeroberfläche in den Menümodus eintritt. Wenn sich die Anwendung im Menümodus befindet, können alle Tastatureingaben für die Menünavigation erfasst  werden (wenn Sie z. B. "s" eingeben, kann das Menü Speichern aufgerufen werden, anstatt das Zeichen im Anwendungsclientbereich eintippen zu müssen). Das **UIA \_ MenuModeStartEventId-Ereignis** muss dem ersten [**\_ UIA-MenuOpenedEventId-Ereignis**](uiauto-event-ids.md) voran stehen, um die logische Konsistenz sicherzustellen. Das [**UIA \_ MenuModeEndEventId-Ereignis**](uiauto-event-ids.md) folgt auf das letzte [**UIA \_ MenuClosedEventId-Ereignis.**](uiauto-event-ids.md) Wenn Sie auf ein Menüelement klicken, wird möglicherweise sofort das **UIA \_ MenuModeStartEventId-Ereignis** ausgelöst, gefolgt von einem **UIA \_ MenuOpenedEventId-Ereignis.**

Ein Menüleisten-Steuerelement kann innerhalb seiner Struktur andere Steuerelemente enthalten, z. B. Bearbeitungssteuerelemente und Kombinationsfelder. Diese weiteren Steuerelemente sind oben in der Inhalts- und der Steuerelementansicht mit „Andere Steuerelemente“ gemeint.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, deren Wert oder Definition für den **MenuBar-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert       | Hinweise                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | NULL        | Menüleisten verfügen in der Regel nicht über Zugriffstasten.                                                                                                                                                                                          |
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | „ALT“       | Wenn Sie die ALT-TASTE drücken, sollte in der Regel der Fokus auf die Menüleiste in der Anwendung gedrückt werden.                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.  | Der von dieser Eigenschaft verfügbar gemachte Wert muss sämtliche darin enthaltenen Steuerelemente umfassen.                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuBar** |                                                                                                                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE       | Das Menüleisten-Steuerelement ist nicht in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Das Menüleisten-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE        | Menüleisten-Steuerelemente können den Tastaturfokus erhalten, da die in ihnen enthaltenen Steuerelemente den Tastaturfokus übernehmen können.                                                                                                                                      |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Siehe Hinweise.  | Der Wert dieser Eigenschaft ist hängt davon ab, ob das Steuerelement auf dem Bildschirm angezeigt werden kann.                                                                                                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Menüleisten-Steuerelemente verfügen in der Regel nicht über eine Bezeichnung.                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.  | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp MenuBar** entspricht. Der Standardwert ist "Menüleiste" für en-US oder Englisch (USA).                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.  | Das Menüleisten-Steuerelement muss nur dann einen Namen haben, wenn eine Anwendung mehrere Menüleisten hat. Wenn in einer Anwendung mehrere Menüleisten enthalten sind, verwenden Sie diese Eigenschaft, um unterscheidende Namen verfügbar zu machen, z. B. "Formatierung" oder "Lining". |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Depends (Abhängig)     | Diese Eigenschaft gibt an, ob das Menüleisten-Steuerelement horizontal oder vertikal verläuft.                                                                                                                                                            |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von Menüleisten-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Wenn das Steuerelement erweitert oder reduziert werden kann, muss es das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) implementieren. |
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Depends (Abhängig) | Wenn das Steuerelement an verschiedene Teile des Bildschirms angedockt werden kann, muss es das [Dock-Steuerelementmuster](uiauto-implementingdock.md) implementieren.   |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Depends (Abhängig) | Wenn die Größe des Steuerelements geändert, gedreht oder verschoben werden kann, muss es das [Steuerelementmuster Transformieren](uiauto-implementingtransform.md) implementieren.      |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Menüleistensteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                                | Hinweise                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                              | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.         |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                          | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




