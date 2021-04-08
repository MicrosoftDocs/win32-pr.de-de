---
title: P (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben "P" beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bc7b0c93-af06-44a4-8bb8-adc0c6fedb6e
keywords:
- parameters
- Perspektiven Division
- Pixel
- Punkte
- Polygone
- Primitives
- Projektions Matrizen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9970b3eb84920184e693ace93b14120828573e30
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103949335"
---
# <a name="p-opengl"></a><span data-ttu-id="6cf3b-110">P (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="6cf3b-110">P (OpenGL)</span></span>

<span data-ttu-id="6cf3b-111">[a](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="6cf3b-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="6cf3b-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**Parame**</span><span class="sxs-lookup"><span data-stu-id="6cf3b-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6cf3b-113">Ein Wert, der als Argument an einen OpenGL-Befehl übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-113">A value passed as an argument to an OpenGL command.</span></span> <span data-ttu-id="6cf3b-114">Manchmal einer der Werte, die als Verweis an einen OpenGL-Befehl übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-114">Sometimes one of the values passed by reference to an OpenGL command.</span></span>

</dd> <dt>

<span data-ttu-id="6cf3b-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**Perspektiven Division**</span><span class="sxs-lookup"><span data-stu-id="6cf3b-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**perspective division**</span></span>
</dt> <dd>

<span data-ttu-id="6cf3b-116">Die Division von x, y und z durch w, die in Clip Koordinaten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-116">The division of x, y, and z by w, carried out in clip coordinates.</span></span> <span data-ttu-id="6cf3b-117">Siehe auch [Clip-Koordinaten](c.md).</span><span class="sxs-lookup"><span data-stu-id="6cf3b-117">See also [clip coordinates](c.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cf3b-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**Megapixel**</span><span class="sxs-lookup"><span data-stu-id="6cf3b-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**pixel**</span></span>
</dt> <dd>

<span data-ttu-id="6cf3b-119">Bildelement.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-119">Picture element.</span></span> <span data-ttu-id="6cf3b-120">Die Bits an der Position (x, y) aller bitflächen im Frame Puffer bilden das einzelne Pixel (x, y).</span><span class="sxs-lookup"><span data-stu-id="6cf3b-120">The bits at location (x, y) of all the bitplanes in the framebuffer constitute the single pixel (x, y).</span></span> <span data-ttu-id="6cf3b-121">In einem Bild im Client Speicher ist ein Pixel eine Gruppe von Elementen.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-121">In an image in client memory, a pixel is one group of elements.</span></span> <span data-ttu-id="6cf3b-122">In den OpenGL-Fenster Koordinaten entspricht jedes Pixel einem Bildschirmbereich von 1.0 x 1.0.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-122">In OpenGL window coordinates, each pixel corresponds to a 1.0x1.0 screen area.</span></span> <span data-ttu-id="6cf3b-123">Die Koordinaten der unteren linken Ecke der Pixel Namen x, y sind (x, y) und die obere rechte Ecke (x + 1, y + 1).</span><span class="sxs-lookup"><span data-stu-id="6cf3b-123">The coordinates of the lower-left corner of the pixel names x, y are (x, y), and the upper-right corner are (x+1, y+1).</span></span>

</dd> <dt>

<span data-ttu-id="6cf3b-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**Punkt**</span><span class="sxs-lookup"><span data-stu-id="6cf3b-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**point**</span></span>
</dt> <dd>

<span data-ttu-id="6cf3b-125">Eine genaue Position im Raum, die als Punkt mit Endpunkten gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-125">An exact location in space, which is rendered as a finite-diameter dot.</span></span>

</dd> <dt>

<span data-ttu-id="6cf3b-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**Polygon**</span><span class="sxs-lookup"><span data-stu-id="6cf3b-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**polygon**</span></span>
</dt> <dd>

<span data-ttu-id="6cf3b-127">Eine near-planare Oberfläche, die durch von Scheitel Punkten angegebene Kanten begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-127">A near-planar surface bounded by edges specified by vertices.</span></span> <span data-ttu-id="6cf3b-128">Jedes Dreieck eines Dreiecks Netzes ist ein Polygon, ebenso wie jedes Viereck eines vierseitigen Mesh.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-128">Each triangle of a triangle mesh is a polygon, as is each quadrilateral of a quadrilateral mesh.</span></span> <span data-ttu-id="6cf3b-129">Das von glrect angegebene Rechteck ist ebenfalls ein Polygon.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-129">The rectangle specified by glRect is also a polygon.</span></span>

</dd> <dt>

<span data-ttu-id="6cf3b-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**Christentum**</span><span class="sxs-lookup"><span data-stu-id="6cf3b-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**primitive**</span></span>
</dt> <dd>

<span data-ttu-id="6cf3b-131">Eine Form (z. b. ein Punkt, eine Linie, ein Polygon, eine Bitmap oder ein Bild), die als diskrete Entität gezeichnet, gespeichert und manipuliert werden kann. Elemente, aus denen große Grafik Entwürfe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-131">A shape (such as a point, line, polygon, bitmap, or image) that can be drawn, stored, and manipulated as a discrete entity; elements from which large graphic designs are created.</span></span>

</dd> <dt>

<span data-ttu-id="6cf3b-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**Projektions Matrix**</span><span class="sxs-lookup"><span data-stu-id="6cf3b-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**projection matrix**</span></span>
</dt> <dd>

<span data-ttu-id="6cf3b-133">Die 4X4-Matrix, die Punkte, Linien, Polygone und Raster Positionen von Augen Koordinaten zu Clip Koordinaten transformiert.</span><span class="sxs-lookup"><span data-stu-id="6cf3b-133">The 4x4 matrix that transforms points, lines, polygons, and raster positions from eye coordinates to clip coordinates.</span></span>

</dd> </dl>

 

 




