---
title: Zeichnen eines Bilds
description: In diesem Thema wird veranschaulicht, wie Sie die ImageList \_ Draw-Funktion verwenden, um ein Bild zu zeichnen.
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7b42e97ad9b7cab8693431654dc31b473267414f31ae5811f4f66a6663ce8e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878330"
---
# <a name="how-to-draw-an-image"></a>Zeichnen eines Bilds

In diesem Thema wird veranschaulicht, wie Sie die [**ImageList \_ Draw-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) verwenden, um ein Bild zu zeichnen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Um ein Bild zu zeichnen, verwenden Sie die [**Funktion ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) oder [**ImageList \_ DrawEx.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) Sie geben das Handle für eine Bildliste, den Index des zu zeichnende Bilds, das Handle für den Zielgerätekontext, eine Position im Gerätekontext und mindestens einen Zeichnungsstil an.

Die benutzerdefinierte Funktion im folgenden C++-Codebeispiel verwendet die [**ImageList \_ Draw-Funktion,**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) um ein Bild zu zeichnen, und speichert die Clientkoordinaten des umgebenden Rechtecks des Bilds. Eine nachfolgende Funktion verwendet das umgrenzende Rechteck, um zu bestimmen, ob der Benutzer auf das Bild geklickt hat.



```C++
// DrawTheImage - draws an image transparently and saves 
// the bounding rectangle of the drawn image.
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which to draw the image. 
// himl - handle to the image list that contains the image. 
// cx and cy - client coordinates for the upper-left corner of the image. 
// 
// Global variables and constants 
//     g_nImage - index of the image to draw. 
//     g_rcImage - bounding rectangle of the image. 
//     CX_IMAGE and CY_IMAGE - width and height of the image. 
extern int g_nImage; 
extern RECT g_rcImage; 
 
#define CX_IMAGE 32 
#define CY_IMAGE 32 
 
BOOL DrawTheImage(HWND hwnd, HIMAGELIST himl, int cx, int cy) 
{ 
    HDC hdc; 
 
    if ((hdc = GetDC(hwnd)) == NULL) 
        return FALSE; 
    if (!ImageList_Draw(himl, g_nImage, hdc, cx, cy, ILD_TRANSPARENT)) 
        return FALSE; 
    ReleaseDC(hwnd, hdc); 
 
    SetRect(&g_rcImage, cx, cy, CX_IMAGE + cx, CY_IMAGE + cy); 
 
    return TRUE; 
} 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu Bildlisten](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Informationen zu Bildlisten](image-lists.md)
</dt> <dt>

[Verwenden von Bildlisten](using-image-lists.md)
</dt> </dl>

 

 




