---
title: Glx und WGL/Windows
description: Einige der WGL-Funktionen und Windows-Funktionen sind mehr oder weniger analog zu den Funktionen von glx X-Fenstern. Die folgende Liste zeigt die glx-Funktionen und die zugehörigen WGL-/Windows-Funktionen, falls verfügbar.
ms.assetid: 428c0fdc-a541-4720-908f-99f0539d9f4b
keywords:
- OpenGL unter Windows, glx-Funktionen
- Glx-Funktionen OpenGL
- WGL-Funktionen im Vergleich zu glx-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaa2c0ce28bd22e8b6efee4edc395223be2bf11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728881"
---
# <a name="glx-and-wglwindows"></a>Glx und WGL/Windows

Einige der WGL-Funktionen und Windows-Funktionen sind mehr oder weniger analog zu den Funktionen von glx X-Fenstern. Die folgende Liste zeigt die glx-Funktionen und die zugehörigen WGL-/Windows-Funktionen, falls verfügbar.



| Glx-Funktionen             | WGL/Windows-Funktionen                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glxchoosevisual**       | [**Auswahl Pixel Format**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                              |
| **glxcopycontext**        |                                                                                                                                                             |
| **glxkreatecontext**      | [**wglkreatecontext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                                |
| **glxkreateglxpixmap**    | " [**Kreatedibitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)  /  " " [ **Kreatedibsection** "](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                     |
| **glxdestroycontext**     | [**wgldeletecontext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                                |
| **glxdestroyglxpixmap**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                        |
| **glxgetconfig**          | [**Describepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                          |
| **glxgetcurrentcontext**  | [**wglgetcurrentcontext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                        |
| **glxgetcurrentdrawable** | [**wglgetcurrentdc**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                                  |
| **glxisdirect**           |                                                                                                                                                             |
| **glxmakecurrent**        | [**wglmakecurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                                    |
| **glxqueryextension**     | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                           |
| **glxqueryversion**       | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                           |
| **glxtauapbuffers**        | [**Austausch Puffer**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                          |
| **glxusexfont**           | [**wgluseefontbitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)  /  [ **wgluseelfontgliederungen**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa)                                                           |
| **glxwaitgl**             |                                                                                                                                                             |
| **glxwaitx**              |                                                                                                                                                             |
| **Xgetvisualinfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                                    |
| **Xkreatewindow**         | " [**Kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)  /  " " [**Kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " und " [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc)  /  [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) " |
| **XSync**                 | [**Gdiflush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                                |
|                           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                                    |
|                           | [**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)                                                                                                              |
|                           | [**wglsharelists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists)                                                                                                                      |



 

Weitere Informationen finden Sie im Leitfaden zum *portieren*.

 

 