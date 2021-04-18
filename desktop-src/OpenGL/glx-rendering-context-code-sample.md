---
title: Kontext Code Beispiel für glx-Rendering
description: Das folgende Codebeispiel zeigt, wie ein X-Window-System-OpenGL-Programm glx-renderingkontextfunktionen verwendet
ms.assetid: 6cee5e5f-ee2f-4fe4-a988-402802e4a1b8
keywords:
- renderingkontexte
- Portieren auf OpenGL, renderingkontexte
- OpenGL-portieren, Rendern von Kontexten
- X-Fenster System, renderingkontexte
- Glx-Funktionen, renderingkontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03259cb9b540db3076a0baa4122906e5aeb3e8f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339385"
---
# <a name="glx-rendering-context-code-sample"></a><span data-ttu-id="52914-108">Kontext Code Beispiel für glx-Rendering</span><span class="sxs-lookup"><span data-stu-id="52914-108">GLX Rendering Context Code Sample</span></span>

<span data-ttu-id="52914-109">Das folgende Codebeispiel zeigt, wie ein X-Window-System-OpenGL-Programm glx-renderingkontextfunktionen verwendet</span><span class="sxs-lookup"><span data-stu-id="52914-109">The following code sample shows how an X Window System OpenGL program uses GLX rendering context functions.</span></span>


```C++
Display *dpy;             /* display variable */ 
XVisualInfo *vi;          /* visual variable */ 
Window win;               /* window variable */ 
GLXDrawable drawable;     /* drawable variable */ 
GLXContext cx, cxTemp;    /* rendering context variables */ 
 
/* Code to open a display and get a visual. */ 
        
/* Create a GLX context. */ 
cx = glXCreateContext(dpy, vi, 0, GL_FALSE); 
if (!cx) { 
    fprintf(stderr, "Cannot create context.\n"); 
    exit(-1); 
} 
        
        .    
/* Connect the context to the window. */ 
glXMakeCurrent(dpy, win, cx); 
        
        .    
/* When it's time to destroy the rendering context. . . */ 
cx = glXGetCurrentContext; 
glXDestroyContext(dpy, cx);
```



 

 




