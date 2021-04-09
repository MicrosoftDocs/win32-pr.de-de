---
title: DataItem-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den DataItem-Steuerelement Typen.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für DataItem-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, DataItem-Steuerelement Typen
- UI-Automatisierung, Baumstruktur für DataItem-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für DataItem-Steuerelement Typen
- UI-Automatisierung, Steuerelement Muster für DataItem-Steuerelement Typen
- UI-Automatisierung, Ereignisse für DataItem-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, große Listen und DataItem-Steuerelement Typen
- Struktur Strukturen, DataItem-Steuerelement Typen
- Eigenschaften, DataItem-Steuerelement Typen
- Steuerelement Muster, DataItem-Steuerelement Typen
- Ereignisse, DataItem-Steuerelement Typen
- große Listen
- Unterstützung für DataItem-Steuerelement Typen
- DataItem-Steuerelement Typen
- Steuerelement Typen, Baumstruktur für DataItem-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für DataItem-Steuerelement Typen
- Steuerelement Typen, große Listen und DataItem-Steuerelement Typen
- Steuerelement Typen, Unterstützung für DataItem
- Steuerelement Typen, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0902cc593ec7f9104ed27031caa2785b7cb9756
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036857"
---
# <a name="dataitem-control-type"></a>DataItem-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **DataItem** -Steuerelement Typen.

Ein Eintrag in einer Kontaktliste ist ein Beispiel für ein Datenelement-Steuerelement. Ein Datenelement-Steuerelement enthält Informationen, die für einen Endbenutzer von Interesse sind. Es ist komplizierter als das einfache Listenelement, da es mehr Informationen enthält.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **DataItem** -Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Datenelement-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung für die Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Arbeiten mit dataItems in großen Listen](#working-with-dataitems-in-large-lists)
-   [Erforderliche Ereignisse](#required-events)
-   [Beispiel für DataItem-Steuerelementtyp](#dataitem-control-type-example)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Datenelement-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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



 

Ein DataItem-Element in einem Datenraster kann eine Vielzahl von Objekten hosten, wie etwa eine andere Ebene von Datenelementen oder bestimmte Rasterelemente, z. B. Text, Bilder oder Bearbeitungssteuerelemente. Wenn das Datenelement Element über eine bestimmte Objekt Rolle verfügt, muss das Element als bestimmter Steuer Elementtyp verfügbar gemacht werden. beispielsweise ein [ListItem](uiauto-supportlistitemcontroltype.md) -Steuer Elementtyp für ein auswählbares Datenelement im Raster.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den DataItem-Steuerelement-Typ besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Notizen                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **DataItem** |                                                                                                                                                                                                      |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Das Datenelement-Steuerelement muss immer ein Inhaltselement sein.                                                                                                                                                        |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Das Datenelement-Steuerelement muss immer ein Steuerelement sein.                                                                                                                                                      |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                            |
| [**UIA \_ itemstatuspropertyid**](uiauto-automation-element-propids.md)                     | Siehe Hinweise.   | Wenn das Steuerelement den Status enthält, der dynamisch aktualisiert wird, muss diese Eigenschaft unterstützt werden, damit eine Hilfstechnologie Updates empfangen kann, wenn sich der Status des Elements ändert.        |
| [**UIA \_ itemtypepropertyid**](uiauto-automation-element-propids.md)                         | Siehe Hinweise.   | Dies ist der Zeichenfolgenwert, der dem Endbenutzer das zugrunde liegende Objekt übermittelt, das vom Element dargestellt wird. Beispiele hierfür sind "Media File" und "Contact".                                                   |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Null         | Datenelement-Steuerelemente verfügen nicht über eine statische Textbezeichnung.                                                                                                                                                  |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge, die dem **DataItem** -Steuerelement Typen entspricht. Der Standardwert ist "Datenelement" für en-US oder Englisch (USA).                                                              |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Das Datenelement-Steuerelement enthält immer ein primäres Textelement, das der Benutzer als Bezeichner für das Element erkennen würde.                                                                           |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von allen Datenelement Steuerelementen unterstützt werden müssen Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support | Notizen                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depends (Abhängig) | Wenn das Datenelement erweitert oder reduziert werden kann, um Informationen anzuzeigen und auszublenden, muss das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützt werden.                                            |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depends (Abhängig) | Datenelemente unterstützen das [GridItem](uiauto-implementinggriditem.md) -Steuerelement Muster, wenn eine Auflistung von Datenelementen in einem Container verfügbar ist, der räumlich navigiert werden kann.                 |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depends (Abhängig) | Alle Datenelemente unterstützen die Möglichkeit, mit dem [ScrollItem](uiauto-implementingscrollitem.md) -Steuerelement Muster in die Ansicht zu scrollen, wenn Ihr Datencontainer mehr Elemente enthält, als auf den Bildschirm passen.             |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depends (Abhängig) | Die Möglichkeit, die Datenelemente auszuwählen, hängt vom Inhalt ab.                                                                                                                                                          |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | Depends (Abhängig) | Wenn das Datenelement in einem [DataGrid-](uiauto-supportdatagridcontroltype.md) Steuer Elementtyp enthalten ist, der über ein Header Element verfügt, sollte das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster unterstützt werden. |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depends (Abhängig) | Wenn das Datenelement einen Zustand enthält, der durchlaufen werden kann, sollte es das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster unterstützen.                                                                          |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depends (Abhängig) | Wenn der primäre Text des Datenelements bearbeitbar ist, muss das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt werden.                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a>Arbeiten mit dataItems in großen Listen

Da große Listen häufig innerhalb von Benutzeroberflächen-Frameworks virtualisiert werden, um die Leistung zu unterstützen, kann ein Benutzeroberflächenautomatisierungs-Client die Funktion "UI Automation Query" nicht verwenden, um den Inhalt der gesamten Struktur auf die gleiche Weise zu durchsuchen wie in anderen Element Containern. Ein Client sollte den Bildlauf im Element anzeigen (oder das Steuerelement erweitern, um alle verfügbaren Optionen anzuzeigen), bevor er auf den vollständigen Satz von Informationen aus dem Datenelement zugreift.

Wenn Sie [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) für das Benutzeroberflächenautomatisierungs-Element für das Datenelement aufrufen, gibt Microsoft Windows-Explorer erfolgreich zurück und bewirkt, dass der Fokus auf das Bearbeitungs Steuerelement innerhalb der Datenelement-Teilstruktur festgelegt wird.

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Datenelement-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                                | Notizen                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                              |                                                                                                                                  |
| [**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ aufrufen \_ invokedebug-ID**](uiauto-event-ids.md)                                                                                  | Wenn das Steuerelement das [Aufruf](uiauto-implementinginvoke.md) Steuerungs Muster unterstützt, muss es dieses Ereignis unterstützen.                 |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                              | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.         |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                          | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ Itemstatuspropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                            | Wenn das Steuerelement die [**ItemStatus**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.        |
| [**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                                        |                                                                                                                                  |
| [**UIA \_ SelectionItem \_ elementaddecodto selectioneventid**](uiauto-event-ids.md)                                    | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**](uiauto-event-ids.md)                            | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ SelectionItem \_ elementselectedebug**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                                 | Wenn das Steuerelement das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                 |
| [**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                                               | Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                   |



 

## <a name="dataitem-control-type-example"></a>Beispiel für DataItem-Steuerelementtyp

Die folgende Abbildung veranschaulicht einen DataItem-Steuerelement Typen in einem Listenansicht-Steuerelement.

![Screenshot des Listenansicht-Steuer Elements mit DataItem-Steuerelement Typen](images/dataitemxmpl.jpg)

Die Steuerelement Ansicht und die Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur, die sich auf das Datenelement-Steuerelement bezieht, werden unten angezeigt. Die Steuerelementmuster für jedes Automatisierungselement sind in Klammern aufgeführt. Die **Gruppe** "Configuration Manager" ist auch Teil des Rasters des Datenraster-Host Steuer Elements. Ein Beispiel für eine Raster Struktur höherer Ebene finden Sie unter [DataGrid-Steuerelement Typen](uiauto-supportdatagridcontroltype.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Benutzeroberflächenautomatisierungs-Struktur-Steuerelement Ansicht</th>
<th>Benutzeroberflächenautomatisierungs-Struktur-Inhaltsansicht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Group &quot; &quot; (Tabelle, Raster)
<ul>
<li>DataItem- &quot; Konten Receivable.doc&quot; (TableItem, GridItem, SelectionItem, aufrufen)
<ul>
<li>Receivable.docfür Image &quot; Konten &quot;</li>
<li>&quot;Name bearbeiten &quot; (TableItem, GridItem, Wert &quot; Konten Receivable.doc&quot; )</li>
<li>Änderungs &quot; Datum geändert &quot; (TableItem, GridItem, Wert &quot; 8/25/2006 3:29 PM &quot; )</li>
<li>&quot;Größe bearbeiten &quot; (GridItem, TableItem, Wert &quot; 11,0 KB &quot; )</li>
</ul></li>
<li>DataItem- &quot; Konten Payable.doc&quot; (TableItem, GridItem, SelectionItem, aufrufen)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Group &quot; &quot; (Tabelle, Raster)
<ul>
<li>DataItem- &quot; Konten Receivable.doc&quot; (TableItem, GridItem, SelectionItem, aufrufen)
<ul>
<li>Receivable.docfür Image &quot; Konten &quot;</li>
<li>&quot;Name bearbeiten &quot; (TableItem, GridItem, Wert &quot; Konten Receivable.doc&quot; )</li>
<li>Änderungs &quot; Datum geändert &quot; (TableItem, GridItem, Wert &quot; 8/25/2006 3:29 PM &quot; )</li>
<li>&quot;Größe bearbeiten &quot; (GridItem, TableItem, Wert &quot; 11,0 KB &quot; )</li>
</ul></li>
<li>DataItem- &quot; Konten Payable.doc&quot; (TableItem, GridItem, SelectionItem, aufrufen)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Wenn ein Raster eine Liste auswählbarer Elemente darstellt, können die entsprechenden auswählbaren Benutzeroberflächen Elemente mit dem Steuer Elementtyp " [ListItem](uiauto-supportlistitemcontroltype.md) " statt mit dem Steuer Elementtyp "DataItem" verfügbar gemacht werden. Im vorherigen Beispiel können die **DataItem** -Elemente ("Accounts Receivable.doc" und "Accounts Payable.doc") unter " **Group** (" ")" ("kontoso") verbessert werden, indem Sie als ListItem-Steuerelement Typen verfügbar gemacht werden, da dieser Typ bereits das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




