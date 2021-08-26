---
title: GLX-Renderingkontextcodebeispiel
description: Das folgende Codebeispiel zeigt, wie ein X Window System OpenGL-Programm GLX-Renderingkontextfunktionen verwendet.
ms.assetid: 6cee5e5f-ee2f-4fe4-a988-402802e4a1b8
keywords:
- Renderingkontexte
- Portieren zu OpenGL, Rendern von Kontexten
- OpenGL-Portierung, Renderingkontexte
- X-Fenstersystem, Renderingkontexte
- GLX-Funktionen, Renderingkontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c15ef1c1e1eddba86da56f8036adfa0724d8c997ba5f4c262f3d14446e86441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035270"
---
# <a name="glx-rendering-context-code-sample"></a>GLX-Renderingkontextcodebeispiel

Das folgende Codebeispiel zeigt, wie ein X Window System OpenGL-Programm GLX-Renderingkontextfunktionen verwendet.


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



 

 




