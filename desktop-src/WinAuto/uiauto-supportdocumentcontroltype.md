---
title: Dokument Steuerelement-Typ
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer ungstyp "Dokument".
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für Dokument Steuerelement Typen
- UI-Automatisierung, Dokument Steuerelement-Typ
- UI-Automatisierung, Baumstruktur für Dokument Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Eigenschaften für Dokument Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Dokument Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für Dokument Steuerelement Typen
- Struktur Strukturen, Dokument Steuerelement-Typ
- Eigenschaften, Dokument Steuerelement-Typ
- Steuerelement Muster, Dokument Steuerelement-Typ
- Ereignisse, Dokument Steuerelement-Typ
- Unterstützung für Dokument Steuerelement Typen
- Document-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Dokument Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Dokument Steuerelement Typen
- Steuerelement Typen, Unterstützung für Dokumente
- Steuerelement Typen, Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ca481df812e3321da7bb4bbb39bdcb5628fb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036856"
---
# <a name="document-control-type"></a>Dokument Steuerelement-Typ

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer ungstyp " **Dokument** ".

Mithilfe von Dokumentsteuerelementen kann ein Benutzer mehrere Seiten Text anzeigen und bearbeiten. Im Gegensatz zu Bearbeitungs Steuerelementen, die nur eine einfache Zeile unformatierten Texts unterstützen, können Dokument Steuerelemente den umfangreichen und formatierten Text hosten.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Dokument** Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Dokument Steuerelemente, bei denen das UI-Framework/die Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Dokument Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Dokument
<ul>
<li>Varies</li>
</ul></li>
</ul></td>
<td><ul>
<li>Dokument
<ul>
<li>Varies</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Dokument Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Notizen                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                      |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                          |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Das Dokument hat einen klickbaren Punkt, über den veranlasst werden kann, dass das Dokument oder eines seiner Elemente im Dokumentcontainer den Fokus erhält.                   |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Dokument** |                                                                                                                                                   |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Das Dokument Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                            |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Das Dokument Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                            |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                         |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss die Bezeichnung des Dokumentsteuerelements sein. In der Regel wird der Titel des Dokuments verwendet.                             |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem **Dokument** Steuerelement-Typ entspricht. Der Standardwert ist "Document" für en-US oder Englisch (USA).            |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Das Dokument Steuerelement erhält seinen Namen in der Regel aus dem Dateinamen, aus dem er geladen wurde. Dieser wird häufig im Titel eines umgebenden Fensters oder Rahmens angezeigt. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von Dokument Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                  | Unterstützung/Wert | Notizen                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | Depends (Abhängig)       | Das Dokumentsteuerelement kann einen Bereich umfassen, der größer ist als der Bereich des Viewports. Das-Steuerelement muss das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützen, wenn der Inhalt ScrollBar ist.                                                                                                                              |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Erforderlich      | Alle Dokument Steuerelemente müssen das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützen.                                                                                                                                                                                                                |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Depends (Abhängig)       | Während Benutzeroberflächenautomatisierungs-Clients mit [**iuiautomationtextpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) Textinformationen zu einem Dokument abrufen können, benötigen Sie das [value](uiauto-implementingvalue.md) -Steuerelement Muster, um den inneren Wert festzulegen. Ein einfacher Text Eintrag ist nur über das Value-Steuerelement Muster möglich. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Dokument Steuerelementen unterstützt werden müssen Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                        | Notizen                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                      |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                      | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                  | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.   | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.           | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.       | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.     | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.               | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA- \_ Auswahl \_ invalidatedeventid**](uiauto-event-ids.md)                                                            | Wenn das Steuerelement das [Selection](uiauto-implementingselection.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.     |
| [**UIA \_ \_ -Text textselectionchangedebug**](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [**UIA \_ \_ -Text textchangedebug**](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| [**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                                       | Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




