---
title: OpenGL-Verarbeitungs Pipeline
description: OpenGL-Verarbeitungs Pipeline
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, Verarbeitungs Pipeline
- Pipeline-OpenGL wird verarbeitet
- Pipeline-OpenGL
- Framebuffers, Verarbeitungs Pipeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104570571"
---
# <a name="opengl-processing-pipeline"></a><span data-ttu-id="30400-107">OpenGL-Verarbeitungs Pipeline</span><span class="sxs-lookup"><span data-stu-id="30400-107">OpenGL Processing Pipeline</span></span>

<span data-ttu-id="30400-108">Viele OpenGL-Funktionen werden speziell zum Zeichnen von Objekten verwendet, z. b. Punkte, Linien, Polygone und Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="30400-108">Many OpenGL functions are used specifically for drawing objects such as points, lines, polygons, and bitmaps.</span></span> <span data-ttu-id="30400-109">Einige Funktionen steuern die Art und Weise, wie einige dieser Zeichen auftreten (z. b. solche, die Antialiasing oder Texturierung ermöglichen).</span><span class="sxs-lookup"><span data-stu-id="30400-109">Some functions control the way that some of this drawing occurs (such as those that enable antialiasing or texturing).</span></span> <span data-ttu-id="30400-110">Andere Funktionen betreffen speziell die Frame Puffer-Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="30400-110">Other functions are specifically concerned with framebuffer manipulation.</span></span> <span data-ttu-id="30400-111">In den Themen in diesem Abschnitt wird beschrieben, wie alle OpenGL-Funktionen zusammenarbeiten, um die OpenGL-Verarbeitungs Pipeline zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="30400-111">The topics in this section describe how all of the OpenGL functions work together to create the OpenGL processing pipeline.</span></span> <span data-ttu-id="30400-112">In diesem Abschnitt werden auch die Phasen, in denen die Daten tatsächlich verarbeitet werden, genauer betrachtet und diese Phasen mit OpenGL-Funktionen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="30400-112">This section also takes a closer look at the stages in which data is actually processed, and ties these stages to OpenGL functions.</span></span>

<span data-ttu-id="30400-113">Im folgenden Diagramm wird die OpenGL-Verarbeitungs Pipeline ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="30400-113">The following diagram details the OpenGL processing pipeline.</span></span> <span data-ttu-id="30400-114">Für den Großteil der Pipeline können Sie drei vertikale Pfeile zwischen den Hauptphasen sehen.</span><span class="sxs-lookup"><span data-stu-id="30400-114">For most of the pipeline, you can see three vertical arrows between the major stages.</span></span> <span data-ttu-id="30400-115">Diese Pfeile stellen Scheitel Punkte und die beiden primären Datentypen dar, die Vertices zugeordnet werden können: Farbwerte und Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="30400-115">These arrows represent vertices and the two primary types of data that can be associated with vertices: color values and texture coordinates.</span></span> <span data-ttu-id="30400-116">Beachten Sie außerdem, dass Scheitel Punkte in primitive und dann in Fragmente und schließlich in Pixel im Framebuffer zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="30400-116">Also note that vertices are assembled into primitives, then into fragments, and finally into pixels in the framebuffer.</span></span> <span data-ttu-id="30400-117">Diese fort [Schritte werden in](vertices.md)Scheitel Punkten, [primitiven](primitives.md), [Fragmenten](fragments.md)und [Pixeln](pixels.md)ausführlicher erläutert.</span><span class="sxs-lookup"><span data-stu-id="30400-117">This progression is discussed in more detail in [Vertices](vertices.md), [Primitives](primitives.md), [Fragments](fragments.md), and [Pixels](pixels.md).</span></span>

![Diagramm mit der OpenGL-Verarbeitungs Pipeline.](images/proc01.png)

 

 




