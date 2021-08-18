---
title: StatusBar-Steuerelementtyp
description: Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den StatusBar-Steuerelementtyp.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung des StatusBar-Steuerelementtyps
- Benutzeroberflächenautomatisierung,StatusBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für StatusBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den StatusBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den StatusBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den StatusBar-Steuerelementtyp
- Strukturstrukturen, StatusBar-Steuerelementtyp
- Properties, StatusBar-Steuerelementtyp
- Steuerelementmuster, StatusBar-Steuerelementtyp
- Ereignisse, StatusBar-Steuerelementtyp
- Unterstützung für den StatusBar-Steuerelementtyp
- StatusBar-Steuerelementtyp
- Steuerelementtypen, Struktur für StatusBar-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für StatusBar-Steuerelementtyp
- Steuerelementtypen,Unterstützung für StatusBar
- Steuerelementtypen,StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f52f3f04db86a8c8ff0e9cad9a3938a17e996e8210960912c3abc5039468e178
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614250"
---
# <a name="statusbar-control-type"></a>StatusBar-Steuerelementtyp

Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den **StatusBar-Steuerelementtyp.**

Ein StatusBar-Steuerelement zeigt Informationen zu einem Objekt an, das in einem Fenster einer Anwendung angezeigt wird, zur Komponente des Objekts oder Kontextinformationen, die sich auf die Operation dieses Objekts in Ihrer Anwendung beziehen.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **StatusBar-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Statusleistensteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf Statusleistensteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).



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

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für die Statusleistensteuerelemente besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert         | Hinweise                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.    | Der Wert dieser Eigenschaft muss für alle Peerelemente in der Rohansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.    | Das umschließende Rechteck einer Statusleiste muss alle darin enthaltenen Steuerelemente umfassen.                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise.    | Unterstützt, wenn es ein umschließendes Rechteck gibt. Wenn innerhalb des umschließenden Rechtecks Bereiche vorhanden sind, die nicht angeklickt werden können, und das Element spezielle Treffertests durchführt, überschreiben Sie dies, und geben Sie einen klickbaren Punkt an. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **StatusBar** |                                                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | Das Statusleisten-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | Das Statusleisten-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Depends (Abhängig)       | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depends (Abhängig)       | Wenn ein Statusleisten-Steuerelement derzeit nicht sichtbar ist, gibt es TRUE für diese Eigenschaft zurück.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Das Statusleisten-Steuerelement verfügt in der Regel nicht über eine Bezeichnung.                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.    | Lokalisierte Zeichenfolge, die dem **StatusBar-Steuerelementtyp entspricht.** Der Standardwert ist "Statusleiste" für en-US oder Englisch (USA).                                                                           |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise.    | Das StatusBar-Steuerelement muss nur dann einen Namen haben, wenn in einer Anwendung mehrere Statusleisten verwendet werden. Unterscheiden Sie in diesem Fall jede Leiste mit Namen wie "Internetstatus" oder "Anwendungsstatus".                    |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Depends (Abhängig)       | Ein -Wert, der die Ausrichtung des Steuerelements angibt: horizontal oder vertikal.                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die für Statusleistensteuerelemente unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                               | Support  | Notizen                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | Optional | Statusleistensteuerelemente sollten das [Raster-Steuerelementmuster](uiauto-implementinggrid.md) unterstützen, damit einzelne Teile überwacht und leicht auf Informationen verwiesen werden können. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Statusleistensteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md) |                                                                                   |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die **IsEnabled-Eigenschaft unterstützt,** muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die **IsOffscreen-Eigenschaft unterstützt,** muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a>Hinweise

Es wird empfohlen, Bearbeitungssteuerelemente als untergeordnete Rasterelemente in einer Statusleiste zu verwenden. Die Verwendung von Bearbeitungssteuerelementen erleichtert das Zuordnen des Zwecks des Statusfelds zu dessen Wert mithilfe des Elementnamens und der Werteigenschaft. Da Textsteuerelemente das  Value-Steuerelementmuster nicht unterstützen sollten, sollten sie nicht als untergeordnete Rasterelemente verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




