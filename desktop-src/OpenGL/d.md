---
title: D (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben "D" beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f97470e7-a500-47d7-84f0-b3045d04b8fc
keywords:
- depth
- tiefen Cueing
- Anzeigen von Listen
- Dithering
- Doppelte Pufferung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cb068f06135c6ba29e8a61f472d98907090a78
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739497"
---
# <a name="d-opengl"></a><span data-ttu-id="5ecfd-108">D (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="5ecfd-108">D (OpenGL)</span></span>

<span data-ttu-id="5ecfd-109">[a](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="5ecfd-109">[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="5ecfd-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**Eingeh**</span><span class="sxs-lookup"><span data-stu-id="5ecfd-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**depth**</span></span>
</dt> <dd>

<span data-ttu-id="5ecfd-111">Bezieht sich im Allgemeinen auf die z-Fenster Koordinate.</span><span class="sxs-lookup"><span data-stu-id="5ecfd-111">Generally refers to the z window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="5ecfd-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**tiefen Cueing**</span><span class="sxs-lookup"><span data-stu-id="5ecfd-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**depth cueing**</span></span>
</dt> <dd>

<span data-ttu-id="5ecfd-113">Eine renderingtechnik, die eine Farbe basierend auf der Entfernung vom Standpunkt zuweist.</span><span class="sxs-lookup"><span data-stu-id="5ecfd-113">A rendering technique that assigns color based on distance from the viewpoint.</span></span>

</dd> <dt>

<span data-ttu-id="5ecfd-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**Liste anzeigen**</span><span class="sxs-lookup"><span data-stu-id="5ecfd-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**display list**</span></span>
</dt> <dd>

<span data-ttu-id="5ecfd-115">Eine benannte Liste von OpenGL-Befehlen.</span><span class="sxs-lookup"><span data-stu-id="5ecfd-115">A named list of OpenGL commands.</span></span> <span data-ttu-id="5ecfd-116">Anzeigelisten werden immer auf dem Server gespeichert, sodass mit Anzeigelisten der Netzwerk Datenverkehr in Client-/Server-Umgebungen reduziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5ecfd-116">Display lists are always stored on the server, so display lists can be used to reduce the network traffic in client/server environments.</span></span> <span data-ttu-id="5ecfd-117">Der Inhalt einer Anzeigeliste ist möglicherweise vorverarbeitet und wird daher möglicherweise effizienter ausgeführt als derselbe Satz von OpenGL-Befehlen, die im unmittelbaren Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5ecfd-117">The contents of a display list may be preprocessed, and might therefore execute more efficiently than the same set of OpenGL commands executed in immediate mode.</span></span> <span data-ttu-id="5ecfd-118">Eine solche Vorverarbeitung ist besonders wichtig für die Berechnung intensiver Befehle wie z. b. [**glteximage**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="5ecfd-118">Such preprocessing is especially important for computing intensive commands such as [**glTexImage**](glteximage1d.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ecfd-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**Dithering**</span><span class="sxs-lookup"><span data-stu-id="5ecfd-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**dithering**</span></span>
</dt> <dd>

<span data-ttu-id="5ecfd-120">Eine Technik, mit der der wahrgenommene Bereich von Farben in einem Bild auf Kosten der räumlichen Auflösung erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="5ecfd-120">A technique for increasing the perceived range of colors in an image at the cost of spatial resolution.</span></span> <span data-ttu-id="5ecfd-121">Angrenzenden Pixeln werden unterschiedliche Farbwerte zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="5ecfd-121">Adjacent pixels are assigned differing color values.</span></span> <span data-ttu-id="5ecfd-122">Wenn Sie von einer Entfernung aus angezeigt werden, scheinen diese Farben in eine einzelne zwischen Farbe zu mischen.</span><span class="sxs-lookup"><span data-stu-id="5ecfd-122">When viewed from a distance, these colors seem to blend into a single intermediate color.</span></span> <span data-ttu-id="5ecfd-123">Die Vorgehensweise ähnelt der Hälfte der Verwendung in schwarz-und weißen Veröffentlichungen, um Grauschattierungen zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="5ecfd-123">The technique is similar to the half-toning used in black-and-white publications to achieve shades of gray.</span></span>

</dd> <dt>

<span data-ttu-id="5ecfd-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**doppelte Pufferung**</span><span class="sxs-lookup"><span data-stu-id="5ecfd-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**double buffering**</span></span>
</dt> <dd>

<span data-ttu-id="5ecfd-125">Die Verwendung von OpenGL-Kontexten, in denen die Vorder-und Hintergrund Farb Puffer doppelt gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="5ecfd-125">Using OpenGL contexts in which both front and back color buffers are double-buffered.</span></span> <span data-ttu-id="5ecfd-126">Die Smooth Animation wird durch Rendering in nur den zurück-Puffer (der nicht angezeigt wird) ausgeführt und bewirkt dann, dass die Vorder-und Hintergrund Puffer ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="5ecfd-126">Smooth animation is accomplished by rendering into only the back buffer (which isn't displayed), then causing the front and back buffers to be swapped.</span></span>

</dd> </dl>

 

 




