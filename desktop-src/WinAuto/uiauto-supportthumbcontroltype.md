---
title: Thumb-Steuerelement
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuerelement-Steuerelement.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für den Steuerelement
- Benutzeroberflächenautomatisierungs-, Thumb-Steuerelement
- Benutzeroberflächenautomatisierungs, Struktur für den Steuerelement-Steuerelement
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Thumb-Steuerelement
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den Thumb-Steuerelement
- Benutzeroberflächenautomatisierungs, Ereignisse für Steuerelement-Steuerelement
- Struktur Strukturen, Typ des Thumb-Steuer Elements
- Eigenschaften, Typ des Thumb-Steuer Elements
- Steuerelement Muster, Typ des Thumb-Steuer Elements
- Ereignisse, Typ des Thumb-Steuer Elements
- Unterstützung für den Thumb-Steuerelement
- Thumb-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Thumb-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den Thumb-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Thumb
- Steuerelement Typen, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388689"
---
# <a name="thumb-control-type"></a>Thumb-Steuerelement

Dieses Thema enthält **Informationen zur Unterstützung der Microsoft** -Benutzeroberflächen Automatisierung für den Steuerelement-Steuerelement.

Thumb-Steuerelemente bieten die Funktionen, mit denen ein Steuerelement bewegt (oder gezogen) werden kann, wie ein Schieberegler für Bildlaufleisten, oder in der Größe angepasst werden kann, wie ein Widget für die Größenanpassung von Fenstern. Beachten Sie, dass ein Thumb-Steuerelement keine Drag & Drop-Funktionalität bereitstellt. Thumb-Steuerelemente können den Maus Fokus, aber keinen Tastaturfokus erhalten. Der Entwickler von Steuerelementen muss das Steuerelement implementieren, damit es entsprechend funktioniert (d. h. es kann gezogen bzw. in der Größe angepasst werden).

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse **für den Steuer** Element-Steuerelement Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Ziehpunkt-Steuerelemente, bei denen das UI-Framework/die Benutzeroberflächen Automatisierung für Steuerelement Typen und Steuerelemente

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Thumb-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Ziehpunkt</li>
</ul></td>
<td>(Nicht vorhanden)</td>
</tr>
</tbody>
</table>



 

Thumb-Steuerelemente werden nie in der Inhaltsansicht angezeigt, da Sie nur mit einer Maus bearbeitet werden können. Sie werden über ein anderes Steuerelement Muster verfügbar gemacht, z. b. das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster, das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster oder das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster, das im Container des Thumb-Steuer Elements

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Thumb-Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                 |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                     |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Ein Punkt innerhalb des sichtbaren Client Bereichs des Thumb-Steuer Elements.                                                                                                                                                                                                 |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Thumb**  |                                                                                                                                                                                                                                                              |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | false      | Das Thumb-Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nie enthalten.                                                                                                                                                                           |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Thumb-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                          |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen. Ein Thumb-Steuerelement kann den Fokus erhalten, wenn es als "Zieh Element"-Objekt für die Größenanpassung eines Fensters oder Bereichs verwendet wird. Ein Thumb-Steuerelement in einem Schieberegler oder einer Scrollleiste sollte niemals den Fokus erhalten. |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL       | Thumb-Steuerelemente haben niemals eine Bezeichnung.                                                                                                                                                                                                                           |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, **die dem** Steuerelement-Steuerelement entspricht. Der Standardwert ist "Thumb" für en-US oder Englisch (USA).                                                                                                                             |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | NULL       | Da das Thumb-Steuerelement in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nicht verfügbar ist, ist kein Name erforderlich.                                                                                                                                        |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von Thumb-Steuerelementen unterstützt Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support  | Notizen                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Erforderlich | Ermöglicht, dass das Ziehpunkt-Steuerelement auf dem Bildschirm bewegt werden kann. Da das Thumb-Steuerelement in der Regel nicht geändert oder gedreht werden kann, unterstützt das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster hauptsächlich die [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) -Funktion |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Thumb-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




