---
title: R (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben R beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ab0286f5-cad2-4537-aa98-be0fce55ff53
keywords:
- rasterungs
- Rechtecke
- Rendering
- RGBA
- RGBA-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b82a2db1bade12a0ff844006a1572cdc3b977dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858593"
---
# <a name="r-opengl"></a><span data-ttu-id="76d20-108">R (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="76d20-108">R (OpenGL)</span></span>

<span data-ttu-id="76d20-109">[a](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) R [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="76d20-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) R [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="76d20-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**Raster**</span><span class="sxs-lookup"><span data-stu-id="76d20-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**rasterize**</span></span>
</dt> <dd>

<span data-ttu-id="76d20-111">Zum Konvertieren eines projizierten Punkts, einer Linie oder eines Polygons oder der Pixel einer Bitmap oder eines Bilds in Fragmente, die jeweils einem Pixel im Framebuffer entsprechen.</span><span class="sxs-lookup"><span data-stu-id="76d20-111">To convert a projected point, line, or polygon, or the pixels of a bitmap or image, to fragments, each corresponding to a pixel in the framebuffer.</span></span> <span data-ttu-id="76d20-112">Beachten Sie, dass alle primitiven gerastert werden, nicht nur Punkte, Linien und Polygone.</span><span class="sxs-lookup"><span data-stu-id="76d20-112">Note that all primitives are rasterized, not just points, lines, and polygons</span></span>

</dd> <dt>

<span data-ttu-id="76d20-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**Rollen**</span><span class="sxs-lookup"><span data-stu-id="76d20-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="76d20-114">Ein Viereck, dessen Alternative Ränder in Objekt Koordinaten nebeneinander zueinander sind.</span><span class="sxs-lookup"><span data-stu-id="76d20-114">A quadrilateral whose alternate edges are parallel to each other in object coordinates.</span></span> <span data-ttu-id="76d20-115">Mit glrect () angegebene Polygone \* sind immer Rechtecke. andere Vierecken können Rechtecke sein.</span><span class="sxs-lookup"><span data-stu-id="76d20-115">Polygons specified with glRect\*( ) are always rectangles; other quadrilaterals might be rectangles.</span></span>

</dd> <dt>

<span data-ttu-id="76d20-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**erung**</span><span class="sxs-lookup"><span data-stu-id="76d20-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**rendering**</span></span>
</dt> <dd>

<span data-ttu-id="76d20-117">Konvertierung von primitiven, die in Objekt Koordinaten angegeben sind, in ein Bild im Framebuffer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="76d20-117">Conversion of primitives specified in object coordinates to an image in the framebuffer.</span></span> <span data-ttu-id="76d20-118">Rendering ist der primäre Vorgang von OpenGL.</span><span class="sxs-lookup"><span data-stu-id="76d20-118">Rendering is the primary operation of OpenGL.</span></span>

</dd> <dt>

<span data-ttu-id="76d20-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span><span class="sxs-lookup"><span data-stu-id="76d20-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span></span>
</dt> <dd>

<span data-ttu-id="76d20-120">Die Farben für Rot, grün, blau und Alpha Farben des RGBA-Modus.</span><span class="sxs-lookup"><span data-stu-id="76d20-120">The red, green, blue, and alpha color components of the RGBA mode.</span></span>

</dd> <dt>

<span data-ttu-id="76d20-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**RGBA-Modus**</span><span class="sxs-lookup"><span data-stu-id="76d20-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**RGBA mode**</span></span>
</dt> <dd>

<span data-ttu-id="76d20-122">Ein OpenGL-Kontext, in dem die Farb Puffer die Farbkomponenten Rot, grün, blau und Alpha anstelle von Farbindizes speichern.</span><span class="sxs-lookup"><span data-stu-id="76d20-122">An OpenGL context in which its color buffers store red, green, blue, and alpha color components, rather than color indexes.</span></span>

</dd> </dl>

 

 




