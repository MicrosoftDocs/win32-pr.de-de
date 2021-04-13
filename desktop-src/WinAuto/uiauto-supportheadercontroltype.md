---
title: Header Steuerelement-Typ
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Header-Steuerelement Typen.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für den Header-Steuerelement
- Benutzeroberflächenautomatisierungs, Header Steuerelement-Typ
- UI-Automatisierung, Baumstruktur für den Header-Steuerelement Typen
- Benutzeroberflächen Automatisierung, Eigenschaften für den Header-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Header Steuerelement Typen
- UI-Automatisierung, Ereignisse für den Header-Steuerelement Typen
- Struktur Strukturen, Header Steuerelement-Typ
- Eigenschaften, Header-Steuerelement Typen
- Steuerelement Muster, Header Steuerelement-Typ
- Ereignisse, Header-Steuerelement Typen
- Unterstützung für den Header Steuerungstyp
- Header-Seuerelementtyp
- Steuerelement Typen, Baumstruktur für Header Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den Header Steuerungstyp
- Steuerelement Typen, Unterstützung für Header
- Steuerelement Typen, Header
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38ee0a00749888c624b627db247f2d01d24ff1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388244"
---
# <a name="header-control-type"></a>Header Steuerelement-Typ

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Header** -Steuerelement Typen.

Ein Headersteuerelement stellt einen visuellen Container für Beschriftungen von Zeilen oder Spalten bereit, die Informationen enthalten.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Header** -Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Header Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen und

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Header Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Header
<ul>
<li>HeaderItem (1 oder mehr)</li>
</ul></li>
</ul></td>
<td>(Nicht vorhanden)</td>
</tr>
</tbody>
</table>



 

Header Steuerelemente haben immer mindestens ein untergeordnetes Element in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur.

Header Steuerelemente haben in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur keine untergeordneten Elemente.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle werden die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Werte oder Definitionen für Header Steuerelemente besonders relevant sind. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert                                                            | Notizen                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.                                                       | Der Wert dieser Eigenschaft muss für alle Steuerelemente in einer Anwendung eindeutig sein.                                                                                                                     |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.                                                       | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.                                                       | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Header**                                                       |                                                                                                                                                                                                      |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | false                                                            | Das Header Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nicht enthalten.                                                                                                                    |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE                                                             | Das Header Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                 |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.                                                       | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL                                                             | Headersteuerelemente haben keine statische Bezeichnung.                                                                                                                                                          |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.                                                       | Der Standardwert ist "Header" für en-US oder Englisch (USA).                                                                                                                                  |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.                                                       | Das Headersteuerelement benötigt einen Namen, wenn mehrere Zeilen- oder Spaltenüberschriften vorhanden sind. Dadurch werden die Informationen für den Header (Überschrift) gekennzeichnet.                                              |
| [**UIA- \_ orientationpropertyid**](uiauto-automation-element-propids.md)                   | **OrientationType \_ Horizontal** oder **OrientationType \_ vertikal** | Der Wert dieser Eigenschaft macht die Position des Header Steuer Elements verfügbar – ob es sich um einen Zeilen Header (**OrientationType \_ Horizontal**) oder einen Spaltenheader (**OrientationType \_ vertikal**) handelt.                 |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die für Header Steuerelemente unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support | Notizen                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depends (Abhängig) | Implementieren Sie das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster, wenn die Größe des Header Steuer Elements geändert werden kann. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Header Steuerelementen unterstützt werden müssen Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



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

 

 




