---
title: Separator-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuerelement-Steuer Zeichentyp.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- Benutzeroberflächenautomatisierungs-Unterstützung für Trenn Zeichentyp
- Benutzeroberflächenautomatisierungs-Steuerelement Typen
- UI-Automatisierung, Struktur für Trenn Zeichentyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für Steuerelement-Trennzeichen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Steuerelement-Trennzeichen
- Benutzeroberflächenautomatisierungs, Ereignisse für Trenn Zeichentyp
- Struktur Strukturen, Trenn Steuerelement-Typ
- Eigenschaften, Separator-Steuerelement Typen
- Steuerelement Muster, Trenn Zeichentyp
- Ereignisse, Separator-Steuerelement Typen
- Unterstützung für Trenn Zeichentyp
- Trennzeichensteuerelementtyp
- Steuerelement Typen, Struktur für Trenn Zeichentyp
- Steuerelement Typen, Steuerelement Muster für Trennzeichen-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Trennzeichen
- Steuerelement Typen, Trennzeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cdf6c15dbe461e78877c6b93f0ff4b52f67fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515932"
---
# <a name="separator-control-type"></a>Separator-Steuerelement Typen

Dieses Thema enthält **Informationen zur Unterstützung der Microsoft** -Benutzeroberflächen Automatisierung für den Steuerelement-Steuer Zeichentyp.

Mithilfe von Separator-Steuerelementen wird ein Bereich visuell in zwei Abschnitte unterteilt. Ein Separator-Steuerelement kann z. B. eine Leiste sein, die zwei Bereiche in einem Fenster definiert. Wenn die Trennlinie verschoben werden kann, sollte das Steuerelement als Steuerelementtyp „Thumb“ verfügbar gemacht werden.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den Steuerelement- **Trenn** Zeichentyp definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Trenn Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen und

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Separator-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Trennzeichen</li>
</ul></td>
<td><ul>
<li>Der Steuer Zeichentyp des <strong>Trenn</strong> Zeichens hat nie Inhalt.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Trennzeichen Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert         | Notizen                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.    | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.    | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.    | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Trennzeichen** |                                                                                                                                                                                                      |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | false         | Das Separator-Steuerelement ist nie ein Inhaltselement.                                                                                                                                                              |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE          | Das Separator-Steuerelement muss immer ein Steuerelement sein.                                                                                                                                                      |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.    | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL          | Das Separator-Steuerelement hat keine statische Bezeichnung.                                                                                                                                                  |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.    | Lokalisierte Zeichenfolge für den Steuer Zeichentyp des **Trenn** Zeichens. Der Standardwert ist "Separator" für en-US oder Englisch (USA).                                                             |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | ""            | Das Trennzeichen Steuerelement erfordert keine **Name** -Eigenschaft.                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

Das Separator-Steuerelement ist nicht erforderlich, um Steuerelementmuster zu unterstützen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Trenn Steuerelementen unterstützt werden. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



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

 

 




