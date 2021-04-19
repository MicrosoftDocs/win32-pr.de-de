---
title: F (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben F beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- faces
- flatschattierung
- Nebel
- Schriftarten
- fragments
- framebuffers
- Vorderseite
- Frustum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7085765a5585268acb2f20a77c72bdd7cf1b4b81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337278"
---
# <a name="f-opengl"></a><span data-ttu-id="034b9-111">F (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="034b9-111">F (OpenGL)</span></span>

<span data-ttu-id="034b9-112">[a](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="034b9-112">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="034b9-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**mit**</span><span class="sxs-lookup"><span data-stu-id="034b9-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**face**</span></span>
</dt> <dd>

<span data-ttu-id="034b9-114">Eine Seite eines Polygons.</span><span class="sxs-lookup"><span data-stu-id="034b9-114">One side of a polygon.</span></span> <span data-ttu-id="034b9-115">Jedes Polygon hat zwei Gesichter: eine Vorderseite und eine Rückseite.</span><span class="sxs-lookup"><span data-stu-id="034b9-115">Each polygon has two faces: a front face and a back face.</span></span> <span data-ttu-id="034b9-116">Im Fenster ist immer nur ein Gesicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="034b9-116">Only one face is ever visible in the window.</span></span> <span data-ttu-id="034b9-117">Ob das hintere oder das vordere Gesicht sichtbar ist, wird effektiv festgelegt, nachdem das Polygon auf das Fenster projiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="034b9-117">Whether the back or front face is visible is effectively determined after the polygon is projected onto the window.</span></span> <span data-ttu-id="034b9-118">Wenn die Ränder des Polygons nach dieser Projektion im Uhrzeigersinn weitergeleitet werden, ist eine der Gesichter sichtbar. Wenn das andere Gesicht gegen den Uhrzeigersinn gerichtet ist, ist es sichtbar.</span><span class="sxs-lookup"><span data-stu-id="034b9-118">After this projection, if the polygon's edges are directed clockwise, one of the faces is visible; if directed counterclockwise, the other face is visible.</span></span> <span data-ttu-id="034b9-119">Ob der Uhrzeigersinn dem Vordergrund oder dem Hintergrund entspricht (und gegen den Uhrzeigersinn entsprechen), wird vom OpenGL-Programmierer bestimmt.</span><span class="sxs-lookup"><span data-stu-id="034b9-119">Whether clockwise corresponds to front or back (and counterclockwise corresponds to back or front) is determined by the OpenGL programmer.</span></span>

</dd> <dt>

<span data-ttu-id="034b9-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**flatschattierung**</span><span class="sxs-lookup"><span data-stu-id="034b9-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**flat shading**</span></span>
</dt> <dd>

<span data-ttu-id="034b9-121">Bezieht sich auf die Farbgebung eines Primitivs mit einer einzelnen, Konstanten Farbe in seinem Block, anstatt Farben über das primitive hinweg zu interpolieren.</span><span class="sxs-lookup"><span data-stu-id="034b9-121">Refers to coloring a primitive with a single, constant color across its extent, rather than smoothly interpolating colors across the primitive.</span></span> <span data-ttu-id="034b9-122">Siehe [Gouraud-Schattierung](g.md).</span><span class="sxs-lookup"><span data-stu-id="034b9-122">See [Gouraud shading](g.md).</span></span>

</dd> <dt>

<span data-ttu-id="034b9-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**Neben**</span><span class="sxs-lookup"><span data-stu-id="034b9-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**fog**</span></span>
</dt> <dd>

<span data-ttu-id="034b9-124">Eine renderingtechnik, die verwendet werden kann, um atmosphärische Effekte wie z. b. Dunst, Nebel und Smog zu simulieren, indem Objekt Farben auf Grundlage der Entfernung vom Viewer auf eine Hintergrundfarbe ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="034b9-124">A rendering technique that can be used to simulate atmospheric effects such as haze, fog, and smog by fading object colors to a background color based on distance from the viewer.</span></span> <span data-ttu-id="034b9-125">Der Nebel unterstützt auch die Wahrnehmung der Entfernung vom Viewer und bietet einen tiefen Hinweis.</span><span class="sxs-lookup"><span data-stu-id="034b9-125">Fog also aids in the perception of distance from the viewer, giving a depth cue.</span></span> <span data-ttu-id="034b9-126">Siehe auch [ausführlichere](d.md)Informationen.</span><span class="sxs-lookup"><span data-stu-id="034b9-126">See also [depth-cueing](d.md).</span></span>

</dd> <dt>

<span data-ttu-id="034b9-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**Raster**</span><span class="sxs-lookup"><span data-stu-id="034b9-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**font**</span></span>
</dt> <dd>

<span data-ttu-id="034b9-128">Eine Gruppe grafischer Zeichen Darstellungen, die normalerweise zum Anzeigen von Text Zeichenfolgen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="034b9-128">A group of graphical character representations usually used to display strings of text.</span></span> <span data-ttu-id="034b9-129">Bei den Zeichen kann es sich um römische Buchstaben, mathematische Symbole, asiatische Ideogramme, ägyptische Hieroglyphen usw. handeln.</span><span class="sxs-lookup"><span data-stu-id="034b9-129">The characters may be roman letters, mathematical symbols, Asian ideograms, Egyptian hieroglyphs, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="034b9-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**Bruch**</span><span class="sxs-lookup"><span data-stu-id="034b9-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="034b9-131">Grafikdaten, die von der Rasterung von primitiven generiert werden.</span><span class="sxs-lookup"><span data-stu-id="034b9-131">Graphic data generated by the rasterization of primitives.</span></span> <span data-ttu-id="034b9-132">Jedes Fragment entspricht einem einzelnen Pixel und umfasst Farben, Tiefe und manchmal Texturkoordinaten Werte.</span><span class="sxs-lookup"><span data-stu-id="034b9-132">Each fragment corresponds to a single pixel and includes color, depth, and sometimes texture-coordinate values.</span></span>

</dd> <dt>

<span data-ttu-id="034b9-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**Frame Puffer**</span><span class="sxs-lookup"><span data-stu-id="034b9-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**framebuffer**</span></span>
</dt> <dd>

<span data-ttu-id="034b9-134">Ein Stapel von bitflächen.</span><span class="sxs-lookup"><span data-stu-id="034b9-134">A stack of bitplanes.</span></span> <span data-ttu-id="034b9-135">Alle Puffer eines bestimmten Fensters oder Kontexts.</span><span class="sxs-lookup"><span data-stu-id="034b9-135">All the buffers of a given window or context.</span></span> <span data-ttu-id="034b9-136">Umfasst manchmal den gesamten Pixel Speicher des Grafikhardware-Accelerators.</span><span class="sxs-lookup"><span data-stu-id="034b9-136">Sometimes includes all the pixel memory of the graphics hardware accelerator.</span></span> <span data-ttu-id="034b9-137">Siehe auch [bitplane](b.md).</span><span class="sxs-lookup"><span data-stu-id="034b9-137">See also [bitplane](b.md).</span></span>

</dd> <dt>

<span data-ttu-id="034b9-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**Vorderseite**</span><span class="sxs-lookup"><span data-stu-id="034b9-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**front face**</span></span>
</dt> <dd>

<span data-ttu-id="034b9-139">Siehe Gesicht.</span><span class="sxs-lookup"><span data-stu-id="034b9-139">See face.</span></span>

</dd> <dt>

<span data-ttu-id="034b9-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**Frustum**</span><span class="sxs-lookup"><span data-stu-id="034b9-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**</span></span>
</dt> <dd>

<span data-ttu-id="034b9-141">Das Ansichts Volume, das von der Perspektiven Division zurückgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="034b9-141">The view volume warped by perspective division.</span></span>

</dd> </dl>

 

 




