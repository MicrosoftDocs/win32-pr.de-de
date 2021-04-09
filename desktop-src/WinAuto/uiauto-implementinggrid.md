---
title: Raster-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IGridProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Raster-Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Container für eine Auflistung von untergeordneten Elementen fungieren.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Raster Steuerelement Musters
- UI-Automatisierung, Raster-Steuerelement Muster
- UI-Automatisierung, IGridProvider
- IGridProvider
- Implementieren von Raster Steuerelement Mustern für Benutzeroberflächen Automatisierung
- Raster Steuerelement Muster
- Steuerelement Muster, IGridProvider
- Steuerelement Muster, Implementieren des UI-Automatisierungs Rasters
- Steuerelement Muster, Raster
- Schnittstellen, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036725"
---
# <a name="grid-control-pattern"></a>Raster-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **Raster** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Container für eine Auflistung von untergeordneten Elementen fungieren.

Die untergeordneten Elemente dieses Elements müssen [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) implementieren und in einem zweidimensionalen logischen Koordinatensystem angeordnet sein, das Zeilen-und spaltenweise durchlaufen werden kann. Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IGridProvider**](#required-members-for-igridprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Grid** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Raster Koordinaten sind NULL basiert, wobei die obere linke Zelle (oder die obere rechte Zelle, je nach Gebiets Schema) die Koordinaten (0,0) aufweist.
-   Wenn eine Zelle leer ist, muss ein Microsoft UI Automation-Element zurückgegeben werden, um die [**IGridItemProvider:: ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) -Eigenschaft für diese Zelle zu unterstützen. Dies ist möglich, wenn das Layout von untergeordneten Elementen im Raster dem eines unregelmäßigen Arrays entspricht (siehe folgendes Beispiel).

    ![Beispiel für ein Grid-Steuerelement mit leeren Koordinaten](images/grid.png)

-   Ein Raster mit einem einzelnen Element ist nach wie vor erforderlich, um [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) zu implementieren, wenn es logisch als Raster angesehen wird. Die Anzahl untergeordneter Elemente im Raster ist unwesentlich.
-   Ausgeblendete Zeilen und Spalten können abhängig von der Implementierung des Anbieters in der Benutzeroberflächenautomatisierungs-Struktur geladen werden und werden daher in den Eigenschaften [**IGridProvider:: ROWCOUNT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) und [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) widergespiegelt. Wenn die ausgeblendeten Zeilen und Spalten noch nicht geladen wurden, sollten sie nicht gezählt werden.
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) ermöglicht keine aktive Bearbeitung eines Rasters. [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) muss implementiert werden, um diese Funktionalität zu aktivieren.
-   Verwenden Sie einen [**iuiautomationstructurechangedebug-thandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) zum lauschen auf Struktur-oder Layoutänderungen am Raster, z. b. Zellen, die hinzugefügt, entfernt oder zusammengeführt wurden.
-   Verwenden Sie einen [**iuiautomationfocuschangedebug-thandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) , um den Durchlauf durch die Elemente oder Zellen eines Rasters zu verfolgen.

## <a name="required-members-for-igridprovider"></a>Erforderliche Member für **IGridProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                        | Memberart | Hinweise |
|---------------------------------------------------------|-------------|-------|
| [**RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | Eigenschaft    | Keine  |
| [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | Eigenschaft    | Keine  |
| [**GetItem**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[GridItem-Steuerelement Muster](uiauto-implementinggriditem.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




