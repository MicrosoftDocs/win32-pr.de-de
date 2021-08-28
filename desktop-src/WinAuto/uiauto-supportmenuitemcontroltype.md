---
title: MenuItem-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den MenuItem-Steuerelementtyp.
ms.assetid: a6a04489-8e28-44ff-a3b0-ecf19c24daab
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den MenuItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,MenuItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für MenuItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den MenuItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den MenuItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Events für menuItem-Steuerelementtyp
- Strukturstrukturen,MenuItem-Steuerelementtyp
- properties,MenuItem-Steuerelementtyp
- Steuerelementmuster,MenuItem-Steuerelementtyp
- events,MenuItem-Steuerelementtyp
- Unterstützung für den MenuItem-Steuerelementtyp
- MenuItem-Steuerelementtyp
- Steuerelementtypen,Struktur für MenuItem-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für MenuItem-Steuerelementtyp
- Steuerelementtypen,Unterstützung für MenuItem
- Steuerelementtypen,MenuItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a48b94d7fc18cb9a8a6fe924fb73a250ab28708
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482511"
---
# <a name="menuitem-control-type"></a>MenuItem-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung-Unterstützung für den **MenuItem-Steuerelementtyp.**

Ein Menüsteuerelement ermöglicht die hierarchische Organisation von Elementen, die Befehlen und Ereignishandlern zugeordnet sind. In einer Windows-Anwendung enthält eine Menüleiste mehrere Menüelemente (z. B. Datei **,** **Bearbeiten** und **Fenster**), und jedes Menüelement zeigt ein Menü an. Ein Menü enthält eine Sammlung von Menüelementen (z. B. **Neu**, **Öffnen** und **Schließen**), die erweitert werden können, um weitere Menüelemente anzuzeigen, oder auf die geklickt werden kann, um eine bestimmte Aktion auszuführen.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **MenuItem-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Menüelementsteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Legacyprobleme](#legacy-issues)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf Menüelementsteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>MenuItem „Hilfe“ (?)<ul><li>Menü (Untermenü des Menüelements Hilfe)<ul><li>MenuItem „Hilfethemen“</li><li>MenuItem „Info“</li></ul></li></ul></li></ul> | <ul><li>MenuItem „Hilfe“ (?)<ul><li>MenuItem „Hilfethemen“</li><li>MenuItem „Info“</li></ul></li></ul> | 




 

Die Steuerelementansicht des Menüelement-Steuerelements verfügt über die Benutzeroberflächenautomatisierung oben gezeigte Strukturstruktur. Beachten Sie, dass das Menüelement für **Hilfe** auf der Menüleiste hinzugefügt wurde, um die Struktur besser zu veranschaulichen.

Für die Inhaltsansicht fehlt **Menu** in der Benutzeroberflächenautomatisierung Struktur, da es dem Endbenutzer keine aussagekräftigen Informationen vermittelt.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren Wert oder Definition für den **MenuItem-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Hinweise                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein. Ordnen Sie **die AutomationId-Eigenschaft** einem Menüelement zu, wenn bekannt ist, dass das Element über verschiedene Instanzen der Benutzeroberfläche hinweg konsistent ist. Wenn das Menüelement dynamisch aufgefüllt und nicht vorhersagbar ist, lassen Sie die **AutomationId-Eigenschaft** leer. |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebundenen Rechtecks angeklickt werden kann und das Element spezielle Treffertests ausführt, überschreiben Und stellen Sie einen klickbaren Punkt zur Verfügung.                                                                                                                                                                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuItem** |                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Das Menüelement-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Das Menüelement-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp MenuItem** entspricht. Der Standardwert ist "Menüelement" für en-US oder Englisch (USA).                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Der Name des Menüelement-Steuerelements ist der Text, mit dem es bezeichnet wird.                                                                                                                                                                                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von Menüelementsteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                                |
|-------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Wenn das Steuerelement erweitert oder reduziert werden kann, implementieren Sie [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider).                            |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depends (Abhängig) | Wenn das Steuerelement eine einzelne Aktion oder einen einzelnen Befehl ausgeführt, implementieren [**Sie IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider).                                     |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depends (Abhängig) | Wenn das Steuerelement verwendet wird, um aus einer Liste von Optionen unter Menüelementen auszuwählen, implementieren [**Sie ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider). |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depends (Abhängig) | Wenn das Steuerelement eine Option darstellt, die aktiviert oder deaktiviert werden kann, implementieren [**Sie IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).                       |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Menüelementsteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                                | Hinweise                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Wenn das Steuerelement [](uiauto-implementinginvoke.md) das Invoke-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.                 |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                              | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.         |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                          | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ \_ SelectionItem-ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ \_ SelectionItem-ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ \_ SelectionItem-ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ Das ToggleToggleStatePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)                                 | Wenn das Steuerelement das [Umschalten-Steuerelementmuster](uiauto-implementingtoggle.md) unterstützt, muss es dieses Ereignis unterstützen.                 |



 

## <a name="legacy-issues"></a>Legacyprobleme

Für Microsoft Win32-Menüelemente wird das [Umschalt-Steuerelementmuster](uiauto-implementingtoggle.md) nur unterstützt, wenn ein Menüelement aktiviert ist, und es ist möglich, programmgesteuert zu bestimmen, ob Unterstützung für das Umschalten-Steuerelementmuster erforderlich ist. Da ein Win32-Menüelement nicht verfügbar macht, ob es aktiviert werden kann, wird das Invoke-Steuerelementmuster unterstützt, wenn das Menüelement nicht aktiviert ist. Das Invoke-Steuerelementmuster wird immer unterstützt, auch für Menüelemente, die nur zur Unterstützung des Toggle-Steuerelementmusters erforderlich sind. Dies ist so, dass Clients nicht verwechselt [](uiauto-implementinginvoke.md) werden, wenn ein Menüelement, das das Invoke-Steuerelementmuster unterstützt hat (wenn das Menüelement deaktiviert wurde), dieses Muster nicht mehr unterstützt, wenn es aktiviert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




