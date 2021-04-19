---
title: ListItem-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer Elementtyp "ListItem".
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für den ListItem-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, ListItem-Steuer Elementtyp
- UI-Automatisierung, Baumstruktur für den ListItem-Steuer Elementtyp
- UI-Automatisierung, Eigenschaften für den ListItem-Steuer Elementtyp
- UI-Automatisierung, Steuerelement Muster für den ListItem-Steuer Elementtyp
- UI-Automatisierung, Ereignisse für den ListItem-Steuer Elementtyp
- Baumstrukturen, ListItem-Steuer Elementtyp
- Eigenschaften, ListItem-Steuer Elementtyp
- Steuerelement Muster, ListItem-Steuer Elementtyp
- Ereignisse, ListItem-Steuer Elementtyp
- Unterstützung für den ListItem-Steuer Elementtyp
- ListItem-Steuer Elementtyp
- Steuerelement Typen, Baumstruktur für den ListItem-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den ListItem-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für ListItem
- Steuerelement Typen, ListItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5093ef62793d96a5438c27edd29e96a96cfa407
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341233"
---
# <a name="listitem-control-type"></a>ListItem-Steuer Elementtyp

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer Elementtyp " **ListItem** ".

Listenelement-Steuerelemente sind ein Beispiel für Steuerelemente, die den Steuer Elementtyp " **ListItem** " implementieren.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **ListItem** -Steuer Elementtyp definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Listenelement-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung für die Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Listenelement-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>ListItem
<ul>
<li>Bild (beliebige Anzahl)</li>
<li>Text (beliebige Anzahl)</li>
<li>Bearbeiten (beliebige Anzahl)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ListItem</li>
</ul></td>
</tr>
</tbody>
</table>



 

Die untergeordneten Elemente eines Listenelement-Steuer Elements innerhalb der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur müssen immer untergeordnete Elemente anzeigen. Wenn die Struktur des Steuer Elements darin besteht, dass andere Elemente unterhalb des Listen Elements enthalten sind, sollte es den Anforderungen an die Benutzeroberflächenautomatisierungs-Unterstützung für den [TreeItem](uiauto-supporttreeitemcontroltype.md) -Steuer Elementtyp entsprechen.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **ListItem** -Steuer Elementtyp besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Notizen                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein. Zuordnen der **AutomationId** -Eigenschaft für ein Listenelement, wenn das Element bekanntermaßen über verschiedene Instanzen der Benutzeroberfläche hinweg konsistent ist. Wenn das Listenelement dynamisch aufgefüllt und nicht vorhersagbar ist, lassen Sie die **AutomationId** -Eigenschaft leer.                                                          |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Der Wert dieser Eigenschaft sollte den Bereich des Bilds und den Textinhalt des Listenelements enthalten.                                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Depends (Abhängig)      | Wenn das Listen Steuerelement über einen klickbaren Punkt verfügt (ein Punkt, auf den geklickt werden kann, damit die Liste den Fokus erhält), muss dieser Punkt durch diese Eigenschaft verfügbar gemacht werden. Wenn das Listen Steuerelement vollständig von Nachfolger Listenelementen abgedeckt ist, wird der [**UIA \_ E \_ noclickablepoint**](uiauto-error-codes.md) -Fehler zurückgegeben, um anzugeben, dass der Client ein Element innerhalb des Listen Steuer Elements für einen durch Klicken aktivierbaren Punkt anfordern muss. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **ListItem** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ helptextpropertyid**](uiauto-automation-element-propids.md)                         | Siehe Hinweise.   | Im Hilfetext für Listensteuerelemente sollte erklärt werden, warum der Benutzer aufgefordert wird, eine Auswahl aus einer Liste von Optionen zu treffen. Hierbei handelt es sich in der Regel um dieselben Informationen, die durch ein QuickInfo angezeigt werden. Beispiel: "wählen Sie ein Element aus, um die Bildschirmauflösung für den Monitor festzulegen".                                                                                                                                                    |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**     | Das Listen Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**     | Das Listen Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn der Container Tastatureingaben akzeptieren kann, sollte dieser Eigenschafts Wert " **true**" lauten.                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ isoffscreenpropertyid**](uiauto-automation-element-propids.md)                   | Depends (Abhängig)      | Diese Eigenschaft muss einen Wert zurückgeben, der zeigt, ob das Listenelement zurzeit innerhalb des übergeordneten Containers, der das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster implementiert                                                                                                                                                                                                                                  |
| [**UIA \_ itemstatuspropertyid**](uiauto-automation-element-propids.md)                     | Depends (Abhängig)      | Wenn das Steuerelement den Status enthält, der dynamisch aktualisiert wird, muss diese Eigenschaft unterstützt werden, damit eine Hilfstechnologie Updates empfangen kann, wenn sich der Status des Elements ändert.                                                                                                                                                                                                                                     |
| [**UIA \_ itemtypepropertyid**](uiauto-automation-element-propids.md)                         | Depends (Abhängig)      | Diese Eigenschaft sollte für Listenelement-Steuerelemente verfügbar gemacht werden, die ein zugrunde liegendes Objekt darstellen. Bei diesen Listenelement-Steuerelementen ist dem Steuerelement normalerweise ein Symbol zugeordnet, das Benutzer mit dem zugrunde liegenden Objekt assoziieren.                                                                                                                                                                                                   |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.   | Wenn eine statische Textbezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf das entsprechende Steuerelement verfügbar machen.                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge für den Steuer Elementtyp " **ListItem** ". Der Standardwert ist "list item" für en-US oder Englisch (USA).                                                                                                                                                                                                                                                                                           |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Der Wert der Name-Eigenschaft eines Listenelement-Steuer Elements wird von der Text Bezeichnung des Elements abgeleitet.                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Listenelement-Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Wenn das Element bearbeitet werden kann, um Informationen anzuzeigen oder auszublenden, muss das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster implementiert werden.                                                                                                                                                                                                                        |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depends (Abhängig) | Wenn die räumliche Navigation zwischen Elementen innerhalb des Listen Containers unterstützt wird und der Container in Zeilen und Spalten angeordnet ist, muss das [GridItem](uiauto-implementinggriditem.md) -Steuerelement Muster implementiert werden.                                                                                                                                                                  |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depends (Abhängig) | Wenn das Element über einen Befehl verfügt, der für das Element getrennt von der Auswahl ausgeführt werden kann, muss das [Aufruf](uiauto-implementinginvoke.md) Steuerungs Muster implementiert werden. Dies ist normalerweise eine Aktion, die dem Doppelklicken auf das Listenelement-Steuerelement zugeordnet wird. Beispiele wären das Starten eines Dokuments aus Windows-Explorer oder das Abspielen einer Musikdatei in Microsoft Windows Media Player.        |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depends (Abhängig) | Wenn das Listenelement in einem Bild lauffähigen Container enthalten ist, muss das [ScrollItem](uiauto-implementingscrollitem.md) -Steuerelement Muster implementiert werden.                                                                                                                                                                                                                       |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depends (Abhängig) | Ein Listenelement-Steuerelement, das Auswahl unterstützt, muss das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster implementieren. Dadurch kann die Auswahl eines Listenelement-Steuerelements angezeigt werden.                                                                                                                                                                             |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depends (Abhängig) | Wenn das Listenelement überprüfbar ist und die Aktion keine Auswahl Zustandsänderung ausführt, muss das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster implementiert werden.                                                                                                                                                                                                            |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depends (Abhängig) | Wenn das Element bearbeitet werden kann, muss das [value](uiauto-implementingvalue.md) -Steuerelement Muster implementiert werden. Änderungen am Listenelement-Steuerelement bewirken Änderungen an den Werten der Eigenschaften [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md) und [**UIA \_ valuevaluepropertyid**](uiauto-control-pattern-propids.md) . |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Listenelement-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                                | Notizen                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                              |                                                                                                                                  |
| [**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ aufrufen \_ invokedebug-ID**](uiauto-event-ids.md)                                                                                  | Wenn das Steuerelement das [Aufruf](uiauto-implementinginvoke.md) Steuerungs Muster unterstützt, muss es dieses Ereignis unterstützen.                 |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                              | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.         |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                          | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ Itemstatuspropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                            | Wenn das-Steuerelement die [**ItemStatus**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss dieses Ereignis von unterstützt werden.        |
| [**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                                        |                                                                                                                                  |
| [**UIA \_ SelectionItem \_ elementaddecodto selectioneventid**](uiauto-event-ids.md)                                    | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**](uiauto-event-ids.md)                            | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ SelectionItem \_ elementselectedebug**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                                 | Wenn das Steuerelement das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                 |
| [**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                                               | Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                   |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein Container Listenelemente hostet, sollte das primäre Navigations Mittel zu den Listenelementen werden. Das Platzieren des Fokus auf die unter Elemente durch die Listen Navigation kann für Benutzer und Barrierefreiheits Tools verwirrend sein. Wenn der Container eine vertikale Liste von Elementen hostet, sollten Sie durch Drücken der nach-oben-und nach-unten-Taste durch die Elemente navigieren, aber durch Drücken der nach-rechts-und nach-links-Taste können Sie zu den unter Elementen des Fokus Elements navigieren, z. b. Listen Spalten oder UI-unter Elemente.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




