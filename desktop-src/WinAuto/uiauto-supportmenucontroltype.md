---
title: Menu-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Menü Steuerungstyp.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für den Menü Steuerungstyp
- Benutzeroberflächen Automatisierung, Menü Steuerelement-Typ
- Benutzeroberflächen Automatisierung, Baumstruktur für Menü Steuerelement-Typ
- Benutzeroberflächen Automatisierung, Eigenschaften für den Menü Steuerungstyp
- UI-Automatisierung, Steuerelement Muster für den Menü Steuerungstyp
- Benutzeroberflächenautomatisierungs, Ereignisse für den Menü Steuerungstyp
- Struktur Strukturen, Menü Steuerelement-Typ
- Eigenschaften, Menü Steuerelement-Typ
- Steuerelement Muster, Menü Steuerelement-Typ
- Ereignisse, Menü Steuerelement-Typ
- Unterstützung für den Menü Steuerungstyp
- Menü-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Menü Steuerelement-Typ
- Steuerelement Typen, Steuerelement Muster für Menu-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Menü
- Steuerelement Typen, Menü
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036854"
---
# <a name="menu-control-type"></a>Menu-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Menü** Steuerungstyp.

Ein Menüsteuerelement ermöglicht die hierarchische Organisation von Elementen, die Befehlen und Ereignishandlern zugeordnet sind. In einer typischen Microsoft Windows-Anwendung enthält eine Menüleiste mehrere Menü Schaltflächen (z. b. **Datei**, **Bearbeiten** und **Fenster**), und jede Menü Schaltfläche zeigt ein Menü an. Ein Menü enthält eine Sammlung von Menüelementen (z. B. **Neu**, **Öffnen** und **Schließen**), die erweitert werden können, um weitere Menüelemente anzuzeigen, oder auf die geklickt werden kann, um eine bestimmte Aktion auszuführen.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Menü** Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Menü Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen und

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Menü Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Menü
<ul>
<li>MenuItem (1 oder viele)</li>
</ul>
<ul>
<li>Andere Steuerelemente (0 oder viele)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Menü
<ul>
<li>MenuItem (1 oder viele)</li>
</ul>
<ul>
<li>Andere Steuerelemente (0 oder viele)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Menü Steuerelemente werden immer in der Steuerelement Ansicht und in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt. Menü Steuerelemente sollten unter dem Steuerelement angezeigt werden, auf das Ihre Informationen verweisen. Benutzeroberflächenautomatisierungs-Clients können auf [**UIA \_ menuopenedeventid**](uiauto-event-ids.md) lauschen, um sicherzustellen, dass Sie ständig von Menü Steuerelementen übermittelte Informationen erhalten. Kontextmenü-Steuerelemente sind ein besonderer Fall. Sie können als untergeordnete Elemente des Desktops oder eines Anwendungsfensters der obersten Ebene angezeigt werden.

Ein Menü Steuerelement kann in seiner Struktur andere Steuerelemente enthalten, z. b. Bearbeitungs Steuerelemente und Kombinations Felder. Diese zusätzlichen Steuerelemente entsprechen den "anderen Steuerelementen", die in der vorherigen Tabelle in der Steuerelement-und der Inhaltsansicht aufgeführt sind.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **Menü** Steuerelement-Typ besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                      | Wert      | Notizen                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)           | **Menü**   |                                                                                                                                                                         |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md) | TRUE       | Das Menü Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                      |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md) | TRUE       | Das Menü Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                      |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)               | NULL       | Für ein typisches Menüsteuerelement wird keine Bezeichnung erwartet.                                                                                                                    |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Für das Menü Steuerelement muss keine **Name** -Eigenschaft festgelegt werden, oder es kann derselbe Name wie das zugeordnete Steuerelement sein, z. b. ein Menü Element, das das Untermenü geöffnet hat. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

Für den Menu-Steuerelementtyp gibt es keine erforderlichen Steuerelementmuster.

## <a name="required-events"></a>Erforderliche Ereignisse

Menü Steuerelemente müssen das [**UIA \_ menuopenedeventid-**](uiauto-event-ids.md) Ereignis erhöhen, wenn Sie auf dem Bildschirm angezeigt werden. Das **UIA \_ menuopenedeventid-** Ereignis enthält den Text des Steuer Elements. Das [**UIA \_ menuclosedebug-**](uiauto-event-ids.md) Ereignis muss ausgelöst werden, wenn ein Menü auf dem Bildschirm ausgeblendet wird.

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Menü Steuerelementen unterstützt werden. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ menuclosedebug**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ menuopenedeventid**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




