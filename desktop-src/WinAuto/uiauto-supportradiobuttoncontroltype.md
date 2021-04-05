---
title: RadioButton-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den RadioButton-Steuer Elementtyp.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für RadioButton-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, RadioButton-Steuer Elementtyp
- UI-Automatisierung, Baumstruktur für RadioButton-Steuer Elementtyp
- UI-Automatisierung, Eigenschaften für RadioButton-Steuer Elementtyp
- UI-Automatisierung, Steuerelement Muster für RadioButton-Steuer Elementtyp
- UI-Automatisierung, Ereignisse für RadioButton-Steuer Elementtyp
- Struktur Strukturen, RadioButton-Steuer Elementtyp
- Eigenschaften, RadioButton-Steuer Elementtyp
- Steuerelement Muster, RadioButton-Steuer Elementtyp
- Ereignisse, RadioButton-Steuer Elementtyp
- Unterstützung für RadioButton-Steuer Elementtyp
- RadioButton-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für RadioButton-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für den RadioButton-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für RadioButton
- Steuerelement Typen, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702a2227a5164ff694378c82fa3b7cde33f9823
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712702"
---
# <a name="radiobutton-control-type"></a>RadioButton-Steuer Elementtyp

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **RadioButton** -Steuer Elementtyp.

Ein Optionsfeld besteht aus einer runden Schaltfläche und anwendungsdefiniertem Text (eine Bezeichnung), einem Symbol oder eine Bitmap, die eine Option anzeigt, die der Benutzer durch Aktivieren der Schaltfläche auswählen kann. Eine Anwendung verwendet in der Regel Optionsfelder in einem Gruppenfeld, um es dem Benutzer zu gestatten, aus einer Gruppe von verwandten, aber sich gegenseitig ausschließenden Optionen auszuwählen. Die Anwendung kann z. B. eine Gruppe von Optionsfeldern darstellen, unter denen der Benutzer eine Formateinstellung für Text auswählen kann, der im Clientbereich markiert ist. Der Benutzer kann ein linksbündiges, rechtsbündiges oder zentriertes Format auswählen, indem er das entsprechende Optionsfeld aktiviert. In der Regel kann der Benutzer jeweils nur eine Option zur Zeit aus einer Gruppe von Optionsfeldern auswählen.

> [!Note]  
> Eine weitere Steuerelement Verallgemeinerung für Schaltflächen, bei denen nur eine in einer Gruppe ausgewählt werden kann, ist der Inhalt einer UMSCHALT Fläche. Einige Benutzeroberflächen-Frameworks stellen ein Optionsfeld dar, das eine spezielle UMSCHALT Fläche ist.

 

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **RadioButton** -Steuer Elementtyp definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Schaltflächen-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Optionsfeld-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>RadioButton</li>
</ul></td>
<td><ul>
<li>RadioButton</li>
</ul></td>
</tr>
</tbody>
</table>



 

Es sind keine untergeordneten Elemente in der Steuerelementansicht oder der Inhaltsansicht enthalten.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Steuerelemente besonders relevant ist, die den Steuer Elementtyp " **RadioButton** " implementieren (z. b. Schaltflächen Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert           | Notizen                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.      | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                  |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.      | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                      |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.      | Der durch Klicken aktivierbare Punkt muss ein Punkt sein, der beim Klicken auf das Optionsfeld klickt.                                                             |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **RadioButton** |                                                                                                                                               |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE            | Das Optionsfeld-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                    |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE            | Das Optionsfeld-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                    |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.      | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                     |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL            | Optionsfeld-Steuerelemente werden durch ihren Inhalt selbst beschriftet.                                                                                     |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.      | Lokalisierte Zeichenfolge, die dem **RadioButton** -Steuer Elementtyp entspricht. Der Standardwert ist "Optionsfeld" für en-US oder Englisch (USA). |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.      | Der Name des Optionsfeld-Steuer Elements ist der Text, der neben der Schaltfläche angezeigt wird, die den Auswahl Zustand beibehält.                      |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Optionsfeld-Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                                               | Unterstützung/Wert | Notizen                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | Erforderlich      | Alle Optionsfeld-Steuerelemente müssen das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützen, damit die Auswahl aktiviert werden kann.                                                                                                                                                                                                                                                             |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | Siehe Hinweise.    | Die [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) -Eigenschaft muss immer abgeschlossen werden, damit ein Benutzeroberflächenautomatisierungs-Client ermitteln kann, welche anderen Options Felder in einem bestimmten Kontext zueinander zueinander stehen. Für die Microsoft Win32-Version des Options Felds wird diese Eigenschaft nicht unterstützt, da es nicht möglich ist, diese Informationen von diesem Legacy Framework abzurufen. |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | Nie         | Das Optionsfeld kann seinen Zustand nicht durchlaufen, nachdem es festgelegt wurde. Das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster darf von einem Optionsfeld nie unterstützt werden.                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Schaltflächen- Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                     | Notizen                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                        |                                                                                                                                |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.   |                                                                                                                                |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                   | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.       |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.               | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.     |
| [**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**](uiauto-event-ids.md) | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ SelectionItem \_ elementselectedebug**](uiauto-event-ids.md)                         | Wenn das Steuerelement das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a>Bemerkungen

Ein Optionsfeld stellt eine einzelne auswählbare Option für eine Gruppe von Peer Options Feldern dar. Im Idealfall sollten Options Felder über ein Gruppierungs Element verfügen, das die Grenzen der Peer Options Felder verdeutlicht. Häufig wird die Grenze jedoch von der Benutzeroberflächen-Elementstruktur impliziert. Beispielsweise kann ein Menü eine Reihe von aufeinander folgenden Options Feldern anstelle von Menü Elementen oder eine Reihe von Options Feldern enthalten, die nach einer Gruppen Bezeichnung, aber vor einem handlungsfähigen Element wie Schaltfläche auftreten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




