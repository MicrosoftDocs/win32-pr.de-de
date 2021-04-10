---
title: Struktur Steuerungstyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den-Struktur Steuerungstyp.
ms.assetid: 0fa8f308-7815-4561-a1ce-c5f5582861da
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für Struktur Steuerungstyp
- Benutzeroberflächenautomatisierungs, Struktur Steuerungstyp
- UI-Automatisierung, Baumstruktur für Struktur Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Eigenschaften für Struktur Steuerungstyp
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den Struktur Steuerungstyp
- UI-Automatisierung, Ereignisse für Struktur Steuerungstyp
- Baumstrukturen, Struktur Steuerungstyp
- Eigenschaften, Struktur Steuerungstyp
- Steuerelement Muster, Struktur Steuerungstyp
- Ereignisse, Struktur Steuerungstyp
- Unterstützung für den Struktur Steuerungstyp
- Struktur-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Struktur Steuerungstyp
- Steuerelement Typen, Steuerelement Muster für den Struktur Steuerungstyp
- Steuerelement Typen, Unterstützung für Tree
- Steuerelement Typen, Tree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4679af32f974cd1611cbd31c71e66db62631391
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039428"
---
# <a name="tree-control-type"></a>Struktur Steuerungstyp

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den-Struktur **Steuerungstyp** .

Der **Struktur Steuerungstyp** wird für Container verwendet, deren Inhalt als Hierarchie von Knoten relevant ist, wie die Art und Weise, wie Dateien und Ordner im linken Fensterbereich von Windows-Explorer angezeigt werden. Jeder Knoten kann andere Knoten enthalten, die als untergeordnete Knoten bezeichnet werden. Übergeordnete Knoten oder Knoten mit untergeordneten Knoten können in erweiterter oder reduzierter Form angezeigt werden. Das Windows-Strukturansicht-Steuerelement (wie von [**WC \_ TreeView**](/windows/desktop/Controls/common-control-window-classes)identifiziert) ist ein Beispiel für ein Steuerelement, **das zum Struktur Steuerungstyp** gehört.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse **für den Struktur** Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Strukturelement-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Struktur Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Struktur
<ul>
<li>DataItem (beliebige Anzahl)</li>
<li>TreeItem (beliebige Anzahl)
<ul>
<li>TreeItem (beliebige Anzahl)
<ul>
<li>...</li>
</ul></li>
</ul></li>
<li>ScrollBar (0, 1, 2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Struktur
<ul>
<li>DataItem (beliebige Anzahl)</li>
<li>TreeItem (beliebige Anzahl)
<ul>
<li>TreeItem (beliebige Anzahl)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Die Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur besteht aus folgendem:

-   NULL von vielen Elementen innerhalb des Containers (Elemente können auf den Steuerelement Typen [TreeItem](uiauto-supporttreeitemcontroltype.md) oder [DataItem](uiauto-supportdataitemcontroltype.md) basieren).
-   Kein, ein oder zwei ScrollBar-Steuerelemente

Die Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur besteht aus null oder mehreren Elementen innerhalb des Containers (Elemente können auf den Steuerelement Typen [TreeItem](uiauto-supporttreeitemcontroltype.md) oder [DataItem](uiauto-supportdataitemcontroltype.md) basieren).

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition **für den Struktur Steuerungstyp** besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                               |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                   |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Struktur Steuerelemente haben einen durch Klicken aktivierbaren Punkt, der bewirkt, dass die Struktur oder eines der Elemente im Struktur Container den Fokus erhält. Ein Struktur Steuerelement kann nur dann einen klickbaren Punkt haben, wenn es möglich ist, auf eine Position in der Struktur zu klicken, ohne dass ein Element ausgewählt oder der Fokus empfangen werden soll. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Struktur**   | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                                                                                                              |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Struktur Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                         |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Struktur Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                         |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                  |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn dem Struktur Steuerelement eine Bezeichnung zugeordnet ist, gibt diese Eigenschaft einen [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Zeiger für diese Bezeichnung zurück. Andernfalls gibt die-Eigenschaft einen NULL-Verweis zurück.                                                                          |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Struktur Steuerelement** -Typ entspricht. Der Standardwert ist "Tree" für en-US oder Englisch (USA).                                                                                                                                                             |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Wert der Eigenschaft „Name“ eines Struktursteuerelements entspricht normalerweise dem Text, durch den das Steuerelement bezeichnet wird. Wenn keine Text Bezeichnung vorhanden ist, müssen Sie einen Wert für diese Eigenschaft angeben.                                                                                                                        |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Struktur Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                             | Unterstützung/Wert | Notizen                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depends (Abhängig)       | Implementieren Sie das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster, wenn für Elemente im Struktur Container ein Bildlauf ausgeführt werden kann.                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Depends (Abhängig)       | Struktur Steuerelemente, die einen Satz auswählbarer Elemente enthalten, müssen das [Selection](uiauto-implementingselection.md) -Steuerelement Muster implementieren. Sie muss nicht implementiert werden, wenn die Auswahl eines Elements keine aussagekräftigen Informationen für den Benutzer vermittelt. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Siehe Hinweise.    | Implementieren Sie diese Eigenschaft, wenn das Struktursteuerelement eine Mehrfachauswahl unterstützt (meistens ist dies nicht der Fall).                                                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Siehe Hinweise.    | Der Wert dieser Eigenschaft ist verfügbar, wenn für das Steuerelement die Auswahl eines Elements erforderlich ist.                                                                                                                                               |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die alle Struktur Steuerelemente unterstützen müssen Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                        | Notizen                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                      |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                      | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                  | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.   | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.           | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.     | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.       | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.               | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA- \_ Auswahl \_ invalidatedeventid**](uiauto-event-ids.md)                                                            | Wenn das Steuerelement das [Selection](uiauto-implementingselection.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.     |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 