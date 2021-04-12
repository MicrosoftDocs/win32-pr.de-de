---
title: TabItem-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den TabItem-Steuer Elementtyp.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für TabItem-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, TabItem-Steuer Elementtyp
- UI-Automatisierung, Baumstruktur für TabItem-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für den TabItem-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für TabItem-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Ereignisse für TabItem-Steuer Elementtyp
- Baumstrukturen, TabItem-Steuer Elementtyp
- Eigenschaften, TabItem-Steuer Elementtyp
- Steuerelement Muster, TabItem-Steuer Elementtyp
- Ereignisse, TabItem-Steuer Elementtyp
- Unterstützung für den TabItem-Steuer Elementtyp
- TabItem-Steuer Elementtyp
- Steuerelement Typen, Baumstruktur für TabItem-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den TabItem-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für TabItem
- Steuerelement Typen, TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8f9f900240318de8629048f242cd755994c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207192"
---
# <a name="tabitem-control-type"></a>TabItem-Steuer Elementtyp

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **TabItem** -Steuer Elementtyp.

Ein Registerkartenelement-Steuerelement (TabItem) wird in einem Registerkarten-Steuerelement (Tab) als das Steuerelement verwendet, über das eine bestimmte Seite ausgewählt wird, die in einem Fenster angezeigt werden soll.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **TabItem** -Steuer Elementtyp definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Registerkarten Element-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Registerkarten Element-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>TabItem
<ul>
<li>Bild (0 oder 1)</li>
<li>Text</li>
<li>Bereich
<ul>
<li>Verschiedene Steuerelemente (0 oder mehr)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>TabItem
<ul>
<li>Bereich
<ul>
<li>Verschiedene Steuerelemente (0 oder mehr)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **TabItem** -Steuer Elementtyp besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert       | Notizen                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.  | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.  | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                    |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.  | Das Registerkartenelement-Steuerelement muss einen klickbaren Punkt haben, über den veranlasst wird, dass das Element ausgewählt ist.                                                   |
| [**UIA \_ controllerforpropertyid**](uiauto-automation-element-propids.md)               | Siehe Hinweise.  | Diese Eigenschaft kann als Zeiger auf den zugeordneten Registerkartenbereich verwendet werden. Dies ist nützlich, wenn der Bereich keinen Bereich als untergeordnetes Element des Registerkartenelement-Objekts hosten kann. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **TabItem** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                               |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE        | Das Registerkarten Element-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                      |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE        | Das Registerkarten Element-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                      |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.  | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                   |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Null        | Das Registerkartenelement-Steuerelement hat keine statische Beschriftung.                                                                                     |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.  | Lokalisierte Zeichenfolge für den Steuer Elementtyp " **TabItem** ". Der Standardwert ist "Registerkarten Element" für en-US oder Englisch (USA).       |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.  | Das Registerkarten Element-Steuerelement ist selbst beschriftet.                                                                                                          |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Registerkarten-Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                 | Support  | Notizen                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Erforderlich | Das Registerkarten Element-Steuerelement muss [**iuiautomationselectionitempattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern)unterstützen. |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Nie    | Das Registerkarten Element-Steuerelement unterstützt niemals [**iuiautomationinvokepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).             |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die Registerkarten Element-Steuerelemente zur Unterstützung Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                     | Notizen                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                        |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.   |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                   | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.               | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**](uiauto-event-ids.md) |                                                                                                                            |
| [**UIA \_ SelectionItem \_ elementselectedebug**](uiauto-event-ids.md)                         |                                                                                                                            |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




