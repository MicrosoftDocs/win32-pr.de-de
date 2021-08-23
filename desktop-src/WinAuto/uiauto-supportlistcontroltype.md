---
title: Listensteuertyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den Listensteuertyp.
ms.assetid: e4cde080-32d1-4150-a6be-8bd750e972c9
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den Steuerelementtyp "List"
- Benutzeroberflächenautomatisierung,List-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für List-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Properties für List-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Steuerelementtyp "List"
- Benutzeroberflächenautomatisierung,Events für List-Steuerelementtyp
- Strukturstrukturen,Listensteuertyp
- properties,List-Steuerelementtyp
- Steuerelementmuster, Listensteuertyp
- events,List-Steuerelementtyp
- Unterstützung für den Steuerelementtyp "List"
- List-Steuerelementtyp
- Steuerelementtypen,Struktur für List-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für List-Steuerelementtyp
- Steuerelementtypen,Unterstützung für List
- Steuerelementtypen, Liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac6ecb2e0fc7092507816cf9bbea4f450121c1ec8a2e6a57db3d377506af9d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570460"
---
# <a name="list-control-type"></a>Listensteuertyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **Listensteuertyp.**

Der **Steuerelementtyp** List bietet eine Möglichkeit, eine flache Gruppe oder Gruppen von Elementen zu organisieren, und ermöglicht es einem Benutzer, eines oder mehrere dieser Elemente auszuwählen. Der **Steuerelementtyp** List hat eine lose Einschränkung für die Typen untergeordneter Elemente, die er enthalten kann. Dadurch können Benutzeroberflächenautomatisierungs-Anbieter bekannte Elemente für Auswahlcontainer unterstützen.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **List-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Listensteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster und -eigenschaften](#required-control-patterns-and-properties)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung struktur, die sich auf Listensteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)



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
<td>Entfernt redundante Informationen aus der Struktur, sodass Hilfstechnologien mit den kleinsten Informationen arbeiten, die für den Endbenutzer von Bedeutung sind.</td>
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

-   Null oder mehr Elemente innerhalb des Listensteuerelementes (Elemente können auf den [Steuerelementtypen ListItem](uiauto-supportlistitemcontroltype.md) oder [DataItem](uiauto-supportdataitemcontroltype.md) basieren)
-   Beliebige Anzahl von Gruppensteuerelementen innerhalb eines Listensteuerelements
-   Kein, ein oder zwei ScrollBar-Steuerelemente

Die Inhaltsansicht eines Steuerelements, das den Steuerelementtyp „List“ implementiert (z. B. ein Listensteuerelement), besteht aus folgenden Elementen:

-   Null oder mehr Elemente innerhalb des Listensteuerelementes (Elemente können auf den [Steuerelementtypen ListItem](uiauto-supportlistitemcontroltype.md) oder [DataItem](uiauto-supportdataitemcontroltype.md) basieren)
-   Beliebige Anzahl von Gruppen innerhalb des Listensteuerelements

Ein Listensteuerelement darf keine Elemente enthalten, die andere hierarchische Beziehungen als die Gruppierung aufweisen. Wenn die Elemente in der strukturbasierten Struktur über Benutzeroberflächenautomatisierung verfügen, [](uiauto-supporttreecontroltype.md) sollte der Listencontainer auf dem Struktursteuerelementetyp basieren.

Die auswählbaren Elemente innerhalb des Listensteuerelementes sind über die Nachfolgerelemente in der Benutzeroberflächenautomatisierung des Listensteuerelementes verfügbar. Alle Elemente innerhalb des Listensteuerelements müssen zur gleichen Auswahlgruppe gehören. Die auswählbaren Elemente in der Liste sollten als [ListItem-Steuerelementtypen](uiauto-supportlistitemcontroltype.md) (anstelle von [DataItem)](uiauto-supportdataitemcontroltype.md)verfügbar gemacht werden.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für den **Steuerelementtyp List** besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein.                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Wenn das Listensteuer steuerelement über einen klickbaren Punkt verfügt (ein Punkt, auf den geklickt werden kann, damit die Liste den Fokus besitzt), muss dieser Punkt über diese Eigenschaft verfügbar gemacht werden. Wenn der Wert der [**\_ UIA-Eigenschaft IsOffscreenPropertyId**](uiauto-automation-element-propids.md) **TRUE** ist, führt der Versuch, diese Eigenschaft abzurufen, zum [**UIA \_ E \_ NOCLICKABLEPOINT-Fehler.**](uiauto-error-codes.md)                      |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Liste**   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Der Hilfetext für Listensteuerelemente sollte erläutern, warum der Benutzer aufgefordert wird, aus einer Liste von Optionen auszuwählen. Beispiel: „Durch Auswählen eines Elements in dieser Liste wird die Anzeigeauflösung für den Bildschirm festgelegt.“                                                                                                                                                                                                                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Listensteuer steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Listensteuer steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn eine statische Textbezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf das entsprechende Steuerelement verfügbar machen.                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp List** entspricht. Der Standardwert ist "list" für en-US oder Englisch (USA).                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Wert der Name-Eigenschaft eines Listensteuer steuerelements sollte die Kategorie der Optionen vermitteln, aus der der Benutzer ausgewählt werden soll.  Diese Eigenschaft ruft ihren Namen in der Regel aus einer statischen Textbezeichnung ab. Wenn keine statische Textbezeichnung vorhanden ist, muss der Anwendungsentwickler einen Wert für die **Name-Eigenschaft** verfügbar machen.<br/> Nur wenn das Steuerelement innerhalb der Teilstruktur eines anderen Steuerelements verwendet wird, ist diese Eigenschaft für Listensteuerelemente nicht erforderlich.<br/> |



 

## <a name="required-control-patterns-and-properties"></a>Erforderliche Steuerelementmuster und -eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Listensteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                             | Unterstützung/Wert | Hinweise                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)                                | Depends (Abhängig)       | Implementieren Sie das [Grid-Steuerelementmuster,](uiauto-implementinggrid.md) wenn die Rasternavigation elementweise verfügbar sein muss.                                                                                                                                                                                                                                           |
| [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)                | Depends (Abhängig)       | Implementieren [](uiauto-implementingmultipleview.md) Sie das MultipleView-Steuerelementmuster, wenn das Steuerelement mehrere Ansichten der Elemente im Container unterstützen kann.                                                                                                                                                                                                                       |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depends (Abhängig)       | Implementieren Sie das [Scroll-Steuerelementmuster,](uiauto-implementingscroll.md) wenn Elemente im Container scrollbar sind.                                                                                                                                                                                                                                                                  |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Depends (Abhängig)       | Wenn ein Steuerelement den List-Steuerelementtyp unterstützt, der die Auswahl unterstützt, muss das Steuerelement das [Selection-Steuerelementmuster](uiauto-implementingselection.md) implementieren, wenn ein Auswahlzustand zwischen den im Steuerelement enthaltenen Elementen beibehalten wird. Wenn die Elemente im Steuerelement nicht ausgewählt werden können, kann der [Steuerelementtyp Gruppe](uiauto-supportgroupcontroltype.md) verwendet werden. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Depends (Abhängig)       | Listensteuerelemente können Container für Einfach- oder Mehrfachauswahl sein.                                                                                                                                                                                                                                                                                                                    |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Depends (Abhängig)       | In einem Listensteuerelement muss nicht immer ein Element ausgewählt sein.                                                                                                                                                                                                                                                                                                                    |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)                              | Nie         | Das [Table-Steuerelementmuster](uiauto-implementingtable.md) wird für den **Listensteuerelementtyp** nie unterstützt. Wenn das Steuerelement dieses Steuerelementmuster unterstützen muss, sollte das Steuerelement auf dem [DataGrid-Steuerelementtyp](uiauto-supportdatagridcontroltype.md) basieren.                                                                                                             |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die zur Unterstützung von Steuerelementen erforderlich sind. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                        | Hinweise                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                              |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                      |                                                                                                                              |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                      | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.     |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                  | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     | Wenn das Layout der untergeordneten Elemente geändert werden kann, muss das Steuerelement dieses Ereignis unterstützen.                                            |
| [**UIA \_ Das MultipleViewCurrentViewPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)             | Wenn das Steuerelement das [MultipleView-Steuerelementmuster](uiauto-implementingmultipleview.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)   | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA \_ ScrollHorizontalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)           | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)     | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA \_ ScrollVerticallyScrollablePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)       | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA \_ ScrollVerticalViewSizePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)               | Wenn das Steuerelement [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.             |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            | Wenn das Steuerelement das [Selection-Steuerelementmuster](uiauto-implementingselection.md) unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 





