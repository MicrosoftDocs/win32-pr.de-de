---
title: Windows Pixelformatcodebeispiel
description: Das folgende Codebeispiel zeigt eine Funktion, die das Pixelformat mithilfe Windows Funktionen festlegt.
ms.assetid: fa863999-72f1-4280-b278-d9336f62108d
keywords:
- Pixels OpenGL , Windows Sample
- Portieren zu OpenGL, Pixel
- OpenGL-Portierung, Pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fdd9569b6bef7dd273f6c3ff0370e2e4e44bbbbb6ec41362d1fb7dd32bd7745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932780"
---
# <a name="windows-pixel-format-code-sample"></a>Windows Pixelformatcodebeispiel

Das folgende Codebeispiel zeigt eine Funktion, die das Pixelformat mithilfe Windows Funktionen festlegt:


```C++
BOOL bSetupPixelFormat(HDC hdc) 
{ 
    PIXELFORMATDESCRIPTOR pfd, *ppfd; 
    int pixelformat; 
 
    ppfd = &pfd; 
 
    ppfd->nSize = sizeof(PIXELFORMATDESCRIPTOR); 
    ppfd->nVersion = 1; 
    ppfd->dwFlags = PFD_DRAW_TO_WINDOW | PFD_SUPPORT_OPENGL |  
                        PFD_DOUBLEBUFFER; 
    ppfd->dwLayerMask = PFD_MAIN_PLANE; 
    ppfd->iPixelType = PFD_TYPE_COLORINDEX; 
    ppfd->cColorBits = 8; 
    ppfd->cDepthBits = 16; 
    ppfd->cAccumBits = 0; 
    ppfd->cStencilBits = 0; 
 
    pixelformat = ChoosePixelFormat(hdc, ppfd); 
 
    if ( (pixelformat = ChoosePixelFormat(hdc, ppfd)) == 0 ) 
    { 
        MessageBox(NULL, "ChoosePixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    if (SetPixelFormat(hdc, pixelformat, ppfd) == FALSE) 
    { 
        MessageBox(NULL, "SetPixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    return TRUE; 
}
```



 

 




