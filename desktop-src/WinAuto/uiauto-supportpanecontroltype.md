---
title: Bereichssteuerungstyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den Steuerelementtyp Bereich.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den Steuerelementtyp "Bereich"
- Benutzeroberflächenautomatisierung,Steuerelementtyp "Bereich"
- Benutzeroberflächenautomatisierung,Struktur für Bereich-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den Steuerelementtyp "Bereich"
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Steuerelementtyp "Bereich"
- Benutzeroberflächenautomatisierung,Ereignisse für den Steuerelementtyp "Bereich"
- Strukturstrukturen,Steuerelementtyp "Bereich"
- Eigenschaften,Steuerelementtyp "Bereich"
- Steuerelementmuster, Steuerelementtyp "Bereich"
- events,Pane-Steuerelementtyp
- Unterstützung für den Steuerelementtyp "Bereich"
- Pane-Steuerelementtyp
- Steuerelementtypen,Struktur für Bereich-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für den Steuerelementtyp "Bereich"
- Steuerelementtypen,Unterstützung für Bereich
- Steuerelementtypen, Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b335496d8d40d20ccc68f6bc2b048c87ff608dd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474256"
---
# <a name="pane-control-type"></a>Bereichssteuerungstyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **Steuerelementtyp Bereich.**

Der **Steuerelementtyp** Bereich ist für potenziell bildlauffähige Bereiche mit unterschiedlichen Inhalten. Es wird verwendet, um ein Objekt innerhalb eines Rahmens oder Dokumentfensters zu darstellen. Benutzer können zwischen Bereichssteuerelementen und innerhalb des Inhalts des aktuellen Bereichs navigieren. Bereichssteuerelemente stellen eine Gruppierungsebene dar, die niedriger als Fenster oder Dokumente, aber über einzelnen Steuerelementen ist. Der Benutzer kann je nach Kontext durch Drücken von TAB, F6 oder STRG+TAB zwischen den Bereichen navigieren.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Steuerelementtyp Bereich** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Bereichssteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Beispiel für Pane-Steuerelementtyp](#pane-control-type-example)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung struktur, die sich auf Bereichssteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Bereich</li></ul> | <ul><li>Bereich</li></ul> | 




 

Ein Bereichssteuerfeld wird immer in den Steuerelement- und Inhaltsansichten angezeigt. Machen Sie ein Layoutobjekt weder im Steuerelement noch in der Inhaltsansicht als Bereich verfügbar, wenn das Objekt nur für die visuelle Darstellung verwendet wird.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, deren Wert oder Definition für Bereichssteuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn eine bestimmte Tastenkombination den Fokus auf den Bereich erhält, sollten diese Informationen über diese Eigenschaft verfügbar gemacht werden.                                                                                                                                                                                                      |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                                                                                                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Diese Eigenschaft macht einen durch Klicken aktivierbaren Punkt des Bereichssteuerelements verfügbar, durch den der Bereich den Fokus erhält, wenn auf den Punkt geklickt wird.                                                                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Bereich**   |                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Der Hilfetext für Bereichssteuerelemente sollte den Zweck des Frames und seine Zusammenhang mit anderen Frames erläutern. Eine Beschreibung ist erforderlich, wenn der Zweck und die Beziehung der Frames aus dem Wert der [**\_ UIA-Eigenschaft NamePropertyId nicht eindeutig**](uiauto-automation-element-propids.md) sind. |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Bereichssteuerfeld ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Bereichssteuerfeld ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                             |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Bereichssteuerelemente haben in der Regel keine statische Bezeichnung. Ist eine statische Beschriftung vorhanden, muss sie über diese Eigenschaft verfügbar gemacht werden.                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp Bereich** entspricht. Der Standardwert ist "pane" für en-US oder English (USA).                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Wert für diese Eigenschaft muss immer ein eindeutiger, präziser und aussagekräftiger Titel sein.                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von Bereichssteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support | Notizen                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Depends (Abhängig) | Implementieren [](uiauto-implementingdock.md) Sie das Dock-Steuerelementmuster, wenn das Bereichssteuerfeld angedockt werden kann.                                                                                          |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depends (Abhängig) | Implementieren [](uiauto-implementingscroll.md) Sie das Bildlauf-Steuerelementmuster, wenn für das Bereichssteuerfeld ein Bildlauf möglich ist.                                                                                    |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depends (Abhängig) | Implementieren Sie [das Steuerelementmuster](uiauto-implementingtransform.md) Transformieren, wenn das Bereichssteuerfeld auf dem Bildschirm verschoben, seine Größe geändert oder gedreht werden kann.                                              |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Nie   | Wenn das Element das [](uiauto-implementingwindow.md) Window-Steuerelementmuster implementieren muss, sollte das Steuerelement auf dem [Steuerelementtyp Window](uiauto-supportwindowcontroltype.md) basieren. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die Bereichssteuerelemente unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                        | Hinweise                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                  | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)   | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollHorizontalViewSizePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)           | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticallyScrollablePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)       | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)     | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ ScrollVerticalViewSizePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)               | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a>Beispiel für Pane-Steuerelementtyp

Die folgende Abbildung veranschaulicht ein Steuerelement, das den **Steuerelementtyp Bereich** implementiert.

![Screenshot, der ein Beispiel für ein Bereichssteuerfeld zeigt](images/panexmpl.jpg)




| Benutzeroberflächenautomatisierung Struktur – Steuerelementansicht | Benutzeroberflächenautomatisierung Struktur – Inhaltsansicht | 
|-----------------------------------|-----------------------------------|
| <ul><li>Bereich<ul><li>Struktur (Scroll-Muster)<ul><li>TreeItem</li><li>...</li></ul></li></ul></li><li>Bereich<ul><li>Bearbeiten (Bildlaufmuster)</li></ul></li></ul> | <ul><li>Bereich<ul><li>Struktur (Scroll-Muster)<ul><li>TreeItem</li><li>...</li></ul></li><li>Bereich<ul><li>Bearbeiten (Bildlaufmuster)</li></ul></li></ul></li></ul> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




