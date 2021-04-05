---
title: GridItem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IGridItemProvider, einschließlich Informationen zu Eigenschaften. Das GridItem-Steuerelement Muster wird verwendet, um einzelne untergeordnete Steuerelemente von Containern zu unterstützen, die IGridProvider implementieren.
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des GridItem-Steuerelement Musters
- UI-Automatisierung, GridItem-Steuerelement Muster
- UI-Automatisierung, IGridItemProvider
- IGridItemProvider
- Implementieren von GridItem-Steuerelement Mustern für Benutzeroberflächen
- GridItem-Steuerelement Muster
- Steuerelement Muster, IGridItemProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-GridItem
- Steuerelement Muster, GridItem
- Schnittstellen, IGridItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709695"
---
# <a name="griditem-control-pattern"></a>GridItem-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), einschließlich Informationen zu Eigenschaften. Das **GridItem** -Steuerelement Muster wird verwendet, um einzelne untergeordnete Steuerelemente von Containern zu unterstützen, die [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)implementieren.

Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IGridItemProvider**](#required-members-for-igriditemprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **GridItem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Rasterkoordinaten (Grid-Koordinaten) sind nullbasiert, wobei die obere linke Zelle die Koordinaten (0, 0) hat.
-   Zusammengeführte Zellen melden ihre [**Zeilen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) -und [**Spalten**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) Eigenschaften basierend auf Ihrer zugrunde liegenden Anker Zelle, wie vom Microsoft UI Automation Provider definiert. In der Regel sind dies die oberste Zeile und die am weitesten links liegende Spalte.
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) bietet keine aktive Bearbeitung des Rasters, wie z. b. das Zusammenführen oder aufteilen von Zellen.
-   Steuerelemente, die [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) implementieren, können in der Regel mithilfe der Tastatur durchlaufen werden (d. h., ein Benutzeroberflächenautomatisierungs-Client kann zu benachbarten Steuerelementen wechseln).

## <a name="required-members-for-igriditemprovider"></a>Erforderliche Member für **IGridItemProvider**

Die folgenden Eigenschaften sind erforderlich, um die [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) -Schnittstelle zu implementieren.



| Erforderliche Member                                                  | Memberart | Hinweise |
|-------------------------------------------------------------------|-------------|-------|
| [**Zeile**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | Eigenschaft    | Keine  |
| [**Column**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | Eigenschaft    | Keine  |
| [**RowSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | Eigenschaft    | Keine  |
| [**ColumnSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | Eigenschaft    | Keine  |
| [**ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | Eigenschaft    | Keine  |



 

Diesem Steuerelementmuster sind keine Methoden oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Raster-Steuerelement Muster](uiauto-implementinggrid.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




