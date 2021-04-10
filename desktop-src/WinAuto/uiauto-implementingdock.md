---
title: Dock-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IDockProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Dock-Steuerelement Muster wird verwendet, um die Andock Eigenschaften eines Steuer Elements in einem Docking Container verfügbar zu machen.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- Benutzeroberflächenautomatisierung, Implementieren des Dock-Steuerelement Musters
- Benutzeroberflächenautomatisierungs, Dock-Steuerelement Muster
- UI-Automatisierung, IDockProvider
- IDockProvider
- Implementieren von Dock-Steuerungs Mustern für Benutzeroberflächen Automatisierung
- Dock-Steuerelement Muster
- Steuerelement Muster, IDockProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Dock
- Steuerelement Muster, Andocken
- Schnittstellen, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855991"
---
# <a name="dock-control-pattern"></a>Dock-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **Dock** -Steuerelement Muster wird verwendet, um die Andock Eigenschaften eines Steuer Elements in einem Docking Container verfügbar zu machen.

Ein Dockingcontainer ist ein Steuerelement, mit dem untergeordnete Elemente horizontal oder vertikal zueinander ausgerichtet werden können. Die folgende Abbildung zeigt einen Docking Container mit zwei untergeordneten Elementen. Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

![Screenshot des Docking Containers mit zwei angedockten untergeordneten Elementen](images/dockxmpl.jpg)

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IDockProvider**](#required-members-for-idockprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Dock** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) macht keine Eigenschaften des Docking Containers oder Eigenschaften von Steuerelementen verfügbar, die neben dem aktuellen Steuerelement im Docking Container angedockt sind.
-   Steuerelemente werden relativ zueinander entsprechend ihrer aktuellen z-Reihenfolge angeordnet. Je höher ihre z-Reihenfolgenposition ist, desto weiter entfernt vom angegebenen Rand des Dockingcontainers werden sie platziert.
-   Wenn die Größe des Dockingcontainers geändert wird, werden alle angedockten Steuerelemente im Container bündig zu derselben Kante neu positioniert, an der sie ursprünglich angedockt waren. Die Größe der angedockten Steuerelemente wird ebenfalls geändert, um den Platz innerhalb des Containers entsprechend dem Andock Verhalten Ihrer [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) -Eigenschaft auszufüllen. Wenn z. b. **DockPosition \_ Top** angegeben ist, werden die linke und die Rechte Seite des Steuer Elements erweitert, um den verfügbaren Platz auszufüllen. Wenn **DockPosition \_ Fill** angegeben ist, werden alle vier Seiten des Steuer Elements erweitert, um den verfügbaren Platz auszufüllen.
-   Auf einem System mit mehreren Bildschirmen sollten Steuerelemente auf der linken oder rechten Seite des aktuellen Bildschirms andocken. Ist dies nicht möglich, sollten sie auf der linken Seite des am weitesten links stehenden Bildschirms bzw. auf der rechten Seite des am weitesten rechts stehenden Bildschirms angedockt werden.

## <a name="required-members-for-idockprovider"></a>Erforderliche Member für **IDockProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                | Memberart | Hinweise |
|-----------------------------------------------------------------|-------------|-------|
| [**Dock Position**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | Eigenschaft    | Keine  |
| [**SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




