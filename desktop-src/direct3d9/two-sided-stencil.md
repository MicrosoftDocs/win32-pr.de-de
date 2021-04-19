---
description: Schattenvolumes werden zum Zeichnen von Schatten mit dem Schablonen Puffer verwendet.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Two-Sided Schablone (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346833"
---
# <a name="two-sided-stencil-direct3d-9"></a><span data-ttu-id="dd2e8-103">Two-Sided Schablone (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dd2e8-103">Two-Sided Stencil (Direct3D 9)</span></span>

<span data-ttu-id="dd2e8-104">Schattenvolumes werden zum Zeichnen von Schatten mit dem Schablonen Puffer verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-104">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="dd2e8-105">Die Anwendung berechnet die schattenvolumes, die durch die Schattierung von Geometrie umgewandelt werden, indem die Silhouette-Kanten berechnet und vom Licht in eine Gruppe von 3D-Volumes aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-105">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="dd2e8-106">Diese Volumes werden dann zweimal im Schablonen Puffer gerendert.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-106">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="dd2e8-107">Das erste Rendering zeichnet nach vorne gerichtete Polygone und erhöht die Schablonen Puffer Werte.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-107">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="dd2e8-108">Das zweite Rendering zeichnet die rückwärts gerichteten Polygone des Schatten Volumens und Dekremente die Schablonen Puffer Werte.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-108">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="dd2e8-109">Normalerweise brechen alle inkrementierten und dekrementierten Werte einander ab. Die Szene wurde jedoch bereits mit normaler Geometrie gerendert, sodass einige Pixel den z-Puffer-Test nicht bestanden haben, während das Schatten Volume gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-109">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="dd2e8-110">Werte, die im Schablonen Puffer verbleiben, entsprechen den im Schatten entsprechenden Pixeln.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-110">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="dd2e8-111">Diese verbleibenden Schablone-Puffer Inhalte werden als Maske verwendet, um einen großen, umfassenden, vier Vierfache in die Szene zu mischen.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-111">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="dd2e8-112">Wenn der Schablone-Puffer als Maske fungiert, besteht das Ergebnis darin, die Pixel in den Schatten zu verbergen.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-112">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="dd2e8-113">Dies bedeutet, dass die Schatten Geometrie zweimal pro Lichtquelle gezeichnet wird und somit den Scheitelpunkt Durchsatz der GPU erhöht.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-113">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="dd2e8-114">Das zweiseitige Schablonen Feature wurde entwickelt, um diese Situation zu mindern.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-114">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="dd2e8-115">Bei dieser Vorgehensweise gibt es zwei Sätze von Schablone State (unten genannt), jeweils eine Menge für die Vorder-und die andere für die mit der Rückseite gerichteten Dreiecke.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-115">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="dd2e8-116">Auf diese Weise wird nur ein einzelner Durchlauf pro Schatten Volume pro Licht gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-116">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="dd2e8-117">Die API-Änderungen sind auf einen neuen Satz von Rendering-Zuständen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-117">The API changes are restricted to a new set of render states.</span></span> <span data-ttu-id="dd2e8-118">Der neue renderzustand D3DRS der \_ zwei \_ seitige \_ Schablonen Modus kann auf " **true** " oder " **false**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-118">The new render state D3DRS\_Two\_Sided\_StencilMODE can be set to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="dd2e8-119">Der Standardwert ist **false** . Dies bedeutet das aktuelle Verhalten (DirectX 8).</span><span class="sxs-lookup"><span data-stu-id="dd2e8-119">It is **FALSE** by default, meaning current (DirectX 8) behavior.</span></span> <span data-ttu-id="dd2e8-120">Wenn diese auf **true** festgelegt ist (dies funktioniert nur, wenn D3DSTENCILCAPS \_ twoseitigem festgelegt ist), gelten die folgenden Rendering-Zustände nur für die Front-on-Dreiecke (im Uhrzeigersinn).</span><span class="sxs-lookup"><span data-stu-id="dd2e8-120">When this is set to **TRUE** (it will work only if D3DSTENCILCAPS\_TWOSIDED is set), the following render states will apply only to the front-facing (clockwise) triangles.</span></span>



| <span data-ttu-id="dd2e8-121">Rendering-Zustand</span><span class="sxs-lookup"><span data-stu-id="dd2e8-121">Render state</span></span>        | <span data-ttu-id="dd2e8-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd2e8-122">Description</span></span>                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2e8-123">D3DRS \_ stencilfail</span><span class="sxs-lookup"><span data-stu-id="dd2e8-123">D3DRS\_STENCILFAIL</span></span>  | <span data-ttu-id="dd2e8-124">D3DSTENCILOP, wenn der Schablone-Test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-124">D3DSTENCILOP to do if stencil test fails.</span></span>                                                |
| <span data-ttu-id="dd2e8-125">D3DRS \_ stencilzfail</span><span class="sxs-lookup"><span data-stu-id="dd2e8-125">D3DRS\_STENCILZFAIL</span></span> | <span data-ttu-id="dd2e8-126">D3DSTENCILOP, wenn der Schablone-Test erfolgreich verläuft und z-Test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-126">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                              |
| <span data-ttu-id="dd2e8-127">D3DRS \_ stencilpass</span><span class="sxs-lookup"><span data-stu-id="dd2e8-127">D3DRS\_STENCILPASS</span></span>  | <span data-ttu-id="dd2e8-128">D3DSTENCILOP, wenn sowohl Schablone als auch z-Tests bestanden werden.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-128">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                     |
| <span data-ttu-id="dd2e8-129">D3DRS \_ stencilfunc</span><span class="sxs-lookup"><span data-stu-id="dd2e8-129">D3DRS\_STENCILFUNC</span></span>  | <span data-ttu-id="dd2e8-130">D3DCMPFUNC Fn.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-130">D3DCMPFUNC fn.</span></span> <span data-ttu-id="dd2e8-131">Der Schablone-Test wird durchlaufen, wenn ((Ref & Mask) stencilfn (Schablone & Mask)) "true" ist.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-131">Stencil Test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="dd2e8-132">Ein neuer Satz von Rendering-Zuständen gilt für die nach hinten gerichteten Dreiecke (gegen den Uhrzeigersinn).</span><span class="sxs-lookup"><span data-stu-id="dd2e8-132">A new set of render states apply to the back-facing (counterclockwise) triangles.</span></span>



| <span data-ttu-id="dd2e8-133">Rendering-Zustand</span><span class="sxs-lookup"><span data-stu-id="dd2e8-133">Render state</span></span>             | <span data-ttu-id="dd2e8-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd2e8-134">Description</span></span>                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2e8-135">D3DRS \_ CCW \_ stencilfail</span><span class="sxs-lookup"><span data-stu-id="dd2e8-135">D3DRS\_CCW\_STENCILFAIL</span></span>  | <span data-ttu-id="dd2e8-136">D3DSTENCILOP, wenn der Schablone-Test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-136">D3DSTENCILOP to do if stencil test fails.</span></span>                                                      |
| <span data-ttu-id="dd2e8-137">D3DRS \_ CCW \_ stencilzfail</span><span class="sxs-lookup"><span data-stu-id="dd2e8-137">D3DRS\_CCW\_STENCILZFAIL</span></span> | <span data-ttu-id="dd2e8-138">D3DSTENCILOP, wenn der Schablone-Test erfolgreich verläuft und z-Test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-138">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                                    |
| <span data-ttu-id="dd2e8-139">D3DRS \_ CCW \_ stencilpass</span><span class="sxs-lookup"><span data-stu-id="dd2e8-139">D3DRS\_CCW\_STENCILPASS</span></span>  | <span data-ttu-id="dd2e8-140">D3DSTENCILOP, wenn sowohl Schablone als auch z-Tests bestanden werden.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-140">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                           |
| <span data-ttu-id="dd2e8-141">D3DRS \_ CCW \_ stencilfunc</span><span class="sxs-lookup"><span data-stu-id="dd2e8-141">D3DRS\_CCW\_STENCILFUNC</span></span>  | <span data-ttu-id="dd2e8-142">D3DCMPFUNC-Funktion.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-142">D3DCMPFUNC function.</span></span> <span data-ttu-id="dd2e8-143">Der Schablone-Test wird durchlaufen, wenn ((Ref & Mask) stencilfn (Schablone & Mask)) "true" ist.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-143">Stencil test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="dd2e8-144">Die verbleibenden Schablone-Rendering-Zustände gelten immer für den Uhrzeigersinn und gegen den Uhrzeigersinn.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-144">The remaining stencil render states always apply to both clockwise and counterclockwise triangles.</span></span>

<span data-ttu-id="dd2e8-145">D3DRS \_ \_ der zweiseitige \_ Schablonen Modus wird für Linien und Punkt Sprites ignoriert, was bedeutet, dass das Verhalten von DirectX 8 unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-145">D3DRS\_Two\_Sided\_StencilMODE is ignored for lines and point sprites, which means that the behavior is unchanged from DirectX 8.</span></span> <span data-ttu-id="dd2e8-146">Die D3DRS \_ CCW- \_ Schablonen- \* Rendering-Zustände werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-146">The D3DRS\_CCW\_STENCIL\* render states are ignored.</span></span>

<span data-ttu-id="dd2e8-147">Ein neues Cap-Bit gibt an, ob das Gerät dieses Feature unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-147">A new cap bit indicates if the device supports this feature.</span></span> <span data-ttu-id="dd2e8-148">Treiber, die dieses Feature nicht unterstützen, werden davon ausgehen, dass diese neuen Rendering-Zustände ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-148">Drivers that do not support this feature are expected to ignore these new render states.</span></span> <span data-ttu-id="dd2e8-149">Alle anderen Schablone-deckbits gelten für beide Modi der Schablonen Pufferung.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-149">All other stencil cap bits apply to both modes of stencil buffering.</span></span> <span data-ttu-id="dd2e8-150">Da zwei \_ seitige \_ Schablonen die Fähigkeit zum Zeichnen mit D3DCULLMODE None impliziert \_ , muss die entsprechende Obergrenze vom Treiber festgelegt werden, wenn Sie diesen neuen Schablone-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-150">Because Two\_Sided\_Stencil implies the ability to draw with D3DCULLMODE\_NONE set, the corresponding cap must be set by the driver if it supports this new stencil mode.</span></span> <span data-ttu-id="dd2e8-151">Microsoft Windows Hardware Quality Labs (WHQL) sollte dies erzwingen.</span><span class="sxs-lookup"><span data-stu-id="dd2e8-151">Microsoft Windows Hardware Quality Labs (WHQL) should enforce this.</span></span>

<span data-ttu-id="dd2e8-152">Neue Rendering-Zustände:</span><span class="sxs-lookup"><span data-stu-id="dd2e8-152">New render states:</span></span>


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



<span data-ttu-id="dd2e8-153">Neue Obergrenze:</span><span class="sxs-lookup"><span data-stu-id="dd2e8-153">New cap:</span></span>


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a><span data-ttu-id="dd2e8-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd2e8-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd2e8-155">Techniken für Schablonen Puffer</span><span class="sxs-lookup"><span data-stu-id="dd2e8-155">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> <dt>

[<span data-ttu-id="dd2e8-156">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="dd2e8-156">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
