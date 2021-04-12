---
title: A (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben A beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: e583610f-37da-47bb-bbd6-41d353b88244
keywords:
- Aliasing
- alpha
- Animation
- Antialiasing (antialiasing)
- anwendungsspezifisches Clipping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d161832eb6d81738038e10564233f26920f0d60
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391434"
---
# <a name="a-opengl"></a><span data-ttu-id="cef92-108">A (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="cef92-108">A (OpenGL)</span></span>

<span data-ttu-id="cef92-109">a [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="cef92-109">A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="cef92-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**Aliasing**</span><span class="sxs-lookup"><span data-stu-id="cef92-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**aliasing**</span></span>
</dt> <dd>

<span data-ttu-id="cef92-111">Eine renderingtechnik, die Pixel die Farbe des primitiven, das gerendert wird, zuweist, ob diese primitive den gesamten oder einen Teil des Pixel Bereichs abdeckt.</span><span class="sxs-lookup"><span data-stu-id="cef92-111">A rendering technique that assigns to pixels the color of the primitive being rendered, whether that primitive covers all or part of the pixel's area.</span></span> <span data-ttu-id="cef92-112">Aliasing führt zu verzweigten Kanten oder Verzweigungen.</span><span class="sxs-lookup"><span data-stu-id="cef92-112">Aliasing results in jagged edges, or jaggies.</span></span> <span data-ttu-id="cef92-113">Siehe auch [](jk.md)Verzweigungen.</span><span class="sxs-lookup"><span data-stu-id="cef92-113">See also [jaggies](jk.md).</span></span>

</dd> <dt>

<span data-ttu-id="cef92-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**Alpha**</span><span class="sxs-lookup"><span data-stu-id="cef92-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**alpha**</span></span>
</dt> <dd>

<span data-ttu-id="cef92-115">Eine vierte Farbkomponente, die normalerweise verwendet wird, um Farbmischung zu steuern</span><span class="sxs-lookup"><span data-stu-id="cef92-115">A fourth color component typically used to control color blending.</span></span> <span data-ttu-id="cef92-116">Die Alpha Komponente wird nie direkt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cef92-116">The alpha component is never displayed directly.</span></span> <span data-ttu-id="cef92-117">Gemäß der Konvention gibt OpenGL Alpha die Deckkraft und Transparenz bei einer Skala von 0,0 bis 1,0 an.</span><span class="sxs-lookup"><span data-stu-id="cef92-117">By convention, OpenGL alpha indicates opacity and transparency on a scale of 0.0 to 1.0.</span></span> <span data-ttu-id="cef92-118">Der Alpha-Wert 1,0 impliziert eine komplette Deckkraft. der Alpha Wert 0,0 impliziert eine umfassende Transparenz.</span><span class="sxs-lookup"><span data-stu-id="cef92-118">An alpha value of 1.0 implies complete opacity, an alpha value of 0.0 implies complete transparency.</span></span>

</dd> <dt>

<span data-ttu-id="cef92-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**Animationen**</span><span class="sxs-lookup"><span data-stu-id="cef92-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animation**</span></span>
</dt> <dd>

<span data-ttu-id="cef92-120">Die Generierung von wiederholten Renderings einer Szene ist schnell genug, mit reibungslos veränderlichen Standpunkten oder Objektpositionen, dass die Illusion von Bewegung erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="cef92-120">The generation of repeated renderings of a scene quickly enough, with smoothly changing viewpoint or object positions, that the illusion of motion is achieved.</span></span> <span data-ttu-id="cef92-121">Die OpenGL-Animation verwendet fast immer doppelte Pufferung.</span><span class="sxs-lookup"><span data-stu-id="cef92-121">OpenGL animation almost always uses double-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="cef92-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**Antialiasing**</span><span class="sxs-lookup"><span data-stu-id="cef92-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**antialiasing**</span></span>
</dt> <dd>

<span data-ttu-id="cef92-123">Eine renderingtechnik, die Pixel basierend auf dem Bruchteil des Pixel Bereichs, der durch das primitive, das gerendert wird, abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="cef92-123">A rendering technique that assigns colors to pixels based on the fraction of the pixel area that is covered by the primitive being rendered.</span></span> <span data-ttu-id="cef92-124">Das Rendern mit Antialiasing reduziert oder entfernt die Verzweigungen, die sich aus dem Rendern von Alias ergeben.</span><span class="sxs-lookup"><span data-stu-id="cef92-124">Antialiased rendering reduces or eliminates the jaggies that result from aliased rendering.</span></span> <span data-ttu-id="cef92-125">Siehe auch [](jk.md)Verzweigungen, [Rendering](r.md).</span><span class="sxs-lookup"><span data-stu-id="cef92-125">See also [jaggies](jk.md), [rendering](r.md).</span></span>

</dd> <dt>

<span data-ttu-id="cef92-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**anwendungsspezifisches Clipping**</span><span class="sxs-lookup"><span data-stu-id="cef92-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**application-specific clipping**</span></span> 
</dt> <dd>

<span data-ttu-id="cef92-127">Clipping von primitiven für Flächen in Augen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="cef92-127">Clipping of primitives against planes in eye coordinates.</span></span> <span data-ttu-id="cef92-128">Die Ebenen werden von der Anwendung mithilfe von [**glclipplane**](glclipplane.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="cef92-128">The planes are specified by the application using [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="cef92-129">Siehe auch [Eye-Koordinaten](e.md).</span><span class="sxs-lookup"><span data-stu-id="cef92-129">See also [eye coordinates](e.md).</span></span>

</dd> </dl>

 

 




