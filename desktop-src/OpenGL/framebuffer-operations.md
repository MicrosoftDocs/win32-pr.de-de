---
title: Framebuffer-Vorgänge
description: Verwenden Sie glDrawBuffer, um den Puffer auszuwählen, in den Farbwerte geschrieben werden.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- OpenGL-Verarbeitungspipeline, Framebuffer-Vorgänge
- framebuffers,operations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ad9d3bb04d9c063ecd9ec588843577cc577bbe62f686f136a40cdaddcbfc77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082330"
---
# <a name="framebuffer-operations"></a>Framebuffer-Vorgänge

Verwenden Sie [**glDrawBuffer,**](gldrawbuffer.md)um den Puffer auszuwählen, in den Farbwerte geschrieben werden. Sie verwenden vier verschiedene Funktionen, um das Schreiben von Bits in die einzelnen logischen Framepuffer zu maskieren, nachdem alle Vorgänge pro Fragment ausgeführt wurden:

-   [**glIndexMask**](glindexmask.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glStencilMask**](glstencilmask.md)

Die [**glAccum-Funktion**](glaccum.md) steuert den Betrieb des Akkumulationspuffers. Schließlich legt [**glClear**](glclear.md) jedes Pixel in einer angegebenen Teilmenge der Puffer auf den Mit [**glClearColor,**](glclearcolor.md) [**glClearIndex,**](glclearindex.md) [**glClearDepth,**](glcleardepth.md) [**glClearStencil**](glclearstencil.md)oder [**glClearAccum**](glclearaccum.md)angegebenen Wert fest.

 

 




