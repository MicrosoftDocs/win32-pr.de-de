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
# <a name="porting-rendering-contexts"></a><span data-ttu-id="1d30f-107">Portieren von renderingkontexten</span><span class="sxs-lookup"><span data-stu-id="1d30f-107">Porting Rendering Contexts</span></span>

<span data-ttu-id="1d30f-108">Das X-Fenster System und Windows Rendern durch renderingkontexte.</span><span class="sxs-lookup"><span data-stu-id="1d30f-108">The X Window System and Windows render through rendering contexts.</span></span> <span data-ttu-id="1d30f-109">Sechs glx-Funktionen verwalten renderingkontexte und fünf davon verfügen über eine entsprechende Windows-Funktion.</span><span class="sxs-lookup"><span data-stu-id="1d30f-109">Six GLX functions manage rendering contexts and five of them have an equivalent Windows function.</span></span>

<span data-ttu-id="1d30f-110">In der folgenden Tabelle sind die glx-Renderingfunktionen und ihre entsprechenden Windows-Funktionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d30f-110">The following table lists the GLX rendering functions and their equivalent Windows functions.</span></span>



| <span data-ttu-id="1d30f-111">Glx-Rendering-Kontextfunktion</span><span class="sxs-lookup"><span data-stu-id="1d30f-111">GLX rendering context function</span></span>                                                                            | <span data-ttu-id="1d30f-112">Windows-Rendering-Kontextfunktion</span><span class="sxs-lookup"><span data-stu-id="1d30f-112">Windows rendering context function</span></span>                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="1d30f-113">Glxcontext **glxcopycontext**(Display *\* dpy*, glxcontext *src*, glxcontext *DST*, gluint *Mask*)</span><span class="sxs-lookup"><span data-stu-id="1d30f-113">GLXContext **glXCopyContext**( Display *\*dpy*,GLXContext *src*,GLXContext *dst*,GLuint *mask*)</span></span>            | <span data-ttu-id="1d30f-114">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="1d30f-114">Not applicable.</span></span>                                                         |
| <span data-ttu-id="1d30f-115">Glxcontext **glxkreatecontext**(Display *\* dpy*, xvisualinfo *\* VIS*, glxcontext *sharelist*, bool *Direct*)</span><span class="sxs-lookup"><span data-stu-id="1d30f-115">GLXContext **glXCreateContext**( Display *\*dpy*,XVisualInfo *\*vis*,GLXContext *shareList*,Bool *direct*)</span></span> | <span data-ttu-id="1d30f-116">Hglrc [**wglkreatecontext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)(HDC *hdc*)</span><span class="sxs-lookup"><span data-stu-id="1d30f-116">HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)</span></span>          |
| <span data-ttu-id="1d30f-117">void **glxdeletecontext**(Anzeigen von *\* dpy*, glxcontext *ctx*)</span><span class="sxs-lookup"><span data-stu-id="1d30f-117">void **glXDeleteContext**( Display *\*dpy*,GLXContext *ctx*)</span></span>                                              | <span data-ttu-id="1d30f-118">Bool [**wgldeletecontext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)(hglrc *hglrc*)</span><span class="sxs-lookup"><span data-stu-id="1d30f-118">BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)</span></span>       |
| <span data-ttu-id="1d30f-119">Glxcontext **glxgetcurrentcontext**(*void*)</span><span class="sxs-lookup"><span data-stu-id="1d30f-119">GLXContext **glXGetCurrentContext**(*void*)</span></span>                                                               | <span data-ttu-id="1d30f-120">Hglrc [**wglgetcurrentcontext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*void*)</span><span class="sxs-lookup"><span data-stu-id="1d30f-120">HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)</span></span>      |
| <span data-ttu-id="1d30f-121">Glxdrawable **glxgetcurrentdrawable**(*void*)</span><span class="sxs-lookup"><span data-stu-id="1d30f-121">GLXDrawable **glXGetCurrentDrawable**(*void*)</span></span>                                                             | <span data-ttu-id="1d30f-122">HDC [**wglgetcurrentdc**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*void*)</span><span class="sxs-lookup"><span data-stu-id="1d30f-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)</span></span>                  |
| <span data-ttu-id="1d30f-123">Bool **glxmakecurrent**(Anzeigen von *\* dpy*, glxdrawable *Draw*, glxcontext *ctx*)</span><span class="sxs-lookup"><span data-stu-id="1d30f-123">Bool **glXMakeCurrent**( Display *\*dpy*,GLXDrawable *draw*,GLXContext *ctx*)</span></span>                              | <span data-ttu-id="1d30f-124">Bool [**wglmakecurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)(HDC *hdc*, hglrc *hglrc*)</span><span class="sxs-lookup"><span data-stu-id="1d30f-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc*,HGLRC *hglrc*)</span></span> |



 

<span data-ttu-id="1d30f-125">Rückgabe Typen und andere Typen haben unterschiedliche Namen im X-Fenster System als in Windows.</span><span class="sxs-lookup"><span data-stu-id="1d30f-125">Return types and other types have different names in the X Window System than in Windows.</span></span> <span data-ttu-id="1d30f-126">Sie können nach Vorkommen von glxcontext suchen, um Teile des Codes zu finden, die portiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1d30f-126">You can search for occurrences of GLXContext to help find parts of your code that need to be ported.</span></span>

<span data-ttu-id="1d30f-127">In den folgenden Abschnitten werden die Codebeispiele für das Rendern von Kontext in einem X Window-System Programm und der gleiche Code verglichen, nachdem er zu Windows portiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1d30f-127">The following sections compare rendering context code samples in an X Window System program and the same code after it has been ported to Windows.</span></span>

<span data-ttu-id="1d30f-128">Weitere Informationen zum Rendern von Kontexten finden Sie unter [Rendern von Kontexten](rendering-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="1d30f-128">For more information on rendering contexts, see [Rendering Contexts](rendering-contexts.md).</span></span>

 

 




