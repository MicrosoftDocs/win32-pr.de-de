---
title: Front, Back und andere Puffer
description: OpenGL speichert und manipuliert Pixeldaten in einem Framebuffer.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL unter Windows, Puffer
- Framebuffers OpenGL
- Farb Puffer OpenGL
- tiefen Puffer OpenGL
- Akkumulations Puffer OpenGL
- Schablonen Puffer OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388442"
---
# <a name="front-back-and-other-buffers"></a><span data-ttu-id="792ee-109">Front, Back und andere Puffer</span><span class="sxs-lookup"><span data-stu-id="792ee-109">Front, Back, and Other Buffers</span></span>

<span data-ttu-id="792ee-110">OpenGL speichert und manipuliert Pixeldaten in einem Framebuffer.</span><span class="sxs-lookup"><span data-stu-id="792ee-110">OpenGL stores and manipulates pixel data in a framebuffer.</span></span> <span data-ttu-id="792ee-111">Der Frame Puffer besteht aus einem Satz logischer Puffer: Farb-, tiefen-, Akkumulations-und Schablonen Puffer.</span><span class="sxs-lookup"><span data-stu-id="792ee-111">The framebuffer consists of a set of logical buffers: color, depth, accumulation, and stencil buffers.</span></span> <span data-ttu-id="792ee-112">Der Farb Puffer selbst besteht aus einem Satz logischer Puffer. Diese Menge kann ein Front-Left-, ein Front-Right-, ein-Links-, ein-Rechts-und eine bestimmte Anzahl von zusätzlichen Puffern enthalten.</span><span class="sxs-lookup"><span data-stu-id="792ee-112">The color buffer itself consists of a set of logical buffers; this set can include a front-left, a front-right, a back-left, a back-right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="792ee-113">In einer bestimmten Pixel Format-oder OpenGL-Implementierung werden möglicherweise nicht alle diese Puffer bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="792ee-113">A particular pixel format or OpenGL implementation may not supply all of these buffers.</span></span> <span data-ttu-id="792ee-114">Beispielsweise unterstützt die aktuelle Version der Microsoft-Implementierung von OpenGL in Windows keine Stereotyp-Bilder, sodass ein Pixel Format keine linken und rechten Farb Puffer aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="792ee-114">For example, the current version of Microsoft's implementation of OpenGL in Windows does not support stereoscopic images, so a pixel format cannot have left and right color buffers.</span></span> <span data-ttu-id="792ee-115">Außerdem werden zusätzliche Puffer von der aktuellen Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="792ee-115">In addition, the current version does not support auxiliary buffers.</span></span> <span data-ttu-id="792ee-116">Weitere Informationen zu OpenGL-Puffern und den OpenGL-Funktionen, die darauf angewendet werden, finden Sie im *OpenGL-Referenzhandbuch* und im *OpenGL-Programmier* Handbuch.</span><span class="sxs-lookup"><span data-stu-id="792ee-116">For more information on OpenGL buffers and the OpenGL functions that operate on them, see the *OpenGL Reference Manual* and the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="792ee-117">Die Microsoft-Implementierung von OpenGL in Windows unterstützt die doppelte Pufferung von Bildern.</span><span class="sxs-lookup"><span data-stu-id="792ee-117">Microsoft's implementation of OpenGL in Windows supports double buffering of images.</span></span> <span data-ttu-id="792ee-118">Dabei handelt es sich um eine Technik, bei der eine Anwendung Pixel auf einen Offscreen-Puffer zeichnet und dann, wenn dieses Bild bereit für die Anzeige ist, den Inhalt des Offscreen-Puffers in einen Bildschirm Puffer kopiert.</span><span class="sxs-lookup"><span data-stu-id="792ee-118">This is a technique in which an application draws pixels to an off-screen buffer, and then, when that image is ready for display, copies the contents of the off-screen buffer to an on-screen buffer.</span></span> <span data-ttu-id="792ee-119">Die doppelte Pufferung ermöglicht Smooth-Abbild Änderungen, die für animierte Bilder besonders wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="792ee-119">Double buffering enables smooth image changes, which are especially important for animated images.</span></span>

<span data-ttu-id="792ee-120">Für Anwendungen, die doppelte Pufferung verwenden, sind zwei Farb Puffer verfügbar: ein Front-und ein Hintergrund Puffer.</span><span class="sxs-lookup"><span data-stu-id="792ee-120">Two color buffers are available to applications that use double buffering: a front buffer and a back buffer.</span></span> <span data-ttu-id="792ee-121">Standardmäßig werden Zeichnungs Befehle an den Hintergrund Puffer (den Offscreen-Puffer) umgeleitet, während der Front-Puffer auf dem Bildschirm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="792ee-121">By default, drawing commands are directed to the back buffer (the off-screen buffer), while the front buffer is displayed on the screen.</span></span> <span data-ttu-id="792ee-122">Wenn der Offscreen-Puffer für die Anzeige bereit ist, wird " [**Swap Buffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)" aufgerufen, und Windows kopiert den Inhalt des Offscreen-Puffers in den Bildschirm Puffer.</span><span class="sxs-lookup"><span data-stu-id="792ee-122">When the off-screen buffer is ready for display, you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers), and Windows copies the contents of the off-screen buffer to the on-screen buffer.</span></span>

<span data-ttu-id="792ee-123">Die generische Implementierung verwendet eine geräteunabhängige Bitmap (DIB) als Hintergrund Puffer und die Bildschirm Anzeige als Vorder-Puffer.</span><span class="sxs-lookup"><span data-stu-id="792ee-123">The generic implementation uses a device-independent bitmap (DIB) as the back buffer and the screen display as the front buffer.</span></span> <span data-ttu-id="792ee-124">Hardware Geräte und deren Treiber können unterschiedliche Ansätze verwenden.</span><span class="sxs-lookup"><span data-stu-id="792ee-124">Hardware devices and their drivers may use different approaches.</span></span>

<span data-ttu-id="792ee-125">Die doppelte Pufferung ist eine Eigenschaft im Pixel Format.</span><span class="sxs-lookup"><span data-stu-id="792ee-125">Double buffering is a pixel-format property.</span></span> <span data-ttu-id="792ee-126">Um die doppelte Pufferung für ein Pixel Format anzufordern, legen Sie das PFD- \_ Double Buffer-Flag in der Datenstruktur " [**pixelformatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) " in einem aufzurufenden " [**choosepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)" fest.</span><span class="sxs-lookup"><span data-stu-id="792ee-126">To request double buffering for a pixel format, set the PFD\_DOUBLEBUFFER flag in the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure in a call to [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span>

<span data-ttu-id="792ee-127">Die OpenGL-Kernfunktion, [**gldrawbuffer**](gldrawbuffer.md), wählt Puffer zum Schreiben und löschen aus.</span><span class="sxs-lookup"><span data-stu-id="792ee-127">The OpenGL core function, [**glDrawBuffer**](gldrawbuffer.md), selects buffers for writing and clearing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="792ee-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="792ee-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="792ee-129">Pufferfunktionen</span><span class="sxs-lookup"><span data-stu-id="792ee-129">Buffer Functions</span></span>](buffer-functions.md)
</dt> </dl>

 

 




