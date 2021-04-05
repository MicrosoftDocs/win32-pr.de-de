---
title: Primitive und Befehle
description: Primitive und Befehle
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, primitive
- OpenGL, Befehle
- Primitives OpenGL
- Befehle OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709461"
---
# <a name="primitives-and-commands"></a><span data-ttu-id="4413b-107">Primitive und Befehle</span><span class="sxs-lookup"><span data-stu-id="4413b-107">Primitives and Commands</span></span>

<span data-ttu-id="4413b-108">OpenGL zeichnet *primitive* Punkte, Liniensegmente oder polygonssubject in mehreren auswählbaren Modi.</span><span class="sxs-lookup"><span data-stu-id="4413b-108">OpenGL draws *primitives* points, line segments, or polygonssubject to several selectable modes.</span></span> <span data-ttu-id="4413b-109">Sie können Modi unabhängig voneinander steuern.</span><span class="sxs-lookup"><span data-stu-id="4413b-109">You can control modes independently of one another.</span></span> <span data-ttu-id="4413b-110">Das Festlegen eines Modus wirkt sich nicht darauf aus, ob andere Modi festgelegt sind (obwohl viele Modi interagieren können, um zu bestimmen, was letztendlich im Framebuffer endet).</span><span class="sxs-lookup"><span data-stu-id="4413b-110">That is, setting one mode doesn't affect whether other modes are set (although many modes may interact to determine what eventually ends up in the framebuffer).</span></span> <span data-ttu-id="4413b-111">Um primitive anzugeben, Modi festzulegen und andere OpenGL-Vorgänge auszuführen, geben Sie Befehle in Form von Funktionsaufrufen aus.</span><span class="sxs-lookup"><span data-stu-id="4413b-111">To specify primitives, set modes, and perform other OpenGL operations, you issue commands in the form of function calls.</span></span>

<span data-ttu-id="4413b-112">Primitive werden durch eine Gruppe mit einem oder mehreren *Vertices* definiert.</span><span class="sxs-lookup"><span data-stu-id="4413b-112">Primitives are defined by a group of one or more *vertices*.</span></span> <span data-ttu-id="4413b-113">Ein Scheitelpunkt definiert einen Punkt, einen Endpunkt einer Linie oder eine Ecke eines Polygons, in dem zwei Ränder übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4413b-113">A vertex defines a point, an endpoint of a line, or a corner of a polygon where two edges meet.</span></span> <span data-ttu-id="4413b-114">Daten (bestehend aus Scheitelpunkt Koordinaten, Farben, normellen, Texturkoordinaten und randflags) werden einem Scheitelpunkt zugeordnet, und jeder Scheitelpunkt und die zugehörigen Daten werden unabhängig voneinander und in der richtigen Reihenfolge verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="4413b-114">Data (consisting of vertex coordinates, colors, normals, texture coordinates, and edge flags) is associated with a vertex, and each vertex and its associated data are processed independently, in order, and in the same way.</span></span> <span data-ttu-id="4413b-115">Die einzige Ausnahme von dieser Regel sind Fälle, in denen die Gruppe der Vertices abgeschnitten werden muss, damit ein bestimmtes primitiv in einen angegebenen Bereich passt.</span><span class="sxs-lookup"><span data-stu-id="4413b-115">The only exceptions to this rule are cases in which the group of vertices must be clipped so that a particular primitive fits within a specified region.</span></span> <span data-ttu-id="4413b-116">In diesem Fall können Scheitelpunkt Daten geändert und neue Vertices erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4413b-116">In this case, vertex data may be modified and new vertices created.</span></span> <span data-ttu-id="4413b-117">Der clippingtyp hängt davon ab, welches primitive die Gruppe von Vertices darstellt.</span><span class="sxs-lookup"><span data-stu-id="4413b-117">The type of clipping depends on which primitive the group of vertices represents.</span></span>

<span data-ttu-id="4413b-118">Befehle werden immer in der Reihenfolge verarbeitet, in der Sie empfangen werden, obwohl es möglicherweise zu einer unbestimmten Verzögerung kommt, bevor ein Befehl in Kraft tritt.</span><span class="sxs-lookup"><span data-stu-id="4413b-118">Commands are always processed in the order in which they are received, although there may be an indeterminate delay before a command takes effect.</span></span> <span data-ttu-id="4413b-119">Dies bedeutet, dass jedes primitive vollständig gezeichnet wird, bevor der nachfolgende Befehl in Kraft tritt.</span><span class="sxs-lookup"><span data-stu-id="4413b-119">This means that each primitive is drawn completely before any subsequent command takes effect.</span></span> <span data-ttu-id="4413b-120">Dies bedeutet auch, dass Zustands Abfrage Befehle Daten zurückgeben, die mit der vollständigen Ausführung aller zuvor ausgestellten OpenGL-Befehle konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="4413b-120">It also means that state-querying commands return data that is consistent with complete execution of all previously issued OpenGL commands.</span></span>

 

 




