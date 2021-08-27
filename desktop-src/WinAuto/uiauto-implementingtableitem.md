---
title: TableItem-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von ITableItemProvider, einschließlich Informationen zu Methoden. Das TableItem-Steuerelementmuster wird verwendet, um untergeordnete Steuerelemente von Containern zu unterstützen, die ITableProvider implementieren.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des TableItem-Steuerelementmusters
- Benutzeroberflächenautomatisierung,TableItem-Steuerelementmuster
- Benutzeroberflächenautomatisierung,ITableItemProvider
- ITableItemProvider
- Implementieren Benutzeroberflächenautomatisierung TableItem-Steuerelementmustern
- TableItem-Steuerelementmuster
- Steuerelementmuster, ITableItemProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung TableItem
- Steuerelementmuster, TableItem
- interfaces,ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babb64114bb761b0b6e93a7cc9c0036cb01bb8946eb813bcd0fc3e821d44a183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098270"
---
# <a name="tableitem-control-pattern"></a>TableItem-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung [**von ITableItemProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)einschließlich Informationen zu Methoden. Das **TableItem-Steuerelementmuster** wird verwendet, um untergeordnete Steuerelemente von Containern zu unterstützen, die [**ITableProvider implementieren.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)

Der Zugriff auf die Funktionalität einzelner Zellen wird durch die erforderliche, gleichzeitige Implementierung von [**IGridItemProvider bereitgestellt.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) Dieses Steuerelementmuster entspricht **IGridItemProvider** mit dem Unterschied, dass jedes Steuerelement, das [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) implementiert, programmgesteuert die Beziehung zwischen der einzelnen Zelle und ihren Zeilen- und Spalteninformationen verfügbar machen muss. Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ITableItemProvider**](#required-members-for-itableitemprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim **Implementieren des TableItem-Steuerelementmusters** die folgenden Richtlinien und Konventionen:

-   Informationen zu verwandten Rasterelementfunktionen finden Sie unter [GridItem-Steuerelementmuster](uiauto-implementinggriditem.md).

## <a name="required-members-for-itableitemprovider"></a>Erforderliche Member für **ITableItemProvider**

Die folgenden Methoden sind für die Implementierung der [**ITableItemProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) erforderlich.



| Erforderliche Member                                                               | Memberart | Hinweise |
|--------------------------------------------------------------------------------|-------------|-------|
| [**GetColumnHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | Methode      | Keine  |
| [**GetRowHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Eigenschaften oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Tabellensteuermuster](uiauto-implementingtable.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




