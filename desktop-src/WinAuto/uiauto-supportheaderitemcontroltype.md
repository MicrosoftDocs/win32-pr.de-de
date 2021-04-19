---
title: Header Item-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Header Item-Steuer Elementtyp.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für den Header Item-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Header Item-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs-, Baumstruktur für Header Item-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Header Item-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den Header Item-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Ereignisse für Header Item-Steuer Elementtyp
- Struktur Strukturen, Header Item-Steuer Elementtyp
- Eigenschaften, Header Item-Steuer Elementtyp
- Steuerelement Muster, Header Item-Steuer Elementtyp
- Ereignisse, Header Item-Steuer Elementtyp
- Unterstützung für den Header Item-Steuer Elementtyp
- Header Item-Steuer Elementtyp
- Steuerelement Typen, Baumstruktur für Header Item-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den Header Item-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für Header Item
- Steuerelement Typen, Header Item
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bab61f92a6ab4db221810f9f083279ade4bf353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342263"
---
# <a name="headeritem-control-type"></a>Header Item-Steuer Elementtyp

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Header** Item-Steuer Elementtyp.

Der **Header** Item-Steuer Elementtyp stellt eine visuelle Bezeichnung für eine Zeile oder Spalte mit Informationen bereit.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Header** Item-Steuer Elementtyp definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Header Element-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung für die Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Header Element-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>HeaderItem</li>
</ul></td>
<td>(Nicht vorhanden)</td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **Header** Item-Steuer Elementtyp besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert          | Notizen                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.     | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.     | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.     | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **HeaderItem** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                        |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | false          | Das Header Element-Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nicht enthalten.                                                                                                               |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE           | Das Header Element-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                            |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.     | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ itemstatuspropertyid**](uiauto-automation-element-propids.md)                     | Siehe Hinweise      | Diese Eigenschaft stellt Informationen für Sortierreihenfolgen nach Headerelement bereit.                                                                                                                               |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL           | Header Element-Steuerelemente verfügen nicht über eine statische Text Bezeichnung.                                                                                                                                                |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.     | Lokalisierte Zeichenfolge für den Steuer Elementtyp " **Header** Item". Der Standardwert ist "Header Element" für en-US oder Englisch (USA).                                                          |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.     | Das Headerelement-Steuerelement ist immer selbstbezeichnend.                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Header Element-Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support | Notizen                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | Depends (Abhängig) | Implementieren Sie das [Aufruf](uiauto-implementinginvoke.md) Steuerelement Muster, wenn zum Sortieren der Daten auf das Header Element-Steuerelement geklickt werden kann. |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depends (Abhängig) | Implementieren Sie das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster, wenn die Größe des Header Element-Steuer Elements geändert werden kann.            |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Header Element-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ aufrufen \_ invokedebug-ID**](uiauto-event-ids.md)                                                     | Wenn das Steuerelement das [Aufruf](uiauto-implementinginvoke.md) Steuerungs Muster unterstützt, muss es dieses Ereignis unterstützen.           |
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

 

 




