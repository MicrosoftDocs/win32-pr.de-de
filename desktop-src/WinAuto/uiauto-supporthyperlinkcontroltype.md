---
title: Hyperlink-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Link Steuerelement-Typ.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für Hyperlink-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Hyperlink-Steuerelement Typen
- UI-Automatisierung, Struktur für Hyperlink-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für Hyperlink-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Hyperlink-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für Hyperlink-Steuerelement Typen
- Struktur Strukturen, Hyperlink-Steuerelement Typen
- Eigenschaften, Hyperlink-Steuerelement Typen
- Steuerelement Muster, Hyperlink-Steuerelement Typen
- Ereignisse, Hyperlink-Steuerelement Typen
- Unterstützung für Hyperlink-Steuerelement Typen
- HyperLink-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Hyperlink-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Hyperlink-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Hyperlink
- Steuerelement Typen, Hyperlink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710313"
---
# <a name="hyperlink-control-type"></a>Hyperlink-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Link** Steuerelement-Typ.

Hyperlink-Steuerelemente erstellen Links, die es Benutzern ermöglichen, innerhalb derselben Seite oder von einer Seite zu einer anderen zu navigieren.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Link** Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Link Steuerelemente, bei denen das UI-Framework/die Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Link Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Hyperlink</li>
</ul></td>
<td><ul>
<li>Hyperlink</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Link Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert         | Notizen                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.    | Der Wert dieser Eigenschaft muss für alle Steuerelemente in einer Anwendung eindeutig sein.                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.    | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                 |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.    | Der durch Klicken aktivierbare Punkt des Link Steuer Elements muss ein Punkt sein, der den Hyperlink öffnet, wenn mit einem Mauszeiger darauf geklickt wird.                     |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Link** |                                                                                                                                          |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE          | Das Link Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                  |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE          | Das Link Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                  |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.    | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.    | Wenn eine statische Text Bezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.                                                  |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.    | Lokalisierte Zeichenfolge für den Steuerelement Typ " **Hyperlink** ". Der Standardwert ist "Hyperlink" für en-US oder Englisch (USA). |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.    | Der Name des Link Steuer Elements ist der Text, der auf dem Bildschirm unterstrichen angezeigt wird.                                                  |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die für die Unterstützung von Link- Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                  | Unterstützung/Wert                | Notizen                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | Erforderlich                     | Alle Link Steuerelemente müssen das Steuerelement Muster " [aufrufen](uiauto-implementinginvoke.md) " unterstützen.                                                                                                                                                       |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Depends (Abhängig)                      | Link Steuerelemente sollten das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützen, wenn der Link Informationen enthält, die für den Benutzer verwendbar und aussagekräftig sind.                                                                              |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | Beispiel: „https://www..“. | Eine URL für eine Internet-oder Intranetadresse ist ein Beispiel für einen Hyperlink, der Informationen enthält, die für den Benutzer von Bedeutung sind. Ein Programm gesteuerter Link ist jedoch nur für eine Anwendung sinnvoll und wird für die **value** -Eigenschaft nicht empfohlen. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Link Steuerelementen Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ aufrufen \_ invokedebug-ID**](uiauto-event-ids.md)                                                     |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Der Typ des Hyperlink-Steuer Elements sollte nur auf ein Objekt angewendet werden, das beim Klicken auf die Navigation bewirkt. Er sollte nicht auf den Container des Links angewendet werden. Beispielsweise sollten nur die durch Klicken aktivierbaren "Hotspots" innerhalb einer ImageMap den **Hyperlink** -Steuer Elementtyp aufweisen. Das gleiche gilt für Hyperlinks in einem Textfeld oder Dokument Container. In diesem Fall sollte nur der Hyperlink-Text oder das Bild den **Hyperlink** -Steuer ungstyp haben, nicht den Container.

Das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster ist ideal für die Unterstützung eingebetteter Hyperlinks in Text-oder Dokument Elementen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




