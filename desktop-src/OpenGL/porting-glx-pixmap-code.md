---
title: Portieren von glx-pixmap-Code
description: Portieren von glx-pixmap-Code
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- Pixmaps
- OpenGL unter Windows, Pixmaps
- Portieren auf OpenGL, Pixmaps
- OpenGL-Portierung, Pixmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0dbd7f94736f25346a9136d60feb4fa1bb6c68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039529"
---
# <a name="porting-glx-pixmap-code"></a>Portieren von glx-pixmap-Code

Das X-Fenster System verwendet *Pixmaps*, bei denen es sich um virtuelle Zeichen Flächen außerhalb des Bildschirms in Form eines dreidimensionalen Arrays von Bits handelt. Sie können sich eine pixmap als Stapel von Bitmaps vorstellen: ein zweidimensionales Array von Pixeln, wobei jedes Pixel einen Wert zwischen 0 und 2N1 hat, wobei N die Tiefe der pixmap ist.

Für OpenGL-Programme verwenden Sie die glx-Funktionen, **glxkreateglxpixmap** und **glxdestroyglxpixmap**, um die für das Offscreen-Rendering verwendeten glx-Pixmaps zu erstellen und zu zerstören.

Windows verwendet geräteunabhängige Bitmaps, die die gleiche Funktion wie X Window System-Pixmaps erfüllen. Verwenden Sie die standardmäßigen Windows-Bitmap-Funktionen zum Erstellen und zerstören von Bitmaps.

In der folgenden Tabelle sind die glx-pixmap-Funktionen und ihre entsprechenden Windows-Bitmap-Funktionen aufgelistet.



| Glx-pixmap und Font-Funktion                                                          | Windows-Bitmap und-Schriftart Funktion                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Glxpixmap **glxkreateglxpixmap**(Display *\* dpy*, xvisualinfo *\* VIS*, pixmap *pixmap*) | HBITMAP- [Editor](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) für *hdc-HDC* lpbitmapinfoheader *lpbmih*, DWORD *fdwinit*, Konstanten Byte *\* lpbinit*, lpbitmapinfo *lpbmi*, uint * fuusage ***)** HBITMAP [kreatedibsection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*, lpbitmapinfo *lpbmi*, DWORD *finit*, DWORD *IUsage*)<br/> |
| void **glxdestroyglxpixmap**(Display *\* dpy*, glxpixmap *pix*)                        | Bool [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(hgdiobj- *hobject*)                                                                                                                                                                                                                                  |



 

 

