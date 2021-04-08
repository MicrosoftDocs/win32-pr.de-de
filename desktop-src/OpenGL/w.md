---
title: W (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben "W" beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7f8235a3-ea48-40eb-8957-e7a55a5778af
keywords:
- Windows
- Fenster Ausrichtung
- Fenster Koordinaten
- Draht Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f6f1897af46c85ed48171d251ebe1b2de8c5e1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739273"
---
# <a name="w-opengl"></a><span data-ttu-id="bb6ac-107">W (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="bb6ac-107">W (OpenGL)</span></span>

<span data-ttu-id="bb6ac-108">[a](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="bb6ac-108">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="bb6ac-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**ster**</span><span class="sxs-lookup"><span data-stu-id="bb6ac-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**window**</span></span>
</dt> <dd>

<span data-ttu-id="bb6ac-110">Ein Unterbereich des Framebuffer (normalerweise rechteckig), dessen Pixel alle die gleiche Puffer Konfiguration aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-110">A subregion of the framebuffer, usually rectangular, whose pixels all have the same buffer configuration.</span></span> <span data-ttu-id="bb6ac-111">Ein OpenGL-Kontext wird in einem Fenster gleichzeitig gerendert.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-111">An OpenGL context renders to one window at a time.</span></span>

</dd> <dt>

<span data-ttu-id="bb6ac-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**Fenster Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="bb6ac-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**window-aligned**</span></span>
</dt> <dd>

<span data-ttu-id="bb6ac-113">Beim Verweis auf Liniensegmente oder Polygon Ränder impliziert, dass diese parallel zu den Fenstergrenzen sind.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-113">When referring to line segments or polygon edges, implies that these are parallel to the window boundaries.</span></span> <span data-ttu-id="bb6ac-114">(In OpenGL ist das Fenster rechteckig mit horizontaler und vertikaler Kanten).</span><span class="sxs-lookup"><span data-stu-id="bb6ac-114">(In OpenGL, the window is rectangular, with horizontal and vertical edges).</span></span> <span data-ttu-id="bb6ac-115">Beim Verweis auf ein Polygon Muster impliziert, dass das Muster relativ zum Fenster Ursprung fest ist.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-115">When referring to a polygon pattern, implies that the pattern is fixed relative to the window origin.</span></span>

</dd> <dt>

<span data-ttu-id="bb6ac-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**Fenster Koordinaten**</span><span class="sxs-lookup"><span data-stu-id="bb6ac-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**window coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="bb6ac-117">Das Koordinatensystem eines Fensters.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-117">The coordinate system of a window.</span></span> <span data-ttu-id="bb6ac-118">Es ist wichtig, die Namen von Pixeln, die diskret sind, und das Fenster Koordinatensystem, das kontinuierlich ist, zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-118">It's important to distinguish between the names of pixels, which are discrete, and the window-coordinate system, which is continuous.</span></span> <span data-ttu-id="bb6ac-119">Beispielsweise ist das Pixel in der unteren linken Ecke eines Fensters Pixel (0,0); die Fenster Koordinaten der Mitte dieses Pixels sind (0,5, 0,5, z).</span><span class="sxs-lookup"><span data-stu-id="bb6ac-119">For example, the pixel at the lower-left corner of a window is pixel (0, 0); the window coordinates of the center of this pixel are (0.5, 0.5, z).</span></span> <span data-ttu-id="bb6ac-120">Beachten Sie, dass Fenster Koordinaten eine Tiefe oder z-Komponente enthalten, und dass diese Komponente ebenfalls kontinuierlich ist.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-120">Note that window coordinates include a depth, or z, component, and that this component is continuous as well.</span></span>

</dd> <dt>

<span data-ttu-id="bb6ac-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**Draht Modell**</span><span class="sxs-lookup"><span data-stu-id="bb6ac-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**wireframe**</span></span>
</dt> <dd>

<span data-ttu-id="bb6ac-122">Eine Darstellung eines Objekts, das nur Liniensegmente enthält.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-122">A representation of an object that contains line segments only.</span></span> <span data-ttu-id="bb6ac-123">In der Regel geben die Liniensegmente Polygon Kanten an.</span><span class="sxs-lookup"><span data-stu-id="bb6ac-123">Typically, the line segments indicate polygon edges.</span></span>

</dd> </dl>

 

 




