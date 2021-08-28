---
title: TreeItem-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den TreeItem-Steuerelementtyp.
ms.assetid: 03d8a2a7-0b9a-41f8-a9d3-cebba9c25c63
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den TreeItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,TreeItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den TreeItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den TreeItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den TreeItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Events für den TreeItem-Steuerelementtyp
- Strukturstrukturen,TreeItem-Steuerelementtyp
- properties,TreeItem-Steuerelementtyp
- Steuerelementmuster,TreeItem-Steuerelementtyp
- events,TreeItem-Steuerelementtyp
- Unterstützung für den TreeItem-Steuerelementtyp
- TreeItem-Steuerelementtyp
- Steuerelementtypen,Struktur für TreeItem-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für TreeItem-Steuerelementtyp
- Steuerelementtypen,Unterstützung für TreeItem
- Steuerelementtypen,TreeItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07f55ab6d9df8af46253a2428964bdf4ded64c4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482926"
---
# <a name="treeitem-control-type"></a>TreeItem-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **TreeItem-Steuerelementtyp.**

Der **TreeItem-Steuerelementtyp** stellt einen Knoten in einem Strukturcontainer dar. Jeder Knoten kann andere Knoten enthalten, die als untergeordnete Knoten bezeichnet werden. Übergeordnete Knoten oder Knoten mit untergeordneten Knoten können in erweiterter oder reduzierter Form angezeigt werden.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **TreeItem-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Strukturelementsteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf Strukturelementsteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>TreeItem<ul><li>CheckBox (0 oder 1)</li><li>Bild (0 oder 1)</li><li>Button (0 oder 1)</li><li>TreeItem (beliebige Anzahl)</li></ul></li></ul> | <ul><li>TreeItem<ul><li>TreeItem (beliebige Anzahl)</li></ul></li></ul> | 




 

Strukturelement-Steuerelemente können in der Inhaltsansicht der Struktur 0 (null) oder mehr Benutzeroberflächenautomatisierung haben. Wenn das Strukturelement-Steuerelement über Funktionen verfügt, die über die funktionen hinausgehen, die in den unten aufgeführten Steuerelementmustern verfügbar gemacht werden, sollte das Steuerelement auf dem [DataItem-Steuerelementtyp](uiauto-supportdataitemcontroltype.md) basieren.

Reduzierte Strukturelemente werden erst in der Steuerelement- oder Inhaltsansicht angezeigt, wenn sie erweitert und sichtbar werden (oder in die Ansicht gescrollt werden können).

Die Steuerelementansicht kann weitere Details für ein Steuerelement enthalten, wie etwa für ein zugeordnetes Bild oder eine Schaltfläche. Ein Element in einer Gliederungsansicht kann beispielsweise ein Bild sowie eine Schaltfläche zum Erweitern oder Reduzieren der Gliederung enthalten. Diese Detailobjekte werden nicht in der Inhaltsansicht angezeigt, da die Informationen bereits durch das übergeordnete Strukturelement dargestellt werden.

Strukturelemente, die vom Bildschirm gescrollt werden, werden sowohl in den Steuerelement- als auch in den Inhaltsansichten der Benutzeroberflächenautomatisierung-Struktur angezeigt und müssen die [**IUIAutomationElement::CurrentIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen) -Eigenschaft (oder [**CachedIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen)) auf **TRUE** festlegen.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren Wert oder Definition für den **TreeItem-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Hinweise                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Diese Eigenschaft muss eine Position zurückgeben, die bewirkt, dass das Strukturelement den Auswahlzustand ändert oder den Fokus erhalten kann.                                                                                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TreeItem** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Das Strukturelement-Steuerelement ist immer in der Inhaltsansicht der Struktur Benutzeroberflächenautomatisierung enthalten.                                                                                                       |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Das Strukturelement-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                       |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                     |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Siehe Hinweise.   | Diese Eigenschaft gibt an, ob ein Strukturelement-Steuerelement vom Bildschirm gescrollt wird.                                                                                                               |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Siehe Hinweise.   | Wenn das Steuerelement den Status enthält, der dynamisch aktualisiert wird, muss diese Eigenschaft unterstützt werden, damit eine Hilfstechnologie Updates empfangen kann, wenn sich der Status des Elements ändert. |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise.   | Wenn das Strukturelementsteuerelement ein visuelles Symbol verwendet, um anzugeben, dass es sich um einen bestimmten Elementtyp handelt, muss diese Eigenschaft unterstützt werden und muss den Elementtyp angeben.                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | **NULL**     | Strukturelement-Steuerelemente sind selbstbezeichnend.                                                                                                                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge für den Steuerelementtyp „TreeItem“. Der Standardwert ist "Tree item" für en-US oder English (USA).                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Diese Eigenschaft macht den für jedes Strukturelement-Steuerelement angezeigten Text verfügbar.                                                                                                                          |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von allen Strukturelementsteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                                  | Unterstützung/Wert                     | Hinweise                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)                 | Erforderlich                          | Alle Strukturelemente müssen das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) unterstützen, da alle Elemente erweitert oder reduziert werden können.                                           |
| [**Expandcollapsestate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) | Erweitert, reduziert oder Blattknoten | Strukturelemente sind Blattknoten, wenn sie nicht erweitert oder reduziert werden.                                                                                                                                |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                                 | Depends (Abhängig)                           | Implementieren Sie das [Invoke-Steuerelementmuster,](uiauto-implementinginvoke.md) wenn das Strukturelement einen Befehl ausführen kann.                                                                                     |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)                         | Depends (Abhängig)                           | Implementieren Sie das [ScrollItem-Steuerelementmuster,](uiauto-implementingscrollitem.md) wenn der Strukturcontainer das [Scroll-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt.                         |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                   | Depends (Abhängig)                           | Implementieren Sie das [SelectionItem-Steuerelementmuster,](uiauto-implementingselectionitem.md) wenn eine aktive Auswahl möglich ist, die beibehalten wird, wenn der Benutzer zum Strukturcontainer zurückkehrt. |
| [**Selectioncontainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)    | Erforderlich                          | Diese Eigenschaft macht denselben Container für alle Elemente im Container verfügbar.                                                                                                                      |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Strukturelementsteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                                | Hinweise                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                              |                                                                                                                                |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md) |                                                                                                                                |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Wenn das Steuerelement [](uiauto-implementinginvoke.md) das Invoke-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.               |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                              | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                          | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.     |
| [**UIA \_ ItemStatusPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                            | Wenn das Steuerelement die [**ItemStatus-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.      |
| [**UIA \_ Das MultipleViewCurrentViewPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)                     | Wenn das Steuerelement das [MultipleView-Steuerelementmuster](uiauto-implementingmultipleview.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Das NamePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                                        |                                                                                                                                |
| [**UIA \_ \_ SelectionItem-ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ \_ SelectionItem-ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ \_ SelectionItem-ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                |
| [**UIA \_ Das ToggleToggleStatePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)                                 | Wenn das Steuerelement das [Umschalten-Steuerelementmuster](uiauto-implementingtoggle.md) unterstützt, muss es dieses Ereignis unterstützen.               |
| [**UIA \_ ValueValuePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)                                               | Wenn das Steuerelement das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützt, muss es dieses Ereignis unterstützen.                 |



 

## <a name="remarks"></a>Hinweise

Wenn ein Strukturelement über andere Unterelemente als untergeordnete Gliederungsknoten verfügt, muss der Anbieter die untergeordneten Objektinformationen sorgfältig und eindeutig behandeln. In Benutzeroberflächenautomatisierung wird die Struktur von der Strukturhierarchie selbst behandelt. Wenn mindestens ein untergeordnetes Element ohne Gliederungsknoten vorkommt, werden die Unterschiede zwischen ihnen und den tatsächlichen untergeordneten Gliederungsknoten schwerwiegend mehrdeutig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




