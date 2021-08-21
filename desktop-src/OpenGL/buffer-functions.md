---
title: Pufferfunktionen
description: Um den Inhalt eines Off-Screen-Puffers in einen Bildschirmpuffer zu kopieren, rufen Sie SwapBuffers auf.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- WGL-Funktionen, Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b03a12cd07b76d1329f51cc982508c707e011701b072a42b099df05327842d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618595"
---
# <a name="buffer-functions"></a>Pufferfunktionen

Um den Inhalt eines Off-Screen-Puffers in einen Bildschirmpuffer zu kopieren, rufen Sie [**SwapBuffers auf.**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) Die **SwapBuffers-Funktion** verwendet ein Handle für einen Gerätekontext. Das aktuelle Pixelformat für den angegebenen Gerätekontext muss einen Hintergrundpuffer enthalten. Standardmäßig befindet sich der Hintergrundpuffer außerhalb des Bildschirms und der Frontpuffer auf dem Bildschirm.

> [!Note]  
> Die **SwapBuffers-Funktion tauscht** den Inhalt der beiden Puffer nicht wirklich aus, sondern kopiert den Inhalt eines Puffers in einen anderen. Der Inhalt des Off-Screen-Puffers ist nach einem Aufruf von **SwapBuffers** nicht definiert. Daher ist das Ergebnis von zwei aufeinanderfolgenden Aufrufen von **SwapBuffers** nicht definiert.

 

Die folgende Abbildung zeigt, wie der Inhalt der Puffer beim Aufrufen von **SwapBuffers** kopiert wird.

![Diagramm der nicht definierten Ergebnisse aufeinanderfolgender Aufrufe der SwapBuffers-Funktion.](images/opengl00.png)

Mehrere OpenGL-Kernfunktionen verwalten auch Puffer. Die [**glDrawBuffer-Funktion**](gldrawbuffer.md) ist die funktion, die für die doppelte Pufferung am relevantesten ist. gibt den Framepuffer oder die Puffer an, in die OpenGL zeichnet.

Die folgenden Funktionen wirken sich auch auf Puffer aus:

-   [**glReadBuffer**](glreadbuffer.md)
-   [**glReadPixels**](glreadpixels.md)
-   [**glCopyPixels**](glcopypixels.md)
-   [**glAccum**](glaccum.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glIndexMask**](glindexmask.md)
-   [**glStencilMask**](glstencilmask.md)
-   [**glClearAccum**](glclearaccum.md)
-   [**glClearColor**](glclearcolor.md)
-   [**glClearDepth**](glcleardepth.md)
-   [**glClearIndex**](glclearindex.md)
-   [**glClearStencil**](glclearstencil.md)

 

 




