---
title: Struktursteuertyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den Struktursteuertyp.
ms.assetid: 0fa8f308-7815-4561-a1ce-c5f5582861da
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den Struktursteuertyp
- Benutzeroberflächenautomatisierung,Struktursteuertyp
- Benutzeroberflächenautomatisierung,Struktur für Struktur-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für Den Struktur-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für Den Struktur-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den Struktursteuertyp
- Strukturstrukturen,Struktursteuertyp
- properties,Tree-Steuerelementtyp
- Steuerelementmuster,Struktur-Steuerelementtyp
- events,Tree-Steuerelementtyp
- Unterstützung für den Struktursteuersteuertyp
- Struktur-Steuerelementtyp
- Steuerelementtypen,Struktur für Struktur-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für Struktur-Steuerelementtyp
- Steuerelementtypen,Unterstützung für Tree
- Steuerelementtypen,Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7ac6330428c2e79fca1e9a51d4ca0f7c63e8a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472846"
---
# <a name="tree-control-type"></a>Struktursteuertyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **Struktursteuertyp.**

Der  Struktur-Steuerelementtyp wird für Container verwendet, deren Inhalt als Hierarchie von Knoten relevant ist, wie bei der Anzeige von Dateien und Ordnern im linken Bereich des Windows Explorers. Jeder Knoten kann andere Knoten enthalten, die als untergeordnete Knoten bezeichnet werden. Übergeordnete Knoten oder Knoten mit untergeordneten Knoten können in erweiterter oder reduzierter Form angezeigt werden. Das Windows-Steuerelement (wie durch WC [**\_ TREEVIEW**](/windows/desktop/Controls/common-control-window-classes)identifiziert) ist ein Beispiel für ein Steuerelement, das zum **Tree-Steuerelementtyp** gehört.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster  und Ereignisse für den Tree-Steuerelementtyp definiert. Die Benutzeroberflächenautomatisierung gelten für alle Strukturelementsteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf Struktursteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Struktur<ul><li>DataItem (beliebige Anzahl)</li><li>TreeItem (beliebige Anzahl)<ul><li>TreeItem (beliebige Anzahl)<ul><li>...</li></ul></li></ul></li><li>ScrollBar (0, 1, 2)</li></ul></li></ul> | <ul><li>Struktur<ul><li>DataItem (beliebige Anzahl)</li><li>TreeItem (beliebige Anzahl)<ul><li>TreeItem (beliebige Anzahl)<ul><li>...</li></ul></li></ul></li></ul></li></ul> | 




 

Die Steuerelementansicht der Benutzeroberflächenautomatisierung besteht aus:

-   Null von vielen Elementen im Container (Elemente können auf den [Steuerelementtypen TreeItem](uiauto-supporttreeitemcontroltype.md) oder [DataItem](uiauto-supportdataitemcontroltype.md) basieren).
-   Kein, ein oder zwei ScrollBar-Steuerelemente

Die Inhaltsansicht der Benutzeroberflächenautomatisierung besteht aus null oder vielen Elementen innerhalb des Containers (Elemente können auf den [Steuerelementtypen TreeItem](uiauto-supporttreeitemcontroltype.md) oder [DataItem](uiauto-supportdataitemcontroltype.md) basieren).

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren  Wert oder Definition für den Struktur-Steuerelementtyp besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Struktursteuerelemente verfügen über einen klickbaren Punkt, der bewirkt, dass die Struktur oder eines der Elemente im Strukturcontainer den Fokus erhält. Ein Struktursteuerelement kann nur dann einen klickbaren Punkt haben, wenn es möglich ist, auf eine Position in der Struktur zu klicken, ohne ein Element zu aktivieren oder den Fokus zu erhalten. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Struktur**   | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Struktursteuer steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                         |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Struktursteuer steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn dem Struktursteuerelement eine Bezeichnung zugeordnet ist, gibt diese Eigenschaft einen [**IUIAutomationElement-Zeiger**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für diese Bezeichnung zurück. Andernfalls gibt die -Eigenschaft einen NULL-Verweis zurück.                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Tree-Steuerelementtyp** entspricht. Der Standardwert ist "tree" für en-US oder Englisch (USA).                                                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Wert der Eigenschaft „Name“ eines Struktursteuerelements entspricht normalerweise dem Text, durch den das Steuerelement bezeichnet wird. Wenn keine Textbezeichnung enthalten ist, müssen Sie einen Wert für diese Eigenschaft bereitstellen.                                                                                                                        |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von allen Struktursteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                             | Unterstützung/Wert | Hinweise                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depends (Abhängig)       | Implementieren [](uiauto-implementingscroll.md) Sie das Bildlauf-Steuerelementmuster, wenn elemente im Strukturcontainer gescrollt werden können.                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Depends (Abhängig)       | Struktursteuerelemente, die einen Satz auswählbarer Elemente enthalten, müssen das [Selection-Steuerelementmuster](uiauto-implementingselection.md) implementieren. Sie muss nicht implementiert werden, wenn die Auswahl eines Elements dem Benutzer keine aussagekräftigen Informationen übermittelt. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Siehe Hinweise.    | Implementieren Sie diese Eigenschaft, wenn das Struktursteuerelement eine Mehrfachauswahl unterstützt (meistens ist dies nicht der Fall).                                                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Siehe Hinweise.    | Der Wert dieser Eigenschaft ist verfügbar, wenn für das Steuerelement die Auswahl eines Elements erforderlich ist.                                                                                                                                               |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von allen Struktursteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                        | Hinweise                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                      | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                  | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)   | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)           | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)     | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)       | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)               | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            | Wenn das Steuerelement das [Selection-Steuerelementmuster](uiauto-implementingselection.md) unterstützt, muss es dieses Ereignis unterstützen.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 
