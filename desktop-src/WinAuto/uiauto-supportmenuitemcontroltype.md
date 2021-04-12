---
title: MenuItem-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer Elementtyp "MENUITEM".
ms.assetid: a6a04489-8e28-44ff-a3b0-ecf19c24daab
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für MenuItem-Steuer Elementtyp
- UI-Automatisierung, MenuItem-Steuer Elementtyp
- UI-Automatisierung, Baumstruktur für MenuItem-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für MenuItem-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für MenuItem-Steuer Elementtyp
- UI-Automatisierung, Ereignisse für MenuItem-Steuer Elementtyp
- Struktur Strukturen, MenuItem-Steuer Elementtyp
- Eigenschaften, MenuItem-Steuer Elementtyp
- Steuerelement Muster, MenuItem-Steuer Elementtyp
- Ereignisse, MenuItem-Steuer Elementtyp
- Unterstützung für MenuItem-Steuer Elementtyp
- MenuItem-Steuer Elementtyp
- Steuerelement Typen, Baumstruktur für MenuItem-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den MenuItem-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für MENUITEM
- Steuerelement Typen, MenuItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24033866f749974a41d39094b416e70f3c40f796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309952"
---
# <a name="menuitem-control-type"></a>MenuItem-Steuer Elementtyp

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer Elementtyp " **MenuItem** ".

Ein Menüsteuerelement ermöglicht die hierarchische Organisation von Elementen, die Befehlen und Ereignishandlern zugeordnet sind. In einer typischen Windows-Anwendung enthält eine Menüleiste mehrere Menü Elemente (z. b. **Datei**, **Bearbeiten** und **Fenster**), und jedes Menü Element zeigt ein Menü an. Ein Menü enthält eine Sammlung von Menüelementen (z. B. **Neu**, **Öffnen** und **Schließen**), die erweitert werden können, um weitere Menüelemente anzuzeigen, oder auf die geklickt werden kann, um eine bestimmte Aktion auszuführen.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **MenuItem** -Steuer Elementtyp definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Menü Element-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Legacyprobleme](#legacy-issues)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Menü Element-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>MenuItem- &quot; Hilfe&quot;
<ul>
<li>Menü (Untermenü des Menü Elements "Hilfe")
<ul>
<li>MenuItem- &quot; Hilfe Themen&quot;</li>
<li>MenuItem Info &quot; zum Editor&quot;</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>MenuItem- &quot; Hilfe&quot;
<ul>
<li>MenuItem- &quot; Hilfe Themen&quot;</li>
<li>MenuItem Info &quot; zum Editor&quot;</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Die Steuerelement Ansicht des Menü Element-Steuer Elements verfügt über die oben gezeigte Benutzeroberflächenautomatisierungs-Struktur. Beachten Sie, dass das Menü Element für die **Hilfe** in der Menüleiste hinzugefügt wurde, um die Struktur besser zu veranschaulichen.

Für die Inhaltsansicht fehlt das **Menü** in der Benutzeroberflächenautomatisierungs-Struktur, da es keine aussagekräftigen Informationen an den Endbenutzer vermittelt.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **MenuItem** -Steuer Elementtyp besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Notizen                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein. Zuordnen der **AutomationId** -Eigenschaft für ein Menü Element, wenn das Element bekanntermaßen über verschiedene Instanzen der Benutzeroberfläche hinweg konsistent ist. Wenn das Menü Element dynamisch aufgefüllt und nicht vorhersagbar ist, lassen Sie die **AutomationId** -Eigenschaft leer. |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.                                                                                                                                                                     |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **MenuItem** |                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Das Menü Element-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Das Menü Element-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                                                                                |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge für den Steuer Elementtyp " **MenuItem** ". Der Standardwert ist "Menü Element" für en-US oder Englisch (USA).                                                                                                                                                                                                                                  |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Der Name des Menü Element-Steuer Elements ist der Text, der für die Bezeichnung verwendet wird.                                                                                                                                                                                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von Menü Element Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                                |
|-------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Wenn das Steuerelement erweitert oder reduziert werden kann, implementieren Sie [**iexpandreduseprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider).                            |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depends (Abhängig) | Wenn das Steuerelement eine einzelne Aktion oder einen Befehl ausführt, implementieren Sie [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider).                                     |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depends (Abhängig) | Wenn das Steuerelement für die Auswahl aus einer Liste von Optionen unter Menü Elementen verwendet wird, implementieren Sie [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider). |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depends (Abhängig) | Wenn das Steuerelement eine Option darstellt, die aktiviert oder deaktiviert werden kann, implementieren Sie [**ideggleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).                       |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Menü Element-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                                | Notizen                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                              |                                                                                                                                  |
| [**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ aufrufen \_ invokedebug-ID**](uiauto-event-ids.md)                                                                                  | Wenn das Steuerelement das [Aufruf](uiauto-implementinginvoke.md) Steuerungs Muster unterstützt, muss es dieses Ereignis unterstützen.                 |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                              | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.         |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                          | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ SelectionItem \_ elementaddecodto selectioneventid**](uiauto-event-ids.md)                                    | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**](uiauto-event-ids.md)                            | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ SelectionItem \_ elementselectedebug**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                                 | Wenn das Steuerelement das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                 |



 

## <a name="legacy-issues"></a>Legacyprobleme

Für Microsoft Win32-Menü Elemente wird das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster nur unterstützt, wenn ein Menü Element aktiviert ist, und es ist möglich, Programm gesteuert zu ermitteln, ob die Unterstützung für das Toggle-Steuerelement Muster erforderlich ist. Da ein Win32-Menü Element nicht verfügbar macht, ob es aktiviert werden kann, wird das Steuerelement für das Aufrufen von Steuerelementen unterstützt, wenn das Menü Element nicht aktiviert ist. Das Aufruf Steuerelement-Muster wird immer unterstützt, auch für Menü Elemente, die nur zur Unterstützung des Toggle-Steuerelement Musters erforderlich sind. Dies ist so, dass Clients nicht verwirrt werden, wenn ein Menü Element [, das das Start Steuerelement](uiauto-implementinginvoke.md) -Muster unterstützt hat (bei deaktiviertem Menü Element) dieses Muster nicht mehr unterstützt, wenn es überprüft wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




