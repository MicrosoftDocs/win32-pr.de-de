---
title: Dock-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IDockProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Dock-Steuerelementmuster wird verwendet, um die Dock-Eigenschaften eines Steuerelements in einem Andockcontainer verfügbar zu machen.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des Dock-Steuerelementmusters
- Benutzeroberflächenautomatisierung, Dock-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IDockProvider
- IDockProvider
- Implementieren von Benutzeroberflächenautomatisierung Dock-Steuerelementmustern
- Dock-Steuerelementmuster
- Steuerelementmuster,IDockProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung Andockens
- Steuerelementmuster, Andocken
- interfaces,IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb0afd6a291a9e26c43d1aff957c7b7e9cd8c752040a661551b8eaf5b12b86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115099"
---
# <a name="dock-control-pattern"></a>Dock-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**IDockProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)einschließlich Informationen zu Eigenschaften und Methoden. Das **Dock-Steuerelementmuster** wird verwendet, um die Dock-Eigenschaften eines Steuerelements in einem Andockcontainer verfügbar zu machen.

Ein Dockingcontainer ist ein Steuerelement, mit dem untergeordnete Elemente horizontal oder vertikal zueinander ausgerichtet werden können. Die folgende Abbildung zeigt einen Andockcontainer mit zwei untergeordneten Elementen. Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und deren unterstützte Steuerelementmuster.](uiauto-controlpatternmapping.md)

![Screenshot: Dockingcontainer mit zwei angedockten untergeordneten Elemente](images/dockxmpl.jpg)

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IDockProvider**](#required-members-for-idockprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie  beim Implementieren des Dock-Steuerelementmusters die folgenden Richtlinien und Konventionen:

-   [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) macht keine Eigenschaften des Andockcontainers oder Eigenschaften von Steuerelementen verfügbar, die neben dem aktuellen Steuerelement im Andockcontainer angedockt sind.
-   Steuerelemente werden relativ zueinander entsprechend ihrer aktuellen z-Reihenfolge angeordnet. Je höher ihre z-Reihenfolgenposition ist, desto weiter entfernt vom angegebenen Rand des Dockingcontainers werden sie platziert.
-   Wenn die Größe des Dockingcontainers geändert wird, werden alle angedockten Steuerelemente im Container bündig zu derselben Kante neu positioniert, an der sie ursprünglich angedockt waren. Die angedockten Steuerelemente ändern auch die Größe, um entsprechend dem Andockverhalten ihrer [**DockPosition-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) speicherplatz innerhalb des Containers zu füllen. Wenn beispielsweise **DockPosition \_ Top** angegeben ist, wird die linke und rechte Seite des Steuerelements erweitert, um den verfügbaren Platz auszufüllen. Wenn **DockPosition \_ Fill** angegeben ist, werden alle vier Seiten des Steuerelements erweitert, um den verfügbaren Platz auszufüllen.
-   Auf einem System mit mehreren Bildschirmen sollten Steuerelemente auf der linken oder rechten Seite des aktuellen Bildschirms andocken. Ist dies nicht möglich, sollten sie auf der linken Seite des am weitesten links stehenden Bildschirms bzw. auf der rechten Seite des am weitesten rechts stehenden Bildschirms angedockt werden.

## <a name="required-members-for-idockprovider"></a>Erforderliche Member für **IDockProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IDockProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) erforderlich.



| Erforderliche Member                                                | Memberart | Hinweise |
|-----------------------------------------------------------------|-------------|-------|
| [**Dockposition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | Eigenschaft    | Keine  |
| [**SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und deren unterstützte Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




