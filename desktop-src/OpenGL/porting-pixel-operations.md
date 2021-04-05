---
title: Portieren von Pixel Vorgängen
description: Portieren von Pixel Vorgängen
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- IRIS GL Porting, Pixel
- Portieren von IRIS GL, Pixel
- Portieren auf OpenGL von IRIS GL, Pixel
- OpenGL-Portierung von IRIS GL, Pixel
- Pixel, Portieren von IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712509"
---
# <a name="porting-pixel-operations"></a><span data-ttu-id="dae92-108">Portieren von Pixel Vorgängen</span><span class="sxs-lookup"><span data-stu-id="dae92-108">Porting Pixel Operations</span></span>

<span data-ttu-id="dae92-109">Beachten Sie beim Portieren von Code, der Pixel Vorgänge umfasst, die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="dae92-109">When porting code that involves pixel operations, keep the following points in mind:</span></span>

-   <span data-ttu-id="dae92-110">Logische Pixel Vorgänge werden nicht auf RGBA-Farb Puffer angewendet.</span><span class="sxs-lookup"><span data-stu-id="dae92-110">Logical pixel operations are not applied to RGBA color buffers.</span></span> <span data-ttu-id="dae92-111">Weitere Informationen finden Sie unter [**gllogicop**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="dae92-111">For more information, see [**glLogicOp**](gllogicop.md).</span></span>
-   <span data-ttu-id="dae92-112">Im Allgemeinen verwendet IRIS GL das Format ABGR für Pixel, während OpenGL RGBA verwendet.</span><span class="sxs-lookup"><span data-stu-id="dae92-112">In general, IRIS GL uses the format ABGR for pixels, whereas OpenGL uses RGBA.</span></span> <span data-ttu-id="dae92-113">Sie können das Format mit [**glpixelstore**](glpixelstore-functions.md)ändern.</span><span class="sxs-lookup"><span data-stu-id="dae92-113">You can change the format with [**glPixelStore**](glpixelstore-functions.md).</span></span>
-   <span data-ttu-id="dae92-114">Beachten Sie bei der Portierung von **lrectwrite** -Funktionen, dass **lrectwrite** schreibt (z. b. könnte es in den tiefen Puffer schreiben).</span><span class="sxs-lookup"><span data-stu-id="dae92-114">When porting **lrectwrite** functions, be careful to note where **lrectwrite** is writing (for example, it could be writing to the depth buffer).</span></span>

<span data-ttu-id="dae92-115">OpenGL bietet Ihnen zusätzliche Flexibilität bei Pixel Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="dae92-115">OpenGL gives you some additional flexibility in pixel operations.</span></span> <span data-ttu-id="dae92-116">In der folgenden Tabelle werden die Iris GL-Funktionen für Pixel Vorgänge und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dae92-116">The following table lists IRIS GL functions for pixel operations and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="dae92-117">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="dae92-117">IRIS GL function</span></span>                                   | <span data-ttu-id="dae92-118">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="dae92-118">OpenGL function</span></span>                                                                           | <span data-ttu-id="dae92-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dae92-119">Meaning</span></span>                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="dae92-120">**lrectread**, **rectread**, Read **RGB**</span><span class="sxs-lookup"><span data-stu-id="dae92-120">**lrectread**, **rectread**,**readRGB**</span></span><br/> | [<span data-ttu-id="dae92-121">**glread Pixels**</span><span class="sxs-lookup"><span data-stu-id="dae92-121">**glReadPixels**</span></span>](glreadpixels.md)                                                      | <span data-ttu-id="dae92-122">Liest einen Pixel Block aus dem Framebuffer.</span><span class="sxs-lookup"><span data-stu-id="dae92-122">Reads a block of pixels from the framebuffer.</span></span>                           |
| <span data-ttu-id="dae92-123">**lrectwrite**, **rectwrite**</span><span class="sxs-lookup"><span data-stu-id="dae92-123">**lrectwrite**, **rectwrite**</span></span>                      | [<span data-ttu-id="dae92-124">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="dae92-124">**glDrawPixels**</span></span>](gldrawpixels.md)                                                      | <span data-ttu-id="dae92-125">Schreibt einen Pixel Block in den Framebuffer.</span><span class="sxs-lookup"><span data-stu-id="dae92-125">Writes a block of pixels to the framebuffer.</span></span>                            |
| <span data-ttu-id="dae92-126">**neu kopieren**</span><span class="sxs-lookup"><span data-stu-id="dae92-126">**rectcopy**</span></span>                                       | [<span data-ttu-id="dae92-127">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="dae92-127">**glCopyPixels**</span></span>](glcopypixels.md)                                                      | <span data-ttu-id="dae92-128">Kopiert Pixel im Framebuffer.</span><span class="sxs-lookup"><span data-stu-id="dae92-128">Copies pixels in the framebuffer.</span></span>                                       |
| <span data-ttu-id="dae92-129">**rectzoom**</span><span class="sxs-lookup"><span data-stu-id="dae92-129">**rectzoom**</span></span>                                       | [<span data-ttu-id="dae92-130">**glpixelzoom**</span><span class="sxs-lookup"><span data-stu-id="dae92-130">**glPixelZoom**</span></span>](glpixelzoom.md)                                                        | <span data-ttu-id="dae92-131">Gibt die Pixel Zoomfaktoren für **gldrawpixels** und **glcopypixels** an.</span><span class="sxs-lookup"><span data-stu-id="dae92-131">Specifies pixel zoom factors for **glDrawPixels** and **glCopyPixels**.</span></span> |
| <span data-ttu-id="dae92-132">**cmov**</span><span class="sxs-lookup"><span data-stu-id="dae92-132">**cmov**</span></span>                                           | [<span data-ttu-id="dae92-133">glRasterPos</span><span class="sxs-lookup"><span data-stu-id="dae92-133">glRasterPos</span></span>](glrasterpos-functions.md)                                                  | <span data-ttu-id="dae92-134">Gibt die Raster Position für Pixel Vorgänge an.</span><span class="sxs-lookup"><span data-stu-id="dae92-134">Specifies raster position for pixel operations.</span></span>                         |
| <span data-ttu-id="dae92-135">**"lesen"**</span><span class="sxs-lookup"><span data-stu-id="dae92-135">**readsource**</span></span>                                     | [<span data-ttu-id="dae92-136">**glread Buffer**</span><span class="sxs-lookup"><span data-stu-id="dae92-136">**glReadBuffer**</span></span>](glreadbuffer.md)                                                      | <span data-ttu-id="dae92-137">Wählt eine Farb Puffer Quelle für Pixel aus.</span><span class="sxs-lookup"><span data-stu-id="dae92-137">Selects a color buffer source for pixels.</span></span>                               |
| <span data-ttu-id="dae92-138">**pixmode**</span><span class="sxs-lookup"><span data-stu-id="dae92-138">**pixmode**</span></span>                                        | <span data-ttu-id="dae92-139">[**glpixelstore**](glpixelstore-functions.md),[**glpixeltransfer**](glpixeltransfer.md)</span><span class="sxs-lookup"><span data-stu-id="dae92-139">[**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md)</span></span> | <span data-ttu-id="dae92-140">Legt die Pixel Speicher Modi fest. Legen Sie Pixel Übertragungsmodi fest.</span><span class="sxs-lookup"><span data-stu-id="dae92-140">Sets pixel storage modes.Set pixel transfer modes.</span></span>                      |
| <span data-ttu-id="dae92-141">**logicop**</span><span class="sxs-lookup"><span data-stu-id="dae92-141">**logicop**</span></span>                                        | [<span data-ttu-id="dae92-142">**gllogicop**</span><span class="sxs-lookup"><span data-stu-id="dae92-142">**glLogicOp**</span></span>](gllogicop.md)                                                            | <span data-ttu-id="dae92-143">Gibt eine logische Operation für Pixel Schreibvorgänge an.</span><span class="sxs-lookup"><span data-stu-id="dae92-143">Specifies a logical operation for pixel writes.</span></span>                         |
|                                                    | <span data-ttu-id="dae92-144">[**glEnable**](glenable.md) (GL \_ Logic \_ OP)</span><span class="sxs-lookup"><span data-stu-id="dae92-144">[**glEnable**](glenable.md) ( GL\_LOGIC\_OP )</span></span>                                            | <span data-ttu-id="dae92-145">Schaltet Pixel Logik Vorgänge ein.</span><span class="sxs-lookup"><span data-stu-id="dae92-145">Turns on pixel logic operations.</span></span>                                        |



 

<span data-ttu-id="dae92-146">Eine umfassende Liste der möglichen logischen Vorgänge finden Sie unter [**gllogicop**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="dae92-146">For a complete list of possible logical operations, see [**glLogicOp**](gllogicop.md).</span></span>

<span data-ttu-id="dae92-147">Dieses IRIS GL-Codebeispiel zeigt einen typischen Pixel Schreibvorgang:</span><span class="sxs-lookup"><span data-stu-id="dae92-147">This IRIS GL code sample shows a typical pixel write:</span></span>

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

<span data-ttu-id="dae92-148">Der vorangehende Code sieht wie folgt aus, wenn er in OpenGL übersetzt wird:</span><span class="sxs-lookup"><span data-stu-id="dae92-148">The preceding code looks like this when translated to OpenGL:</span></span>

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





