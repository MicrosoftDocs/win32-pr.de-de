---
description: Indiziertes Vertex-Blending erweitert die Scheitelpunkt Mischungs Unterstützung in Direct3D, damit Matrizen zum Mischen verwendet werden können.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Indiziertes Vertex-Blending (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480715"
---
# <a name="indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="3f41f-103">Indiziertes Vertex-Blending (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3f41f-103">Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="3f41f-104">Indiziertes Vertex-Blending erweitert die Scheitelpunkt Mischungs Unterstützung in Direct3D, damit Matrizen zum Mischen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3f41f-104">Indexed vertex blending extends the vertex blending support in Direct3D to allow matrices to be used for blending.</span></span> <span data-ttu-id="3f41f-105">Auf diese Matrizen wird mithilfe eines Matrix Indexes verwiesen.</span><span class="sxs-lookup"><span data-stu-id="3f41f-105">These matrices are referred to by using a matrix index.</span></span> <span data-ttu-id="3f41f-106">Diese Indizes werden pro Scheitelpunkt Basis bereitgestellt und verweisen auf eine Palette von bis zu 256 Matrizen.</span><span class="sxs-lookup"><span data-stu-id="3f41f-106">These indices are supplied on a per-vertex basis and refer to a palette of up to 256 matrices.</span></span> <span data-ttu-id="3f41f-107">Jeder Index ist 8 Bit, und jeder Scheitelpunkt kann bis zu vier Indizes aufweisen, sodass vier Matrizen pro Scheitelpunkt gemischt werden können.</span><span class="sxs-lookup"><span data-stu-id="3f41f-107">Each index is 8 bits and each vertex can have up to four indices, which allows four matrices to be blended per vertex.</span></span> <span data-ttu-id="3f41f-108">Die Indizes werden in ein DWORD gepackt.</span><span class="sxs-lookup"><span data-stu-id="3f41f-108">The indices are packed into a DWORD.</span></span> <span data-ttu-id="3f41f-109">Da Indizes pro Scheitelpunkt Basis angegeben werden, können sich bis zu 12 Matrizen auf ein einzelnes Dreieck auswirken, und jede Matrix in der Palette kann die Scheitel Punkte eines zeichnen-Aufrufs beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="3f41f-109">Because indices are specified on a per-vertex basis, up to 12 matrices can affect a single triangle, and any matrix in the palette can affect the vertices of one draw call.</span></span> <span data-ttu-id="3f41f-110">Dieser Ansatz bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="3f41f-110">This approach has the following advantages.</span></span>

-   <span data-ttu-id="3f41f-111">Es ermöglicht mehr Matrizen, sich auf ein einzelnes Dreieck zu auswirken.</span><span class="sxs-lookup"><span data-stu-id="3f41f-111">It enables more matrices to affect a single triangle.</span></span>
-   <span data-ttu-id="3f41f-112">Dadurch können mehr gemischte Dreiecke im selben zeichnen-Befehl weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3f41f-112">It enables more blended triangles to be passed in the same draw call.</span></span>
-   <span data-ttu-id="3f41f-113">Die Vertex-Mischung ist unabhängig von Dreiecks Indizes.</span><span class="sxs-lookup"><span data-stu-id="3f41f-113">It makes vertex blending independent of triangle indices.</span></span> <span data-ttu-id="3f41f-114">Dies ermöglicht die Zusammenarbeit progressiver Netze in Verbindung mit der Vertex-Mischung.</span><span class="sxs-lookup"><span data-stu-id="3f41f-114">This enables progressive meshes to work in conjunction with vertex blending.</span></span>

<span data-ttu-id="3f41f-115">Ein Nachteil dieses Ansatzes besteht darin, dass er nicht mit gekrümmten Oberflächen primitiven funktioniert, wenn das Mosaik vor der Scheitelpunkt Verarbeitung auftritt.</span><span class="sxs-lookup"><span data-stu-id="3f41f-115">One disadvantage of this approach is that it does not work with curved-surface primitives when tessellation occurs before vertex processing.</span></span>

<span data-ttu-id="3f41f-116">Im folgenden Diagramm wird veranschaulicht, wie sich vier Matrizen auf einen Scheitelpunkt auswirken können.</span><span class="sxs-lookup"><span data-stu-id="3f41f-116">The following diagram demonstrates how four matrices can affect a vertex.</span></span> <span data-ttu-id="3f41f-117">Jeder Scheitelpunkt verfügt über bis zu vier Indizes, sodass vier Matrizen pro Scheitelpunkt gemischt werden können.</span><span class="sxs-lookup"><span data-stu-id="3f41f-117">Each vertex has up to four indices, so four matrices can be blended per vertex.</span></span> <span data-ttu-id="3f41f-118">Das Diagramm verwendet die Matrizen, die bei 0, 2, 5 und 6 indiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="3f41f-118">The diagram uses the matrices indexed at 0, 2, 5, and 6.</span></span>

![Diagramm der indizierten Vertex-Mischung mithilfe von 4 von 256 verfügbaren Matrizen](images/dword1.png)

<span data-ttu-id="3f41f-120">Im folgenden Diagramm wird veranschaulicht, wie sich bis zu 12 Matrizen auf ein Dreieck auswirken können.</span><span class="sxs-lookup"><span data-stu-id="3f41f-120">The following diagram demonstrates how up to 12 matrices can affect a triangle.</span></span> <span data-ttu-id="3f41f-121">Durch die Verwendung von Indizes, die pro Scheitelpunkt Basis angegeben werden, können bis zu 12 Matrizen das Dreieck beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="3f41f-121">Using indices specified on a per-vertex basis, up to 12 matrices can affect the triangle.</span></span>

![Diagramm der indizierten Vertex-Blending für ein Dreieck mithilfe von 12 von 256 verfügbaren Matrizen](images/dword2.png)

<span data-ttu-id="3f41f-123">Die folgende Gleichung bestimmt den allgemeinen Fall, dass Matrizen einen Scheitelpunkt beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="3f41f-123">The following equation determines the general case for how matrices effect a vertex.</span></span>

![Gleichung der indizierten Vertex-Blending](images/indexedvblend.png)

<span data-ttu-id="3f41f-125">V <sub>Model</sub> ist die Vertex-Position des Eingabe Modell Raums.</span><span class="sxs-lookup"><span data-stu-id="3f41f-125">V <sub>model</sub> is the input model space vertex position.</span></span> <span data-ttu-id="3f41f-126">Index0.. Index3 sind die pro-Vertex-Matrix Indizes, die in ein DWORD gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="3f41f-126">Index0..Index3 are the per-vertex matrix indices packed into a DWORD.</span></span> <span data-ttu-id="3f41f-127">M \[ \] ist das Array von Welt Matrizen, die in indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="3f41f-127">M\[\] is the array of world matrices that get indexed into.</span></span> <span data-ttu-id="3f41f-128">b ₀.. b-Gewichtung sind die Blend-Gewichtungen.</span><span class="sxs-lookup"><span data-stu-id="3f41f-128">b₀..b₂ are the blend weights.</span></span> <span data-ttu-id="3f41f-129">V<sub>World</sub> ist die Ausgabe Raum-Vertex-Position.</span><span class="sxs-lookup"><span data-stu-id="3f41f-129">V<sub>world</sub> is the output world space vertex position.</span></span>

<span data-ttu-id="3f41f-130">Weitere Informationen zum indizierten Vertex-Blending finden [Sie unter Verwenden der indizierten vertexmischung (Direct3D 9)](using-indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="3f41f-130">For more information about indexed vertex blending, see [Using Indexed Vertex Blending (Direct3D 9)](using-indexed-vertex-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f41f-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f41f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f41f-132">Geometrie Mischung</span><span class="sxs-lookup"><span data-stu-id="3f41f-132">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



