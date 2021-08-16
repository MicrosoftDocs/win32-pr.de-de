---
title: Windows Beispiel für Renderingkontextcode
description: Im folgenden Codebeispiel wird veranschaulicht, wie der GLX-Renderingkontextcode im vorherigen Abschnitt aussieht, wenn er zu einem Windows.
ms.assetid: 12992faa-eb64-4a21-8015-3c73c2914189
keywords:
- Renderingkontexte
- Portieren zu OpenGL, Rendern von Kontexten
- OpenGL-Portierung, Renderingkontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9693b140083210ce0865b18463f4595c2f1fc731c8fc1d837f61342ede50b9d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794693"
---
# <a name="windows-rendering-context-code-sample"></a>Windows Beispiel für Renderingkontextcode

Im folgenden Codebeispiel wird veranschaulicht, wie der GLX-Renderingkontextcode im vorherigen Abschnitt aussieht, wenn er zu einem Windows.


```C++
HGLRC hRC;           // rendering context variable  
 
/* Create and initialize a window */ 
        
/* Window message switch in a window procedure */ 
case WM_CREATE:      // Message when window is created  
{ 
    HDC hDC, hDCTemp;    // device context handles   
 
    /* Get the handle of the windows device context. */ 
    hDC = GetDC(hWnd); 
 
    /* Create a rendering context and make it the current context */  
    hRC = wglCreateContext(hDC); 
    if (!hRC)  
    { 
        MessageBox(NULL, "Cannot create context.", "Error", MB_OK); 
        return FALSE; 
    }  
    wglMakeCurrent(hDC, hRC); 
} 
break; 
        
        .    
case WM_DESTROYED:   // Message when window is destroyed  
{ 
    HGLRC hRC        // rendering context handle  
    HDC   hDC;       // device context handle  
 
    /* Release and free the device context and rendering context. */ 
    hDC = wglGetCurrentDC; 
    hRC = wglGetCurrentContext; 
 
    wglMakeCurrent(NULL, NULL); 
 
    if (hRC) 
        wglDeleteContext(hRC); 
 
    if (hDC) 
        ReleaseDC(hWnd, hDC); 
 
    PostQuitMessage (0); 
} 
break;
```



 

 




