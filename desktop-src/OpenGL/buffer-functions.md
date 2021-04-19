---
title: Pufferfunktionen
description: Um den Inhalt eines Offscreen-Puffers in einen Bildschirm Puffer zu kopieren, nennen Sie die Anwendung "Austausch Puffer".
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- WGL-Funktionen, Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a93858b8085171a9139bc5ab329e531ddbb699
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351828"
---
# <a name="buffer-functions"></a><span data-ttu-id="045da-104">Pufferfunktionen</span><span class="sxs-lookup"><span data-stu-id="045da-104">Buffer Functions</span></span>

<span data-ttu-id="045da-105">Um den Inhalt eines Offscreen-Puffers in einen Bildschirm Puffer zu kopieren, nennen Sie die [**Anwendung "Austausch Puffer**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)".</span><span class="sxs-lookup"><span data-stu-id="045da-105">To copy the contents of an off-screen buffer to an on-screen buffer, call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="045da-106">Die Funktion " **Swap-Puffer** " übernimmt ein Handle für einen Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="045da-106">The **SwapBuffers** function takes a handle to a device context.</span></span> <span data-ttu-id="045da-107">Das aktuelle Pixel Format für den angegebenen Gerätekontext muss einen Hintergrund Puffer enthalten.</span><span class="sxs-lookup"><span data-stu-id="045da-107">The current pixel format for the specified device context must include a back buffer.</span></span> <span data-ttu-id="045da-108">Standardmäßig ist der Hintergrund Puffer außerhalb des Bildschirms, und der vordere Puffer ist auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="045da-108">By default, the back buffer is off-screen, and the front buffer is on-screen.</span></span>

> [!Note]  
> <span data-ttu-id="045da-109">Die **swapbuffers** -Funktion tauscht nicht wirklich den Inhalt der beiden Puffer aus, sondern kopiert den Inhalt eines Puffers in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="045da-109">The **SwapBuffers** function does not really swap the contents of the two buffers, but rather copies the contents of one buffer to another.</span></span> <span data-ttu-id="045da-110">Der Inhalt des Offscreen-Puffers ist nach einem **callapbuffers-Austausch** nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="045da-110">The contents of the off-screen buffer are undefined after a call to **SwapBuffers**.</span></span> <span data-ttu-id="045da-111">Folglich ist das Ergebnis von zwei aufeinander folgenden Aufrufen von " **Austausch Puffer** " nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="045da-111">Thus, the result of two consecutive calls to **SwapBuffers** is undefined.</span></span>

 

<span data-ttu-id="045da-112">In der folgenden Abbildung wird gezeigt, wie die Inhalte der Puffer beim Aufrufen von " **Austausch Puffern**" kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="045da-112">The following illustration shows how the contents of the buffers are copied when calling **SwapBuffers**.</span></span>

![Das Diagramm zeigt die nicht definierten Ergebnisse von aufeinander folgenden Aufrufen der Funktion "Swap" an.](images/opengl00.png)

<span data-ttu-id="045da-114">Mehrere OpenGL Core-Funktionen verwalten auch Puffer.</span><span class="sxs-lookup"><span data-stu-id="045da-114">Several OpenGL core functions also manage buffers.</span></span> <span data-ttu-id="045da-115">Die [**gldrawbuffer**](gldrawbuffer.md) -Funktion ist die für die doppelte Pufferung relevanteste. Sie gibt die Frame Puffer oder Puffer an, die OpenGL in zeichnet.</span><span class="sxs-lookup"><span data-stu-id="045da-115">The [**glDrawBuffer**](gldrawbuffer.md) function is the one most relevant to double buffering; it specifies the framebuffer or buffers that OpenGL draws into.</span></span>

<span data-ttu-id="045da-116">Die folgenden Funktionen wirken sich auch auf Puffer aus:</span><span class="sxs-lookup"><span data-stu-id="045da-116">The following functions also affect buffers:</span></span>

-   [<span data-ttu-id="045da-117">**glread Buffer**</span><span class="sxs-lookup"><span data-stu-id="045da-117">**glReadBuffer**</span></span>](glreadbuffer.md)
-   [<span data-ttu-id="045da-118">**glread Pixels**</span><span class="sxs-lookup"><span data-stu-id="045da-118">**glReadPixels**</span></span>](glreadpixels.md)
-   [<span data-ttu-id="045da-119">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="045da-119">**glCopyPixels**</span></span>](glcopypixels.md)
-   [<span data-ttu-id="045da-120">**glaccum**</span><span class="sxs-lookup"><span data-stu-id="045da-120">**glAccum**</span></span>](glaccum.md)
-   [<span data-ttu-id="045da-121">**glcolormask**</span><span class="sxs-lookup"><span data-stu-id="045da-121">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="045da-122">**gldepthmask**</span><span class="sxs-lookup"><span data-stu-id="045da-122">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="045da-123">**glindexmask**</span><span class="sxs-lookup"><span data-stu-id="045da-123">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="045da-124">**glstencilmask**</span><span class="sxs-lookup"><span data-stu-id="045da-124">**glStencilMask**</span></span>](glstencilmask.md)
-   [<span data-ttu-id="045da-125">**glclearaccum**</span><span class="sxs-lookup"><span data-stu-id="045da-125">**glClearAccum**</span></span>](glclearaccum.md)
-   [<span data-ttu-id="045da-126">**glclearcolor**</span><span class="sxs-lookup"><span data-stu-id="045da-126">**glClearColor**</span></span>](glclearcolor.md)
-   [<span data-ttu-id="045da-127">**glcleartiefe**</span><span class="sxs-lookup"><span data-stu-id="045da-127">**glClearDepth**</span></span>](glcleardepth.md)
-   [<span data-ttu-id="045da-128">**glclearindex**</span><span class="sxs-lookup"><span data-stu-id="045da-128">**glClearIndex**</span></span>](glclearindex.md)
-   [<span data-ttu-id="045da-129">**glclearstencil**</span><span class="sxs-lookup"><span data-stu-id="045da-129">**glClearStencil**</span></span>](glclearstencil.md)

 

 




