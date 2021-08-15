---
title: DataItem-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den DataItem-Steuerelementtyp.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den DataItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,DataItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für den DataItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den DataItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den DataItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den DataItem-Steuerelementtyp
- Benutzeroberflächenautomatisierung, große Listen und DataItem-Steuerelementtyp
- Strukturstrukturen,DataItem-Steuerelementtyp
- properties,DataItem-Steuerelementtyp
- Steuerelementmuster,DataItem-Steuerelementtyp
- ereignisse,DataItem-Steuerelementtyp
- Große Listen
- Unterstützung für den DataItem-Steuerelementtyp
- DataItem-Steuerelementtyp
- Steuerelementtypen, Struktur für DataItem-Steuerelementtyp
- Steuerelementtypen, Steuerelementmuster für den DataItem-Steuerelementtyp
- Steuerelementtypen, große Listen und DataItem-Steuerelementtyp
- Steuerelementtypen,Unterstützung für DataItem
- Steuerelementtypen,DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ec4612b43855578256d52bf6647b105ea666882cfe2f72dcdbf355559a7e5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826315"
---
# <a name="dataitem-control-type"></a>DataItem-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **DataItem-Steuerelementtyp.**

Ein Eintrag in einer Kontaktliste ist ein Beispiel für ein Datenelement-Steuerelement. Ein Datenelement-Steuerelement enthält Informationen, die für einen Endbenutzer von Interesse sind. Es ist komplizierter als das einfache Listenelement, da es mehr Informationen enthält.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **DataItem-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Datenelementsteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Arbeiten mit DataItems in großen Listen](#working-with-dataitems-in-large-lists)
-   [Erforderliche Ereignisse](#required-events)
-   [Beispiel für DataItem-Steuerelementtyp](#dataitem-control-type-example)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die datenelementsteuerelemente betrifft, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).



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
<li>DataItem
<ul>
<li>Variabel (0 oder mehr, kann hierarchisch strukturiert werden)</li>
</ul></li>
</ul></td>
<td><ul>
<li>DataItem
<ul>
<li>Variabel (0 oder mehr, kann hierarchisch strukturiert werden)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Ein DataItem-Element in einem Datenraster kann eine Vielzahl von Objekten hosten, wie etwa eine andere Ebene von Datenelementen oder bestimmte Rasterelemente, z. B. Text, Bilder oder Bearbeitungssteuerelemente. Wenn das Datenelementelement über eine bestimmte Objektrolle verfügt, sollte das Element als bestimmter Steuerelementtyp verfügbar gemacht werden. Beispielsweise ein [ListItem-Steuerelementtyp](uiauto-supportlistitemcontroltype.md) für ein auswählbares Datenelement im Raster.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für den DataItem-Steuerelementtyp besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Hinweise                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umschließenden Rechtecks klickbar ist und das Element spezielle Treffertests durchführt, überschreibt und stellt einen klickbaren Punkt bereit. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataItem** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Das Datenelement-Steuerelement muss immer ein Inhaltselement sein.                                                                                                                                                        |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Das Datenelement-Steuerelement muss immer ein Steuerelement sein.                                                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Siehe Hinweise.   | Wenn das Steuerelement den Status enthält, der dynamisch aktualisiert wird, muss diese Eigenschaft unterstützt werden, damit eine Hilfstechnologie Updates erhalten kann, wenn sich der Status des Elements ändert.        |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Siehe Hinweise.   | Dies ist der Zeichenfolgenwert, der dem Endbenutzer das zugrunde liegende Objekt übermittelt, das vom Element dargestellt wird. Beispiele hierfür sind "Mediendatei" und "Kontakt".                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null         | Datenelement-Steuerelemente verfügen nicht über eine statische Textbezeichnung.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem **DataItem-Steuerelementtyp entspricht.** Der Standardwert ist "data item" für en-US oder Englisch (USA).                                                              |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Das Datenelement-Steuerelement enthält immer ein primäres Textelement, das der Benutzer als Bezeichner für das Element erkennen würde.                                                                           |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Datenelementsteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Wenn das Datenelement erweitert oder reduziert werden kann, um Informationen anzuzeigen und auszublenden, muss das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) unterstützt werden.                                            |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depends (Abhängig) | Datenelemente unterstützen das [GridItem-Steuerelementmuster,](uiauto-implementinggriditem.md) wenn eine Sammlung von Datenelementen in einem Container verfügbar ist, in dem zwischen Elementen räumlich navigiert werden kann.                 |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depends (Abhängig) | Alle Datenelemente unterstützen die Möglichkeit, mit dem [ScrollItem-Steuerelementmuster](uiauto-implementingscrollitem.md) in die Ansicht gescrollt zu werden, wenn ihr Datencontainer mehr Elemente enthält, als auf den Bildschirm passen können.             |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depends (Abhängig) | Die Möglichkeit, die Datenelemente auszuwählen, hängt vom Inhalt ab.                                                                                                                                                          |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | Depends (Abhängig) | Wenn das Datenelement in einem [DataGrid-Steuerelementtyp](uiauto-supportdatagridcontroltype.md) enthalten ist, der über ein Headerelement verfügt, sollte es das [TableItem-Steuerelementmuster](uiauto-implementingtableitem.md) unterstützen. |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depends (Abhängig) | Wenn das Datenelement einen Zustand enthält, der durchlaufen [](uiauto-implementingtoggle.md) werden kann, sollte es das Umschalten-Steuerelementmuster unterstützen.                                                                          |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depends (Abhängig) | Wenn der primäre Text des Datenelements bearbeitet werden kann, muss das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützt werden.                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a>Arbeiten mit DataItems in großen Listen

Da große Listen häufig in Benutzeroberflächenframeworks virtualisiert werden, um die Leistung zu verbessern, kann ein Benutzeroberflächenautomatisierung-Client das Abfragefeature Benutzeroberflächenautomatisierung nicht verwenden, um den Inhalt der vollständigen Struktur auf die gleiche Weise wie in anderen Elementcontainern zu durchsuchen. Ein Client sollte das Element in die Ansicht scrollen (oder das Steuerelement erweitern, um alle verfügbaren Optionen anzuzeigen), bevor er auf den vollständigen Satz von Informationen aus dem Datenelement zugreift.

Wenn [**Sie SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) für das Benutzeroberflächenautomatisierung -Element für das Datenelement aufrufen, gibt Microsoft Windows Explorer erfolgreich zurück und bewirkt, dass der Fokus auf das Edit-Steuerelement innerhalb der Datenelementunterstruktur festgelegt wird.

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Datenelementsteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                                | Hinweise                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md) | Wenn das Steuerelement das [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Wenn das Steuerelement [](uiauto-implementinginvoke.md) das Invoke-Steuerelementmuster unterstützt, muss es dieses Ereignis unterstützen.                 |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                              | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.         |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                          | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ ItemStatusPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                            | Wenn das Steuerelement die [**ItemStatus-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.        |
| [**UIA \_ Das NamePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                                                        |                                                                                                                                  |
| [**UIA \_ \_ SelectionItem-ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ \_ SelectionItem-ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ \_ SelectionItem-ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ Das ToggleToggleStatePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)                                 | Wenn das Steuerelement das [Umschalten-Steuerelementmuster](uiauto-implementingtoggle.md) unterstützt, muss es dieses Ereignis unterstützen.                 |
| [**UIA \_ ValueValuePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)                                               | Wenn das Steuerelement das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützt, muss es dieses Ereignis unterstützen.                   |



 

## <a name="dataitem-control-type-example"></a>Beispiel für DataItem-Steuerelementtyp

Die folgende Abbildung veranschaulicht einen DataItem-Steuerelementtyp in einem Listenansicht-Steuerelement.

![Screenshot des Listenansicht-Steuerelements mit dem Steuerelementtyp "dataitem"](images/dataitemxmpl.jpg)

Die Steuerelementansicht und die Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf das Datenelementsteuerelement bezieht, werden unten angezeigt. Die Steuerelementmuster für jedes Automatisierungselement sind in Klammern aufgeführt. Die **Gruppe** "Contoso" ist auch Teil des Rasters des Datenraster-Hoststeuerelements. Ein Beispiel für eine Rasterstruktur auf höherer Ebene finden Sie unter [DataGrid-Steuerelementtyp.](uiauto-supportdatagridcontroltype.md)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Benutzeroberflächenautomatisierung-Struktur – Steuerelementansicht</th>
<th>Benutzeroberflächenautomatisierung-Struktur – Inhaltsansicht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Gruppe &quot; Contoso &quot; (Tabelle, Raster)
<ul>
<li>&quot;DataItem-Konten Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>&quot;image accounts Receivable.doc&quot;</li>
<li>Edit &quot; Name &quot; (TableItem, GridItem, Value &quot; Accounts Receivable.doc&quot; )</li>
<li>Edit &quot; Date modified &quot; (TableItem, GridItem, Value &quot; 8/25/2006 15:29 &quot; PM)</li>
<li>Größe bearbeiten &quot; &quot; (GridItem, TableItem, Wert &quot; 11,0 &quot; KB)</li>
</ul></li>
<li>&quot;DataItem-Konten Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Gruppe &quot; Contoso &quot; (Tabelle, Raster)
<ul>
<li>&quot;DataItem-Konten Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>&quot;image accounts Receivable.doc&quot;</li>
<li>Edit &quot; Name &quot; (TableItem, GridItem, Value &quot; Accounts Receivable.doc&quot; )</li>
<li>Edit &quot; Date modified &quot; (TableItem, GridItem, Value &quot; 8/25/2006 15:29 &quot; PM)</li>
<li>Größe bearbeiten &quot; &quot; (GridItem, TableItem, Wert &quot; 11,0 &quot; KB)</li>
</ul></li>
<li>&quot;DataItem-Konten Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Wenn ein Raster eine Liste auswählbarer Elemente darstellt, können die entsprechenden auswählbaren UI-Elemente mit dem [ListItem-Steuerelementtyp](uiauto-supportlistitemcontroltype.md) anstelle des DataItem-Steuerelementtyps verfügbar gemacht werden. Im vorherigen Beispiel können die **DataItem-Elemente** ("Accounts Receivable.doc" und "Accounts Payable.doc") unter **Group** ("Contoso") verbessert werden, indem sie als ListItem-Steuerelementtypen verfügbar sind, da dieser Typ bereits das [SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md) unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




