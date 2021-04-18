---
description: Der Schattierungs Modus zum rendieren eines Polygons hat eine Tiefe Auswirkung auf seine Darstellung. Mit den Schattierungs Modi wird die Intensität der Farbe und der Beleuchtung an einem beliebigen Punkt auf einer Polygon Seite festgelegt. Direct3D unterstützt zwei Schattierungs Modi.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Schattierungs Modi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564619"
---
# <a name="shading-modes-direct3d-9"></a><span data-ttu-id="2cc4c-105">Schattierungs Modi (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2cc4c-105">Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="2cc4c-106">Der Schattierungs Modus zum rendieren eines Polygons hat eine Tiefe Auswirkung auf seine Darstellung.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-106">The shading mode used to render a polygon has a profound effect on its appearance.</span></span> <span data-ttu-id="2cc4c-107">Mit den Schattierungs Modi wird die Intensität der Farbe und der Beleuchtung an einem beliebigen Punkt auf einer Polygon Seite festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-107">Shading modes determine the intensity of color and lighting at any point on a polygon face.</span></span> <span data-ttu-id="2cc4c-108">Direct3D unterstützt zwei Schattierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-108">Direct3D supports two shading modes.</span></span>

-   [<span data-ttu-id="2cc4c-109">Flatschattierung</span><span class="sxs-lookup"><span data-stu-id="2cc4c-109">Flat Shading</span></span>](#flat-shading)
-   [<span data-ttu-id="2cc4c-110">Gouraud-Schattierung</span><span class="sxs-lookup"><span data-stu-id="2cc4c-110">Gouraud Shading</span></span>](#gouraud-shading)

## <a name="flat-shading"></a><span data-ttu-id="2cc4c-111">Flatschattierung</span><span class="sxs-lookup"><span data-stu-id="2cc4c-111">Flat Shading</span></span>

<span data-ttu-id="2cc4c-112">Im Flatshading-Modus rendert die Direct3D-Renderingpipeline ein Polygon und verwendet dabei die Farbe des Polygon Materials im ersten Scheitelpunkt als Farbe für das gesamte Polygon.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-112">In the flat shading mode, the Direct3D rendering pipeline renders a polygon, using the color of the polygon material at its first vertex as the color for the entire polygon.</span></span> <span data-ttu-id="2cc4c-113">3D-Objekte, die mit flacher Schattierung gerendert werden, haben sichtbare Kanten zwischen Polygonen, wenn Sie nicht Coplanar sind.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-113">3D objects that are rendered with flat shading have visibly sharp edges between polygons if they are not coplanar.</span></span>

<span data-ttu-id="2cc4c-114">Die folgende Abbildung zeigt eine mit flacher Schattierung gerenderte Teekanne.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-114">The following illustration shows a teapot rendered with flat shading.</span></span> <span data-ttu-id="2cc4c-115">Die Gliederung der einzelnen Polygon ist eindeutig sichtbar.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-115">The outline of each polygon is clearly visible.</span></span> <span data-ttu-id="2cc4c-116">Die flache Schattierung ist die schnellste Form der Schattierung.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-116">Flat shading is the fastest form of shading.</span></span>

![Darstellung eines Teekanne mit flacher Schattierung](images/flattea.png)

## <a name="gouraud-shading"></a><span data-ttu-id="2cc4c-118">Gouraud-Schattierung</span><span class="sxs-lookup"><span data-stu-id="2cc4c-118">Gouraud Shading</span></span>

<span data-ttu-id="2cc4c-119">Wenn Direct3D ein Polygon mithilfe von Gouraud-Schattierung rendert, wird für jeden Scheitelpunkt eine Farbe berechnet, indem der Scheitelpunkt normale und Beleuchtungs Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-119">When Direct3D renders a polygon using Gouraud shading, it computes a color for each vertex by using the vertex normal and lighting parameters.</span></span> <span data-ttu-id="2cc4c-120">Dann interpoliert Sie die Farbe auf der Vorderseite der Polygone, die die Interpolation linear durchführt.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-120">Then, it interpolates the color across the face of the polygons The interpolation is done linearly.</span></span> <span data-ttu-id="2cc4c-121">Wenn z. b. die rote Komponente der Farbe von Vertex 1 0,8 und die rote Komponente von Vertex 2 0,4 ist, wenn der Modus "Gouraud-Schattierung" und das RGB-Farbmodell verwendet werden, weist das Direct3D-Beleuchtungs Modul dem Pixel in der Mitte der Linie zwischen diesen Scheitel Punkten eine rote Komponente von 0,6 zu.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-121">For example, if the red component of the color of vertex 1 is 0.8 and the red component of vertex 2 is 0.4, using the Gouraud shading mode and the RGB color model, the Direct3D lighting module assigns a red component of 0.6 to the pixel at the midpoint of the line between these vertices.</span></span>

<span data-ttu-id="2cc4c-122">In der folgenden Abbildung wird die Schattierung von Gouraud veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-122">The following illustration demonstrates Gouraud shading.</span></span> <span data-ttu-id="2cc4c-123">Diese Teekanne besteht aus vielen flachen, dreieckigen Polygonen.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-123">This teapot is composed of many flat, triangular polygons.</span></span> <span data-ttu-id="2cc4c-124">Allerdings wird durch die Schattierung von Gouraud die Oberfläche des Objekts gekrümmert und glatt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-124">However, Gouraud shading makes the surface of the object appear curved and smooth.</span></span>

![Abbildung von "Teekanne" mithilfe von "Gouraud-Schattierung"](images/gourtea.png)

<span data-ttu-id="2cc4c-126">Mithilfe von Gouraud-Schattierung können auch Objekte mit Spitzen Kanten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2cc4c-126">Gouraud shading can also be used to display objects with sharp edges.</span></span>

<span data-ttu-id="2cc4c-127">Weitere Informationen finden Sie unter [Gesichts-und Scheitel Punkte (normale Vektoren) (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="2cc4c-127">For more information, see [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cc4c-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2cc4c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cc4c-129">Schattierung</span><span class="sxs-lookup"><span data-stu-id="2cc4c-129">Shading</span></span>](shading.md)
</dt> </dl>

 

 



