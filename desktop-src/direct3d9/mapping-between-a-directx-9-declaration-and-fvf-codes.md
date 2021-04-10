---
description: Diese Tabelle ordnet Member einer D3DVERTEXELEMENT9-Deklaration einem FVF-Code zu.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Zuordnung zwischen einer Direct3D-Deklaration und einem f-Code (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124478"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a><span data-ttu-id="73715-103">Zuordnung zwischen einer Direct3D-Deklaration und einem f-Code (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="73715-103">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="73715-104">Diese Tabelle ordnet Member einer [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Deklaration einem FVF-Code zu.</span><span class="sxs-lookup"><span data-stu-id="73715-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a FVF code.</span></span>



| <span data-ttu-id="73715-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="73715-105">Data type</span></span>             | <span data-ttu-id="73715-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="73715-106">Usage</span></span>                      | <span data-ttu-id="73715-107">Verwendungs Index</span><span class="sxs-lookup"><span data-stu-id="73715-107">Usage index</span></span> | <span data-ttu-id="73715-108">F-VF</span><span class="sxs-lookup"><span data-stu-id="73715-108">FVF</span></span>                       |
|-----------------------|----------------------------|-------------|---------------------------|
| <span data-ttu-id="73715-109">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="73715-109">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="73715-110">D3DDECLUSAGE- \_ Position</span><span class="sxs-lookup"><span data-stu-id="73715-110">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="73715-111">0</span><span class="sxs-lookup"><span data-stu-id="73715-111">0</span></span>           | <span data-ttu-id="73715-112">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="73715-112">D3DFVF\_XYZ</span></span>               |
| <span data-ttu-id="73715-113">D3DDECLTYPE \_ float4</span><span class="sxs-lookup"><span data-stu-id="73715-113">D3DDECLTYPE\_FLOAT4</span></span>   | <span data-ttu-id="73715-114">D3DDECLUSAGE \_ positiont</span><span class="sxs-lookup"><span data-stu-id="73715-114">D3DDECLUSAGE\_POSITIONT</span></span>    | <span data-ttu-id="73715-115">0</span><span class="sxs-lookup"><span data-stu-id="73715-115">0</span></span>           | <span data-ttu-id="73715-116">D3DFVF \_ xyzrhw</span><span class="sxs-lookup"><span data-stu-id="73715-116">D3DFVF\_XYZRHW</span></span>            |
| <span data-ttu-id="73715-117">D3DDECLTYPE \_ floatn</span><span class="sxs-lookup"><span data-stu-id="73715-117">D3DDECLTYPE\_FLOATn</span></span>   | <span data-ttu-id="73715-118">D3DDECLUSAGE \_ blendweight</span><span class="sxs-lookup"><span data-stu-id="73715-118">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="73715-119">0</span><span class="sxs-lookup"><span data-stu-id="73715-119">0</span></span>           | <span data-ttu-id="73715-120">D3DFVF \_ xyzbn</span><span class="sxs-lookup"><span data-stu-id="73715-120">D3DFVF\_XYZBn</span></span>             |
| <span data-ttu-id="73715-121">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="73715-121">D3DDECLTYPE\_UBYTE4</span></span>   | <span data-ttu-id="73715-122">D3DDECLUSAGE \_ blendindices</span><span class="sxs-lookup"><span data-stu-id="73715-122">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="73715-123">0</span><span class="sxs-lookup"><span data-stu-id="73715-123">0</span></span>           | <span data-ttu-id="73715-124">D3DFVF \_ xyzb (ngewichtungen + 1)</span><span class="sxs-lookup"><span data-stu-id="73715-124">D3DFVF\_XYZB (nWeights+1)</span></span> |
| <span data-ttu-id="73715-125">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="73715-125">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="73715-126">D3DDECLUSAGE \_ Normal</span><span class="sxs-lookup"><span data-stu-id="73715-126">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="73715-127">0</span><span class="sxs-lookup"><span data-stu-id="73715-127">0</span></span>           | <span data-ttu-id="73715-128">D3DFVF \_ Normal</span><span class="sxs-lookup"><span data-stu-id="73715-128">D3DFVF\_NORMAL</span></span>            |
| <span data-ttu-id="73715-129">D3DDECLTYPE \_ FLOAT1</span><span class="sxs-lookup"><span data-stu-id="73715-129">D3DDECLTYPE\_FLOAT1</span></span>   | <span data-ttu-id="73715-130">D3DDECLUSAGE \_ Psize</span><span class="sxs-lookup"><span data-stu-id="73715-130">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="73715-131">0</span><span class="sxs-lookup"><span data-stu-id="73715-131">0</span></span>           | <span data-ttu-id="73715-132">D3DFVF \_ Psize</span><span class="sxs-lookup"><span data-stu-id="73715-132">D3DFVF\_PSIZE</span></span>             |
| <span data-ttu-id="73715-133">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="73715-133">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="73715-134">D3DDECLUSAGE- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="73715-134">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="73715-135">0</span><span class="sxs-lookup"><span data-stu-id="73715-135">0</span></span>           | <span data-ttu-id="73715-136">D3DFVF \_ diffuses</span><span class="sxs-lookup"><span data-stu-id="73715-136">D3DFVF\_DIFFUSE</span></span>           |
| <span data-ttu-id="73715-137">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="73715-137">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="73715-138">D3DDECLUSAGE- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="73715-138">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="73715-139">1</span><span class="sxs-lookup"><span data-stu-id="73715-139">1</span></span>           | <span data-ttu-id="73715-140">D3DFVF \_ Glanz</span><span class="sxs-lookup"><span data-stu-id="73715-140">D3DFVF\_SPECULAR</span></span>          |
| <span data-ttu-id="73715-141">D3DDECLTYPE \_ floatm</span><span class="sxs-lookup"><span data-stu-id="73715-141">D3DDECLTYPE\_FLOATm</span></span>   | <span data-ttu-id="73715-142">D3DDECLUSAGE \_ texcoord</span><span class="sxs-lookup"><span data-stu-id="73715-142">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="73715-143">n</span><span class="sxs-lookup"><span data-stu-id="73715-143">n</span></span>           | <span data-ttu-id="73715-144">D3DFVF \_ texcoordsizem (n)</span><span class="sxs-lookup"><span data-stu-id="73715-144">D3DFVF\_TEXCOORDSIZEm(n)</span></span>  |
| <span data-ttu-id="73715-145">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="73715-145">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="73715-146">D3DDECLUSAGE- \_ Position</span><span class="sxs-lookup"><span data-stu-id="73715-146">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="73715-147">1</span><span class="sxs-lookup"><span data-stu-id="73715-147">1</span></span>           | <span data-ttu-id="73715-148">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="73715-148">N/A</span></span>                       |
| <span data-ttu-id="73715-149">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="73715-149">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="73715-150">D3DDECLUSAGE \_ Normal</span><span class="sxs-lookup"><span data-stu-id="73715-150">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="73715-151">1</span><span class="sxs-lookup"><span data-stu-id="73715-151">1</span></span>           | <span data-ttu-id="73715-152">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="73715-152">N/A</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="73715-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73715-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73715-154">Vertex-Deklaration</span><span class="sxs-lookup"><span data-stu-id="73715-154">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



