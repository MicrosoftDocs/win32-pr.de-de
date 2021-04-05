---
title: Code Beispiel für das glx-Pixel Format
description: Das folgende Codebeispiel zeigt, wie ein X-Window-System-OpenGL-Programmfunktionen für die visuelle und Pixel Formatierung von glx verwendet.
ms.assetid: f01193a9-c0ff-4399-a86e-06bb4603b3f1
keywords:
- Portieren auf OpenGL, Pixel
- OpenGL-portieren, Pixel
- X-Fenster System, Pixel
- Glx-Funktionen, Pixel
- Pixel, glx-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0ab6464d54e696c136a6c987b94124f52b0ee2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707817"
---
# <a name="glx-pixel-format-code-sample"></a>Code Beispiel für das glx-Pixel Format

Das folgende Codebeispiel zeigt, wie ein X-Window-System-OpenGL-Programmfunktionen für die visuelle und Pixel Formatierung von glx verwendet.


```C++
/* X globals, defines, and prototypes */ 
Display *dpy; 
Window glwin; 
static int attributes[] = {GLX_DEPTH_SIZE, 16, GLX_DOUBLEBUFFER, None}; 
        
    /* find an OpenGL-capable Color Index visual with depth buffer */ 
    vi = glXChooseVisual(dpy, DefaultScreen(dpy), attributes); 
    if (vi == NULL) { 
        fprintf(stderr, "could not get visual\n"); 
        exit(1); 
    }
```



Das visuelle Element kann verwendet werden, um ein Fenster und einen renderingkontext zu erstellen.

 

 




