---
description: Um ein schattiertes Dreieck zu zeichnen, definieren Sie eine TRIVERTEX-Struktur mit drei Elementen und einer einzelnen GRADIENT \_ TRIANGLE-Struktur.
ms.assetid: 78834f92-00cb-4899-851a-1de5e3c1f4fa
title: Zeichnen eines schattierten Dreiecks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1b6742f8ff6a3e2d543592e86cac87489048ca4d9748dc4e111cd4613b2f207
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062410"
---
# <a name="drawing-a-shaded-triangle"></a>Zeichnen eines schattierten Dreiecks

Um ein schattiertes Dreieck zu zeichnen, definieren Sie eine [**TRIVERTEX-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) mit drei Elementen und einer einzelnen [**GRADIENT \_ TRIANGLE-Struktur.**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) Das folgende Codebeispiel zeigt, wie sie ein schattiertes Dreieck mithilfe der [**GradientFill-Funktion**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) zeichnen, für die der GRADIENT \_ FILL \_ TRIANGLE-Modus definiert ist.


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_PAINT:
        {hdc = BeginPaint(hWnd, &ps);
// Create an array of TRIVERTEX structures that describe
// positional and color values for each vertex.
TRIVERTEX vertex[3];
vertex[0].x     = 150;
vertex[0].y     = 0;
vertex[0].Red   = 0xff00;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x0000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 0;
vertex[1].y     = 150;
vertex[1].Red   = 0x9000;
vertex[1].Green = 0x0000;
vertex[1].Blue  = 0x9000;
vertex[1].Alpha = 0x0000;

vertex[2].x     = 300;
vertex[2].y     = 150; 
vertex[2].Red   = 0x9000;
vertex[2].Green = 0x0000;
vertex[2].Blue  = 0x9000;
vertex[2].Alpha = 0x0000;

// Create a GRADIENT_TRIANGLE structure that
// references the TRIVERTEX vertices.
GRADIENT_TRIANGLE gTriangle;
gTriangle.Vertex1 = 0;
gTriangle.Vertex2 = 1;
gTriangle.Vertex3 = 2;

// Draw a shaded triangle.
GradientFill(hdc, vertex, 3, &gTriangle, 1, GRADIENT_FILL_TRIANGLE);
        EndPaint(hWnd, &ps);
        break;}
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



Die folgende Abbildung zeigt die Zeichnungsausgabe des vorherigen Codebeispiels.

![Abbildung eines Dreiecks, das sich von orange am oberen Punkt bis zum Magenta am unteren Rand ausfüllt](images/gradientfilltriangle.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Bitmaps](bitmaps.md)
</dt> <dt>

[Bitmapfunktionen](bitmap-functions.md)
</dt> <dt>

[Zeichnen eines schattierten Rechtecks](drawing-a-shaded-rectangle.md)
</dt> <dt>

[**EMRGRADIENTFILL**](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[**\_FARBVERLAUFSDREIECK**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)
</dt> <dt>

[**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



