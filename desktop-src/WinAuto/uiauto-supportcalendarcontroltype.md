---
title: Calendar-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den Calendar-Steuerelementtyp. Mit einem Kalender-Steuerelement kann der Benutzer das Datum leicht bestimmen und andere Datumsangaben auswählen.
ms.assetid: 886cf1a4-0e6f-4ae1-9dc4-e97ac6a22359
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für calendar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Calendar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für Calendar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für calendar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Calendar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,events für calendar-Steuerelementtyp
- Strukturstrukturen,Calendar-Steuerelementtyp
- properties,Calendar-Steuerelementtyp
- Steuerelementmuster,Calendar-Steuerelementtyp
- events,Calendar-Steuerelementtyp
- Unterstützung für den Calendar-Steuerelementtyp
- Calendar-Steuerelementtyp
- Steuerelementtypen,Struktur für Calendar-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für Calendar-Steuerelementtyp
- Steuerelementtypen,Unterstützung für Calendar
- Steuerelementtypen, Kalender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d51271fb2e9526bc293b9c5d36acc0a65b3b639
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482946"
---
# <a name="calendar-control-type"></a>Calendar-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **Calendar-Steuerelementtyp.** Mit einem Kalender-Steuerelement kann der Benutzer das Datum leicht bestimmen und andere Datumsangaben auswählen.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Calendar-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Kalendersteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

In der folgenden Tabelle werden ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung dargestellt, die sich auf Kalendersteuerelemente bezieht, und es wird beschrieben, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Kalender<ul><li>DataGrid<ul><li>Header (0 oder 1)<ul><li>HeaderItem (0 oder 7, Menge hängt davon ab, wie viele Tage in Spalten angezeigt werden)</li></ul></li><li>ListItem (die Menge hängt davon ab, wie viele Tage angezeigt werden)</li><li>Button (0 oder 2; für Seitenverwaltung der Kalenderansicht)</li></ul></li></ul></li></ul> | <ul><li>Kalender<ul><li>ListItem (die Menge hängt davon ab, wie viele Tage angezeigt werden)</li></ul></li></ul> | 




 

Kalendersteuerelemente können in vielen verschiedenen Formen in der Benutzeroberfläche dargestellt werden. Die einzigen Steuerelemente, die sich garantiert in der Steuerelementansicht der Benutzeroberflächenautomatisierung struktur befinden, sind das Datenraster, der Header, das Headerelement und das Listenelement-Steuerelement.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren  Wert oder Definition für den Calendar-Steuerelementtyp besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Hinweise                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebundenen Rechtecks angeklickt werden kann und das Element spezielle Treffertests ausführt, überschreiben Und stellen Sie einen klickbaren Punkt zur Verfügung. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Kalender** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Das Calendar-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Das Kalendersteuer steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss die Bezeichnung des Dokumentsteuerelements sein. In der Regel wird der Titel des Dokuments verwendet.                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem **Calendar-Steuerelementtyp** entspricht. Der Standardwert ist "calendar" für en-US oder English (USA).                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Das Kalendersteuer steuerelement ruft seinen Namen in der Regel ab dem aktuellen Datum ab.                                                                                                                                  |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von allen Kalendersteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                        | Unterstützung/Wert | Hinweise                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Erforderlich      | Das Kalendersteuerfeld unterstützt immer das [Grid-Steuerelementmuster,](uiauto-implementinggrid.md) da die Tage innerhalb eines Monats Elemente sind, durch die räumlich navigiert werden kann.                                                                                                                                                        |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depends (Abhängig)       | Die meisten Kalendersteuerelemente unterstützen seitenbezogenes Kippen der Ansicht. Das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) wird empfohlen, um die Pagingnavigation zu unterstützen.                                                                                                                                                    |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depends (Abhängig)       | Die meisten Kalendersteuerelemente behalten einen bestimmten Tag, Monat oder Jahr als Auswahl des Unterelements bei. Einige Kalender sind mehrfach auswählbar und andere nur einzeln auswählbar. Das Kalendersteuerelement mit auswählbaren Unterelementen sollte das [Selection-Steuerelementmuster](uiauto-implementingselection.md) unterstützen.                         |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Erforderlich      | Da das Calendar-Steuerelement für die Wochentage immer über einen Header in der Unterstruktur verfügt, muss das [Tabellensteuermuster](uiauto-implementingtable.md) unterstützt werden.                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | Nein            | Das [Value-Steuerelementmuster](uiauto-implementingvalue.md) ist für Kalendersteuerelemente nicht erforderlich, da das Element den Wert nicht direkt für das Steuerelement festlegen kann. Wenn dem Steuerelement ein bestimmtes Datum zugeordnet ist, [](uiauto-implementingselection.md) sollten die Informationen vom Selection-Steuerelementmuster bereitgestellt werden. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die kalendersteuerelemente unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                        | Hinweise                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                              |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                      |                                                                                                                                                                                                              |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                      | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.                                                                                     |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                  | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.                                                                                   |
| [**\_UIA-LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                              |
| [**UIA \_ MultipleViewCurrentViewPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)             | Wenn das Steuerelement die [**CurrentView-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview) des [MultipleView-Steuerelementmusters](uiauto-implementingmultipleview.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                              |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)   | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA \_ ScrollHorizontalViewSizePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)           | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)     | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA \_ ScrollVerticallyScrollablePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)       | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA \_ ScrollVerticalViewSizePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)               | Wenn das Steuerelement das [Bildlauf-Steuerelementmuster](uiauto-implementingscroll.md) unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            |                                                                                                                                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




