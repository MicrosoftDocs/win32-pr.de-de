---
title: Appbar-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den appbar-Steuerelement-Typ.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für appbar-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, appbar-Steuerelement
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den appbar-Steuerelement
- Steuerelement Muster, appbar-Steuerelement Typen
- Unterstützung für appbar-Steuerelement Typen
- Appbar-Steuerelement Typen
- Steuerelement Typen, appbar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151aecc0f5f97878e10b59b091c4c59ec98cb26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473860"
---
# <a name="appbar-control-type"></a>Appbar-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **appbar** -Steuerelement-Typ.

Eine APP-Leiste ist ein Benutzeroberflächen Element, das dem Benutzernavigation, Befehle und Tools präsentiert. Für Windows Store-Apps können APP-leisten für Apps durch Drücken von Windows-Taste + Z angezeigt werden.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **appbar** -Steuerelement-Typ definiert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Ereignisse](#required-events)
-   [Relevante Ereignisse](#relevant-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für **appbar** -Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. **Schaltfläche** ist das gängigste Element innerhalb einer **appbar** , aber andere Steuerelemente, die Aktionen für eine APP aufrufen, sind ebenfalls möglich. Eine **appbar** kann auch 0 oder mehr Trennzeichen (**Trenn** Zeichentyp) enthalten, die in der Steuerelement Ansicht als zwischen den anderen Steuerelementen platziert werden. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>AppBar
<ul>
<li>Schaltfläche (0 oder viele)</li>
<li>Andere Steuerelemente (0 oder viele)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Nicht verfügbar
<ul>
<li>Schaltfläche (0 oder viele)</li>
<li>Andere Steuerelemente (0 oder viele)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Steuerelemente besonders relevant ist, die den **appbar** -Steuerelement Typen implementieren Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Der von dieser Eigenschaft verfügbar gemachte Wert muss sämtliche darin enthaltenen Steuerelemente umfassen.                                                                                                                                    |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **AppBar** |                                                                                                                                                                                                                             |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | false      | Ein App-leisten-Steuerelement ist in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur nicht enthalten.                                                                                                                                           |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Ein App-leisten-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                        |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise  | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen. Steuerelemente in der APP-Leiste können in der Regel den Tastaturfokus haben.                                                                                    |
| [**UIA \_ isoffscreenpropertyid**](uiauto-automation-element-propids.md)                   | Siehe Hinweise. | Der Wert dieser Eigenschaft ist hängt davon ab, ob das Steuerelement auf dem Bildschirm angezeigt werden kann.                                                                                                                                        |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Null       | Die Steuerelemente der APP-Leiste haben in der Regel keine Bezeichnung.                                                                                                                                                                               |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **appbar** -Steuerelement entspricht. Der Standardwert ist "App-Leiste" für en-US oder Englisch (USA).                                                                                         |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Das Steuerelement der APP-Leiste benötigt keinen Namen, es sei denn, eine Anwendung verfügt über mehr als eine APP-Leiste. Wenn in einer Anwendung mehr als eine APP-Leiste vorhanden ist, verwenden Sie diese Eigenschaft, um Unterscheidungs Namen verfügbar zu machen, z. b. "Top" oder "Bottom". |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von App-Bar- Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a>Relevante Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Steuerelemente, die den **appbar** -Steuerelement Typen implementieren, jedoch nicht unbedingt erforderlich sind



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                 | Notizen                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**UIA \_ menuclosedebug**](uiauto-event-ids.md)                            | Platt Form Implementierungen können dieses Ereignis auslösen, wenn das Steuerelement der APP-Leiste geschlossen wird. |
| [**UIA \_ menuopenedeventid**](uiauto-event-ids.md)                            | Platt Form Implementierungen können dieses Ereignis auslösen, wenn das Steuerelement der APP-Leiste geöffnet wird. |
| [**Iuiautomationpropertychangeabventhandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Ereignishandler für geänderte Eigenschaften.                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> <dt>

**Verweis**
</dt> <dt>

[**Appbar-XAML-Steuerelement**](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

[**Winjs. UI. appbar-Objekt**](/previous-versions/windows/apps/br229670(v=win.10))
</dt> </dl>

 

 