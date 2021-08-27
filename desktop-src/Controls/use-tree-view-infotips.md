---
title: Verwenden von Tree-View Infos
description: Wenn Sie den TVS INFOTIP-Stil auf ein \_ Strukturansicht-Steuerelement anwenden, werden TVN GETINFOTIP-Benachrichtigungen generiert, wenn sich der Cursor über einem Element in der \_ Strukturansicht befindet. Wenn Sie auf diese Benachrichtigung reagieren, können Sie den Text festlegen, der in der Infotip angezeigt wird.
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff9273b28b614e7935f6ac507288a5733271fb455a6be1e85b52c5b0ba8bbb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132030"
---
# <a name="how-to-use-tree-view-infotips"></a>Verwenden von Tree-View Infos

Wenn Sie den [**TVS \_ INFOTIP-Stil**](tree-view-control-window-styles.md) auf ein Strukturansicht-Steuerelement anwenden, werden [TVN \_ GETINFOTIP-Benachrichtigungen](tvn-getinfotip.md) generiert, wenn sich der Cursor über einem Element in der Strukturansicht befindet. Wenn Sie auf diese Benachrichtigung reagieren, können Sie den Text festlegen, der in der Infotip angezeigt wird.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-tree-view-infotips"></a>Verwenden Tree-View Infotips

Der folgende Beispielcode zeigt, wie eine Anwendung auf die Benachrichtigung reagieren kann. Der Einfachheit halber kopiert das Beispiel nur den Text für das Element in die Infotip.


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

[Verwenden Tree-View-Steuerelementen](using-treeview.md)
</dt> <dt>

[CustDTv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View Steuerelement](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




