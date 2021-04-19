---
description: Während des Renderings interpoliert die Pipeline Scheitelpunkt Daten in jedem Dreieck.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Dreiecks interpolung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346834"
---
# <a name="triangle-interpolation-direct3d-9"></a><span data-ttu-id="d5bb6-103">Dreiecks interpolung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d5bb6-103">Triangle Interpolation (Direct3D 9)</span></span>

<span data-ttu-id="d5bb6-104">Während des Renderings interpoliert die Pipeline Scheitelpunkt Daten in jedem Dreieck.</span><span class="sxs-lookup"><span data-stu-id="d5bb6-104">During rendering, the pipeline interpolates vertex data across each triangle.</span></span> <span data-ttu-id="d5bb6-105">Bei Scheitelpunkt Daten kann es sich um eine große Bandbreite von Daten handeln, die Sie einschließen können (aber nicht beschränkt auf): diffuse Farbe, Glanz Farbe, diffuse Alpha (Dreiecks Deckkraft), Glanz Alpha und einen Nebel Faktor (von Glanz Alpha für die Vertex-Pipeline mit fester Funktion und aus dem Nebel Register für eine programmierbare vertexpipeline entnommen).</span><span class="sxs-lookup"><span data-stu-id="d5bb6-105">Vertex data can be a broad variety of data and can include (but is not limited to): diffuse color, specular color, diffuse alpha (triangle opacity), specular alpha, and a fog factor (taken from specular alpha for fixed function vertex pipeline and from fog register for programmable vertex pipeline).</span></span> <span data-ttu-id="d5bb6-106">Die Vertex-Daten werden durch die [Vertexdeklaration (Direct3D 9)](vertex-declaration.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="d5bb6-106">The vertex data is defined by the [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

<span data-ttu-id="d5bb6-107">Bei einigen Scheitelpunkt Daten ist die Interpolation vom aktuellen Schattierungs Modus abhängig, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d5bb6-107">For some vertex data, the interpolation is dependent on the current shading mode, as shown in the following table.</span></span>



| <span data-ttu-id="d5bb6-108">Schattierungs Modus</span><span class="sxs-lookup"><span data-stu-id="d5bb6-108">Shading mode</span></span> | <span data-ttu-id="d5bb6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5bb6-109">Description</span></span>                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5bb6-110">Flach</span><span class="sxs-lookup"><span data-stu-id="d5bb6-110">Flat</span></span>         | <span data-ttu-id="d5bb6-111">Nur der Nebel Faktor wird im flatschatmodus interpoliert.</span><span class="sxs-lookup"><span data-stu-id="d5bb6-111">Only the fog factor is interpolated in flat shade mode.</span></span> <span data-ttu-id="d5bb6-112">Für alle anderen interinterpolierten Werte wird die Farbe des ersten Scheitel Punkts im Dreieck auf die gesamte Oberfläche angewendet.</span><span class="sxs-lookup"><span data-stu-id="d5bb6-112">For all other interpolated values, the color of the first vertex in the triangle is applied across the entire face.</span></span> |
| <span data-ttu-id="d5bb6-113">Gouraud</span><span class="sxs-lookup"><span data-stu-id="d5bb6-113">Gouraud</span></span>      | <span data-ttu-id="d5bb6-114">Lineare Interpolationen werden zwischen allen drei Scheitel Punkten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5bb6-114">Linear interpolation is performed between all three vertices.</span></span>                                                                                                               |



 

<span data-ttu-id="d5bb6-115">Die diffuse Farbe und die Glanz Farbe werden je nach Farbmodell anders behandelt.</span><span class="sxs-lookup"><span data-stu-id="d5bb6-115">The diffuse color and specular color are treated differently, depending on the color model.</span></span> <span data-ttu-id="d5bb6-116">Im RGB-Farbmodell verwendet das System die roten, grünen und blauen Farbkomponenten in der interpolung.</span><span class="sxs-lookup"><span data-stu-id="d5bb6-116">In the RGB color model, the system uses the red, green, and blue color components in the interpolation.</span></span>

<span data-ttu-id="d5bb6-117">Die Alpha Komponente einer Farbe wird als separater interinterintererter Wert behandelt, da Gerätetreiber Transparenz auf zwei verschiedene Arten implementieren können: mithilfe von Textur Mischungen oder mithilfe von stippling.</span><span class="sxs-lookup"><span data-stu-id="d5bb6-117">The alpha component of a color is treated as a separate interpolated value because device drivers can implement transparency in two different ways: by using texture blending or by using stippling.</span></span>

<span data-ttu-id="d5bb6-118">Verwenden Sie den ShadeCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur, um zu bestimmen, welche Formen der Interpolationen der aktuelle Gerätetreiber unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d5bb6-118">Use the ShadeCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure to determine what forms of interpolation the current device driver supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5bb6-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5bb6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5bb6-120">Koordinatensysteme und Geometrie</span><span class="sxs-lookup"><span data-stu-id="d5bb6-120">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



