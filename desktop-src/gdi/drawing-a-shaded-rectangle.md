---
description: Zum Zeichnen eines schattierten Rechtecks definieren Sie ein Array mit zwei Elementen und einer einzelnen Farbverlauf- \_ Rect-Struktur. Das folgende Codebeispiel veranschaulicht das Zeichnen eines schattierten Rechtecks mithilfe der GradientFill-Funktion mit dem definierten Farbverlauf- \_ \_ Rect-Modus.
ms.assetid: a4277e22-03f8-470f-87e9-5aeab258b6d2
title: Zeichnen eines schattierten Rechtecks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665e76c730ada1bd8efc9967fd10e550f0aa2e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528361"
---
# <a name="drawing-a-shaded-rectangle"></a>Zeichnen eines schattierten Rechtecks

Zum Zeichnen eines schattierten Rechtecks definieren Sie [**ein Array mit**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) zwei Elementen und einer einzelnen [**Farbverlauf- \_ Rect**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) -Struktur. Das folgende Codebeispiel veranschaulicht das Zeichnen eines schattierten Rechtecks mithilfe der [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) -Funktion mit dem definierten Farbverlauf- \_ \_ Rect-Modus.


```C++
// Create an array of TRIVERTEX structures that describe 
// positional and color values for each vertex. For a rectangle, 
// only two vertices need to be defined: upper-left and lower-right. 
TRIVERTEX vertex[2] ;
vertex[0].x     = 0;
vertex[0].y     = 0;
vertex[0].Red   = 0x0000;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x8000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 300;
vertex[1].y     = 80; 
vertex[1].Red   = 0x0000;
vertex[1].Green = 0xd000;
vertex[1].Blue  = 0xd000;
vertex[1].Alpha = 0x0000;

// Create a GRADIENT_RECT structure that 
// references the TRIVERTEX vertices. 
GRADIENT_RECT gRect;
gRect.UpperLeft  = 0;
gRect.LowerRight = 1;

// Draw a shaded rectangle. 
GradientFill(hdc, vertex, 2, &gRect, 1, GRADIENT_FILL_RECT_H);
```



Die folgende Abbildung zeigt die Zeichnungs Ausgabe des vorangehenden Code Beispiels.

![Darstellung eines Rechtecks mit einer Farbverlaufsfüllung auf der linken Seite auf der linken Seite zu "Hell" auf der rechten Seite](images/gradientfillrectangle.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Bitmaps](bitmaps.md)
</dt> <dt>

[Bitmap-Funktionen](bitmap-functions.md)
</dt> <dt>

[Zeichnen eines schattierten Dreiecks](drawing-a-shaded-triangle.md)
</dt> <dt>

[**Emrgradientfill**](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[**\_gradientenrect**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)
</dt> <dt>

[**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**"Drei"**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



