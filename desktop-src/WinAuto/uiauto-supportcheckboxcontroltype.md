---
title: CheckBox-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den CheckBox-Steuerelement-Typ.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für CheckBox-Steuerelement Typen
- UI-Automatisierung, CheckBox-Steuerelement Typen
- UI-Automatisierung, Struktur für CheckBox-Steuerelement Typen
- UI-Automatisierung, Eigenschaften für CheckBox-Steuerelement Typen
- UI-Automatisierung, Steuerelement Muster für CheckBox-Steuerelement Typen
- UI-Automatisierung, Ereignisse für CheckBox-Steuerelement Typen
- Baumstrukturen, CheckBox-Steuerelement Typen
- Eigenschaften, CheckBox-Steuerelement Typen
- Steuerelement Muster, CheckBox-Steuerelement Typen
- Ereignisse, CheckBox-Steuerelement Typen
- Unterstützung für CheckBox-Steuerelement Typen
- CheckBox-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für CheckBox-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für CheckBox-Steuerelement Typen
- Steuerelement Typen, Unterstützung für CheckBox
- Steuerelement Typen, Kontrollkästchen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e5bac106c8ba3bbf58c7f5b06c087ceb7b3418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856084"
---
# <a name="checkbox-control-type"></a>CheckBox-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **CheckBox** -Steuerelement-Typ.

Ein Kontrollkästchen ist ein Objekt, mit dem ein Zustand gekennzeichnet wird und das Benutzer dazu verwenden können, diesen Zustand zu durchlaufen. Kontrollkästchen bieten dem Benutzer eine binäre Option [(Ja/Nein) oder (Ein/Aus)] oder eine tertiäre Option (Ein, Aus, Unbestimmt).

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **CheckBox** -Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Kontrollkästchen-Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [DEFAULTACTION](#defaultaction)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Kontrollkästchen-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>CheckBox</li>
</ul></td>
<td><ul>
<li>CheckBox</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für den **CheckBox** -Steuerelement-Typ besonders relevant ist Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert        | Notizen                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.   | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                       |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.   | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                           |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.   | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn nicht jeder Punkt innerhalb des umgebenden Rechtecks klickbar ist und das Element spezialisierte Treffer Tests durchführt, überschreiben und einen durch Klicken aktivierbaren Punkt bereitstellen.                                                                               |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **CheckBox** |                                                                                                                                                                                                                                                                                    |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Der Wert dieser Eigenschaft muss immer " **true**" sein. Dies bedeutet, dass das Kontrollkästchen-Steuerelement immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten sein muss.                                                                                                                   |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE         | Der Wert dieser Eigenschaft muss immer " **true**" sein. Dies bedeutet, dass das Kontrollkästchen-Steuerelement immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten sein muss.                                                                                                                   |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.   | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                          |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Null         | Kontrollkästchen-Steuerelemente sind selbst beschriftet.                                                                                                                                                                                                                                              |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.   | Lokalisierte Zeichenfolge für den Steuerelement-Typ " **CheckBox** ". Der Standardwert ist "Kontrollkästchen" für en-US oder Englisch (USA).                                                                                                                                            |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.   | Der Wert der [**iuiautomationelement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (oder [**cachedname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname))-Eigenschaft des Kontrollkästchen-Steuer Elements ist der Text, der neben dem Feld angezeigt wird, das den UMSCHALT Zustand beibehält. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen Kontrollkästchen-Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                  | Unterstützung/Wert | Notizen                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Erforderlich      | Kontrollkästchen unterstützen das [Toggle](uiauto-implementingtoggle.md) -Steuerelement Muster, damit das Kontrollkästchen Programm gesteuert durch den internen Zustand des Kontrollkästchens durchlaufen werden kann. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Kontrollkästchen-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Toggletogglestatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.    |                                                                                                                            |



 

## <a name="defaultaction"></a>DEFAULTACTION

Die Standardaktion für ein Kontrollkästchen besteht darin, einem Optionsfeld den Fokus zu geben und dessen aktuellen Status umzuschalten. Wie bereits erwähnt, bieten Kontrollkästchen dem Benutzer eine binäre (Yes/No-oder on/off)-Entscheidung, oder eine tertiäre (ein-, ausschalten, unbestimmt). Ist das Kontrollkästchen binär, bewirkt die Standardaktion, dass aus dem Zustand „Ein“ in den Zustand „Aus“ oder aus dem Zustand „Aus“ in den Zustand „Ein“ geschaltet wird. In einem tertiären Kontrollkästchen durchläuft die Standardaktion die Status des Kontrollkästchens in derselben Reihenfolge, in der der Benutzer aufeinander folgende Mausklicks an das Steuerelement gesendet hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




