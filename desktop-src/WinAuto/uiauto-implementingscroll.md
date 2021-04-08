---
title: Scroll-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IScrollProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Scroll-Steuerelement Muster wird zur Unterstützung eines Steuer Elements verwendet, das als Bild lauffähigen Container für eine Auflistung von untergeordneten Objekten fungiert.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines scrollsteuerungsmusters
- UI-Automatisierung, scrollsteuerungsmuster
- UI-Automatisierung, IScrollProvider
- IScrollProvider
- Implementieren von scrollsteuermustern für Benutzeroberflächen Automatisierung
- Scrollsteuerungmuster
- Steuerelement Muster, IScrollProvider
- Steuerelement Muster, Implementieren von Benutzeroberflächen Automatisierung-Scroll
- Steuerelement Muster, scrollen
- Schnittstellen, IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712173"
---
# <a name="scroll-control-pattern"></a>Scroll-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **Scroll** -Steuerelement Muster wird zur Unterstützung eines Steuer Elements verwendet, das als Bild lauffähigen Container für eine Auflistung von untergeordneten Objekten fungiert.

Das-Steuerelement ist nicht erforderlich, um Scrollleisten zur Unterstützung der Scrollfunktion zu verwenden, obwohl dies häufig der Fall ist. Die folgende Abbildung zeigt ein scrollsteuer Element, das keine Bild Lauf leisten verwendet. Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

![Screenshot mit einem scrollsteuer Element ohne Scrollleisten](images/uia-scrollpattern-without-scrollbars.jpg)

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IScrollProvider**](#required-members-for-iscrollprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Scroll** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Die untergeordneten Elemente dieses Steuer Elements müssen [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)implementieren.
-   Die Bild Lauf leisten eines Container Steuer Elements unterstützen das **Scroll** -Steuerelement Muster nicht. Sie müssen stattdessen das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster unterstützen.
-   Wenn das Scrollen in Prozentwerten gemessen wird, müssen alle Werte oder Beträge, die sich auf die Einteilung der Bildlaufleiste beziehen, auf einen Bereich von 0 bis 100 normalisiert werden.
-   Die [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) -Eigenschaft und die [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) -Eigenschaft sind unabhängig von der **isaktivierten** Eigenschaft.
-   Wenn die [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) -Eigenschaft auf **false** festgelegt ist, sollte die [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) -Eigenschaft auf 100 (100%) festgelegt werden. die [**horizontalscrollprozent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) -Eigenschaft sollte auf **UIA \_ scrollpatternnoscroll** (-1) festgelegt werden. Wenn die [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) -Eigenschaft auf **false** festgelegt ist, sollte die [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) -Eigenschaft auf 100 (100%) festgelegt werden. die [**verticalscrollprozent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) -Eigenschaft sollte auf **UIA \_ scrollpatternnoscroll** (-1) festgelegt werden. Dadurch kann ein Microsoft UI Automation-Client diese Eigenschaftswerte innerhalb der [**setscrollprozent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) -Methode verwenden, während eine Racebedingung vermieden wird, wenn eine Richtung aktiviert wird, für die der Client keinen Bildlauf durchführen soll.
-   Die [**IScrollProvider:: horizontalscrollprozent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) -Eigenschaft ist Gebiets Schema spezifisch. Beim Festlegen von **horizontalscrollprozent** auf 100 muss die Bild Lauf Position des Steuer Elements auf die Entsprechung der äußersten rechten Position für Sprachen wie Englisch festgelegt werden, die von links nach rechts gelesen wurden. Für Sprachen, wie z. b. Arabisch, die von rechts nach links gelesen werden, muss bei der Festlegung von **horizontalscrollprozent** auf 100 die Scrollposition auf die äußteste Position festgelegt werden.

## <a name="required-members-for-iscrollprovider"></a>Erforderliche Member für **IScrollProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                                  | Memberart | Hinweise |
|-----------------------------------------------------------------------------------|-------------|-------|
| [**"HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | Eigenschaft    | Keine  |
| [**Verticalscrollprozent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | Eigenschaft    | Keine  |
| [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | Eigenschaft    | Keine  |
| [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | Eigenschaft    | Keine  |
| [**HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | Eigenschaft    | Keine  |
| [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | Eigenschaft    | Keine  |
| [**Scroll**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | Methode      | Keine  |
| [**Setscrollprozent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




