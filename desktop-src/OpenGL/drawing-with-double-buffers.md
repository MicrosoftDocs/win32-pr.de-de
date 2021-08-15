---
title: Zeichnen mit doppelten Puffern
description: Doppelte Puffer glätten den Übergang zwischen einem Bild und einem anderen auf dem Bildschirm.
ms.assetid: 10801cc7-d26c-4bfd-95c0-f352a1c7a1f5
keywords:
- OpenGL auf Windows,double-Puffern
- double buffers OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133a6e0794eb903215411016aeff14e3426854dcddc3a60bcfb2ba318481bee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361390"
---
# <a name="drawing-with-double-buffers"></a>Zeichnen mit doppelten Puffern

Doppelte Puffer glätten den Übergang zwischen einem Bild und einem anderen auf dem Bildschirm. Austauschpuffer werden in der Regel am Ende einer Sequenz von Zeichnungsbefehlen angezeigt. Standardmäßig wird die Microsoft-Implementierung von OpenGL in Windows in den Off-Screen-Puffer gelost. Wenn das Zeichnen abgeschlossen ist, rufen Sie die [**SwapBuffers-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) auf, um den Off-Screen-Puffer in den Bildschirmpuffer zu kopieren. Das folgende Codebeispiel bereitet das Zeichnen vor, ruft eine Zeichnungsfunktion auf und kopiert dann das fertige Bild auf den Bildschirm, wenn doppelte Pufferung verfügbar ist.


```C++
void myRedraw(void) 
{ 
    // set up for drawing commands  
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective(45, 1.0, 0.1, 100.0); 
 
    // draw our objects  
    myDrawAllObjects(GL_FALSE); 
 
    // if we're double-buffering ...  
    if (bDoubleBuffering)  
 
        // ...draw the copied image to the screen  
        SwapBuffers(hdc); 
}
```



Das folgende Codebeispiel erhält einen Fenstergerätekontext, rendert eine Szene, kopiert das Bild auf den Bildschirm (um das Rendering anzuzeigen) und gibt dann den Gerätekontext frei.


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 




