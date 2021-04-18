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
# <a name="how-to-use-tree-view-infotips"></a>Verwenden von Tree-View infotips

Wenn Sie den [**\_ infotip**](tree-view-control-window-styles.md) -Stil für das TV auf ein Strukturansicht-Steuerelement anwenden, werden [TVN \_ getinfotip](tvn-getinfotip.md) -Benachrichtigungen generiert, wenn sich der Cursor über einem Element in der Strukturansicht befindet. Wenn Sie auf diese Benachrichtigung reagieren, können Sie den Text festlegen, der im infotip angezeigt wird.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-tree-view-infotips"></a>Verwenden von Tree-View infotips

Der folgende Beispielcode zeigt, wie eine Anwendung auf die Benachrichtigung reagieren könnte. Der Einfachheit halber kopiert das Beispiel lediglich den Text für das Element in den infotip.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Tree-View Steuerelementen](using-treeview.md)
</dt> <dt>

[Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




