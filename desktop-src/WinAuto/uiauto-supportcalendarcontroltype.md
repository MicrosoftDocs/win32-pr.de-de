---
title: Typ des Kalender Steuer Elements
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer ungstyp "Kalender". Ein Kalender Steuerelement ermöglicht es dem Benutzer, das Datum leicht zu bestimmen und andere Datumsangaben auszuwählen.
ms.assetid: 886cf1a4-0e6f-4ae1-9dc4-e97ac6a22359
keywords:
- Benutzeroberflächenautomatisierungs-Unterstützung für Kalender Steuerelement
- Benutzeroberflächenautomatisierungs, Calendar-Steuerelement
- Benutzeroberflächenautomatisierungs-Struktur für Kalender Steuerelement
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Steuerelement Kalender
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Kalender Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Ereignisse für Kalender Steuerelement
- Struktur Strukturen, Calendar-Steuerelement Typen
- Eigenschaften, Calendar-Steuerelement Typen
- Steuerelement Muster, Calendar-Steuerelement Typen
- Ereignisse, Calendar-Steuerelement Typen
- Unterstützung für Kalender Steuerelement
- Calendar-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Kalender Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den Calendar-Steuer ungstyp
- Steuerelement Typen, Unterstützung für Kalender
- Steuerelement Typen, Kalender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef936848f764c6937bfe36e6ed919f0a88dac78c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037618"
---
# <a name="calendar-control-type"></a>Typ des Kalender Steuer Elements

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer ungstyp " **Kalender** ". Ein Kalender Steuerelement ermöglicht es dem Benutzer, das Datum leicht zu bestimmen und andere Datumsangaben auszuwählen.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den Steuer ungstyp " **Kalender** " definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Kalender Steuerelemente, bei denen das UI-Framework/die Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Kalender Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Steuerelementansicht</th>
<th>Inhaltsansicht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Kalender
<ul>
<li>DataGrid
<ul>
<li>Header (0 oder 1)
<ul>
<li>Header Item (0 oder 7, Menge hängt davon ab, wie viele Tage in Spalten angezeigt werden)</li>
</ul></li>
<li>ListItem (die Menge hängt davon ab, wie viele Tage angezeigt werden)</li>
<li>Button (0 oder 2; für Seitenverwaltung der Kalenderansicht)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Kalender
<ul>
<li>ListItem (die Menge hängt davon ab, wie viele Tage angezeigt werden)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Kalendersteuerelemente können in vielen verschiedenen Formen in der Benutzeroberfläche dargestellt werden. Die einzigen Steuerelemente, die garantiert in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten sind, sind das Datenraster, Header, Header Element und Listenelement-Steuerelemente.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den Steuer ungstyp " **Calendar** " besonders relevant ist Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Notizen                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Kalender** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                        |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Das Kalender Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                               |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Das Kalender Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                               |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss die Bezeichnung des Dokumentsteuerelements sein. In der Regel wird der Titel des Dokuments verwendet.                                                                                |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem Steuerelement des **Kalender** Typs entspricht. Der Standardwert ist "Calendar" für en-US oder Englisch (USA).                                                               |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Das Kalender Steuerelement erhält seinen Namen in der Regel aus dem aktuellen Datum.                                                                                                                                  |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Kalender Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                        | Unterstützung/Wert | Notizen                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Erforderlich      | Das Kalender Steuerelement unterstützt immer das [Raster](uiauto-implementinggrid.md) -Steuerelement Muster, da die Tage innerhalb eines Monats Elemente sind, die räumlich navigiert werden können.                                                                                                                                                        |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depends (Abhängig)       | Die meisten Kalendersteuerelemente unterstützen seitenbezogenes Kippen der Ansicht. Das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster wird empfohlen, um Paging-Navigation zu unterstützen.                                                                                                                                                    |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depends (Abhängig)       | Die meisten Kalender Steuerelemente behalten einen bestimmten Tag, einen bestimmten Monat oder ein bestimmtes Jahr als Auswahl des unter Elements bei. Einige Kalender sind mehrfach wählbar und können nur mit nur einem einzelnen ausgewählt werden. Ein Kalender Steuerelement mit auswählbaren unter Elementen sollte das [Auswahl](uiauto-implementingselection.md) Steuerelement Muster unterstützen.                         |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Erforderlich      | Da das Kalender Steuerelement immer über einen Header in seiner Unterstruktur für die Wochentage verfügt, muss das [Table](uiauto-implementingtable.md) -Steuerelement Muster unterstützt werden.                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | Nein            | Das [value](uiauto-implementingvalue.md) -Steuerelement Muster ist für Kalender Steuerelemente nicht erforderlich, da der Wert nicht direkt für das Steuerelement festgelegt werden kann. Wenn dem Steuerelement ein bestimmtes Datum zugeordnet ist, sollten die Informationen über das [Auswahl](uiauto-implementingselection.md) Steuerelement Muster bereitgestellt werden. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Kalender Steuerelementen Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                        | Notizen                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                              |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                      |                                                                                                                                                                                                              |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                      | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.                                                                                     |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                  | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.                                                                                   |
| [**UIA \_ layoutinvalidatedeventid**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                              |
| [**UIA \_ Multipleviewcurrentviewpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview) -Eigenschaft des [MultipleView](uiauto-implementingmultipleview.md) -Steuerelement Musters unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                              |
| [**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.   | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.           | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.     | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.       | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.               | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                             |
| [**UIA- \_ Auswahl \_ invalidatedeventid**](uiauto-event-ids.md)                                                            |                                                                                                                                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




