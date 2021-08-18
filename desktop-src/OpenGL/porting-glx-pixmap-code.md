---
title: Portieren von GLX Pixmap-Code
description: Portieren von GLX Pixmap-Code
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- pixmaps
- OpenGL auf Windows,Pixmaps
- Portieren zu OpenGL, Pixmaps
- OpenGL-Portierung, Pixmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e50448c254b8d3e01097f1faec2b4df8aeed56be8ae3abb4f5ce13432582559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012058"
---
# <a name="porting-glx-pixmap-code"></a>Portieren von GLX Pixmap-Code

Das X-Fenstersystem verwendet *Pixmaps,* bei denen es sich um virtuelle Zeichenoberflächen außerhalb des Bildschirms in Form eines dreidimensionalen Arrays von Bits handelt. Sie können sich eine Pixmap als Stapel von Bitmaps vorstellen: ein zweidimensionales Array von Pixeln, wobei jedes Pixel einen Wert von 0 bis 2N1 aufweist, wobei N die Tiefe der Pixmap ist.

Für OpenGL-Programme verwenden Sie die GLX-Funktionen **glXCreateGLXPixmap** und **glXDestroyGLXPixmap,** um GLX-Pixmaps zu erstellen und zu zerstören, die für das Rendering außerhalb des Bildschirms verwendet werden.

Windows verwendet geräteunabhängige Bitmaps, die die gleiche Funktion wie X Window System Pixmaps erfüllen. Verwenden Sie die standardmäßigen Windows Bitmapfunktionen, um Bitmaps zu erstellen und zu zerstören.

In der folgenden Tabelle sind die GLX-Pixmap-Funktionen und die entsprechenden Windows Bitmapfunktionen aufgeführt.



| GLX pixmap and font function (GLX-Pixmap- und Schriftartfunktion)                                                          | Windows Bitmap- und Schriftartfunktion                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GLXPixmap **glXCreateGLXPixmap**( Display *\* dpy*,XVisualInfo *\* vis*,Pixmap *pixmap*) | HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *hdc*,LPBITMAPINFOHEADER *lpbmih*,DWORD *fdwInit*,CONST BYTE *\* lpbInit*,LPBITMAPINFO *lpbmi*,UINT *fuUsage***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*,LPBITMAPINFO *lpbmi*,DWORD *fInit*,DWORD *iUsage*)<br/> |
| void **glXDestroyGLXPixmap**( Display *\* dpy*, GLXPixmap *pix*)                        | BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)( HGDIOBJ *hObject*)                                                                                                                                                                                                                                  |



 

 

