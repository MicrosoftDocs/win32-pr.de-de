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
# <a name="how-to-work-with-state-image-indexes"></a><span data-ttu-id="6df05-103">Arbeiten mit Zustands Image Indizes</span><span class="sxs-lookup"><span data-stu-id="6df05-103">How to Work With State Image Indexes</span></span>

<span data-ttu-id="6df05-104">Häufig gibt es Verwirrung beim Festlegen und Abrufen des Zustands Bild Indexes in einem Strukturansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="6df05-104">There is often confusion about how to set and retrieve the state image index in a tree-view control.</span></span> <span data-ttu-id="6df05-105">In den folgenden Beispielen wird die richtige Methode zum Festlegen und Abrufen des Zustands Bild Indexes veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6df05-105">The following examples demonstrate the proper method for setting and retrieving the state image index.</span></span> <span data-ttu-id="6df05-106">In den Beispielen wird davon ausgegangen, dass im Strukturansicht-Steuerelement nur zwei Status Bild Indizes vorhanden sind, deaktiviert und überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="6df05-106">The examples assume that there are only two state image indexes in the tree-view control, unchecked and checked.</span></span> <span data-ttu-id="6df05-107">Wenn die Anwendung mehr als zwei enthält, müssen diese Funktionen geändert werden, um diesen Fall zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6df05-107">If your application contains more than two, these functions will need to be modified to handle that case.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6df05-108">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="6df05-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6df05-109">Technologien</span><span class="sxs-lookup"><span data-stu-id="6df05-109">Technologies</span></span>

-   [<span data-ttu-id="6df05-110">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="6df05-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="6df05-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="6df05-111">Prerequisites</span></span>

-   <span data-ttu-id="6df05-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="6df05-112">C/C++</span></span>
-   <span data-ttu-id="6df05-113">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="6df05-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="6df05-114">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="6df05-114">Instructions</span></span>

### <a name="set-a-tree-view-items-check-state"></a><span data-ttu-id="6df05-115">Festlegen des Prüf Zustands eines Tree-View Elements</span><span class="sxs-lookup"><span data-stu-id="6df05-115">Set a Tree-View Item's Check State</span></span>

<span data-ttu-id="6df05-116">Im folgenden Beispiel wird veranschaulicht, wie der Prüf Zustand eines Struktur Ansichts Elements festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="6df05-116">The following example demonstrates how to set a tree-view item's check state.</span></span>


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



### <a name="retrieve-a-tree-view-items-check-state"></a><span data-ttu-id="6df05-117">Abrufen des Prüf Zustands eines Tree-View Elements</span><span class="sxs-lookup"><span data-stu-id="6df05-117">Retrieve a Tree-View Item's Check State</span></span>

<span data-ttu-id="6df05-118">Im folgenden Beispiel wird veranschaulicht, wie der Prüf Zustand eines Struktur Ansichts Elements abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6df05-118">The following example demonstrates how to retrieve a tree-view item's check state.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6df05-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6df05-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6df05-120">Verwenden von Tree-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="6df05-120">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="6df05-121">Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6df05-121">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




