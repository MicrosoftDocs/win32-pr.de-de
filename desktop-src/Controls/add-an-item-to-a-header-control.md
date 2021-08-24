---
title: Hinzufügen eines Elements zu einem Headersteuerelement
description: In diesem Thema wird veranschaulicht, wie einem Headersteuerelement ein Element hinzugefügt wird.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4face974c1b04021afdc9e26976c023e1287439eb3d6d63c7ea7f9f34c5b27f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922053"
---
# <a name="how-to-add-an-item-to-a-header-control"></a>Hinzufügen eines Elements zu einem Headersteuerelement

In diesem Thema wird veranschaulicht, wie einem Headersteuerelement ein Element hinzugefügt wird. Ein Headersteuerelemente verfügt in der Regel über mehrere Headerelemente, die die Spalten des Steuerelements definieren. Sie können einem Headersteuerelement ein Element hinzufügen, indem Sie die [**HDM \_ INSERTITEM-Nachricht**](hdm-insertitem.md) an das Steuerelement senden.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Verwenden Sie die [**HDM \_ INSERTITEM-Nachricht,**](hdm-insertitem.md) um dem Headersteuerelement ein Element hinzuzufügen. Die Nachricht muss die Adresse einer [**HDITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-hditema) enthalten. Diese Struktur definiert die Eigenschaften des Headerelements, die eine Zeichenfolge, ein Bitmapbild, eine Anfangsgröße und einen anwendungsdefinierten 32-Bit-Wert enthalten können.

Im folgenden Beispiel wird veranschaulicht, wie sie die [**HDM \_ INSERTITEM-Nachricht**](hdm-insertitem.md) und die [**HDITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-hditema) verwenden, um einem Headersteuerelement ein Element hinzuzufügen. Das neue Element besteht aus einer Zeichenfolge, die innerhalb des Elementrechtecks linksbrechtig ist.



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

[Informationen zu Headersteuerelementen](header-controls.md)
</dt> <dt>

[Header-Steuerelementreferenz](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Verwenden von Headersteuerelementen](using-header-controls.md)
</dt> </dl>

 

 




