---
title: Portieren von Renderingkontexten
description: Portieren von Renderingkontexten
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- Renderingkontexte OpenGL, Portieren
- OpenGL für Windows,Renderingkontexte
- Portieren zu OpenGL, Rendern von Kontexten
- OpenGL-Portierung, Renderingkontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4fcb6a70f6858ac9c11258c681345ee88a8807c91230f8d3d35fc579ab3371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358340"
---
# <a name="porting-rendering-contexts"></a>Portieren von Renderingkontexten

Das X-Fenstersystem und Windows über Renderingkontexte gerendert. Sechs GLX-Funktionen verwalten Renderingkontexte, und fünf davon verfügen über eine entsprechende Windows Funktion.

In der folgenden Tabelle sind die GLX-Renderingfunktionen und die entsprechenden Windows Funktionen aufgeführt.



| GLX-Renderingkontextfunktion                                                                            | Windows Renderingkontextfunktion                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| GLXContext **glXCopyContext**( Display *\* dpy*, GLXContext *src*, GLXContext *dst*, GLuint *mask*)            | Nicht zutreffend                                                         |
| GLXContext **glXCreateContext**( Anzeigen *\* von dpy*, XVisualInfo *\* vis*,GLXContext *shareList*, Bool *direct*) | HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)          |
| void **glXDeleteContext**( Display *\* dpy*,GLXContext *ctx*)                                              | BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)       |
| GLXContext **glXGetCurrentContext**(*void*)                                                               | HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)      |
| GLXDrawable **glXGetCurrentDrawable**(*void*)                                                             | HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)                  |
| Bool **glXMakeCurrent**( Display *\* dpy*, GLXDrawable *draw*, GLXContext *ctx*)                              | BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc*, HGLRC *hglrc*) |



 

Rückgabetypen und andere Typen haben im X-Fenstersystem andere Namen als in Windows. Sie können nach Vorkommen von GLXContext suchen, um Teile Ihres Codes zu finden, die portiert werden müssen.

In den folgenden Abschnitten werden Codebeispiele für den Renderingkontext in einem X-Fenstersystemprogramm mit dem gleichen Code verglichen, nachdem er zu Windows portiert wurde.

Weitere Informationen zu Renderingkontexten finden Sie unter [Renderingkontexte.](rendering-contexts.md)

 

 




