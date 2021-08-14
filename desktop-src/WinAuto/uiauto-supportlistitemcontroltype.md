---
title: ListItem-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den ListItem-Steuerelementtyp.
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den ListItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,ListItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für listItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für listItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den ListItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den ListItem-Steuerelementtyp
- Strukturstrukturen, ListItem-Steuerelementtyp
- properties,ListItem-Steuerelementtyp
- Steuerelementmuster, ListItem-Steuerelementtyp
- events,ListItem-Steuerelementtyp
- Unterstützung für den ListItem-Steuerelementtyp
- ListItem-Steuerelementtyp
- Steuerelementtypen,Struktur für ListItem-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für listItem-Steuerelementtyp
- Steuerelementtypen,Unterstützung für ListItem
- Steuerelementtypen,ListItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fc7df30fc9aeebbabd5a5fdb9572c9f4b81bda4507eac751f283841a14054a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825552"
---
# <a name="listitem-control-type"></a>ListItem-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **ListItem-Steuerelementtyp.**

Listenelementsteuerelemente sind ein Beispiel für Steuerelemente, die den **ListItem-Steuerelementtyp** implementieren.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **ListItem-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Listenelementsteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf Listenelementsteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).



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



 

Die untergeordneten Elemente eines Listenelementsteuerelements in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur müssen immer null untergeordnete Elemente anzeigen. Wenn die Struktur des Steuerelements so ist, dass unter dem Listenelement andere Elemente enthalten sind, sollte es die Anforderungen für die Benutzeroberflächenautomatisierung Unterstützung für den [TreeItem-Steuerelementtyp](uiauto-supporttreeitemcontroltype.md) erfüllen.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für den **ListItem-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Hinweise                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peerelemente in der Rohansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein. Ordnen Sie die **AutomationId-Eigenschaft** für ein Listenelement zu, wenn bekannt ist, dass das Element über verschiedene Instanzen der Benutzeroberfläche hinweg konsistent ist. Wenn das Listenelement dynamisch aufgefüllt und nicht vorhersagbar ist, lassen Sie die **AutomationId-Eigenschaft** leer.                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Der Wert dieser Eigenschaft sollte den Bereich des Bilds und den Textinhalt des Listenelements enthalten.                                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Depends (Abhängig)      | Wenn das Listensteuerelement über einen klickbaren Punkt verfügt (ein Punkt, auf den geklickt werden kann, damit die Liste den Fokus erhält), muss dieser Punkt über diese Eigenschaft verfügbar gemacht werden. Wenn das Listensteuerelement vollständig von Nachfolgerlistenelementen abgedeckt wird, wird der [**UIA \_ E \_ NOCLICKABLEPOINT-Fehler**](uiauto-error-codes.md) zurückgegeben, um anzugeben, dass der Client ein Element innerhalb des Listensteuerelements nach einem klickbaren Punkt fragen muss. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ListItem** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise.   | Im Hilfetext für Listensteuerelemente sollte erklärt werden, warum der Benutzer aufgefordert wird, eine Auswahl aus einer Liste von Optionen zu treffen. Hierbei handelt es sich in der Regel um dieselben Informationen, die durch ein QuickInfo angezeigt werden. Beispiel: "Wählen Sie ein Element aus, um die Anzeigeauflösung für Ihren Monitor festzulegen".                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Das Listensteuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Das Listensteuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn der Container Tastatureingaben akzeptieren kann, sollte dieser Eigenschaftswert **TRUE** sein.                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depends (Abhängig)      | Diese Eigenschaft muss einen Wert zurückgeben, der angibt, ob das Listenelement derzeit innerhalb des übergeordneten Containers, der [das Scroll-Steuerelementmuster](uiauto-implementingscroll.md) implementiert, in die Ansicht gescrollt wird.                                                                                                                                                                                                                                  |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Depends (Abhängig)      | Wenn das Steuerelement den Status enthält, der dynamisch aktualisiert wird, muss diese Eigenschaft unterstützt werden, damit eine Hilfstechnologie Updates erhalten kann, wenn sich der Status des Elements ändert.                                                                                                                                                                                                                                     |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Depends (Abhängig)      | Diese Eigenschaft sollte für Listenelement-Steuerelemente verfügbar gemacht werden, die ein zugrunde liegendes Objekt darstellen. Bei diesen Listenelement-Steuerelementen ist dem Steuerelement normalerweise ein Symbol zugeordnet, das Benutzer mit dem zugrunde liegenden Objekt assoziieren.                                                                                                                                                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.   | Wenn eine statische Textbezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf das entsprechende Steuerelement verfügbar machen.                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem **ListItem-Steuerelementtyp entspricht.** Der Standardwert ist "list item" für en-US oder Englisch (USA).                                                                                                                                                                                                                                                                                           |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Der Wert der Namenseigenschaft eines Listenelementsteuerelements stammt aus der Textbezeichnung des Elements.                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Listenelementsteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Wenn das Element bearbeitet werden kann, um Informationen ein- oder auszublenden, muss das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) implementiert werden.                                                                                                                                                                                                                        |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depends (Abhängig) | Wenn die räumliche Navigation von Element zu Element innerhalb des Listencontainers unterstützt wird und der Container in Zeilen und Spalten angeordnet ist, muss das [GridItem-Steuerelementmuster](uiauto-implementinggriditem.md) implementiert werden.                                                                                                                                                                  |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depends (Abhängig) | Wenn das Element über einen Befehl verfügt, der unabhängig [](uiauto-implementinginvoke.md) von der Auswahl ausgeführt werden kann, muss das Invoke-Steuerelementmuster implementiert werden. Dies ist normalerweise eine Aktion, die dem Doppelklicken auf das Listenelement-Steuerelement zugeordnet wird. Beispiele wären das Starten eines Dokuments über Windows Explorer oder das Wiederspielen einer Musikdatei in Microsoft Windows Media Player.        |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depends (Abhängig) | Wenn das Listenelement in einem Container enthalten ist, der scrollbar ist, muss das [ScrollItem-Steuerelementmuster](uiauto-implementingscrollitem.md) implementiert werden.                                                                                                                                                                                                                       |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depends (Abhängig) | Ein Listenelement-Steuerelement, das die Auswahl unterstützt, muss das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) implementieren. Dadurch kann die Auswahl eines Listenelement-Steuerelements angezeigt werden.                                                                                                                                                                             |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depends (Abhängig) | Wenn das Listenelement überprüft werden kann und die Aktion keine Änderung des Auswahlzustands vorsteuert, muss das [Steuerelementmuster "Umschalten"](uiauto-implementingtoggle.md) implementiert werden.                                                                                                                                                                                                            |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depends (Abhängig) | Wenn das Element bearbeitet werden kann, muss das [Value-Steuerelementmuster](uiauto-implementingvalue.md) implementiert werden. Änderungen am Listenelementsteuerelement führen zu Änderungen an den Werten der [**Eigenschaften UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) und [**UIA \_ ValueValuePropertyId.**](uiauto-control-pattern-propids.md) |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die Elementsteuerelemente unterstützen müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                                | Hinweise                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Wenn das Steuerelement das [Invoke-Steuerelementmuster](uiauto-implementinginvoke.md) unterstützt, muss es dieses Ereignis unterstützen.                 |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                              | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.         |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                          | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.       |
| [**UIA \_ ItemStatusPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                            | Wenn das Steuerelement die [**ItemStatus-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss dieses Ereignis unterstützen.        |
| [**UIA \_ NamePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                                        |                                                                                                                                  |
| [**UIA \_ \_ SelectionItem-ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ \_ SelectionItem-ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ \_ SelectionItem-ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ ToggleToggleStatePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)                                 | Wenn das Steuerelement das [Umschalten-Steuerelementmuster](uiauto-implementingtoggle.md) unterstützt, muss es dieses Ereignis unterstützen.                 |
| [**UIA \_ Durch die ValueValuePropertyId-Eigenschaft**](uiauto-control-pattern-propids.md) geändertes Ereignis.                                               | Wenn das Steuerelement das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützt, muss es dieses Ereignis unterstützen.                   |



 

## <a name="remarks"></a>Hinweise

Wenn ein Container Listenelemente hostet, sollte die primäre Navigationshilfe zu den Listenelementen gehen. Das Platzieren des Fokus auf Unterelemente über die Listennavigation kann für Benutzer und Barrierefreiheitstools verwirrend sein. Wenn der Container eine vertikale Liste von Elementen hostet, sollte durch Drücken der NACH-OBEN-TASTE und DER NACH-UNTEN-TASTE durch die Elemente navigiert werden, aber durch Drücken der NACH-RECHTS-TASTE und DER NACH-LINKS-TASTE können Sie zu Unterelementen des fokussierten Elements navigieren, z. B. Listenspalten oder Benutzeroberflächenunterelemente.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




