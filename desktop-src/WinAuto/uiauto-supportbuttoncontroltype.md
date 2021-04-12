---
title: Button-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Button-Steuerelement-Typ.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Button-Steuerelement Typen
- UI-Automatisierung, Struktur für Schaltflächen-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für Button-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Button-Steuerelement Typen
- UI-Automatisierung, Ereignisse für Button-Steuerelement Typen
- Struktur Strukturen, Schaltflächen-Steuerelement Typen
- Eigenschaften, Schaltflächen-Steuerelement Typen
- Steuerelement Muster, Button-Steuerelement Typen
- Ereignisse, Button-Steuerelement Typen
- Unterstützung für Button-Steuerelement Typen
- Button-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Schaltflächen-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Button-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Schaltfläche
- Steuerelement Typen, Schaltfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207440"
---
# <a name="button-control-type"></a>Button-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Button** -Steuerelement-Typ.

Eine Schaltfläche ist ein Objekt, das ein Benutzer dazu verwendet, eine Aktion auszuführen, z. B. die Schaltflächen OK und Abbrechen in einem Dialogfeld. Das Schaltflächen-Steuerelement ist hinsichtlich des Verfügbarmachens ein einfaches Steuerelement, weil es einem einzelnen Befehl zugeordnet ist, den der Benutzer ausführen möchte.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Button** -Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Schaltflächen-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Schaltflächen-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Schaltfläche
<ul>
<li>Bild (beliebige Anzahl)</li>
<li>Text (beliebige Anzahl)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Schaltfläche</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für **die Steuerelemente, die den** Steuerelement-Steuerelement Typen (z. b. Schaltflächen-Steuerelemente Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ acceleratorkeypropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Ein Schaltflächen-Steuerelement unterstützt in der Regel eine Zugriffstaste, damit der Endbenutzer die durch die Schaltfläche auf der Tastatur dargestellte Aktion schnell ausführen kann.                                             |
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Schaltfläche** |                                                                                                                                                                                                      |
| [**UIA \_ helptextpropertyid**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Der Hilfetext sollte angeben, wie das Endergebnis der Schaltfläche aktiviert wird. Dabei handelt es sich in der Regel um dieselben Informationen, die über eine QuickInfo angezeigt werden.                                      |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Schaltflächen-Steuerelement muss immer ein Inhalt sein.                                                                                                                                                           |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Schaltflächen-Steuerelement muss immer ein Steuerelement sein.                                                                                                                                                         |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Null       | Schaltflächen-Steuerelemente werden durch ihren Inhalt selbstbeschriftet.                                                                                                                                                  |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Button** -Steuerelement Typ entspricht. Der Standardwert ist "Button" für en-US oder Englisch (USA).                                                                   |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Name des Schaltflächen-Steuer Elements ist der Text, der für die Bezeichnung verwendet wird. Wenn ein Bild zum Bezeichnen einer Schaltfläche verwendet wird, muss für die **Name** -Eigenschaft der Schaltfläche alternativer Text angegeben werden.                        |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von Schaltflächen-Steuerelementen unterstützt Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                  | Unterstützung/Wert | Notizen                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Siehe Hinweise.    | Wenn eine Schaltfläche als untergeordnetes Element einer unterteilten Schaltfläche gehostet wird, kann die untergeordnete Schaltfläche das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster anstelle des [Aufruf](uiauto-implementinginvoke.md) -oder [Toggle](uiauto-implementingtoggle.md) -Steuerelement Musters unterstützen. Das ExpandCollapse-Steuerelement Muster kann zum Öffnen oder Schließen eines Menüs oder einer anderen Unterstruktur verwendet werden, die dem Schaltflächen Element zugeordnet ist. |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Siehe Hinweise.    | Alle Schaltflächen sollten das Steuerelement "Start" oder das [Toggle](uiauto-implementingtoggle.md) [-Steuerelement](uiauto-implementinginvoke.md) Muster unterstützen, aber nicht beides. Das Aufruf Steuerelement-Muster muss unterstützt werden, wenn die Schaltfläche einen Befehl bei der Anforderung des Benutzers ausführt. Dieser Befehl ist einem einzelnen Vorgang zugeordnet, etwa Ausschneiden, Kopieren, Einfügen oder Löschen.                                                              |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Siehe Hinweise.    | Alle Schaltflächen sollten das Steuerelement "Start" oder das [Toggle](uiauto-implementingtoggle.md) [-Steuerelement](uiauto-implementinginvoke.md) Muster unterstützen, aber nicht beides. Das Toggle-Steuerelement Muster muss unterstützt werden, wenn die Schaltfläche eine Reihe von bis zu drei Zuständen durchlaufen kann. In der Regel ist dies als Ein-/Ausschalter für bestimmte Features zu sehen.                                                                        |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Schaltflächen- Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ aufrufen \_ invokedebug-ID**](uiauto-event-ids.md)                                                     | Wenn das Steuerelement das [Aufruf](uiauto-implementinginvoke.md) Steuerungs Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                           |                                                                                                                            |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.    | Wenn das Steuerelement das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




