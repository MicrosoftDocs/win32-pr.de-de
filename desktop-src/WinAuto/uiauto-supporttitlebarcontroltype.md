---
title: TitleBar-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den TitleBar-Steuerelement-Typ. Ein Titelleisten-Steuerelement stellt einen Titel oder eine Beschriftungs Leiste in einem Fenster dar.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für den TitleBar-Steuerelement
- Benutzeroberflächenautomatisierungs-Steuerelement (Titlebar)
- UI-Automatisierung, Struktur für TitleBar-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für den TitleBar-Steuerelement
- Benutzeroberflächenautomatisierungs-Steuerelement Muster für TitleBar-Steuerelement
- Benutzeroberflächenautomatisierungs, Ereignisse für TitleBar-Steuerelement Typen
- Baumstrukturen, TitleBar-Steuerelement Typen
- Eigenschaften, TitleBar-Steuerelement Typen
- Steuerelement Muster, TitleBar-Steuerelement Typen
- Ereignisse, TitleBar-Steuerelement Typen
- Unterstützung für TitleBar-Steuerelement Typen
- TitleBar-Steuerelement Typen
- Steuerelement Typen, Baumstruktur für TitleBar-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für TitleBar-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Titlebar
- Steuerelement Typen, Titlebar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9471d08479345bf8c1df118f720bf273d4d89d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948044"
---
# <a name="titlebar-control-type"></a>TitleBar-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **TitleBar** -Steuerelement-Typ. Ein Titelleisten-Steuerelement stellt einen Titel oder eine Beschriftungs Leiste in einem Fenster dar.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **TitleBar** -Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Titelleisten-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Titelleisten-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>TitleBar
<ul>
<li>Menü (0 oder 1)</li>
<li>Schaltfläche (beliebige Anzahl)</li>
</ul></li>
</ul></td>
<td>(Nicht zutreffend; das Titelleisten-Steuerelement hat keinen Inhalt)</td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **TitleBar** -Steuerelement Typ besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Notizen                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Der von dieser Eigenschaft verfügbar gemachte Wert muss sämtliche darin enthaltenen Steuerelemente umfassen.                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **TitleBar** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                        |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | false        | Das Titelleisten-Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nie enthalten.                                                                                                               |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Das Titelleisten-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                              |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | false        | Ein Titelleisten-Steuerelement hat nie den Tastaturfokus.                                                                                                                                                        |
| [**UIA \_ isoffscreenpropertyid**](uiauto-automation-element-propids.md)                   | Depends (Abhängig)      | Ein Titelleisten-Steuerelement gibt einen Wert zurück, abhängig davon, ob es auf dem Bildschirm sichtbar ist.                                                                                                                |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.   | Ein Titelleisten-Steuerelement verfügt in der Regel nicht über eine Bezeichnung.                                                                                                                                                 |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge für den Steuerelementtyp „TitleBar“. Der Standardwert ist "Titelleiste" für en-US oder Englisch (USA).                                                                  |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | ""           | Eine Titelleiste ist kein Inhalt. die Textinformationen werden durch den Namen des übergeordneten Fensters verfügbar gemacht.                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

Der **TitleBar** -Steuerelement-Typ ist nicht erforderlich, um Steuerelement Muster zu unterstützen. Seine Funktionalität wird über das [Window](uiauto-implementingwindow.md) -Steuerelement Muster des [Window](uiauto-supportwindowcontroltype.md) -Steuerelement Typs verfügbar gemacht.

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Steuerelementen für die Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



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

 

 




