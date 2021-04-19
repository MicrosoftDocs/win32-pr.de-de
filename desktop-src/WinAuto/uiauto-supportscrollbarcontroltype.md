---
title: ScrollBar-Steuerelement Typen
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den ScrollBar-Steuerelement-Typ.
ms.assetid: c89ca087-3e93-4e86-ac79-731e3e7a361d
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für ScrollBar-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, ScrollBar-Steuerelement
- UI-Automatisierung, Baumstruktur für ScrollBar-Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für ScrollBar-Steuerelement Typen
- UI-Automatisierung, Steuerelement Muster für ScrollBar-Steuerelement Typen
- UI-Automatisierung, Ereignisse für ScrollBar-Steuerelement Typen
- Struktur Strukturen, ScrollBar-Steuerelement Typen
- Eigenschaften, ScrollBar-Steuerelement Typen
- Steuerelement Muster, ScrollBar-Steuerelement Typen
- Ereignisse, ScrollBar-Steuerelement Typen
- Unterstützung für ScrollBar-Steuerelement Typen
- ScrollBar-Steuerelement Typen
- Steuerelement Typen, Baumstruktur für ScrollBar-Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für ScrollBar-Steuerelement Typen
- Steuerelement Typen, Unterstützung für ScrollBar
- Steuerelement Typen, Scrollleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2168401c313dd9139f44ba615de945802b307d64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339827"
---
# <a name="scrollbar-control-type"></a>ScrollBar-Steuerelement Typen

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den **ScrollBar** -Steuerelement-Typ.

Mit ScrollBar-Steuerelementen können Sie einen Bildlauf für den Inhalt eines Fenster- oder Elementcontainers ausführen. Das-Steuerelement besteht aus einem Satz von Schaltflächen und einem Thumb-Steuerelement.

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **ScrollBar** -Steuerelement Typen definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle ScrollBar-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Unterstützung für die Benutzeroberflächen Automatisierung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

-   [Typische Baumstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelement Muster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle ist eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für ScrollBar-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>ScrollBar
<ul>
<li>Schaltfläche (0, 2 oder 4)</li>
<li>Thumb (0 oder 1)</li>
</ul></li>
</ul></td>
<td>Nicht zutreffend (Das Schiebe leisten-Steuerelement enthält keinen Inhalt.)</td>
</tr>
</tbody>
</table>



 

Das Bild Lauf leisten-Steuerelement kann 0 bis fünf untergeordnete Elemente aufweisen. Da die Teilstruktur mehr als ein Schaltflächen-Steuerelement aufweist, muss das Element einen bestimmten [**UIA- \_ automationidpropertyid**](uiauto-automation-element-propids.md) -Wert für jedes Element festlegen, damit Sie für automatisierte TestTools sichtbar sind.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für ScrollBar-Steuerelemente besonders relevant ist. Beachten Sie, dass ein Bild Lauf leisten-Steuerelement niemals Inhalte enthält. seine Funktionalität wird über das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster verfügbar gemacht, das für den Container unterstützt wird.

Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert         | Notizen                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.    | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise.    | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | NaN           | Das Bildlaufleisten-Steuerelement enthält keine durch Klicken aktivierbaren Punkte.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Bild Lauf Leiste** | Dieser Wert ist für alle Frameworks gleich. Bild Lauf leisten, die als Schieberegler fungieren, müssen den [Schieberegler](uiauto-supportslidercontroltype.md) -Steuerelement Typen verwenden                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | false         | Das Bildlaufleisten-Steuerelement ist nie ein Inhaltselement. Wenn es sich bei der Bild Lauf Leiste um ein eigenständiges Steuerelement handelt, muss Sie den [Schieberegler](uiauto-supportslidercontroltype.md) -Steuer Elementtyp erfüllen und [**UIA \_ slidercontroltypeid**](uiauto-controltype-ids.md) für die [**iuiautomationelement:: currentcontroltype**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (oder [**cachedcontroltype**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype))-Eigenschaft zurückgeben. |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE          | Das ScrollBar-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise.    | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen. Ein Schiebe leisten-Steuerelement geht selten im Fokus, aber wenn es es tut, sollte der Fokus auf dem Scrollleisten-Steuerelement selbst bleiben, nicht auf den untergeordneten Schaltflächen oder dem Ziehpunkt. Der Benutzer sollte alle scrollaktionen mithilfe der nach-oben-und nach-unten-Taste (oder nach-rechts-und nach-links-Taste) oder der Bild-auf-und Bild-ab-Taste ausführen können.                                                                |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | NULL          | Bildlaufleisten weisen keine Bezeichnungen auf.                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise.    | Lokalisierte Zeichenfolge, die dem **ScrollBar** -Steuerelement entspricht. Der Standardwert ist "Scrollleiste" für en-US oder Englisch (USA).                                                                                                                                                                                                                                                                                                                                       |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | NULL          | Das Schiebe leisten-Steuerelement verfügt über keine Inhaltselemente, und die Eigenschaft " [**UIA \_ namepropertyid**](uiauto-automation-element-propids.md) " muss nicht festgelegt werden.                                                                                                                                                                                                                                                                                           |
| [**UIA- \_ orientationpropertyid**](uiauto-automation-element-propids.md)                   | Siehe Hinweise.    | Die horizontale oder vertikale Ausrichtung muss vom Bildlaufleisten-Steuerelement immer verfügbar gemacht werden.                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die von allen ScrollBar-Steuerelementen unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Wenn eine Schiebe Leiste nur für die Maus Bearbeitung als Steuerelement verwendet wird, werden Steuerelement Muster nicht unterstützt. Wenn Sie in einer Anwendung als Schieberegler-Steuerelement verwendet wird, muss Ihr der [Schieberegler](uiauto-supportslidercontroltype.md) -Steuerelement Typ zugewiesen werden.

 



| Steuerelementmuster                                           | Support | Notizen                                                                                                                                                                                                                          |
|-----------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Depends (Abhängig) | Das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster muss nur unterstützt werden, wenn das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster für den Container, der die Bild Lauf Leiste enthält, nicht unterstützt wird. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)         | Nie   | Das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster wird auf der Bild Lauf Leiste nie direkt unterstützt.                                                                                                                     |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die für die Unterstützung von Bild Lauf leisten- Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Rangevaluevaluepropertyid**](uiauto-control-pattern-propids.md) -Eigenschaft-geändertes Ereignis.        | Wenn das Steuerelement das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützt, muss es dieses Ereignis unterstützen.   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




