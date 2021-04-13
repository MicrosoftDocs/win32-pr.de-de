---
title: Übersetzen der glx-Bibliothek
description: Übersetzen der glx-Bibliothek
ms.assetid: 040fe6f1-f6ba-4dfa-b294-447efd686361
keywords:
- OpenGL unter Windows, glx-Bibliothek
- Portieren auf OpenGL, glx-Bibliothek
- OpenGL-Portierung, glx-Bibliothek
- Glx-Bibliothek OpenGL
- Xlib-Funktionen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cede2b74dc2881f867370744ee14c00cceba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390837"
---
# <a name="translating-the-glx-library"></a>Übersetzen der glx-Bibliothek

Die OpenGL x window-Systemprogramme verwenden die OpenGL-Erweiterung mit der x Window System (glx)-Bibliothek. Bei der Bibliothek handelt es sich um eine Reihe von Funktionen und Routinen, die das Pixel Format initialisieren, das Rendering Steuern und andere OpenGL-spezifische Tasks ausführen. Er verbindet die OpenGL-Bibliothek mit dem X-Fenster System, indem Fenster Handles und renderingkontexte verwaltet werden. Sie müssen diese Funktionen in die entsprechenden Windows-Funktionen übersetzen. In der folgenden Tabelle sind die Funktionen des X-Fenstersystems und ihre entsprechenden Windows-Funktionen aufgeführt.



| Glx/Xlib-Funktion         | Windows-Funktion                                                                                                                                       |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glxchoosevisual**       | [**Auswahl Pixel Format**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                         |
| **glxcopycontext**        | Nicht zutreffend                                                                                                                                        |
| **glxkreatecontext**      | [**wglkreatecontext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                           |
| **glxkreateglxpixmap**    | " [**Kreatedibitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)" ([**kreatedibsection** )](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                   |
| **glxdestroycontext**     | [**wgldeletecontext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                           |
| **glxdestroyglxpixmap**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                   |
| **glxgetconfig**          | [**Describepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                     |
| **glxgetcurrentcontext**  | [**wglgetcurrentcontext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                   |
| **glxgetcurrentdrawable** | [**wglgetcurrentdc**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                             |
| **glxisdirect**           | Nicht zutreffend                                                                                                                                        |
| **glxmakecurrent**        | [**wglmakecurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                               |
| **glxqueryextension**     | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glxqueryversion**       | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glxtauapbuffers**        | [**Austausch Puffer**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                     |
| **glxusexfont**           | [**wgluseefontbitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)                                                                                                         |
| **Xgetvisualinfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                               |
| **Xkreatewindow**         | " [**Kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)", "up [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa)", " [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc)", " [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) " |
| **XSync**                 | [**Gdiflush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                           |
| Nicht zutreffend           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                               |



 

Einige glx-Funktionen verfügen nicht über eine entsprechende Windows-Funktion. Um diese Funktionen auf Windows zu portieren, schreiben Sie den Code um, um die gleiche Funktionalität zu erzielen. Beispielsweise hat **glxwaitgl** keine äquivalente Windows-Funktion, aber Sie können das gleiche Ergebnis erzielen, indem Sie alle ausstehenden OpenGL-Befehle ausführen, indem Sie " [**glfinish**](glfinish.md)" aufrufen.

In den folgenden Themen wird beschrieben, wie Sie glx-Funktionen portieren, die das Pixel Format festlegen, und renderingkontexte, Pixmaps und Bitmaps verwalten.

 

 