---
title: Fenster Steuerelement-Typ
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Fenster Steuerelement-Typ.
ms.assetid: 521fb514-e083-48b3-b4a0-52c530154740
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für Fenster Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Fenster Steuerelement-Typ
- UI-Automatisierung, Baumstruktur für Window-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für Window-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für Window-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Ereignisse für Window-Steuerelement Typen
- Baumstrukturen, Fenster Steuerelement-Typ
- Eigenschaften, Fenster Steuerelement-Typ
- Steuerelement Muster, Fenster Steuerelement-Typ
- Ereignisse, Fenster Steuerelement-Typ
- Unterstützung für Window-Steuerelement Typen
- Window-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Window-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für Window-Steuerelement Typen
- Steuerelement Typen, Unterstützung für Fenster
- Steuerelement Typen, Fenster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422742381cd501d295e4cb7e354ca07e10c13360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310816"
---
# <a name="window-control-type"></a>Fenster Steuerelement-Typ

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **Fenster** Steuerelement-Typ.

Das Window-Steuerelement besteht aus dem Fensterrahmen, der untergeordnete Objekte wie Titelleiste, Client sowie andere Objekte enthält.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Fenster** Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Fenster Steuerelemente, bei denen das UI-Framework/die Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Window-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Fenster</li>
</ul></td>
<td><ul>
<li>Fenster</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für Window-Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                            |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Das Fenster Steuerelement muss über einen durch Klicken aktivierbaren Punkt verfügen, der bewirkt, dass das Fenster ausgewählt oder nicht ausgewählt wird.                                                 |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Fenster** | Dieser Wert ist für alle Benutzeroberflächen-Frameworks gleich.                                                                                                           |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Window-Steuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                    |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Window-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                    |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                               |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL       | Window-Steuerelemente haben keine statische Fenster Bezeichnung.                                                                                                      |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Fenster** Steuerelement-Typ entspricht. Der Standardwert ist "Window" für en-US oder Englisch (USA).                      |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Das Window-Steuerelement enthält immer ein primäres Fensterelement, das sich auf den Wert bezieht, den der Benutzer als den semantischen Bezeichner für das Element zuordnen würde. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von Fenster Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                        | Unterstützung/Wert | Notizen                                                                                                                                                                        |
|---------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Bedingt   | Das [Dock](uiauto-implementingdock.md) -Steuerelement Muster muss unterstützt werden, wenn das Fenster angedockt werden kann.                                                                       |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Erforderlich      | Das [Transform](uiauto-implementingtransform.md) -Steuerelement Muster ermöglicht das Verschieben, Ändern der Größe oder Drehen des Fensters auf dem Bildschirm. (Gilt nicht für Windows Store-Apps.) |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Erforderlich      | Das [Window](uiauto-implementingwindow.md) -Steuerelement Muster ermöglicht bestimmte Vorgänge für das Fenster.                                                                      |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von **Fenster** Steuerelementen Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                                        | Notizen                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ asynccontentloadedeventid**](uiauto-event-ids.md)                                                                   |                                                                                                                                                                                                                           |
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                                           |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                      |                                                                                                                                                                                                                           |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                      | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.                                                                                                  |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                  | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.                                                                                                |
| [**UIA \_ layoutinvalidatedeventid**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                                           |
| [**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                                                |                                                                                                                                                                                                                           |
| [**UIA \_ Scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.   | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ Scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis. | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ Scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.           | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ Scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.       | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ Scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.     | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ Scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.               | Wenn das Steuerelement das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.                                                                                                          |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                                           |
| [**UIA \_ \_ -Fenster windowclosedeventid**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**UIA \_ \_ -Fenster windowopenedeventid**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**UIA \_ Windowwindowvisualstatepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**WindowVisualState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-get_cachedwindowvisualstate) -Eigenschaft des [Window](uiauto-implementingwindow.md) -Steuerelement Musters unterstützt, muss dieses Ereignis unterstützt werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




