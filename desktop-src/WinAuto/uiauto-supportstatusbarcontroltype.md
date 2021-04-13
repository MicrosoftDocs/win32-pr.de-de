---
title: StatusBar-Steuer Elementtyp
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den StatusBar-Steuer Elementtyp.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung für StatusBar-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, StatusBar-Steuer Elementtyp
- UI-Automatisierung, Struktur für StatusBar-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Eigenschaften für StatusBar-Steuer Elementtyp
- UI-Automatisierung, Steuerelement Muster für StatusBar-Steuer Elementtyp
- Benutzeroberflächenautomatisierungs, Ereignisse für StatusBar-Steuer Elementtyp
- Baumstrukturen, StatusBar-Steuer Elementtyp
- Eigenschaften, StatusBar-Steuer Elementtyp
- Steuerelement Muster, StatusBar-Steuer Elementtyp
- Ereignisse, StatusBar-Steuer Elementtyp
- Unterstützung für StatusBar-Steuer Elementtyp
- StatusBar-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für StatusBar-Steuer Elementtyp
- Steuerelement Typen, Steuerelement Muster für StatusBar-Steuer Elementtyp
- Steuerelement Typen, Unterstützung für StatusBar
- Steuerelement Typen, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ace64d34429a6d381dfdef2d99d82a3693fca2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310592"
---
# <a name="statusbar-control-type"></a>StatusBar-Steuer Elementtyp

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **StatusBar** -Steuer Elementtyp.

Ein StatusBar-Steuerelement zeigt Informationen zu einem Objekt an, das in einem Fenster einer Anwendung angezeigt wird, zur Komponente des Objekts oder Kontextinformationen, die sich auf die Operation dieses Objekts in Ihrer Anwendung beziehen.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den Steuer Elementtyp " **StatusBar** " definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle StatusBar-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung der Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Status leisten-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>StatusBar
<ul>
<li>Bearbeiten (beliebige Anzahl)</li>
<li>ProgressBar (0 oder viele)</li>
<li>Bild (0 oder viele)</li>
<li>Schaltfläche (0 oder viele)</li>
</ul></li>
</ul></td>
<td><ul>
<li>StatusBar
<ul>
<li>Bearbeiten (beliebige Anzahl)</li>
<li>ProgressBar (0 oder viele)</li>
<li>Bild (0 oder viele)</li>
<li>Schaltfläche (0 oder viele)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Status leisten-Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert         | Notizen                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.    | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                        |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.    | Das umschließende Rechteck einer Statusleiste muss alle darin enthaltenen Steuerelemente umfassen.                                                                                                                      |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise.    | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn Bereiche innerhalb des umgebenden Rechtecks vorhanden sind, die nicht klickbar sind, und das-Element spezialisierte Treffer Tests durchführt, überschreiben Sie diese, und stellen Sie einen klickbaren Punkt bereit. |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **StatusBar** |                                                                                                                                                                                                                     |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE          | Das StatusBar-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                            |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE          | Das StatusBar-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                            |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Depends (Abhängig)       | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                           |
| [**UIA \_ isoffscreenpropertyid**](uiauto-automation-element-propids.md)                   | Depends (Abhängig)       | Wenn ein StatusBar-Steuerelement momentan nicht sichtbar ist, wird für diese Eigenschaft der Wert true zurückgegeben.                                                                                                                            |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL          | Das StatusBar-Steuerelement verfügt in der Regel nicht über eine Bezeichnung.                                                                                                                                                             |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.    | Lokalisierte Zeichenfolge für den Steuer Elementtyp " **StatusBar** ". Der Standardwert ist "Statusleiste" für en-US oder Englisch (USA).                                                                           |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.    | Das StatusBar-Steuerelement muss nur dann einen Namen haben, wenn in einer Anwendung mehrere Statusleisten verwendet werden. Unterscheiden Sie in diesem Fall die einzelnen Balken mit Namen wie "Internet Status" oder "Anwendungs Status".                    |
| [**UIA- \_ orientationpropertyid**](uiauto-automation-element-propids.md)                   | Depends (Abhängig)       | Ein Wert, der die Ausrichtung des Steuer Elements angibt: horizontal oder vertikal.                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die für Status leisten-Steuerelemente unterstützt Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                               | Support  | Notizen                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | Optional | StatusBar-Steuerelemente sollten das [Raster](uiauto-implementinggrid.md) -Steuerelement Muster unterstützen, damit einzelne Teile überwacht und leicht referenziert werden können. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von StatusBar- Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                   |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                   |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die **isaktivierte** Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die **IsOffscreen** -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, Bearbeitungs Steuerelemente als untergeordnete Raster Elemente in einer Statusleiste zu verwenden. Die Verwendung von Bearbeitungs Steuerelementen erleichtert das Zuordnen des Zwecks des Status Felds mit dem Wert, indem der Elementname und die Value-Eigenschaft verwendet werden. Da Text Steuerelemente das **value** -Steuerelement Muster nicht unterstützen sollten, sollten Sie nicht als untergeordnete Raster Elemente verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




