---
title: Framebuffer-Vorgänge
description: Verwenden Sie zum Auswählen des Puffers, in den Farbwerte geschrieben werden, gldrawbuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- OpenGL-Verarbeitungs Pipeline, Framebuffer-Vorgänge
- Framebuffers, Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515597"
---
# <a name="framebuffer-operations"></a><span data-ttu-id="6919c-105">Framebuffer-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="6919c-105">Framebuffer Operations</span></span>

<span data-ttu-id="6919c-106">Verwenden Sie zum Auswählen des Puffers, in den Farbwerte geschrieben werden, [**gldrawbuffer**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="6919c-106">To select the buffer into which color values are written, use [**glDrawBuffer**](gldrawbuffer.md).</span></span> <span data-ttu-id="6919c-107">Sie verwenden vier verschiedene Funktionen, um das Schreiben von Bits für jeden logischen Framebuffer zu maskieren, nachdem alle Vorgänge pro Fragment ausgeführt wurden:</span><span class="sxs-lookup"><span data-stu-id="6919c-107">You use four different functions to mask the writing of bits to each of the logical framebuffers after all per-fragment operations have been performed:</span></span>

-   [<span data-ttu-id="6919c-108">**glindexmask**</span><span class="sxs-lookup"><span data-stu-id="6919c-108">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="6919c-109">**glcolormask**</span><span class="sxs-lookup"><span data-stu-id="6919c-109">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="6919c-110">**gldepthmask**</span><span class="sxs-lookup"><span data-stu-id="6919c-110">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="6919c-111">**glstencilmask**</span><span class="sxs-lookup"><span data-stu-id="6919c-111">**glStencilMask**</span></span>](glstencilmask.md)

<span data-ttu-id="6919c-112">Die Funktion " [**glaccum**](glaccum.md) " steuert den Vorgang des Akkumulations Puffers.</span><span class="sxs-lookup"><span data-stu-id="6919c-112">The [**glAccum**](glaccum.md) function controls the operation of the accumulation buffer.</span></span> <span data-ttu-id="6919c-113">Schließlich legt [**glClear**](glclear.md) jedes Pixel in einer angegebenen Teilmenge der Puffer auf den Wert fest, der mit " [**glclearcolor**](glclearcolor.md)", " [**glclearindex**](glclearindex.md)", " [**glcleartiefe**](glcleardepth.md)", " [**glclearstencil**](glclearstencil.md)" oder " [**glclearaccum**](glclearaccum.md)" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6919c-113">Finally, [**glClear**](glclear.md) sets every pixel in a specified subset of the buffers to the value specified with [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), or [**glClearAccum**](glclearaccum.md).</span></span>

 

 




