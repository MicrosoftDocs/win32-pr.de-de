---
title: Steuerelement-Typ bearbeiten
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Edit-Steuerelement Typen.
ms.assetid: ec45ec5e-4faa-4635-8726-5bbe1f20b843
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für Steuerelement Typen bearbeiten
- Benutzeroberflächenautomatisierungs, Bearbeitungs Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Struktur für Bearbeitungs Steuerelement
- Benutzeroberflächenautomatisierung, Eigenschaften für Steuerelement "Edit"
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Bearbeitungs Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Ereignisse für den Bearbeitungs Steuer ungstyp
- Struktur-Strukturen, Bearbeitungs Steuerelement-Typ
- Eigenschaften, Steuerelement Typ bearbeiten
- Steuerelement Muster, Edit Control Type
- Ereignisse, Bearbeitungs Steuerelement-Typ
- Unterstützung für Edit-Steuerelement Typen
- Edit-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Bearbeitungs Steuerelement-Typ
- Steuerelement Typen, Steuerelement Muster für den Bearbeitungs Steuerelement-Typ
- Steuerelement Typen, Unterstützung für Edit
- Steuerelement Typen, bearbeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7dffb572497df47d65def91dda22f3b8e59299
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856083"
---
# <a name="edit-control-type"></a>Steuerelement-Typ bearbeiten

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Edit** -Steuerelement Typen.

Mit einem Bearbeitungssteuerelement kann ein Benutzer eine einfache Textzeile ohne umfangreiche Formatierungsunterstützung anzeigen und bearbeiten

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den Bearbeitungs Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Bearbeitungs Steuerelemente, bei denen das UI-Framework/die Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Bearbeitungs Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Bearbeiten</li>
</ul></td>
<td><ul>
<li>Bearbeiten</li>
</ul></td>
</tr>
</tbody>
</table>



 

Die Steuerelemente, die den **Edit** -Steuerelement Typen implementieren, haben in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur immer NULL Schiebe leisten, da es sich um ein einzeilige Steuerelement handelt. Die einzelne Textzeile wird in einigen Layoutszenarien möglicherweise umgebrochen. Der **Bearbeitungs** Steuerelement-Typ ist nur für kleine Textmengen vorgesehen.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Bearbeitungs Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                         |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                             |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Das Bearbeitungssteuerelement muss über einen durch Klicken aktivierbaren Punkt verfügen, der den Eingabefokus an den Bearbeitungsbereich des Steuerelements übergibt, wenn ein Benutzer dort mit der Maus klickt.                                                                                                                                           |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Bearbeiten**   |                                                                                                                                                                                                                                                                                      |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Bearbeitungs Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                   |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Bearbeitungs Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                   |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                            |
| [**UIA \_ ispasswordpropertyid**](uiauto-automation-element-propids.md)                     | Siehe Hinweise. | Muss für Bearbeitungs Steuerelemente, die Kenn Wörter enthalten, auf **true** festgelegt werden. Wenn ein Bearbeitungssteuerelement Kennwörter enthält, kann diese Eigenschaft von einer Sprachausgabe verwendet werden, um zu ermitteln, ob Tastatureingaben bei der Eingabe durch den Benutzer vorgelesen werden sollen.                                      |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn dem Steuerelement eine statische Text Bezeichnung zugeordnet ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen. Wenn das Text Steuerelement eine Unterkomponente eines anderen Steuer Elements ist, wird keine **LabeledBy** -Eigenschaft festgelegt.                                                         |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Bearbeitungs** Steuerelement-Typ entspricht. Der Standardwert ist "Edit" für en-US oder Englisch (USA).                                                                                                                                                       |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Name des Bearbeitungssteuerelements wird üblicherweise aus einer statischen Textbezeichnung generiert. Wenn keine statische Text Bezeichnung vorhanden ist, muss der Anwendungsentwickler einen Eigenschafts Wert für den **Namen** zuweisen. Die **Name** -Eigenschaft darf niemals den Text Inhalt des Bearbeitungs Steuer Elements enthalten. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von Bearbeitungs Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                              | Unterstützung/Wert | Notizen                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Depends (Abhängig)       | Alle Bearbeitungs Steuerelemente, die einen numerischen Bereich annehmen, müssen das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster verfügbar machen.                                                                                                                                                                                                                                                                                       |
| [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Siehe Hinweise.    | Diese Eigenschaft muss der kleinste Wert sein, auf den der Inhalt des Bearbeitungs Steuer Elements festgelegt werden kann.                                                                                                                                                                                                                                                                                                                     |
| [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Siehe Hinweise.    | Diese Eigenschaft muss der größte Wert sein, auf den der Inhalt des Bearbeitungs Steuer Elements festgelegt werden kann.                                                                                                                                                                                                                                                                                                                      |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Siehe Hinweise.    | Diese Eigenschaft muss die Anzahl der Dezimalstellen angeben, die für den Wert festgelegt werden kann. Wenn das Bearbeitungs Steuerelement nur ganze Zahlen annimmt, muss der **SmallChange** -Eigenschafts Wert 1 lauten. Wenn das Bearbeitungs Steuerelement einen Bereich von 1,0 bis 2,0 annimmt, muss der **SmallChange** -Eigenschafts Wert 0,1 lauten. Wenn das Bearbeitungs Steuerelement einen Bereich von 1,00 bis 2,00 annimmt, muss der **SmallChange** -Eigenschafts Wert 0,001 lauten.                   |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NULL**      | Diese Eigenschaft muss auf einem Bearbeitungssteuerelement nicht verfügbar gemacht werden.                                                                                                                                                                                                                                                                                                                                                      |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Siehe Hinweise.    | Diese Eigenschaft gibt den numerischen Inhalt des Bearbeitungs Steuer Elements an. Wenn ein Benutzeroberflächenautomatisierungs-Client innerhalb der Bereiche, die in den [**minimalen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum) und [**maximalen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum) Eigenschaften angegeben sind, ein genauerer Wert festgelegt wird, wird die [**value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) -Eigenschaft automatisch auf den nächstgelegenen akzeptierten Wert gerundet. |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)                 | Erforderlich      | Alle Bearbeitungs Steuerelemente müssen das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützen, da ausführliche Informationen immer für Hilfstechnologieclients verfügbar sein müssen.                                                                                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Depends (Abhängig)       | Alle Bearbeitungs Steuerelemente, die eine Zeichenfolge akzeptieren, müssen das [Wert](uiauto-implementingvalue.md) Steuerelement Muster verfügbar machen.                                                                                                                                                                                                                                                                                                        |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | Siehe Hinweise.    | Diese Eigenschaft muss festgelegt werden, um anzugeben, ob für das Steuerelement ein Wert Programm gesteuert festgelegt werden kann oder ob er vom Benutzer bearbeitet werden kann.                                                                                                                                                                                                                                                                                |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Siehe Hinweise.    | Diese Eigenschaft enthält den Text Inhalt des Bearbeitungs Steuer Elements. Wenn die [**UIA \_ ispasswordpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft auf **true** festgelegt ist, muss beim Abfragen der [**value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) -Eigenschaft ein Fehler zurückgegeben werden.                                                                                                                      |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die Bearbeitungs Steuerelemente zur Unterstützung von benötigen Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                        | Notizen                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                      |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                      | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                  | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                                |                                                                                                                            |
| [**UIA \_ Rangevaluevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                             | Wenn das Steuerelement das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.   | Ein Bearbeitungs Steuerelement unterstützt niemals das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster.                                |
| [**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Ein Bearbeitungs Steuerelement unterstützt niemals das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster.                                |
| [**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.           | Ein Bearbeitungs Steuerelement unterstützt niemals das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster.                                |
| [**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.       | Ein Bearbeitungs Steuerelement unterstützt niemals das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster.                                |
| [**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.     | Ein Bearbeitungs Steuerelement unterstützt niemals das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster.                                |
| [**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.               | Ein Bearbeitungs Steuerelement unterstützt niemals das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster.                                |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_ \_ -Text textchangedebug**](uiauto-event-ids.md)                                                                      | Wenn das Steuerelement das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ \_ -Text textselectionchangedebug**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Valuevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.                                      | Wenn das Steuerelement das [value](uiauto-implementingvalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.             |



 

## <a name="remarks"></a>Bemerkungen

Ein Bearbeitungs Steuerelement kann als Schreib geschütztes Textfeld verwendet werden, das die Auswahl oder Bearbeitung von Text nicht unterstützt. Ein solches Bearbeitungs Steuerelement verhält sich wie ein Feld Objekt mit einem bestimmten Namen und Wert.

Wenn ein Bearbeitungs Steuerelement Platzhalter Text enthält (z. b. ein Hinweis Banner), sollte der Text als **HelpText** -Eigenschaft verwendet werden, es sei denn, der Text kann vom Benutzer bearbeitet und dann als Platzhalter Text wieder verwendet werden. Beispielsweise enthält die Windows Internet Explorer-Adressleiste den Text "about: Tabs", wenn eine neue Registerkarte geöffnet wird. Dies ist kein **HelpText** , da es sich um eine programmgesteuerte Adresse handelt, die vom Benutzer verwendet oder bearbeitet werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




