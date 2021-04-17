---
title: Pane-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Pane-Steuerelement Typen.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für Pane-Steuerelement
- Benutzeroberflächenautomatisierungs, Bereich-Steuerelement Typen
- UI-Automatisierung, Struktur für Pane-Steuerelement Typen
- UI-Automatisierung, Eigenschaften für den Pane-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Pane-Steuerelement Typen
- UI-Automatisierung, Ereignisse für den Pane-Steuerelement Typen
- Struktur Strukturen, Pane-Steuerelement Typen
- Eigenschaften, Fenster Steuerelement-Typ
- Steuerelement Muster, Fenster Steuerelement-Typ
- Ereignisse, Pane-Steuerelement Typen
- Unterstützung für Pane-Steuerelement Typen
- Pane-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für den Pane-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den Pane-Steuer ungstyp
- Steuerelement Typen, Unterstützung für Bereich
- Steuerelement Typen, Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51b7f22e6fb302ebb160a174c27c61119b8f09fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104566785"
---
# <a name="pane-control-type"></a>Pane-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Pane** -Steuerelement Typen.

Der **Pane** -Steuer ungstyp ist für potenziell Bild lauffähigen Bereiche mit unterschiedlichen Inhalten. Sie wird verwendet, um ein Objekt innerhalb eines Frame-oder Dokument Fensters darzustellen. Benutzer können zwischen Pane-Steuerelementen und innerhalb des Inhalts des aktuellen Bereichs navigieren. Bereichs Steuerelemente stellen eine Gruppierungs Ebene unterhalb von Fenstern oder Dokumenten dar, jedoch oberhalb einzelner Steuerelemente. Der Benutzer kann je nach Kontext durch Drücken von TAB, F6 oder STRG+TAB zwischen den Bereichen navigieren.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Pane** -Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Bereichs Steuerelemente, in denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen und

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Beispiel für Pane-Steuerelementtyp](#pane-control-type-example)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Bereichs Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Bereich</li>
</ul></td>
<td><ul>
<li>Bereich</li>
</ul></td>
</tr>
</tbody>
</table>



 

Ein Pane-Steuerelement wird immer in der Steuerelement-und der Inhaltsansicht angezeigt. Machen Sie ein Layoutobjekt nicht als Bereich in der Steuerelement-oder der Inhaltsansicht verfügbar, wenn das Objekt nur für die visuelle Darstellung verwendet wird.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle werden die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Werte oder Definitionen für Bereichs Steuerelemente besonders relevant sind. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ accesskeypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn eine bestimmte Tastenkombination den Fokus auf den Bereich legt, müssen diese Informationen über diese Eigenschaft verfügbar gemacht werden.                                                                                                                                                                                                      |
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                                                          |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                              |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Diese Eigenschaft macht einen durch Klicken aktivierbaren Punkt des Bereichssteuerelements verfügbar, durch den der Bereich den Fokus erhält, wenn auf den Punkt geklickt wird.                                                                                                                                                                                                |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Bereich**   |                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ helptextpropertyid**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Der Hilfetext für Bereichs Steuerelemente sollte den Zweck des Frames und seine Beziehung zu anderen Frames erläutern. Eine Beschreibung ist erforderlich, wenn der Zweck und die Beziehung der Frames nicht aus dem Wert der Eigenschaft [**UIA \_ namepropertyid**](uiauto-automation-element-propids.md) gelöscht werden. |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Bereichs Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                    |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Pane-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                    |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                             |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Bereichssteuerelemente haben in der Regel keine statische Bezeichnung. Ist eine statische Beschriftung vorhanden, muss sie über diese Eigenschaft verfügbar gemacht werden.                                                                                                                                                                                      |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge für den Steuerelement-Typ " **Pane** ". Der Standardwert ist "Pane" für en-US oder Englisch (USA).                                                                                                                                                                                        |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Wert für diese Eigenschaft muss immer ein eindeutiger, präziser und aussagekräftiger Titel sein.                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Steuerelement Muster aufgelistet, die von Bereichs Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support | Notizen                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Depends (Abhängig) | Implementieren Sie das [Dock](uiauto-implementingdock.md) -Steuerelement Muster, wenn das Bereichs Steuerelement angedockt werden kann.                                                                                          |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depends (Abhängig) | Implementieren Sie das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster, wenn das Bereichs Steuerelement gescrollt werden kann.                                                                                    |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depends (Abhängig) | Implementieren Sie das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster, wenn das Pane-Steuerelement auf dem Bildschirm verschoben, verkleinert oder gedreht werden kann.                                              |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Nie   | Wenn das Element das [Window](uiauto-implementingwindow.md) -Steuerelement Muster implementieren muss, sollte das Steuerelement auf dem Steuer Elementtyp " [Window](uiauto-supportwindowcontroltype.md) " basieren. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Bereichs Steuerelementen Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                        | Notizen                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ asynccontentloadedeventid**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                      |                                                                                                                            |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                  | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.   | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.           | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.       | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.     | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.               | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.           |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a>Beispiel für Pane-Steuerelementtyp

Die folgende Abbildung veranschaulicht **ein Steuerelement, das den Steuer** Element-Steuerelement Typ implementiert.

![Screenshot mit einem Beispiel für ein Pane-Steuerelement](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Benutzeroberflächenautomatisierungs-Struktur – Steuerelement Ansicht</th>
<th>Benutzeroberflächenautomatisierungs-Struktur – Inhaltsansicht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Bereich
<ul>
<li>Struktur (Scroll-Muster)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
</ul></li>
<li>Bereich
<ul>
<li>Bearbeiten (Scroll-Muster)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Bereich
<ul>
<li>Struktur (Scroll-Muster)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
<li>Bereich
<ul>
<li>Bearbeiten (Scroll-Muster)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




