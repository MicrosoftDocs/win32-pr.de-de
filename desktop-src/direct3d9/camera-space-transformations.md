---
description: Scheitel Punkte im Kamerabereich werden berechnet, indem die Objekt Scheitel Punkte mit der World View Matrix transformiert werden.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Kamera Raum Transformationen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126884"
---
# <a name="camera-space-transformations-direct3d-9"></a><span data-ttu-id="33321-103">Kamera Raum Transformationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="33321-103">Camera Space Transformations (Direct3D 9)</span></span>

<span data-ttu-id="33321-104">Scheitel Punkte im Kamerabereich werden berechnet, indem die Objekt Scheitel Punkte mit der World View Matrix transformiert werden.</span><span class="sxs-lookup"><span data-stu-id="33321-104">Vertices in the camera space are computed by transforming the object vertices with the world view matrix.</span></span>

<span data-ttu-id="33321-105">V = v \* wvmatrix</span><span class="sxs-lookup"><span data-stu-id="33321-105">V = V \* wvMatrix</span></span>

<span data-ttu-id="33321-106">Vertex-Normale werden im Kamerabereich berechnet, indem die Objekt normale mit der umgekehrten Umwandlung der World View Matrix transformiert werden.</span><span class="sxs-lookup"><span data-stu-id="33321-106">Vertex normals, in camera space, are computed by transforming the object normals with the inverse transpose of the world view matrix.</span></span> <span data-ttu-id="33321-107">Die World View Matrix ist möglicherweise orthogonal.</span><span class="sxs-lookup"><span data-stu-id="33321-107">The world view matrix may or may not be orthogonal.</span></span>

<span data-ttu-id="33321-108">N = n \* (wvmatrix ⁻ ¹)<sup>T</sup></span><span class="sxs-lookup"><span data-stu-id="33321-108">N = N \* (wvMatrix⁻¹)<sup>T</sup></span></span>

<span data-ttu-id="33321-109">Die Matrix-Inversion und die Matrix werden in einer 4 x 4-Matrix verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="33321-109">The matrix inversion and matrix transpose operate on a 4x4 matrix.</span></span> <span data-ttu-id="33321-110">Das Multiplizieren kombiniert den normalen mit dem 3X3-Teil der resultierenden 4 x 4-Matrix.</span><span class="sxs-lookup"><span data-stu-id="33321-110">The multiply combines the normal with the 3x3 portion of the resulting 4x4 matrix.</span></span>

<span data-ttu-id="33321-111">Wenn der Rendering-Zustand, D3DRENDERSTATE \_ normalizenormals auf **true** festgelegt ist, werden Scheitelpunkt normale Vektoren nach der Transformation wie folgt normalisiert:</span><span class="sxs-lookup"><span data-stu-id="33321-111">If the render state, D3DRENDERSTATE\_NORMALIZENORMALS is set to **TRUE**, vertex normal vectors are normalized after transformation to camera space as follows:</span></span>

<span data-ttu-id="33321-112">N = Norm (n)</span><span class="sxs-lookup"><span data-stu-id="33321-112">N = norm(N)</span></span>

<span data-ttu-id="33321-113">Die helle Position im Kamerabereich wird berechnet, indem die Licht Quell Position mit der Ansichts Matrix transformiert wird.</span><span class="sxs-lookup"><span data-stu-id="33321-113">Light position in camera space is computed by transforming the light source position with the view matrix.</span></span>

<span data-ttu-id="33321-114">LP = LP- \* vmatrix</span><span class="sxs-lookup"><span data-stu-id="33321-114">Lₚ = Lₚ \* vMatrix</span></span>

<span data-ttu-id="33321-115">Die Richtung des Lichts im Kamera Raum für ein Direktionales Licht wird berechnet, indem die Lichtquellen Richtung der Ansichts Matrix multipliziert, das Ergebnis normalisiert und nealisiert wird.</span><span class="sxs-lookup"><span data-stu-id="33321-115">The direction to the light in camera space for a directional light is computed by multiplying the light source direction by the view matrix, normalizing, and negating the result.</span></span>

<span data-ttu-id="33321-116">L<sub>dir</sub> =-Norm (l<sub>dir</sub> \* wvmatrix)</span><span class="sxs-lookup"><span data-stu-id="33321-116">L<sub>dir</sub> = -norm(L<sub>dir</sub> \* wvMatrix)</span></span>

<span data-ttu-id="33321-117">Für D3DLIGHT \_ Point und D3DLIGHT \_ wird die Richtung "Light" wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="33321-117">For the D3DLIGHT\_POINT and D3DLIGHT\_SPOT the direction to light is computed as follows:</span></span>

<span data-ttu-id="33321-118">L<sub>dir</sub> = Norm (V \* LP), wobei die Parameter in der folgenden Tabelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="33321-118">L<sub>dir</sub> = norm(V \* Lₚ), where the parameters are defined in the following table.</span></span>



| <span data-ttu-id="33321-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="33321-119">Parameter</span></span>       | <span data-ttu-id="33321-120">Standardwert</span><span class="sxs-lookup"><span data-stu-id="33321-120">Default value</span></span> | <span data-ttu-id="33321-121">type</span><span class="sxs-lookup"><span data-stu-id="33321-121">Type</span></span>      | <span data-ttu-id="33321-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33321-122">Description</span></span>                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| <span data-ttu-id="33321-123">L-<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="33321-123">L<sub>dir</sub></span></span> | <span data-ttu-id="33321-124">–</span><span class="sxs-lookup"><span data-stu-id="33321-124">N/A</span></span>           | <span data-ttu-id="33321-125">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="33321-125">D3DVECTOR</span></span> | <span data-ttu-id="33321-126">Richtung Vektor vom Objekt Scheitelpunkt zum Licht</span><span class="sxs-lookup"><span data-stu-id="33321-126">Direction vector from object vertex to the light</span></span>          |
| <span data-ttu-id="33321-127">V</span><span class="sxs-lookup"><span data-stu-id="33321-127">V</span></span>               | <span data-ttu-id="33321-128">–</span><span class="sxs-lookup"><span data-stu-id="33321-128">N/A</span></span>           | <span data-ttu-id="33321-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="33321-129">D3DVECTOR</span></span> | <span data-ttu-id="33321-130">Scheitelpunkt Position im Kamerabereich</span><span class="sxs-lookup"><span data-stu-id="33321-130">Vertex position in camera space</span></span>                           |
| <span data-ttu-id="33321-131">wvmatrix</span><span class="sxs-lookup"><span data-stu-id="33321-131">wvMatrix</span></span>        | <span data-ttu-id="33321-132">Identity</span><span class="sxs-lookup"><span data-stu-id="33321-132">Identity</span></span>      | <span data-ttu-id="33321-133">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="33321-133">D3DMATRIX</span></span> | <span data-ttu-id="33321-134">Zusammengesetzte Matrix mit Transformationen der Welt und Ansicht</span><span class="sxs-lookup"><span data-stu-id="33321-134">Composite matrix containing the world and view transforms</span></span> |
| <span data-ttu-id="33321-135">N</span><span class="sxs-lookup"><span data-stu-id="33321-135">N</span></span>               | <span data-ttu-id="33321-136">–</span><span class="sxs-lookup"><span data-stu-id="33321-136">N/A</span></span>           | <span data-ttu-id="33321-137">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="33321-137">D3DVECTOR</span></span> | <span data-ttu-id="33321-138">Scheitelpunkt normal</span><span class="sxs-lookup"><span data-stu-id="33321-138">Vertex normal</span></span>                                             |
| <span data-ttu-id="33321-139">LP</span><span class="sxs-lookup"><span data-stu-id="33321-139">Lₚ</span></span>              | <span data-ttu-id="33321-140">–</span><span class="sxs-lookup"><span data-stu-id="33321-140">N/A</span></span>           | <span data-ttu-id="33321-141">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="33321-141">D3DVECTOR</span></span> | <span data-ttu-id="33321-142">Helle Position im Kamerabereich</span><span class="sxs-lookup"><span data-stu-id="33321-142">Light position in camera space</span></span>                            |
| <span data-ttu-id="33321-143">vmatrix</span><span class="sxs-lookup"><span data-stu-id="33321-143">vMatrix</span></span>         | <span data-ttu-id="33321-144">Identity</span><span class="sxs-lookup"><span data-stu-id="33321-144">Identity</span></span>      | <span data-ttu-id="33321-145">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="33321-145">D3DMATRIX</span></span> | <span data-ttu-id="33321-146">Matrix mit der Ansichts Transformation</span><span class="sxs-lookup"><span data-stu-id="33321-146">Matrix containing the view transform</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="33321-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33321-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33321-148">Mathematik der Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="33321-148">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



