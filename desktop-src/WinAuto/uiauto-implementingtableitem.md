---
title: TableItem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ITableItemProvider, einschließlich Informationen zu-Methoden. Das TableItem-Steuerelement Muster wird verwendet, um untergeordnete Steuerelemente von Containern zu unterstützen, die ITableProvider implementieren.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des TableItem-Steuerelement Musters
- UI-Automatisierung, TableItem-Steuerelement Muster
- UI-Automatisierung, ITableItemProvider
- ITableItemProvider
- Implementieren von TableItem-Steuerelement Mustern für Benutzeroberflächen
- TableItem-Steuerelement Muster
- Steuerelement Muster, ITableItemProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-TableItem
- Steuerelement Muster, TableItem
- Schnittstellen, ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709276"
---
# <a name="tableitem-control-pattern"></a>TableItem-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), einschließlich Informationen zu-Methoden. Das **TableItem** -Steuerelement Muster wird verwendet, um untergeordnete Steuerelemente von Containern zu unterstützen, die [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)implementieren.

Der Zugriff auf die Funktionalität einzelner Zellen wird von der erforderlichen, gleichzeitigen Implementierung von [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)bereitgestellt. Dieses Steuerelement Muster ist analog zu **IGridItemProvider** , wobei jedes Steuerelement, das [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) implementiert, die Beziehung zwischen der einzelnen Zelle und den zugehörigen Zeilen-und Spalten Informationen Programm gesteuert verfügbar machen muss. Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für " **ITableItemProvider** "](#required-members-for-itableitemprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **TableItem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Weitere Informationen zu verwandten Raster Elementen finden Sie unter [GridItem-Steuerelement Muster](uiauto-implementinggriditem.md).

## <a name="required-members-for-itableitemprovider"></a>Erforderliche Member für " **ITableItemProvider** "

Die folgenden Methoden sind erforderlich, um die [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) -Schnittstelle zu implementieren.



| Erforderliche Member                                                               | Memberart | Hinweise |
|--------------------------------------------------------------------------------|-------------|-------|
| [**GetColumnHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | Methode      | Keine  |
| [**GetRowHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Eigenschaften oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Table-Steuerelement Muster](uiauto-implementingtable.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




