---
title: Clipping (OpenGL)
description: Clipping erfolgt in zwei Schritten.
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- OpenGL-Verarbeitungs Pipeline, Clipping
- Clipping OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa35458e7e0a137759fe22be95f4b399b4d56b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391419"
---
# <a name="clipping-opengl"></a><span data-ttu-id="3267d-105">Clipping (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="3267d-105">Clipping (OpenGL)</span></span>

<span data-ttu-id="3267d-106">Das Clipping erfolgt in zwei Schritten:</span><span class="sxs-lookup"><span data-stu-id="3267d-106">Clipping occurs in two steps:</span></span>

1.  <span data-ttu-id="3267d-107">**Anzeigen von Volume clippingapplication-Specific Clipping.**</span><span class="sxs-lookup"><span data-stu-id="3267d-107">**View volume clippingApplication-specific clipping.**</span></span> <span data-ttu-id="3267d-108">Unmittelbar nach dem Zusammenstellen von primitiven werden Sie bei Bedarf für alle clippingflächen, die Sie mit [**glclipplane**](glclipplane.md)definiert haben, in Augen Koordinaten abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="3267d-108">Immediately after primitives are assembled, they're clipped in eye coordinates as necessary for any clipping planes you've defined with [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="3267d-109">(OpenGL erfordert Unterstützung für mindestens sechs anwendungsspezifische Clippingebenen.)</span><span class="sxs-lookup"><span data-stu-id="3267d-109">(OpenGL requires support for at least six such application-specific clipping planes.)</span></span>
2.  <span data-ttu-id="3267d-110">Primitive werden von der Projektions Matrix in Clip Koordinaten transformiert und durch das entsprechende Ansichts Volume abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="3267d-110">Primitives are transformed by the projection matrix into clip coordinates and clipped by the corresponding view volume.</span></span> <span data-ttu-id="3267d-111">Diese Matrix kann von den Matrix Transformations Funktionen gesteuert werden (siehe [Matrix Transformationen](matrix-transformations.md)), wird jedoch in der Regel von [**glfrustum**](glfrustum.md) oder [**glortho**](glortho.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="3267d-111">This matrix can be controlled by the matrix transformation functions (see [Matrix Transformations](matrix-transformations.md)) but is typically specified by [**glFrustum**](glfrustum.md) or [**glOrtho**](glortho.md).</span></span>

<span data-ttu-id="3267d-112">Punkte, Liniensegmente und Polygone werden während des Clipping anders behandelt:</span><span class="sxs-lookup"><span data-stu-id="3267d-112">Points, line segments, and polygons are handled differently during clipping:</span></span>

-   <span data-ttu-id="3267d-113">Punkte werden entweder in Ihrem ursprünglichen Zustand (wenn Sie sich im Ausschneide Volume befinden) aufbewahrt oder verworfen (wenn Sie sich außerhalb des Clip-Volumes befinden).</span><span class="sxs-lookup"><span data-stu-id="3267d-113">Points are either retained in their original state (if they're inside the clip volume) or discarded (if they're outside the clip volume).</span></span>
-   <span data-ttu-id="3267d-114">Wenn Teile von Liniensegmenten oder Polygone außerhalb des Clip Volumens liegen, werden an den Clip Punkten neue Scheitel Punkte generiert.</span><span class="sxs-lookup"><span data-stu-id="3267d-114">If portions of line segments or polygons are outside the clip volume, new vertices are generated at the clip points.</span></span>
-   <span data-ttu-id="3267d-115">Bei Polygonen muss möglicherweise ein ganzer Rand zwischen neuen Scheitel Punkten erstellt werden, die an den Clip Punkten generiert werden.</span><span class="sxs-lookup"><span data-stu-id="3267d-115">For polygons, an entire edge may need to be constructed between new vertices generated at the clip points.</span></span>
-   <span data-ttu-id="3267d-116">Bei Liniensegmenten und Polygonen, die abgeschnitten werden, werden das Edge-Flag, die Farbe und die Textur Informationen allen neuen Scheitel Punkten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3267d-116">For line segments and polygons that are clipped, the edge flag, color, and texture information is assigned to all new vertices.</span></span>

 

 




