---
title: Arbeiten mit Zustandsbildindizes
description: Häufig gibt es Verwirrung darüber, wie der Statusbildindex in einem Strukturansicht-Steuerelement festgelegt und abgerufen wird.
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04504019f79a388b6c21f940724de884d8516263daf6d410a841a96fc2e557b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059300"
---
# <a name="how-to-work-with-state-image-indexes"></a>Arbeiten mit Zustandsbildindizes

Häufig gibt es Verwirrung darüber, wie der Statusbildindex in einem Strukturansicht-Steuerelement festgelegt und abgerufen wird. Die folgenden Beispiele veranschaulichen die richtige Methode zum Festlegen und Abrufen des Statusbildindexes. In den Beispielen wird davon ausgegangen, dass im Strukturansicht-Steuerelement nur zwei Statusbildindizes (deaktiviert und aktiviert) verfügbar sind. Wenn Ihre Anwendung mehr als zwei enthält, müssen diese Funktionen geändert werden, um diesen Fall zu behandeln.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="set-a-tree-view-items-check-state"></a>Festlegen des Tree-View des Elements

Im folgenden Beispiel wird veranschaulicht, wie der Überprüfungszustand eines Strukturansichtselements festgelegt wird.


```C++
  BOOL TreeView_SetCheckState(HWND hwndTreeView, HTREEITEM hItem, BOOL fCheck)
  {
      TVITEM tvItem;

      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Image 1 in the tree-view check box image list is the unchecked box. 
      // Image 2 is the checked box.

      tvItem.state = INDEXTOSTATEIMAGEMASK((fCheck ? 2 : 1));

      return TreeView_SetItem(hwndTreeView, &tvItem);
  }
```



### <a name="retrieve-a-tree-view-items-check-state"></a>Abrufen des Tree-View eines Elements

Im folgenden Beispiel wird veranschaulicht, wie der Überprüfungszustand eines Strukturansichtselements abgerufen wird.


```C++
  BOOL TreeView_GetCheckState(HWND hwndTreeView, HTREEITEM hItem)
  {
      TVITEM tvItem;

      // Prepare to receive the desired information.
      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Request the information.
      TreeView_GetItem(hwndTreeView, &tvItem);

      // Return zero if it's not checked, or nonzero otherwise.
      return ((BOOL)(tvItem.state >> 12) - 1);
  }
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Tree-View Steuerelementen](using-treeview.md)
</dt> <dt>

[CustDTv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View Steuerelement](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




