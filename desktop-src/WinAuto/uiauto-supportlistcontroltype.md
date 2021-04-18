---
title: List-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Listen Steuerelement-Typ.
ms.assetid: e4cde080-32d1-4150-a6be-8bd750e972c9
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für Listen Steuerelement
- Benutzeroberflächenautomatisierungs, Listen Steuerelement-Typ
- UI-Automatisierung, Struktur für Listen Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für Listen Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Listen Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für Listen Steuerelement Typen
- Struktur Strukturen, Listen Steuerelement-Typ
- Eigenschaften, Listen Steuerelement-Typ
- Steuerelement Muster, Listen Steuerelement-Typ
- Ereignisse, Listen Steuerelement-Typ
- Unterstützung für den Listen Steuerungstyp
- List-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Listen Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den Listen Steuerelement-Typ
- Steuerelement Typen, Unterstützung für Liste
- Steuerelement Typen, Liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a493418750bff1932fe933340b3eb2cb05829e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388243"
---
# <a name="list-control-type"></a>List-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Listen** Steuerelement-Typ.

Der Steuer Elementtyp " **List** " bietet eine Möglichkeit zum Organisieren einer flachen Gruppe oder einer Gruppe von Elementen und ermöglicht es einem Benutzer, mindestens eines dieser Elemente auszuwählen. Der **Listen** Steuerelement-Typ hat eine lose Einschränkung für die Typen von untergeordneten Elementen, die es enthalten kann. Dadurch können Benutzeroberflächenautomatisierungs-Anbieter bekannte Elemente für Auswahlcontainer unterstützen.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Listen** Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Listen Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen und

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster und-Eigenschaften](#required-control-patterns-and-properties)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Listen Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<td>Enthält die Elemente, die Steuerelementen entsprechen.</td>
<td>Entfernt redundante Informationen aus der Struktur, sodass Hilfstechnologien mit dem kleinsten Satz von Informationen arbeiten, die für den Endbenutzer von Bedeutung sind.</td>
</tr>
<tr class="even">
<td><ul>
<li>List
<ul>
<li>DataItem (beliebige Anzahl)</li>
<li>ListItem (beliebige Anzahl)</li>
<li>Group (beliebige Anzahl)</li>
<li>ScrollBar (0, 1 oder 2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>List
<ul>
<li>DataItem (beliebige Anzahl)</li>
<li>ListItem (beliebige Anzahl)</li>
<li>Group (beliebige Anzahl)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Die Steuerelementansicht für ein Steuerelement, das den Steuerelementtyp „List“ implementiert (z. B. ein Listensteuerelement), umfasst die folgenden Elemente:

-   0 (null) oder mehr Elemente innerhalb des Listen Steuer Elements (Elemente können auf dem Steuer Elementtyp " [ListItem](uiauto-supportlistitemcontroltype.md) " oder " [DataItem](uiauto-supportdataitemcontroltype.md) " basieren)
-   Beliebige Anzahl von Gruppensteuerelementen innerhalb eines Listensteuerelements
-   Kein, ein oder zwei ScrollBar-Steuerelemente

Die Inhaltsansicht eines Steuerelements, das den Steuerelementtyp „List“ implementiert (z. B. ein Listensteuerelement), besteht aus folgenden Elementen:

-   0 (null) oder mehr Elemente innerhalb des Listen Steuer Elements (Elemente können auf dem Steuer Elementtyp " [ListItem](uiauto-supportlistitemcontroltype.md) " oder " [DataItem](uiauto-supportdataitemcontroltype.md) " basieren)
-   Beliebige Anzahl von Gruppen innerhalb des Listensteuerelements

Ein Listensteuerelement darf keine Elemente enthalten, die andere hierarchische Beziehungen als die Gruppierung aufweisen. Wenn die Elemente in der Benutzeroberflächenautomatisierungs-Struktur über untergeordnete Elemente verfügen, sollte der Listen Container auf dem Steuer Elementtyp " [Tree](uiauto-supporttreecontroltype.md) " basieren.

Die auswählbaren Elemente innerhalb des Listen Steuer Elements sind über die nachfolgenden Elemente in der Benutzeroberflächenautomatisierungs-Struktur des Listen Steuer Elements verfügbar. Alle Elemente innerhalb des Listensteuerelements müssen zur gleichen Auswahlgruppe gehören. Die auswählbaren Elemente in der Liste sollten als [ListItem](uiauto-supportlistitemcontroltype.md) -Steuerelement Typen (anstelle von [DataItem](uiauto-supportdataitemcontroltype.md)-Steuerelement Typen) verfügbar gemacht werden.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **Listen** Steuerelement-Typ besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Wenn das Listen Steuerelement über einen klickbaren Punkt verfügt (ein Punkt, auf den geklickt werden kann, damit die Liste den Fokus erhält), muss dieser Punkt durch diese Eigenschaft verfügbar gemacht werden. Wenn der Wert der [**UIA \_ isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft **true** ist, wird beim Versuch, diese Eigenschaft abzurufen, der [**UIA \_ E \_ noclickablepoint**](uiauto-error-codes.md) -Fehler angezeigt.                      |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Liste**   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ helptextpropertyid**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Der Hilfetext für Listensteuerelemente sollte erläutern, warum der Benutzer aufgefordert wird, aus einer Liste von Optionen auszuwählen. Beispiel: „Durch Auswählen eines Elements in dieser Liste wird die Anzeigeauflösung für den Bildschirm festgelegt.“                                                                                                                                                                                                                                                |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Listen Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Listen Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn eine statische Textbezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf das entsprechende Steuerelement verfügbar machen.                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Listen** Steuerelement-Typ entspricht. Der Standardwert ist "List" für en-US oder Englisch (USA).                                                                                                                                                                                                                                                                                                                                       |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Wert der **Name** -Eigenschaft eines Listen Steuer Elements sollte die Kategorie der Optionen übermitteln, aus denen der Benutzer aufgefordert wird, auszuwählen. Diese Eigenschaft ruft ihren Namen in der Regel aus einer statischen Textbezeichnung ab. Wenn keine statische Text Bezeichnung vorhanden ist, muss der Anwendungsentwickler einen Wert für die Eigenschaft " **Name** " verfügbar machen.<br/> Nur wenn das Steuerelement innerhalb der Teilstruktur eines anderen Steuerelements verwendet wird, ist diese Eigenschaft für Listensteuerelemente nicht erforderlich.<br/> |



 

## <a name="required-control-patterns-and-properties"></a>Erforderliche Steuerelement Muster und-Eigenschaften

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Listen Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                             | Unterstützung/Wert | Notizen                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)                                | Depends (Abhängig)       | Implementieren Sie das [Raster](uiauto-implementinggrid.md) -Steuerelement Muster, wenn die Raster Navigation auf Element Basis verfügbar sein muss.                                                                                                                                                                                                                                           |
| [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)                | Depends (Abhängig)       | Implementieren Sie das [MultipleView](uiauto-implementingmultipleview.md) -Steuerelement Muster, wenn das Steuerelement mehrere Ansichten der Elemente im Container unterstützen kann.                                                                                                                                                                                                                       |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depends (Abhängig)       | Implementieren Sie das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster, wenn Elemente im Container scrollfähig sind.                                                                                                                                                                                                                                                                  |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Depends (Abhängig)       | Wenn ein Steuerelement den Steuer Elementtyp "List" unterstützt, der die Auswahl unterstützt, muss das Steuerelement das [Auswahl](uiauto-implementingselection.md) Steuerelement Muster implementieren, wenn ein Auswahl Zustand zwischen den im Steuerelement enthaltenen Elementen beibehalten wird. Wenn die Elemente innerhalb des Steuer Elements nicht auswählbar sind, kann der Steuer Elementtyp " [Group](uiauto-supportgroupcontroltype.md) " verwendet werden. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Depends (Abhängig)       | Listensteuerelemente können Container für Einfach- oder Mehrfachauswahl sein.                                                                                                                                                                                                                                                                                                                    |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Depends (Abhängig)       | In einem Listensteuerelement muss nicht immer ein Element ausgewählt sein.                                                                                                                                                                                                                                                                                                                    |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)                              | Nie         | Das [Table](uiauto-implementingtable.md) -Steuerelement Muster wird für den **Listen** Steuerelement-Typ nie unterstützt. Wenn das Steuerelement dieses Steuerelement Muster unterstützen muss, sollte das Steuerelement auf dem [DataGrid-](uiauto-supportdatagridcontroltype.md) Steuerelement Typen basieren.                                                                                                             |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Listen Steuerelementen zur Unterstützung von Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                        | Notizen                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                           |                                                                                                                              |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                      |                                                                                                                              |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                      | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.     |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                  | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ layoutinvalidatedeventid**](uiauto-event-ids.md)                                                                     | Wenn das Layout von untergeordneten Elementen geändert werden kann, muss das Steuerelement dieses Ereignis unterstützen.                                            |
| [**UIA \_ Multipleviewcurrentviewpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement das [MultipleView](uiauto-implementingmultipleview.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.   | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.           | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.     | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.       | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.               | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA- \_ Auswahl \_ invalidatedeventid**](uiauto-event-ids.md)                                                            | Wenn das Steuerelement das [Selection](uiauto-implementingselection.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                       |                                                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 





