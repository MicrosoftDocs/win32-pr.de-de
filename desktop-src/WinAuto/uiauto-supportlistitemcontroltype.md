---
title: ListItem-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den ListItem-Steuerelementtyp.
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den ListItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,ListItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den ListItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Properties für den ListItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den ListItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,events für den ListItem-Steuerelementtyp
- Strukturstrukturen,ListItem-Steuerelementtyp
- properties,ListItem-Steuerelementtyp
- Steuerelementmuster,ListItem-Steuerelementtyp
- events,ListItem-Steuerelementtyp
- Unterstützung für den ListItem-Steuerelementtyp
- ListItem-Steuerelementtyp
- Steuerelementtypen,Struktur für ListItem-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für den ListItem-Steuerelementtyp
- Steuerelementtypen,Unterstützung für ListItem
- Steuerelementtypen, ListItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf7275212d44b795f354cb895c2d64727e375ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483196"
---
# <a name="listitem-control-type"></a>ListItem-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **ListItem-Steuerelementtyp.**

Listenelementsteuerelemente sind ein Beispiel für Steuerelemente, die den **ListItem-Steuerelementtyp** implementieren.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **ListItem-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Listenelementsteuerelemente, bei denen das Benutzeroberflächenframework/die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf Listenelementsteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>ListItem<ul><li>Bild (beliebige Anzahl)</li><li>Text (beliebige Anzahl)</li><li>Bearbeiten (beliebige Anzahl)</li></ul></li></ul> | <ul><li>ListItem</li></ul> | 




 

Die unteren Elemente eines Listenelement-Steuerelements in der Inhaltsansicht der Benutzeroberflächenautomatisierung struktur muss immer 0 (null) elemente anzeigen. Wenn die Struktur des Steuerelements so ist, dass andere Elemente unter dem Listenelement enthalten sind, sollte es die Anforderungen für die Benutzeroberflächenautomatisierung-Unterstützung für den [TreeItem-Steuerelementtyp](uiauto-supporttreeitemcontroltype.md) erfüllen.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, deren Wert oder Definition für den **ListItem-Steuerelementtyp** besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Hinweise                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein. Ordnen Sie **die AutomationId-Eigenschaft** für ein Listenelement zu, wenn bekannt ist, dass das Element über verschiedene Instanzen der Benutzeroberfläche hinweg konsistent ist. Wenn das Listenelement dynamisch aufgefüllt und nicht vorhersagbar ist, lassen Sie die **AutomationId-Eigenschaft** leer.                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Der Wert dieser Eigenschaft sollte den Bereich des Bilds und den Textinhalt des Listenelements enthalten.                                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Depends (Abhängig)      | Wenn das Listensteuer steuerelement über einen klickbaren Punkt verfügt (ein Punkt, auf den geklickt werden kann, damit die Liste den Fokus besitzt), muss dieser Punkt über diese Eigenschaft verfügbar gemacht werden. Wenn das Listensteuerelement vollständig von Nachfolgerlistenelementen abgedeckt wird, wird der [**UIA \_ E \_ NOCLICKABLEPOINT-Fehler**](uiauto-error-codes.md) zurückgegeben, um anzugeben, dass der Client ein Element innerhalb des Listensteuerelements nach einem klickbaren Punkt fragen muss. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ListItem** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise.   | Im Hilfetext für Listensteuerelemente sollte erklärt werden, warum der Benutzer aufgefordert wird, eine Auswahl aus einer Liste von Optionen zu treffen. Hierbei handelt es sich in der Regel um dieselben Informationen, die durch ein QuickInfo angezeigt werden. Beispiel: "Wählen Sie ein Element aus, um die Anzeigeauflösung für Ihren Monitor fest."                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Das Listensteuer steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Das Listensteuer steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung enthalten.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn der Container Tastatureingaben akzeptieren kann, sollte dieser Eigenschaftswert **TRUE sein.**                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depends (Abhängig)      | Diese Eigenschaft muss einen Wert zurückgeben, um zu bestimmen, ob das Listenelement derzeit innerhalb des übergeordneten Containers, der das Bildlauf-Steuerelementmuster implementiert, in die Ansicht [gescrollt](uiauto-implementingscroll.md) wird.                                                                                                                                                                                                                                  |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Depends (Abhängig)      | Wenn das Steuerelement den Status enthält, der dynamisch aktualisiert wird, muss diese Eigenschaft unterstützt werden, damit eine Hilfstechnologie Updates empfangen kann, wenn sich der Status des Elements ändert.                                                                                                                                                                                                                                     |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Depends (Abhängig)      | Diese Eigenschaft sollte für Listenelement-Steuerelemente verfügbar gemacht werden, die ein zugrunde liegendes Objekt darstellen. Bei diesen Listenelement-Steuerelementen ist dem Steuerelement normalerweise ein Symbol zugeordnet, das Benutzer mit dem zugrunde liegenden Objekt assoziieren.                                                                                                                                                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise.   | Wenn eine statische Textbezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf das entsprechende Steuerelement verfügbar machen.                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem **ListItem-Steuerelementtyp** entspricht. Der Standardwert ist "Listenelement" für en-US oder Englisch (USA).                                                                                                                                                                                                                                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Der Wert der Name-Eigenschaft eines Listenelement-Steuerelements stammt aus der Textbezeichnung des Elements.                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von allen Listenelementsteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



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

 

 




