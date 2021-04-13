---
title: Portieren von renderingkontexten
description: Portieren von renderingkontexten
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- Rendern von Kontexten OpenGL, portieren
- OpenGL unter Windows, renderingkontexte
- Portieren auf OpenGL, renderingkontexte
- OpenGL-portieren, Rendern von Kontexten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388481"
---
# <a name="porting-rendering-contexts"></a>Portieren von renderingkontexten

Das X-Fenster System und Windows Rendern durch renderingkontexte. Sechs glx-Funktionen verwalten renderingkontexte und fünf davon verfügen über eine entsprechende Windows-Funktion.

In der folgenden Tabelle sind die glx-Renderingfunktionen und ihre entsprechenden Windows-Funktionen aufgeführt.



| Glx-Rendering-Kontextfunktion                                                                            | Windows-Rendering-Kontextfunktion                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Glxcontext **glxcopycontext**(Display *\* dpy*, glxcontext *src*, glxcontext *DST*, gluint *Mask*)            | Nicht zutreffend                                                         |
| Glxcontext **glxkreatecontext**(Display *\* dpy*, xvisualinfo *\* VIS*, glxcontext *sharelist*, bool *Direct*) | Hglrc [**wglkreatecontext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)(HDC *hdc*)          |
| void **glxdeletecontext**(Anzeigen von *\* dpy*, glxcontext *ctx*)                                              | Bool [**wgldeletecontext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)(hglrc *hglrc*)       |
| Glxcontext **glxgetcurrentcontext**(*void*)                                                               | Hglrc [**wglgetcurrentcontext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*void*)      |
| Glxdrawable **glxgetcurrentdrawable**(*void*)                                                             | HDC [**wglgetcurrentdc**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*void*)                  |
| Bool **glxmakecurrent**(Anzeigen von *\* dpy*, glxdrawable *Draw*, glxcontext *ctx*)                              | Bool [**wglmakecurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)(HDC *hdc*, hglrc *hglrc*) |



 

Rückgabe Typen und andere Typen haben unterschiedliche Namen im X-Fenster System als in Windows. Sie können nach Vorkommen von glxcontext suchen, um Teile des Codes zu finden, die portiert werden müssen.

In den folgenden Abschnitten werden die Codebeispiele für das Rendern von Kontext in einem X Window-System Programm und der gleiche Code verglichen, nachdem er zu Windows portiert wurde.

Weitere Informationen zum Rendern von Kontexten finden Sie unter [Rendern von Kontexten](rendering-contexts.md).

 

 




