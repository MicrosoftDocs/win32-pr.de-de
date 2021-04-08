---
title: Vorgehensweise beim Hinzufügen eines Elements zu einem Header Steuerelement
description: In diesem Thema wird veranschaulicht, wie ein Element einem Header-Steuerelement hinzugefügt wird.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949243"
---
# <a name="how-to-add-an-item-to-a-header-control"></a>Vorgehensweise beim Hinzufügen eines Elements zu einem Header Steuerelement

In diesem Thema wird veranschaulicht, wie ein Element einem Header-Steuerelement hinzugefügt wird. Ein Header Steuerelement verfügt in der Regel über mehrere Header Elemente, die die Spalten des Steuer Elements definieren. Sie können einem Header-Steuerelement ein Element hinzufügen, indem Sie die [**HDM \_ InsertItem**](hdm-insertitem.md) -Nachricht an das-Steuerelement senden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Verwenden Sie die [**HDM \_ InsertItem**](hdm-insertitem.md) -Nachricht, um dem Header Steuerelement ein Element hinzuzufügen. Die Nachricht muss die Adresse einer [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur enthalten. Diese Struktur definiert die Eigenschaften des Header Elements, das eine Zeichenfolge, ein Bitmap-Bild, eine Anfangs Größe und einen Anwendungs definierten 32-Bit-Wert enthalten kann.

Im folgenden Beispiel wird veranschaulicht, wie die [**HDM- \_ InsertItem**](hdm-insertitem.md) -Nachricht und die [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur verwendet werden, um ein Element zu einem Header-Steuerelement hinzuzufügen. Das neue Element besteht aus einer Zeichenfolge, die innerhalb des Element Rechtecks linksbündig ausgerichtet ist.



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über Header Steuerelemente](header-controls.md)
</dt> <dt>

[Header Steuerelement Verweis](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Verwenden von Header Steuerelementen](using-header-controls.md)
</dt> </dl>

 

 




