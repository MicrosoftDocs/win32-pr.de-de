---
title: ToolTip-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuerelement-Steuerelement Typ. QuickInfo-Steuerelemente sind Popup Fenster, die Text enthalten.
ms.assetid: 810f85a9-4d3b-4ceb-bd2c-bf70e8712ae2
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für QuickInfo
- Benutzeroberflächenautomatisierungs, QuickInfo-Steuerelement
- Benutzeroberflächenautomatisierungs-Struktur für QuickInfo-Steuerelement Typen
- UI-Automatisierung, Eigenschaften für QuickInfo-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für QuickInfo-Steuerelement
- UI-Automatisierung, Ereignisse für QuickInfo-Steuerelement Typen
- Baumstrukturen, QuickInfo-Steuerelement Typen
- Eigenschaften, QuickInfo-Steuerelement Typen
- Steuerelement Muster, QuickInfo-Steuerelement Typen
- Ereignisse, QuickInfo-Steuerelement Typen
- Unterstützung für ToolTip-Steuerelement Typen
- ToolTip-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für QuickInfo-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für QuickInfo-Steuerelement Typen
- Steuerelement Typen, Unterstützung für QuickInfo
- Steuerelement Typen, QuickInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3c9f227faf5dd9844f809dac43cf160371490d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710307"
---
# <a name="tooltip-control-type"></a>ToolTip-Steuerelement Typen

Dieses Thema enthält **Informationen zur Unterstützung der Microsoft** -Benutzeroberflächen Automatisierung für den Steuerelement-Steuerelement Typ. QuickInfo-Steuerelemente sind Popup Fenster, die Text enthalten.

In den folgenden Abschnitten **werden die erforderliche** Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den QuickInfo-Steuerelement Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle QuickInfo-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für QuickInfo-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>ToolTip
<ul>
<li>Text (beliebige Anzahl)</li>
<li>Bild (beliebige Anzahl)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ToolTip</li>
</ul></td>
</tr>
</tbody>
</table>



 

QuickInfo-Steuerelemente werden nur in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt, wenn Sie den Tastaturfokus erhalten können. Andernfalls sind alle QuickInfo-Informationen über die [**iuiautomationelement:: accessthelptext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (oder [**cachedhelptext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext))-Eigenschaft des Elements verfügbar, auf das die QuickInfo verweist.

Quick Infos sollten unter dem Steuerelement angezeigt werden, auf das Ihre Informationen verweisen. Clients müssen auf die [**UIA \_ tooltipopenedeventid**](uiauto-event-ids.md) lauschen, um sicherzustellen, dass Sie die in Quick Infos enthaltenen Informationen konsistent erhalten.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition **für den** QuickInfo-Steuerelement-Typ besonders relevant Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert       | Notizen                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.  | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                                                                                                   |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.  | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.  | Der durch Klicken aktivierbare Punkt sollte der Teil der QuickInfo sein, der das Steuerelement schließt. Einige Quick Infos haben diese Fähigkeit nicht und haben keinen klickbaren Punkt.                                                                                                                                                                                                  |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **ToolTip** |                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | Depends (Abhängig)     | Wenn das QuickInfo-Steuerelement den Tastaturfokus erhalten kann, muss es in der Inhaltsansicht der-Struktur angezeigt werden. Wenn es sich nur um Text handelt, steht es als [**iuiautomationelement:: accessthelptext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (oder [**cachedhelptext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext))-Eigenschaft des Steuer Elements zur Verfügung, das es ausgelöst hat. |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | Richtig        | Das ToolTip-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                                                          |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.  | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                                                                      |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL        | QuickInfo-Steuerelemente werden immer durch ihren Inhalt selbst beschriftet.                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.  | Lokalisierte Zeichenfolge für den Steuerelementtyp „ToolTip“. Der Standardwert ist "Tooltip" für en-US oder Englisch (USA).                                                                                                                                                                                                                               |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.  | Der Name des QuickInfo-Steuer Elements ist der Text, der in der QuickInfo angezeigt wird.                                                                                                                                                                                                                                                                              |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von Quick Infos unterstützt werden müssen Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                   | Support | Notizen                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Depends (Abhängig) | Zur besseren Barrierefreiheit kann ein QuickInfo-Steuerelement das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützen, obwohl es nicht erforderlich ist. Das Text-Steuerelementmuster ist nützlich, wenn der Text viele Formate und Attribute hat (z. B., Farbe, Fettdruck und Kursivdruck). |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) | Depends (Abhängig) | Quick Infos, die durch Klicken auf ein Benutzeroberflächen Element geschlossen werden können, müssen das [Window](uiauto-implementingwindow.md) -Steuerelement Muster unterstützen, damit Sie automatisch geschlossen werden können.                                                                                                                 |



 

## <a name="required-events"></a>Erforderliche Ereignisse

QuickInfo-Steuerelemente müssen das [**UIA- \_ Tool tipopeinedeventid-**](uiauto-event-ids.md) Ereignis aufrufen, wenn Sie auf dem Bildschirm angezeigt werden. Das Ereignis enthält einen Verweis auf das Benutzeroberflächenautomatisierungs-Element der QuickInfo selbst.

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die QuickInfo-Steuerelemente zur Unterstützung Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                            | Notizen                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                               |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.          |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                          | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                      | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                    |                                                                                                                            |
| [**UIA \_ \_ -Text textchangedebug**](uiauto-event-ids.md)                                                          | Wenn das Steuerelement das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ -tooltipclosedebug**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ tooltipopeinedeventid**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ \_ -Fenster windowclosedeventid**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [Window](uiauto-implementingwindow.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ \_ -Fenster windowopenedeventid**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [Window](uiauto-implementingwindow.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Windowwindowvisualstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [Window](uiauto-implementingwindow.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




