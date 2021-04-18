---
title: MenuBar-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den MenuBar-Steuer Elementtyp.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für MenuBar-Steuer Elementtyp
- UI-Automatisierung, MenuBar-Steuer Elementtyp
- UI-Automatisierung, Baumstruktur für den MenuBar-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für den MenuBar-Steuer Elementtyp
- UI-Automatisierung, Steuerelement Muster für den MenuBar-Steuer Elementtyp
- UI-Automatisierung, Ereignisse für den MenuBar-Steuer Elementtyp
- Struktur Strukturen, MenuBar-Steuer Elementtyp
- Eigenschaften, MenuBar-Steuer Elementtyp
- Steuerelement Muster, MenuBar-Steuer Elementtyp
- Ereignisse, MenuBar-Steuer Elementtyp
- Unterstützung für den MenuBar-Steuer Elementtyp
- MenuBar-Steuer Elementtyp
- Steuerelement Typen, Baumstruktur für den MenuBar-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den MenuBar-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für Menubar
- Steuerelement Typen, Menüleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94bb60c13b5999bc8020eb70b84f6c932a2fb94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337778"
---
# <a name="menubar-control-type"></a>MenuBar-Steuer Elementtyp

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **MenuBar** -Steuer Elementtyp.

Menüleisten-Steuerelemente sind ein Beispiel für Steuerelemente, die den **MenuBar** -Steuer Elementtyp implementieren. Menüleisten geben dem Benutzer die Möglichkeit, Befehle und Optionen zu aktivieren, die in einer Anwendung enthalten sind.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **MenuBar** -Steuer Elementtyp definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Menüleisten-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Menüleisten-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>MenuBar
<ul>
<li>MenuItem (1 oder mehr)</li>
<li>Andere Steuerelemente (0 oder viele)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Nicht verfügbar
<ul>
<li>MenuItem (1 oder mehr)</li>
<li>Andere Steuerelemente (0 oder viele)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Ein Menüleisten-Steuerelement wird immer in der Steuerelement Ansicht, aber nicht in der Inhaltsansicht angezeigt, weil es in der Regel keine aussagekräftigen Informationen an den Endbenutzer weitergibt (es sei denn, die Anwendung enthält mehr als eine Menüleiste).

Benutzeroberflächenautomatisierungs-Clients können das [**UIA \_ menumodestarteventid-**](uiauto-event-ids.md) Ereignis überwachen, um sicherzustellen, dass Sie konsistent benachrichtigt werden, wenn die Benutzeroberfläche in den Menü Modus wechselt Wenn sich die Anwendung im Menü Modus befindet, können alle Tastatureingaben für die Menü Navigation aufgezeichnet werden (z. b. können Sie das Menü **Speichern** aufrufen, anstatt das Zeichen im Anwendungs Client Bereich einzugeben). Das **UIA \_ menumodestarteventid-** Ereignis muss vor dem ersten [**UIA \_ menuopenedeventid-**](uiauto-event-ids.md) Ereignis stehen, um die logische Konsistenz sicherzustellen. Das [**UIA \_ menumodeendeventid-**](uiauto-event-ids.md) Ereignis folgt dem letzten [**UIA \_ menuclosedebug-**](uiauto-event-ids.md) Ereignis. Wenn Sie auf ein Menü Element klicken, wird möglicherweise auch sofort das **UIA \_ menumodestarteventid-** Ereignis, gefolgt von einem **UIA \_ menuopenedeventid-** Ereignis, aufgerufen.

Ein Menüleisten-Steuerelement kann in seiner Struktur andere Steuerelemente enthalten, z. b. Bearbeitungs Steuerelemente und Kombinations Felder. Diese weiteren Steuerelemente sind oben in der Inhalts- und der Steuerelementansicht mit „Andere Steuerelemente“ gemeint.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **MenuBar** -Steuer Elementtyp besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert       | Notizen                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ acceleratorkeypropertyid**](uiauto-automation-element-propids.md)             | NULL        | Menüleisten verfügen in der Regel nicht über Tastenkombinationen.                                                                                                                                                                                          |
| [**UIA \_ accesskeypropertyid**](uiauto-automation-element-propids.md)                       | „ALT“       | Durch Drücken der Alt-Taste sollte in der Regel der Fokus auf die Menüleiste innerhalb der Anwendung gebracht werden.                                                                                                                                                  |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.  | Der von dieser Eigenschaft verfügbar gemachte Wert muss sämtliche darin enthaltenen Steuerelemente umfassen.                                                                                                                                                 |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **MenuBar** |                                                                                                                                                                                                                                          |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | false       | Das Menüleisten-Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nicht enthalten.                                                                                                                                                      |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE        | Das Menüleisten-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                   |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | TRUE        | Menüleisten-Steuerelemente können den Tastaturfokus erhalten, da die in ihnen enthaltenen Steuerelemente den Tastaturfokus übernehmen können.                                                                                                                                      |
| [**UIA \_ isoffscreenpropertyid**](uiauto-automation-element-propids.md)                   | Siehe Hinweise.  | Der Wert dieser Eigenschaft ist hängt davon ab, ob das Steuerelement auf dem Bildschirm angezeigt werden kann.                                                                                                                                                     |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL        | Menüleisten-Steuerelemente haben in der Regel keine Bezeichnung.                                                                                                                                                                                           |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.  | Lokalisierte Zeichenfolge für den Steuer Elementtyp " **MenuBar** ". Der Standardwert ist "Menüleiste" für en-US oder Englisch (USA).                                                                                                    |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.  | Das Menüleisten-Steuerelement muss nur dann einen Namen haben, wenn eine Anwendung mehrere Menüleisten hat. Wenn in einer Anwendung mehr als eine Menüleiste vorhanden ist, verwenden Sie diese Eigenschaft, um Unterscheidungs Namen (z. b. "Formatierung" oder "Gliederung") verfügbar zu machen. |
| [**UIA- \_ orientationpropertyid**](uiauto-automation-element-propids.md)                   | Depends (Abhängig)     | Diese Eigenschaft gibt an, ob das Menüleisten-Steuerelement horizontal oder vertikal verläuft.                                                                                                                                                            |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von Menüleisten Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Wenn das Steuerelement erweitert oder reduziert werden kann, muss es das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster implementieren. |
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Depends (Abhängig) | Wenn das Steuerelement an verschiedenen Teilen des Bildschirms angedockt werden kann, muss es das [Dock](uiauto-implementingdock.md) -Steuerelement Muster implementieren.   |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Depends (Abhängig) | Wenn die Größe des Steuer Elements geändert, gedreht oder verschoben werden kann, muss es das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster implementieren.      |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Menüleisten-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                                | Notizen                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                              |                                                                                                                                  |
| [**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                              | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.         |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                          | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




