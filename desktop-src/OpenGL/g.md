---
title: G (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben "G" beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 588df117-d03c-4a1f-9666-84004cb3d97b
keywords:
- Gammakorrektur
- geometrisches Modell
- geometrische Objekte
- geometrische Primitive
- Gouraud-Schattierung
- groups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c369c5c2af949bed221d1afd5fb0c05aebf14849
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106342397"
---
# <a name="g-opengl"></a><span data-ttu-id="0c2cc-109">G (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="0c2cc-109">G (OpenGL)</span></span>

<span data-ttu-id="0c2cc-110">[a](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) G [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="0c2cc-110">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) G [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="0c2cc-111"><span id="opengl_gamma_correction"></span><span id="OPENGL_GAMMA_CORRECTION"></span>**Gammakorrektur**</span><span class="sxs-lookup"><span data-stu-id="0c2cc-111"><span id="opengl_gamma_correction"></span><span id="OPENGL_GAMMA_CORRECTION"></span>**gamma correction**</span></span>
</dt> <dd>

<span data-ttu-id="0c2cc-112">Eine Funktion, die auf Farben angewendet wird, die im Frame Puffer gespeichert werden, um die nichtlineare Reaktion des Auges (und manchmal des Monitors) auf lineare Änderungen in Farb Intensitäts Werten zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-112">A function applied to colors stored in the frame buffer to correct for the nonlinear response of the eye (and sometimes of the monitor) to linear changes in color-intensity values.</span></span>

</dd> <dt>

<span data-ttu-id="0c2cc-113"><span id="opengl_geometric_model"></span><span id="OPENGL_GEOMETRIC_MODEL"></span>**geometrisches Modell**</span><span class="sxs-lookup"><span data-stu-id="0c2cc-113"><span id="opengl_geometric_model"></span><span id="OPENGL_GEOMETRIC_MODEL"></span>**geometric model**</span></span>
</dt> <dd>

<span data-ttu-id="0c2cc-114">Die Objekt Koordinaten Vertices und Parameter, die ein Objekt beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-114">The object-coordinate vertices and parameters that describe an object.</span></span> <span data-ttu-id="0c2cc-115">Beachten Sie, dass OpenGL keine Syntax für geometrische Modelle definiert, sondern vielmehr eine Syntax und Semantik für das Rendering von geometrischen Modellen.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-115">Note that OpenGL doesn't define a syntax for geometric models, but rather a syntax and semantics for the rendering of geometric models.</span></span>

</dd> <dt>

<span data-ttu-id="0c2cc-116"><span id="opengl_geometric_object"></span><span id="OPENGL_GEOMETRIC_OBJECT"></span>**geometrisches Objekt**</span><span class="sxs-lookup"><span data-stu-id="0c2cc-116"><span id="opengl_geometric_object"></span><span id="OPENGL_GEOMETRIC_OBJECT"></span>**geometric object**</span></span>
</dt> <dd>

<span data-ttu-id="0c2cc-117">Ein geometrisches Modell.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-117">A geometric model.</span></span>

</dd> <dt>

<span data-ttu-id="0c2cc-118"><span id="opengl_geometric_primitive"></span><span id="OPENGL_GEOMETRIC_PRIMITIVE"></span>**geometrisch primitiv**</span><span class="sxs-lookup"><span data-stu-id="0c2cc-118"><span id="opengl_geometric_primitive"></span><span id="OPENGL_GEOMETRIC_PRIMITIVE"></span>**geometric primitive**</span></span>
</dt> <dd>

<span data-ttu-id="0c2cc-119">Ein Punkt, eine Linie oder ein Polygon.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-119">A point, line, or polygon.</span></span>

</dd> <dt>

<span data-ttu-id="0c2cc-120"><span id="opengl_gouraud_shading"></span><span id="OPENGL_GOURAUD_SHADING"></span>**Gouraud-Schattierung**</span><span class="sxs-lookup"><span data-stu-id="0c2cc-120"><span id="opengl_gouraud_shading"></span><span id="OPENGL_GOURAUD_SHADING"></span>**Gouraud shading**</span></span>
</dt> <dd>

<span data-ttu-id="0c2cc-121">Glatte interpolung von Farben in einem Polygon-oder Liniensegment.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-121">Smooth interpolation of colors across a polygon or line segment.</span></span> <span data-ttu-id="0c2cc-122">Farben werden bei Scheitel Punkten und linear interpoliert, um eine relativ glatte Variation der Farbe zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-122">Colors are assigned at vertices and linearly interpolated across the primitive to produce a relatively smooth variation in color.</span></span> <span data-ttu-id="0c2cc-123">Wird auch als Smooth Schattierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-123">Also called smooth shading.</span></span>

</dd> <dt>

<span data-ttu-id="0c2cc-124"><span id="opengl_group"></span><span id="OPENGL_GROUP"></span>**Kreis**</span><span class="sxs-lookup"><span data-stu-id="0c2cc-124"><span id="opengl_group"></span><span id="OPENGL_GROUP"></span>**group**</span></span>
</dt> <dd>

<span data-ttu-id="0c2cc-125">Eine Gruppe von einem, zwei, drei oder vier Elementen, die jedes Pixel eines Bilds im Client Speicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-125">A group of one, two, three, or four elements that represents each pixel of an image in client memory.</span></span> <span data-ttu-id="0c2cc-126">Daher sind eine Gruppe und ein Pixel im Kontext eines Client Speicher Abbilds identisch.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-126">Thus, in the context of a client memory image, a group and a pixel are the same thing.</span></span>

</dd> </dl>

 

 




