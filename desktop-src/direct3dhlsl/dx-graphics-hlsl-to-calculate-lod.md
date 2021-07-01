---
title: CalculateLevelOfDetail (DirectX HLSL-Texturobjekt)
description: Berechnet die Detailebene.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e307527f93c153f0f78ce58b4d70ead4f7c1bc4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120555"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a><span data-ttu-id="b7aac-103">CalculateLevelOfDetail (DirectX HLSL-Texturobjekt)</span><span class="sxs-lookup"><span data-stu-id="b7aac-103">CalculateLevelOfDetail (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="b7aac-104">Berechnet die Detailebene.</span><span class="sxs-lookup"><span data-stu-id="b7aac-104">Calculates the level of detail.</span></span>

<span data-ttu-id="b7aac-105">ret Object.CalculateLevelOfDetail( sampler \_ state S, float x );</span><span class="sxs-lookup"><span data-stu-id="b7aac-105">ret Object.CalculateLevelOfDetail( sampler\_state S, float x );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="b7aac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7aac-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7aac-107">Element</span><span class="sxs-lookup"><span data-stu-id="b7aac-107">Item</span></span></th>
<th><span data-ttu-id="b7aac-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7aac-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7aac-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="b7aac-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="b7aac-110">Beliebiger <a href="dx-graphics-hlsl-to-type.md">Texturobjekttyp</a> (außer Texture2DMS und Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="b7aac-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7aac-111"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="b7aac-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="b7aac-112">[in] Ein <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Samplerzustand.</a></span><span class="sxs-lookup"><span data-stu-id="b7aac-112">[in] A <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Sampler state</a>.</span></span> <span data-ttu-id="b7aac-113">Dies ist ein Objekt, das in einer Effektdatei deklariert ist, die Zustandszuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="b7aac-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7aac-114"><span id="x"></span><span id="X"></span><em>X</em></span><span class="sxs-lookup"><span data-stu-id="b7aac-114"><span id="x"></span><span id="X"></span><em>x</em></span></span><br/></td>
<td><span data-ttu-id="b7aac-115">[in] Der oder die linearen Interpolationswerte, bei denen es sich um eine Gleitkommazahl zwischen 0,0 und einschließlich 1,0 handelt.</span><span class="sxs-lookup"><span data-stu-id="b7aac-115">[in] The linear interpolation value or values, which is a floating-point number between 0.0 and 1.0 inclusive.</span></span> <span data-ttu-id="b7aac-116">Die Anzahl der Komponenten hängt vom Texturobjekttyp ab.</span><span class="sxs-lookup"><span data-stu-id="b7aac-116">The number of components is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b7aac-117">Texture-Object Typ</span><span class="sxs-lookup"><span data-stu-id="b7aac-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="b7aac-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="b7aac-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7aac-119">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b7aac-119">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="b7aac-120">float1</span><span class="sxs-lookup"><span data-stu-id="b7aac-120">float1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7aac-121">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b7aac-121">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="b7aac-122">float2</span><span class="sxs-lookup"><span data-stu-id="b7aac-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7aac-123">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b7aac-123">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="b7aac-124">float3</span><span class="sxs-lookup"><span data-stu-id="b7aac-124">float3</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="b7aac-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7aac-125">Return Value</span></span>

<span data-ttu-id="b7aac-126">Gibt die berechnete LOD zurück, einen einzelnen Gleitkommawert.</span><span class="sxs-lookup"><span data-stu-id="b7aac-126">Returns the calculated LOD, a single floating-point value.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="b7aac-127">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b7aac-127">Minimum Shader Model</span></span>

<span data-ttu-id="b7aac-128">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7aac-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b7aac-129">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b7aac-129">vs\_4\_0</span></span> | <span data-ttu-id="b7aac-130">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b7aac-130">vs\_4\_1</span></span>  | <span data-ttu-id="b7aac-131">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b7aac-131">ps\_4\_0</span></span> | <span data-ttu-id="b7aac-132">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b7aac-132">ps\_4\_1</span></span>  | <span data-ttu-id="b7aac-133">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b7aac-133">gs\_4\_0</span></span> | <span data-ttu-id="b7aac-134">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b7aac-134">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | <span data-ttu-id="b7aac-135">x</span><span class="sxs-lookup"><span data-stu-id="b7aac-135">x</span></span>         |          |           |



 

1.  <span data-ttu-id="b7aac-136">TextureCubeArray ist in Shader Model 4.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b7aac-136">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="b7aac-137">ShaderModell 4.1 ist in Direct3D 10.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b7aac-137">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7aac-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b7aac-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7aac-139">Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b7aac-139">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

