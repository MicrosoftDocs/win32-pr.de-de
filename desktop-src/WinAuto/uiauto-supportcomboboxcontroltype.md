---
title: ComboBox-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den ComboBox-Steuerelement Typen.
ms.assetid: e7c64dc1-e1e3-4f99-adde-d0d63eb6c4c9
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für ComboBox-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, ComboBox-Steuerelement Typen
- UI-Automatisierung, Struktur für ComboBox-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für ComboBox-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für ComboBox-Steuerelement Typen
- UI-Automatisierung, Ereignisse für ComboBox-Steuerelement Typen
- Struktur Strukturen, ComboBox-Steuerelement Typen
- Eigenschaften, ComboBox-Steuerelement Typen
- Steuerelement Muster, ComboBox-Steuerelement Typen
- Ereignisse, ComboBox-Steuerelement Typen
- Unterstützung für ComboBox-Steuerelement Typen
- ComboBox-Steuerelement Typen
- Steuerelement Typen, Baumstruktur für ComboBox-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für ComboBox-Steuerelement Typen
- Steuerelement Typen, Unterstützung für ComboBox
- Steuerelement Typen, ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410cca4887c04a00d6da53feb9fcf1242476a979
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710319"
---
# <a name="combobox-control-type"></a>ComboBox-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **ComboBox** -Steuerelement Typen.

Ein Kombinationsfeld ist ein Listenfeld, das mit einem statischen Steuerelement oder einem Bearbeitungssteuerelement kombiniert ist und das momentan ausgewählte Element im Listenfeldbereich des Kombinationsfelds anzeigt. Der Listenfeldbereich des Steuerelements wird dauerhaft oder nur dann angezeigt, wenn der Dropdownpfeil (der eine Schaltfläche ist) neben dem Steuerelement ausgewählt wurde. Wenn das Auswahlfeld ein Bearbeitungssteuerelement ist, kann der Benutzer Informationen eingeben, die in der Liste nicht vorhanden sind. Andernfalls kann er nur Elemente in der Liste auswählen.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **ComboBox** -Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Kombinations Feld-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Kombinations Feld-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Kombinationsfeld
<ul>
<li>Bearbeitung (0 oder 1)</li>
<li>List (0 oder 1)</li>
<li>Listenelement (untergeordnetes Element von Liste; 0 bis viele)</li>
<li>Schaltfläche (1)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Kombinationsfeld
<ul>
<li>Listenelement (0 bis viele)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Das Bearbeitungs Steuerelement in der Steuerelement Ansicht des Kombinations Felds ist nur erforderlich, wenn das Kombinations Feld bearbeitet werden kann, um Eingaben zu übernehmen. Dies ist der Fall, wenn das Kombinations Feld im Dialogfeld **Ausführen** vorhanden ist.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **ComboBox** -Steuerelement Typ besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                                                     |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                         |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.                                                                                                             |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | Kombinationsfeld   |                                                                                                                                                                                                                                                                                                                  |
| [**UIA \_ helptextpropertyid**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Der Hilfetext für Kombinations Feld-Steuerelemente sollte erläutern, warum der Benutzer gefragt wird, wählen Sie eine Option aus dem Kombinations Feld aus. Der Text ist mit den in einer QuickInfo angezeigten Informationen vergleichbar. Beispiel: „Wählen Sie ein Element aus, um die Anzeigeauflösung des Bildschirms festzulegen.“                                                |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Kombinations Feld-Steuerelemente sind immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                            |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Kombinations Feld-Steuerelemente sind immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                            |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | TRUE       | Kombinations Feld-Steuerelemente können den Tastaturfokus erhalten. Wenn jedoch ein Benutzeroberflächenautomatisierungs-Client den Fokus auf ein Kombinations Feld setzt, kann jedes Element in der Unterstruktur des Kombinations Felds den Fokus erhalten.                                                                                                                                          |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Ein Kombinationsfeld-Steuerelement hat normalerweise eine statische Textbezeichnung, auf die diese Eigenschaft verweist.                                                                                                                                                                                                                             |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **ComboBox** -Steuerelement Typ entspricht. Der Standardwert ist "Kombinations Feld" für en-US oder Englisch (USA).                                                                                                                                                                          |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Name des Kombinations Feld-Steuer Elements wird in der Regel aus einer statischen Text Bezeichnung generiert. Wenn keine statische Text Bezeichnung vorhanden ist, müssen Sie einen Wert für die **Name** -Eigenschaft zuweisen. Die **Name** -Eigenschaft darf niemals den aktuellen Inhalt des Kombinations Felds enthalten oder sich ändern, wenn sich die Inhalte des Kombinations Felds ändern. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Kombinations Feld-Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                                   | Support  | Notizen                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Erforderlich | Das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster muss unterstützt werden, da ein Kombinations Feld-Steuerelement immer eine Dropdown Schaltfläche enthalten muss.                                                                                                                                                                                |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)           | Depends (Abhängig)  | Zeigt die aktuelle Auswahl im Kombinationsfeld an. Unterstützung für das [Selection](uiauto-implementingselection.md) -Steuerelement Muster wird an das Listenfeld unter dem Kombinations Feld delegiert, ist aber möglicherweise nicht immer möglich.                                                                                                                               |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depends (Abhängig)  | Wenn das Kombinations Feld beliebige Textwerte aufnehmen kann, muss das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt werden. Mit diesem Muster kann der Zeichen folgen Inhalt des Kombinations Felds Programm gesteuert festgelegt werden. Wenn das Value-Steuerelement Muster nicht unterstützt wird, muss der Benutzer aus den Listenelementen in der Teilstruktur des Kombinations Felds auswählen. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                 | Nie    | Das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster wird niemals direkt in einem Kombinations Feld unterstützt. Es wird unterstützt, wenn ein Listenfeld, das in einem Kombinations Feld enthalten ist, einen Bildlauf durchführen kann und nur wenn das Listenfeld auf dem Bildschirm sichtbar ist                                                                                                              |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Kombinations Feld-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                                | Notizen                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                              |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                              | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                          | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                               |                                                                                                                            |
| [**UIA \_ Expandredugenexpandredugenstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                                               | Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




