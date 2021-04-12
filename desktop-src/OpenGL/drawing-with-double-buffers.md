---
title: Zeichnen mit doppelten Puffern
description: Doppelte Puffer glätten den Übergang zwischen einem Bild und einem anderen auf dem Bildschirm.
ms.assetid: 10801cc7-d26c-4bfd-95c0-f352a1c7a1f5
keywords:
- OpenGL unter Windows, doppelte Puffer
- doppelte Puffer OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe52d427467b2a6e460ea56a9e72e580ea6f97d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311081"
---
# <a name="drawing-with-double-buffers"></a>Zeichnen mit doppelten Puffern

Doppelte Puffer glätten den Übergang zwischen einem Bild und einem anderen auf dem Bildschirm. Das Austauschen von Puffern erfolgt in der Regel am Ende einer Sequenz von Zeichnungs Befehlen. Standardmäßig zeichnet sich die Microsoft-Implementierung von OpenGL in Windows auf den Offscreen-Puffer aus. Wenn die Zeichnung vollständig ist, wird die Funktion " [**Swap-Puffer**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) " aufgerufen, um den Offscreen-Puffer in den Bildschirm Puffer zu kopieren. Im folgenden Codebeispiel wird vorbereitet, um zu zeichnen, eine Zeichnungs Funktion aufzurufen und das abgeschlossene Bild dann auf den Bildschirm zu kopieren, wenn die doppelte Pufferung verfügbar ist.


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



Im folgenden Codebeispiel wird ein Fenster Gerätekontext abgerufen, eine Szene gerendert, das Bild auf den Bildschirm kopiert (um das Rendering anzuzeigen) und dann der Gerätekontext freigegeben.


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 




