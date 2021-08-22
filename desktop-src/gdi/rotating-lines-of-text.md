---
description: Sie können TrueType-Schriftarten in einem beliebigen Winkel drehen.
ms.assetid: 371ddb04-410a-425b-857f-ed3d4749b0f9
title: Drehen von Textzeilen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ee17428e8f3727ed2d2798bacb4a1f6e43f39dc7422db2968f359359bb3cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037638"
---
# <a name="rotating-lines-of-text"></a>Drehen von Textzeilen

Sie können TrueType-Schriftarten in einem beliebigen Winkel drehen. Dies ist hilfreich beim Beschriften von Diagrammen und anderen Abbildungen. Im folgenden Beispiel wird eine Zeichenfolge in 10-Grad-Schritten um die Mitte des Clientbereichs gedreht, indem der Wert der Elemente **lfEscapement** und **lfOrientation** der [LOGFONT-Struktur](/windows/win32/api/wingdi/ns-wingdi-logfonta) geändert wird, die zum Erstellen der Schriftart verwendet werden.


```C++
#include "strsafe.h"
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    
    case WM_PAINT:
        {
        hdc = BeginPaint(hWnd, &ps);
        RECT rc; 
        int angle; 
        HGDIOBJ hfnt, hfntPrev; 
        WCHAR lpszRotate[22] = TEXT("String to be rotated.");
        HRESULT hr; 
        size_t pcch = 22;
 
// Allocate memory for a LOGFONT structure. 
 
PLOGFONT plf = (PLOGFONT) LocalAlloc(LPTR, sizeof(LOGFONT)); 
 
 
// Specify a font typeface name and weight. 
 
hr = StringCchCopy(plf->lfFaceName, 6, TEXT("Arial"));
if (FAILED(hr))
{
// TODO: write error handler
}

plf->lfWeight = FW_NORMAL; 
 
// Retrieve the client-rectangle dimensions. 
 
GetClientRect(hWnd, &rc); 
 
// Set the background mode to transparent for the 
// text-output operation. 
 
SetBkMode(hdc, TRANSPARENT); 
 
// Draw the string 36 times, rotating 10 degrees 
// counter-clockwise each time. 
 
for (angle = 0; angle < 3600; angle += 100) 
{ 
    plf->lfEscapement = angle; 
    hfnt = CreateFontIndirect(plf); 
    hfntPrev = SelectObject(hdc, hfnt);
    
    //
    // The StringCchLength call is fitted to the lpszRotate string
    //
    hr = StringCchLength(lpszRotate, 22, &pcch);
    if (FAILED(hr))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, rc.right / 2, rc.bottom / 2, 
        lpszRotate, pcch); 
    SelectObject(hdc, hfntPrev); 
    DeleteObject(hfnt); 
} 
 
// Reset the background mode to its default. 
 
SetBkMode(hdc, OPAQUE); 
 
// Free the memory allocated for the LOGFONT structure. 
 
LocalFree((LOCALHANDLE) plf); 
        EndPaint(hWnd, &ps);
        break;
        }
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



 

 



