---
title: Übersetzen der GLX-Bibliothek
description: Übersetzen der GLX-Bibliothek
ms.assetid: 040fe6f1-f6ba-4dfa-b294-447efd686361
keywords:
- OpenGL auf Windows,GLX-Bibliothek
- Portieren zu OpenGL, GLX-Bibliothek
- OpenGL-Portierung, GLX-Bibliothek
- GLX-Bibliothek OpenGL
- Xlib-Funktionen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6864173cf85e0db24e77c53a7627a90e6110a1ff3ec3d94a7c85e456f98ffd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034450"
---
# <a name="translating-the-glx-library"></a>Übersetzen der GLX-Bibliothek

OpenGL X Window System-Programme verwenden die OpenGL-Erweiterung mit der BIBLIOTHEK X Window System (GLX). Die Bibliothek besteht aus einer Reihe von Funktionen und Routinen, die das Pixelformat initialisieren, das Rendering steuern und andere OpenGL-spezifische Aufgaben ausführen. Die OpenGL-Bibliothek wird mit dem X-Fenstersystem verbunden, indem Fensterhandles und Renderingkontexte verwaltet werden. Sie müssen diese Funktionen in die entsprechenden Windows Funktionen übersetzen. In der folgenden Tabelle sind die GLX-Funktionen des X-Fenstersystems und die entsprechenden Windows Funktionen aufgeführt.



| GLX/Xlib-Funktion         | Windows-Funktion                                                                                                                                       |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glXChooseVisual**       | [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                         |
| **glXCopyContext**        | Nicht zutreffend                                                                                                                                        |
| **glXCreateContext**      | [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                           |
| **glXCreateGLXPixmap**    | [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)[**CreateDIBSection**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                   |
| **glXDestroyContext**     | [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                           |
| **glXDestroyGLXPixmap**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                   |
| **glXGetConfig**          | [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                     |
| **glXGetCurrentContext**  | [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                   |
| **glXGetCurrentDrawable** | [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                             |
| **glXIsDirect**           | Nicht zutreffend                                                                                                                                        |
| **glXMakeCurrent**        | [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                               |
| **glXQueryExtension**     | [**Getversion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXQueryVersion**       | [**Getversion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXSwapBuffers**        | [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                     |
| **glXUseXFont**           | [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)                                                                                                         |
| **XGetVisualInfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                               |
| **XCreateWindow**         | [**CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) [**GetDC,**](/windows/desktop/api/winuser/nf-winuser-getdc) [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **XSync**                 | [**GdiFlush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                           |
| Nicht zutreffend           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                               |



 

Einige GLX-Funktionen verfügen nicht über eine entsprechende Windows Funktion. Um diese Funktionen in Windows zu portieren, schreiben Sie Ihren Code neu, um die gleiche Funktionalität zu erzielen. Beispielsweise verfügt **glXWaitGL** über keine entsprechende Windows Funktion, aber Sie können das gleiche Ergebnis erzielen, indem Sie alle ausstehenden OpenGL-Befehle ausführen, indem Sie [**glFinish**](glfinish.md)aufrufen.

In den folgenden Themen wird beschrieben, wie GLX-Funktionen portiert werden, die das Pixelformat festlegen, und wie Renderingkontexte, Pixmaps und Bitmaps verwaltet werden.

 

 