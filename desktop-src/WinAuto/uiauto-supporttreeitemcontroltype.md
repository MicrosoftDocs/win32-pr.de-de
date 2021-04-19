---
title: TreeItem-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den TreeItem-Steuerelement Typen.
ms.assetid: 03d8a2a7-0b9a-41f8-a9d3-cebba9c25c63
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für den TreeItem-Steuerelement Typen
- UI-Automatisierung, TreeItem-Steuerelement Typen
- UI-Automatisierung, Baumstruktur für TreeItem-Steuerelement Typen
- UI-Automatisierung, Eigenschaften für den TreeItem-Steuerelement Typen
- UI-Automatisierung, Steuerelement Muster für den TreeItem-Steuerelement Typen
- UI-Automatisierung, Ereignisse für den TreeItem-Steuerelement Typen
- Baumstrukturen, TreeItem-Steuerelement Typen
- Eigenschaften, TreeItem-Steuerelement Typen
- Steuerelement Muster, TreeItem-Steuerelement Typen
- Ereignisse, TreeItem-Steuerelement Typen
- Unterstützung für den TreeItem-Steuerelement Typen
- TreeItem-Steuerelement Typen
- Steuerelement Typen, Baumstruktur für TreeItem-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den TreeItem-Steuerelement Typen
- Steuerelement Typen, Unterstützung für TreeItem
- Steuerelement Typen, TreeItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c837428a0aeef900779cfccf0a28b46aa276369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342291"
---
# <a name="treeitem-control-type"></a>TreeItem-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **TreeItem** -Steuerelement Typen.

Der **TreeItem** -Steuerelement-Typ stellt einen Knoten innerhalb eines Struktur Containers dar. Jeder Knoten kann andere Knoten enthalten, die als untergeordnete Knoten bezeichnet werden. Übergeordnete Knoten oder Knoten mit untergeordneten Knoten können in erweiterter oder reduzierter Form angezeigt werden.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **TreeItem** -Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Strukturelement-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Strukturelement-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>TreeItem
<ul>
<li>CheckBox (0 oder 1)</li>
<li>Bild (0 oder 1)</li>
<li>Button (0 oder 1)</li>
<li>TreeItem (beliebige Anzahl)</li>
</ul></li>
</ul></td>
<td><ul>
<li>TreeItem
<ul>
<li>TreeItem (beliebige Anzahl)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Strukturelement-Steuerelemente können in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur keine oder mehrere untergeordnete Strukturelement Elemente aufweisen. Wenn das Strukturelement-Steuerelement über mehr Funktionen verfügt, die in den unten aufgeführten Steuerelement Mustern verfügbar gemacht werden, sollte das Steuerelement auf dem [DataItem](uiauto-supportdataitemcontroltype.md) -Steuer Elementtyp basieren.

Reduzierte Strukturelemente werden erst dann in der Steuerelement Ansicht oder in der Inhaltsansicht angezeigt, wenn Sie erweitert und sichtbar werden (oder in die Ansicht gescrollt werden kann).

Die Steuerelementansicht kann weitere Details für ein Steuerelement enthalten, wie etwa für ein zugeordnetes Bild oder eine Schaltfläche. Ein Element in einer Gliederungsansicht kann beispielsweise ein Bild sowie eine Schaltfläche zum Erweitern oder Reduzieren der Gliederung enthalten. Diese Detail Objekte werden nicht in der Inhaltsansicht angezeigt, da die Informationen bereits vom übergeordneten Strukturelement dargestellt werden.

Strukturelemente, die sich auf dem Bildschirm befinden, werden sowohl in der Steuerelement-als auch in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt, und die [**iuiautomationelement:: accesstisoffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen) (oder [**cachedisoffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen))-Eigenschaft muss auf **true** festgelegt sein.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **TreeItem** -Steuerelement Typ besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Notizen                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                  |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                      |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Diese Eigenschaft muss einen Speicherort zurückgeben, der bewirkt, dass das Strukturelement den Auswahl Zustand ändert oder fokussiert wird.                                                                                   |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **TreeItem** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                 |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**     | Das Strukturelement-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                       |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**     | Das Strukturelement-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                       |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                     |
| [**UIA \_ isoffscreenpropertyid**](uiauto-automation-element-propids.md)                   | Siehe Hinweise.   | Diese Eigenschaft gibt an, ob ein Strukturelement-Steuerelement vom Bildschirm entfernt wird.                                                                                                               |
| [**UIA \_ itemstatuspropertyid**](uiauto-automation-element-propids.md)                     | Siehe Hinweise.   | Wenn das Steuerelement den Status enthält, der dynamisch aktualisiert wird, muss diese Eigenschaft unterstützt werden, damit eine Hilfstechnologie Updates empfangen kann, wenn sich der Status des Elements ändert. |
| [**UIA \_ itemtypepropertyid**](uiauto-automation-element-propids.md)                         | Siehe Hinweise.   | Wenn das Strukturelement-Steuerelement mit einem visuellen Symbol anzeigt, dass es sich um einen bestimmten Elementtyp handelt, muss diese Eigenschaft unterstützt werden und muss den Elementtyp angeben.                                   |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | **NULL**     | Strukturelement-Steuerelemente sind selbstbezeichnend.                                                                                                                                                         |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge für den Steuerelementtyp „TreeItem“. Der Standardwert ist "Tree Item" für en-US oder Englisch (USA).                                                           |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Diese Eigenschaft macht den für jedes Strukturelement-Steuerelement angezeigten Text verfügbar.                                                                                                                          |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Strukturelement-Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                                  | Unterstützung/Wert                     | Notizen                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)                 | Erforderlich                          | Alle Strukturelemente müssen das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützen, da alle Elemente erweitert oder reduziert werden können.                                           |
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) | Erweitert, reduziert oder Blattknoten | Strukturelemente sind Blattknoten, wenn Sie nicht erweitert oder reduziert werden.                                                                                                                                |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                                 | Depends (Abhängig)                           | Implementieren Sie das [Aufruf](uiauto-implementinginvoke.md) Steuerelement Muster, wenn das Strukturelement einen Befehl ausführen kann.                                                                                     |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)                         | Depends (Abhängig)                           | Implementieren Sie das [ScrollItem](uiauto-implementingscrollitem.md) -Steuerelement Muster, wenn der Struktur Container das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt.                         |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                   | Depends (Abhängig)                           | Implementieren Sie das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster, wenn eine aktive Auswahl möglich ist, die beibehalten wird, wenn der Benutzer zum Struktur Container zurückkehrt. |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)    | Erforderlich                          | Diese Eigenschaft macht den gleichen Container für alle Elemente innerhalb des Containers verfügbar.                                                                                                                      |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Strukturelement-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                                | Notizen                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                                   |                                                                                                                                |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                              |                                                                                                                                |
| [**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                                |
| [**UIA \_ aufrufen \_ invokedebug-ID**](uiauto-event-ids.md)                                                                                  | Wenn das Steuerelement das [Aufruf](uiauto-implementinginvoke.md) Steuerungs Muster unterstützt, muss es dieses Ereignis unterstützen.               |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                              | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                          | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.     |
| [**UIA \_ Itemstatuspropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                            | Wenn das Steuerelement die [**ItemStatus**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.      |
| [**UIA \_ Multipleviewcurrentviewpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                     | Wenn das Steuerelement das [MultipleView](uiauto-implementingmultipleview.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                                        |                                                                                                                                |
| [**UIA \_ SelectionItem \_ elementaddecodto selectioneventid**](uiauto-event-ids.md)                                    | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**](uiauto-event-ids.md)                            | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ SelectionItem \_ elementselectedebug**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                               |                                                                                                                                |
| [**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                                 | Wenn das Steuerelement das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.               |
| [**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                                               | Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                 |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein Strukturelement andere unter Elemente als untergeordnete Gliederungs Knoten enthält, muss der Anbieter die untergeordneten Objektinformationen sorgfältig und eindeutig verarbeiten. In der Benutzeroberflächen Automatisierung wird die Baumstruktur von der Struktur Hierarchie selbst behandelt. Wenn Sie über einen oder mehrere untergeordnete Knoten ohne Gliederung verfügen, werden die Unterschiede zwischen Ihnen und den tatsächlichen untergeordneten Gliederungs Knoten ernsthaft mehrdeutig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




