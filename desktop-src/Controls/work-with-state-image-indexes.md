---
title: Arbeiten mit Zustands Image Indizes
description: Häufig gibt es Verwirrung beim Festlegen und Abrufen des Zustands Bild Indexes in einem Strukturansicht-Steuerelement.
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be84035907b69ba98ed60a33046f1a58fd2b47b2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723685"
---
# <a name="how-to-work-with-state-image-indexes"></a>Arbeiten mit Zustands Image Indizes

Häufig gibt es Verwirrung beim Festlegen und Abrufen des Zustands Bild Indexes in einem Strukturansicht-Steuerelement. In den folgenden Beispielen wird die richtige Methode zum Festlegen und Abrufen des Zustands Bild Indexes veranschaulicht. In den Beispielen wird davon ausgegangen, dass im Strukturansicht-Steuerelement nur zwei Status Bild Indizes vorhanden sind, deaktiviert und überprüft werden. Wenn die Anwendung mehr als zwei enthält, müssen diese Funktionen geändert werden, um diesen Fall zu verarbeiten.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="set-a-tree-view-items-check-state"></a>Festlegen des Prüf Zustands eines Tree-View Elements

Im folgenden Beispiel wird veranschaulicht, wie der Prüf Zustand eines Struktur Ansichts Elements festgelegt wird.


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



### <a name="retrieve-a-tree-view-items-check-state"></a>Abrufen des Prüf Zustands eines Tree-View Elements

Im folgenden Beispiel wird veranschaulicht, wie der Prüf Zustand eines Struktur Ansichts Elements abgerufen wird.


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

[Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




