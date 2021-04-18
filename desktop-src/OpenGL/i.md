---
title: I (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben I beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2c78efce-9aed-4bcd-a254-7bff053b0acd
keywords:
- images
- Bild primitive
- sofortiger Modus
- Index
- IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe340cfbd7dbef3d93cc68ba310d863717225c0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517264"
---
# <a name="i-opengl"></a><span data-ttu-id="47d19-108">I (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="47d19-108">I (OpenGL)</span></span>

<span data-ttu-id="47d19-109">[a](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) I [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="47d19-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) I [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="47d19-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**Klang**</span><span class="sxs-lookup"><span data-stu-id="47d19-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**image**</span></span>
</dt> <dd>

<span data-ttu-id="47d19-111">Ein rechteckiges Array von Pixeln, entweder im Client Speicher oder im Framebuffer.</span><span class="sxs-lookup"><span data-stu-id="47d19-111">A rectangular array of pixels, either in client memory or in the framebuffer.</span></span>

</dd> <dt>

<span data-ttu-id="47d19-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**Bild primitiv**</span><span class="sxs-lookup"><span data-stu-id="47d19-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**image primitive**</span></span> 
</dt> <dd>

<span data-ttu-id="47d19-113">Eine Bitmap oder ein Bild.</span><span class="sxs-lookup"><span data-stu-id="47d19-113">A bitmap or an image.</span></span>

</dd> <dt>

<span data-ttu-id="47d19-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**sofortiger Modus**</span><span class="sxs-lookup"><span data-stu-id="47d19-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**immediate mode**</span></span>
</dt> <dd>

<span data-ttu-id="47d19-115">Der Modus, in dem ein OpenGL-Befehl direkt aufgerufen wird, anstatt aus einer Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="47d19-115">Mode in which an OpenGL command is called directly, rather than from a display list.</span></span> <span data-ttu-id="47d19-116">Es ist kein unmittelbares Bit vorhanden. der Modus im unmittelbaren Modus bezieht sich auf die Verwendung von OpenGL anstelle eines bestimmten Bits des OpenGL-Zustands.</span><span class="sxs-lookup"><span data-stu-id="47d19-116">No immediate-mode bit exists; the mode in immediate mode refers to usage of OpenGL, rather than to a specific bit of OpenGL state.</span></span>

</dd> <dt>

<span data-ttu-id="47d19-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**Sin**</span><span class="sxs-lookup"><span data-stu-id="47d19-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**index**</span></span>
</dt> <dd>

<span data-ttu-id="47d19-118">Ein einzelner Wert, der als absoluter Wert interpretiert wird, nicht als normalisierter Wert in einem angegebenen Bereich (wie eine Komponente).</span><span class="sxs-lookup"><span data-stu-id="47d19-118">A single value that is interpreted as an absolute value, rather than as a normalized value in a specified range (as is a component).</span></span> <span data-ttu-id="47d19-119">Farbindizes sind die Namen von Farben, die von der Anzeige Hardware mithilfe der Farbzuordnung dereferenziert werden.</span><span class="sxs-lookup"><span data-stu-id="47d19-119">Color indexes are the names of colors, which are dereferenced by the display hardware using the color map.</span></span> <span data-ttu-id="47d19-120">Indizes werden in der Regel maskiert und nicht geklemmt, wenn Sie außerhalb des gültigen Bereichs liegen.</span><span class="sxs-lookup"><span data-stu-id="47d19-120">Indexes are typically masked, rather than clamped, when out of range.</span></span> <span data-ttu-id="47d19-121">Beispielsweise wird der Index 0xF7 mit 0x7 maskiert, wenn er in einen 4-Bit-Puffer (Farbe oder Schablone) geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="47d19-121">For example, the index 0xf7 is masked to 0x7 when written to a 4-bit buffer (color or stencil).</span></span> <span data-ttu-id="47d19-122">Farbindizes und Schablonen Indizes werden immer als Indizes und nie als Komponenten behandelt.</span><span class="sxs-lookup"><span data-stu-id="47d19-122">Color indexes and stencil indexes are always treated as indexes, never as components.</span></span>

</dd> <dt>

<span data-ttu-id="47d19-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**IRIS GL**</span><span class="sxs-lookup"><span data-stu-id="47d19-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**IRIS GL**</span></span>
</dt> <dd>

<span data-ttu-id="47d19-124">Proprietäre Grafikbibliothek der Silicon Graphics, entwickelt von 1982 bis 1992.</span><span class="sxs-lookup"><span data-stu-id="47d19-124">Silicon Graphics' proprietary graphics library, developed from 1982 through 1992.</span></span> <span data-ttu-id="47d19-125">OpenGL wurde mit Iris GL als Ausgangspunkt entwickelt.</span><span class="sxs-lookup"><span data-stu-id="47d19-125">OpenGL was designed with IRIS GL as a starting point.</span></span>

</dd> </dl>

 

 




