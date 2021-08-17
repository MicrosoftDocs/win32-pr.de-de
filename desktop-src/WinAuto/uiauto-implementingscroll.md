---
title: Bildlauf-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IScrollProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Bildlauf-Steuerelementmuster wird verwendet, um ein Steuerelement zu unterstützen, das als bildlauffähiger Container für eine Auflistung untergeordneter Objekte fungiert.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des Bildlauf-Steuerelementmusters
- Benutzeroberflächenautomatisierung,Bildlauf-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IScrollProvider
- IScrollProvider
- Implementieren Benutzeroberflächenautomatisierung Bildlauf-Steuerelementmustern
- Bildlauf-Steuerelementmuster
- Steuerelementmuster,IScrollProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung Scrollen
- Steuerelementmuster, Scrollen
- interfaces,IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d1cf3c04be18f362a64e619ec4659fac58923f29e6105174057b18a580f8d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324394"
---
# <a name="scroll-control-pattern"></a>Bildlauf-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung [**von IScrollProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)einschließlich Informationen zu Eigenschaften und Methoden. Das **Bildlauf-Steuerelementmuster** wird verwendet, um ein Steuerelement zu unterstützen, das als bildlauffähiger Container für eine Auflistung untergeordneter Objekte fungiert.

Das -Steuerelement ist nicht erforderlich, um Bildlaufleisten zu verwenden, um die Scrollfunktion zu unterstützen, obwohl es dies häufig tut. Die folgende Abbildung zeigt ein Bildlaufsteuerfeld, das keine Bildlaufleisten verwendet. Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md).

![Screenshot eines Bildlaufsteuerfelds ohne Bildlaufleisten](images/uia-scrollpattern-without-scrollbars.jpg)

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IScrollProvider**](#required-members-for-iscrollprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des Bildlauf-Steuerelementmusters die folgenden Richtlinien und Konventionen: 

-   Die unteren Teil dieses Steuerelements müssen [**IScrollItemProvider implementieren.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)
-   Die Bildlaufleisten eines Containersteuerfelds unterstützen das **Bildlauf-Steuerelementmuster** nicht. Sie müssen stattdessen das [RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) unterstützen.
-   Wenn das Scrollen in Prozentwerten gemessen wird, müssen alle Werte oder Beträge, die sich auf die Einteilung der Bildlaufleiste beziehen, auf einen Bereich von 0 bis 100 normalisiert werden.
-   Die [**IScrollProvider::HorizontallyScrollable-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) und [**die VerticallyScrollable-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) sind unabhängig von der **IsEnabled-Eigenschaft.**
-   Wenn die [**IScrollProvider::HorizontallyScrollable-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) **FALSE** ist, sollte die [**HorizontalViewSize-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) auf 100 (100 %) und die [**HorizontalScrollPercent-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) auf **UIA \_ ScrollPatternNoScroll** (-1) festgelegt werden. Wenn die [**VerticallyScrollable-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) **FALSE** ist, sollte die [**VerticalViewSize-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) auf 100 (100 %) und [**die VerticalScrollPercent-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) auf **UIA \_ ScrollPatternNoScroll** (-1) festgelegt werden. Dadurch kann ein Microsoft Benutzeroberflächenautomatisierung-Client diese Eigenschaftswerte innerhalb der [**SetScrollPercent-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) verwenden und gleichzeitig eine Racebedingung vermeiden, wenn eine Richtung aktiviert wird, in der der Client nicht am Scrollen interessiert ist.
-   Die [**IScrollProvider::HorizontalScrollPercent-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) ist localespezifisch. Wenn **Sie HorizontalScrollPercent** auf 100 festlegen, muss die Bildlaufposition des Steuerelements auf das Äquivalent seiner äußersten rechten Position für Sprachen wie Englisch festgelegt werden, die von links nach rechts lesen. Für Sprachen wie Arabisch, die von rechts nach links lesen, muss das **Festlegen von HorizontalScrollPercent** auf 100 alternativ die Bildlaufposition an der äußersten linken Position festlegen.

## <a name="required-members-for-iscrollprovider"></a>Erforderliche Member für **IScrollProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IScrollProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) erforderlich.



| Erforderliche Member                                                                  | Memberart | Hinweise |
|-----------------------------------------------------------------------------------|-------------|-------|
| [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | Eigenschaft    | Keine  |
| [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | Eigenschaft    | Keine  |
| [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | Eigenschaft    | Keine  |
| [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | Eigenschaft    | Keine  |
| [**HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | Eigenschaft    | Keine  |
| [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | Eigenschaft    | Keine  |
| [**Blättern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | Methode      | Keine  |
| [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




