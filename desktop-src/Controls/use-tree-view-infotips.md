---
title: Verwenden von Tree-View infotips
description: Wenn Sie den \_ infotip-Stil für das TV auf ein Strukturansicht-Steuerelement anwenden, werden TVN \_ getinfotip-Benachrichtigungen generiert, wenn sich der Cursor über einem Element in der Strukturansicht befindet. Wenn Sie auf diese Benachrichtigung reagieren, können Sie den Text festlegen, der im infotip angezeigt wird.
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0ef862d68cfd9f6ac5a97e82c80622e9c02121
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "106340687"
---
# <a name="how-to-use-tree-view-infotips"></a><span data-ttu-id="5bca1-104">Verwenden von Tree-View infotips</span><span class="sxs-lookup"><span data-stu-id="5bca1-104">How to Use Tree-View Infotips</span></span>

<span data-ttu-id="5bca1-105">Wenn Sie den [**\_ infotip**](tree-view-control-window-styles.md) -Stil für das TV auf ein Strukturansicht-Steuerelement anwenden, werden [TVN \_ getinfotip](tvn-getinfotip.md) -Benachrichtigungen generiert, wenn sich der Cursor über einem Element in der Strukturansicht befindet.</span><span class="sxs-lookup"><span data-stu-id="5bca1-105">When you apply the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style to a tree-view control, it generates [TVN\_GETINFOTIP](tvn-getinfotip.md) notifications when the cursor is over an item in the tree view.</span></span> <span data-ttu-id="5bca1-106">Wenn Sie auf diese Benachrichtigung reagieren, können Sie den Text festlegen, der im infotip angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5bca1-106">By responding to this notification, you can set the text that appears in the infotip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5bca1-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="5bca1-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5bca1-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="5bca1-108">Technologies</span></span>

-   [<span data-ttu-id="5bca1-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="5bca1-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5bca1-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5bca1-110">Prerequisites</span></span>

-   <span data-ttu-id="5bca1-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="5bca1-111">C/C++</span></span>
-   <span data-ttu-id="5bca1-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="5bca1-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5bca1-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="5bca1-113">Instructions</span></span>

### <a name="use-tree-view-infotips"></a><span data-ttu-id="5bca1-114">Verwenden von Tree-View infotips</span><span class="sxs-lookup"><span data-stu-id="5bca1-114">Use Tree-View Infotips</span></span>

<span data-ttu-id="5bca1-115">Der folgende Beispielcode zeigt, wie eine Anwendung auf die Benachrichtigung reagieren könnte.</span><span class="sxs-lookup"><span data-stu-id="5bca1-115">The following example code shows how an application might respond to the notification.</span></span> <span data-ttu-id="5bca1-116">Der Einfachheit halber kopiert das Beispiel lediglich den Text für das Element in den infotip.</span><span class="sxs-lookup"><span data-stu-id="5bca1-116">For simplicity, the example just copies the text for the item to the infotip.</span></span>


```
  case WM_NOTIFY:
    switch (((LPNMHDR) lParam)->code)
    {
    case TVN_GETINFOTIP:
        {
          LPNMTVGETINFOTIP pTip = (LPNMTVGETINFOTIP)lParam;
          HWND hTree            = GetDlgItem(hDlg, IDC_TREE1);
          HTREEITEM item        = pTip->hItem;

          // Get the text for the item.
          TVITEM tvitem;
          tvitem.mask       = TVIF_TEXT;
          tvitem.hItem      = item;
          TCHAR temp[1024];
          tvitem.pszText    = infoTipBuf;
          tvitem.cchTextMax = sizeof(temp) / sizeof(TCHAR);
          TreeView_GetItem(hTree, &tvitem);

          // Copy the text to the infotip.
          wcscpy_s(pTip->pszText, pTip->cchTextMax, tvitem.pszText);
          break;
        }
      }
      return TRUE;
```



## <a name="related-topics"></a><span data-ttu-id="5bca1-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5bca1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bca1-118">Verwenden von Tree-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="5bca1-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="5bca1-119">Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5bca1-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




