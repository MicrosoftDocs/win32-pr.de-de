---
title: Text Steuerelement-Typ
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuerelement Text.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für Text Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Text Steuerelement-Typ
- UI-Automatisierung, Baumstruktur für Text Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Eigenschaften für Text Steuerelement-Typ
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Text Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für Text Steuerelement-Typ
- Struktur Strukturen, Text Steuerelement-Typ
- Eigenschaften, Text Steuerelement-Typ
- Steuerelement Muster, Text Steuerelement-Typ
- Ereignisse, Text Steuerelement-Typ
- Unterstützung für den Text Steuerungstyp
- Text-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Text Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Text Steuerelement Typen
- Steuerelement Typen, Unterstützung für Text
- Steuerelement Typen, Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310591"
---
# <a name="text-control-type"></a>Text Steuerelement-Typ

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuerelement **Text** .

Ein Text Steuerelement ist ein grundlegendes Element der Benutzeroberfläche, das ein Textelement auf dem Bildschirm darstellt.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den Steuerelement **Text** definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Struktur Steuerelemente, bei denen das UI-Framework/die Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Text Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Text</li>
</ul></td>
<td><ul>
<li>Text (wenn Inhalt)</li>
</ul></td>
</tr>
</tbody>
</table>



 

Ein Textsteuerelement kann eigenständig als Bezeichnung oder als statischer Text auf einem Formular verwendet werden. Sie kann auch in der Struktur eines der folgenden Elemente enthalten sein:

-   [DataItem](uiauto-supportdataitemcontroltype.md)
-   [ListItem](uiauto-supportlistitemcontroltype.md)
-   [TreeItem](uiauto-supporttreeitemcontroltype.md)

Text Steuerelemente werden möglicherweise nicht in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt, weil Text häufig durch die **Name** -Eigenschaft eines anderen Steuer Elements angezeigt wird. Beispielsweise wird der Text, der zum Bezeichnen eines Kombinations Feld-Steuer Elements verwendet wird, über die **Name** -Eigenschaft des Steuer Elements verfügbar gemacht. Da sich das Kombinations Feld-Steuerelement in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur befindet, muss das Text Steuerelement nicht vorhanden sein. Text Steuerelemente können untergeordnete Elemente in der Inhaltsansicht enthalten, wenn ein eingebettetes Objekt wie ein Hyperlink vorhanden ist.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Text Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                                                                                        |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                            |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.                                                                                                                                                |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Text**   |                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | Depends (Abhängig)    | Das Text Steuerelement ist Inhalt, wenn es Informationen enthält, die nicht in der Namenseigenschaft eines anderen Steuer Elements verfügbar gemacht werden                                                                                                                                                                                                                                              |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Textsteuerelement muss stets ein Steuerelement sein.                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                                                           |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL       | Textsteuerelemente haben keine statische Textbezeichnung.                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Text** Steuerelement-Typ entspricht. Der Standardwert ist "Text" für en-US oder Englisch (USA).                                                                                                                                                                                                                      |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Name eines Text Steuer Elements kann der Text sein, der angezeigt wird. Wenn das Steuerelement jedoch auch das [Text](uiauto-implementingtextandtextrange.md) Muster unterstützt, und der Text sehr umfangreich ist, verwenden Sie nicht den voll Text Inhalt als **Name** -Wert. Geben Sie **stattdessen einen** kürzerer Wert an, der von anderen Eigenschaften Ihres Steuer Elements abgeleitet ist. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von Text Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support | Notizen                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Depends (Abhängig) | Wenn das Text Steuerelement in einem Tabellen Steuerelement enthalten ist, muss das [GridItem](uiauto-implementinggriditem.md) -Steuerelement Muster unterstützt werden.                                                                                                                            |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Depends (Abhängig) | Wenn das Text Steuerelement in einem Tabellen Steuerelement enthalten ist, muss das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster unterstützt werden.                                                                                                                          |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | Depends (Abhängig) | Text sollte das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster für eine bessere Barrierefreiheit unterstützen. Es ist jedoch nicht erforderlich. Das Text-Steuerelementmuster ist nützlich, wenn der Text viele Formate und Attribute hat (z. B., Farbe, Fettdruck und Kursivdruck). |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | Nie   | Ein Text Steuerelement unterstützt niemals das [value](uiauto-implementingvalue.md) -Steuerelement Muster. Wenn der Text bearbeitet werden kann, handelt es sich um den [Bearbeitungs](uiauto-supporteditcontroltype.md) Steuerelement-Typ.                                                                                    |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die Text Steuerelemente zur Unterstützung von benötigen Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                           |                                                                                                                            |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ \_ -Text textchangedebug**](uiauto-event-ids.md)                                                 | Wenn das Steuerelement das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




