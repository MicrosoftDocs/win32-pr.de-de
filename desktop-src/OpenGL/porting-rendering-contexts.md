---
title: Portieren von Renderingkontexten
description: Portieren von Renderingkontexten
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- Renderingkontexte OpenGL , portieren
- OpenGL auf Windows,Renderingkontexte
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

Das X-Fenstersystem und Windows durch Renderingkontexte gerendert werden. Sechs GLX-Funktionen verwalten Renderingkontexte, und fünf davon verfügen über eine Windows Funktion.

In der folgenden Tabelle sind die GLX-Renderingfunktionen und die entsprechenden Windows aufgeführt.



| GLX-Renderingkontextfunktion                                                                            | Windows Renderingkontextfunktion                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| GLXContext **glXCopyContext**( *\* Dpy* anzeigen , GLXContext *src*, GLXContext *dst*, GLuint *mask*)            | Nicht zutreffend                                                         |
| GLXContext **glXCreateContext**( *\* Dpy* anzeigen , XVisualInfo *\* gegenüber*, GLXContext *shareList*, Bool *direct*) | HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)          |
| void **glXDeleteContext**( *\* dpy* anzeigen , GLXContext *ctx*)                                              | BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)       |
| GLXContext **glXGetCurrentContext**(*void*)                                                               | HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)      |
| GLXDrawable **glXGetCurrentDrawable**(*void*)                                                             | HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)                  |
| Bool **glXMakeCurrent**( *\* Dpy* anzeigen , GLXDrawable *zeichnen*, GLXContext *ctx*)                              | BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc*, HGLRC *hglrc*) |



 

Rückgabetypen und andere Typen haben im X-Fenstersystem andere Namen als in Windows. Sie können nach Vorkommen von GLXContext suchen, um Teile des Codes zu finden, die portiert werden müssen.

In den folgenden Abschnitten werden Renderingkontext-Codebeispiele in einem X Window System-Programm mit demselben Code verglichen, nachdem dieser portiert Windows.

Weitere Informationen zu Renderingkontexten finden Sie unter [Renderingkontexte.](rendering-contexts.md)

 

 




