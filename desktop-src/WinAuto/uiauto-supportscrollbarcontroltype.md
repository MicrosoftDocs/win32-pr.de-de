---
title: ScrollBar-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den ScrollBar-Steuerelementtyp.
ms.assetid: c89ca087-3e93-4e86-ac79-731e3e7a361d
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung des ScrollBar-Steuerelementtyps
- Benutzeroberflächenautomatisierung,ScrollBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für ScrollBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für ScrollBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den ScrollBar-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Ereignisse für den ScrollBar-Steuerelementtyp
- Strukturstrukturen, ScrollBar-Steuerelementtyp
- Properties, ScrollBar-Steuerelementtyp
- Steuerelementmuster, ScrollBar-Steuerelementtyp
- Ereignisse, ScrollBar-Steuerelementtyp
- Unterstützung für den ScrollBar-Steuerelementtyp
- ScrollBar-Steuerelementtyp
- Steuerelementtypen, Struktur für ScrollBar-Steuerelementtyp
- Steuerelementtypen, Steuerelementmuster für den ScrollBar-Steuerelementtyp
- Steuerelementtypen, Unterstützung für ScrollBar
- Steuerelementtypen, ScrollBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a25d0398ca8e094e1dbec5e06eb725f3e9d7edbb5c193fdc3699e166b118142
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413370"
---
# <a name="scrollbar-control-type"></a>ScrollBar-Steuerelementtyp

Dieses Thema enthält Informationen zu Microsoft Benutzeroberflächenautomatisierung Unterstützung für den **ScrollBar-Steuerelementtyp.**

Mit ScrollBar-Steuerelementen können Sie einen Bildlauf für den Inhalt eines Fenster- oder Elementcontainers ausführen. Das -Steuerelement besteht aus einer Reihe von Schaltflächen und einem Thumb-Steuerelement.

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **ScrollBar-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Scrollleistensteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf Bildlaufleisten-Steuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).



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
<td>Nicht zutreffend (Das Bildlaufleisten-Steuerelement hat keinen Inhalt.)</td>
</tr>
</tbody>
</table>



 

Das Bildlaufleisten-Steuerelement kann 0 (null) bis fünf untergeordnete Elemente aufweisen. Da die Unterstruktur über mehrere Schaltflächensteuerelemente verfügt, muss das Element einen bestimmten [**UIA \_ AutomationIdPropertyId-Wert**](uiauto-automation-element-propids.md) auf jedes Element festlegen, damit sie für automatisierte Testtools erkennbar sind.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für Bildlaufleisten-Steuerelemente besonders relevant ist. Beachten Sie, dass ein Bildlaufleisten-Steuerelement nie über Inhalt verfügt. Seine Funktionalität wird über [](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster verfügbar gemacht, das für den Container unterstützt wird, in dem gescrollt wird.

Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert         | Notizen                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise.    | Der Wert dieser Eigenschaft muss für alle Peerelemente in der Rohansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise.    | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | NaN           | Das Bildlaufleisten-Steuerelement enthält keine durch Klicken aktivierbaren Punkte.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Scrollbar** | Dieser Wert ist für alle Frameworks gleich. Scrollleisten, die als Schieberegler fungieren, müssen den Steuerelementtyp [Schieberegler](uiauto-supportslidercontroltype.md) verwenden.                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE         | Das Bildlaufleisten-Steuerelement ist nie ein Inhaltselement. Wenn die Bildlaufleiste ein eigenständiges Steuerelement ist, muss sie den Typ des [Schiebereglersteuerelements](uiauto-supportslidercontroltype.md) erfüllen und [**UIA \_ SliderControlTypeId**](uiauto-controltype-ids.md) für die [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (oder [**CachedControlType )-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)zurückgeben. |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | Das Bildlaufleisten-Steuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise.    | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen. Ein Bildlaufleisten-Steuerelement nimmt den Fokus nur selten in den Fokus, aber wenn es dies tut, sollte der Fokus auf dem Bildlaufleisten-Steuerelement selbst und nicht auf den untergeordneten Schaltflächen oder dem Daumen bleiben. Der Benutzer sollte in der Lage sein, alle Bildlaufaktionen mithilfe der NACH-OBEN- und NACH-UNTEN-TASTE (oder NACH-RECHTS- und NACH-LINKS-TASTE) oder der TASTEN PAGE UP und PAGE DOWN auszuführen.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Bildlaufleisten weisen keine Bezeichnungen auf.                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise.    | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp ScrollBar entspricht.** Der Standardwert ist "scrollbar" für en-US oder Englisch (USA).                                                                                                                                                                                                                                                                                                                                       |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULL          | Das Bildlaufleisten-Steuerelement verfügt nicht über Inhaltselemente, und die [**UIA \_ NamePropertyId-Eigenschaft**](uiauto-automation-element-propids.md) muss nicht festgelegt werden.                                                                                                                                                                                                                                                                                           |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Siehe Hinweise.    | Die horizontale oder vertikale Ausrichtung muss vom Bildlaufleisten-Steuerelement immer verfügbar gemacht werden.                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von allen Bildlaufleisten-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Wenn eine Bildlaufleiste nur als Steuerelement für die Mausbearbeitung verwendet wird, unterstützt sie keine Steuerelementmuster. Wenn es als Schieberegler-Steuerelement innerhalb einer Anwendung verwendet wird, muss ihm der Steuerelementtyp [Schieberegler](uiauto-supportslidercontroltype.md) erteilt werden.

 



| Steuerelementmuster                                           | Support | Notizen                                                                                                                                                                                                                          |
|-----------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Depends (Abhängig) | Das [RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) muss nur unterstützt werden, wenn das [Scroll-Steuerelementmuster](uiauto-implementingscroll.md) für den Container mit der Scrollleiste nicht unterstützt wird. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)         | Nie   | Das [Scroll-Steuerelementmuster](uiauto-implementingscroll.md) wird nie direkt auf der Scrollleiste unterstützt.                                                                                                                     |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Scrollleistensteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ RangeValueValuePropertyId-Eigenschaftswechselereignis.**](uiauto-control-pattern-propids.md)        | Wenn das Steuerelement das [RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) unterstützt, muss es dieses Ereignis unterstützen.   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




