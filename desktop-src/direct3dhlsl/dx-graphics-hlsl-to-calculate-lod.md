---
title: Calculatelevelof Detail (DirectX HLSL Texture-Objekt)
description: Berechnet den Detailgrad.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c59b8da97ff1cbe0bd88d6a49120a0a040cf3c30
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104976864"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a><span data-ttu-id="c9d2a-103">Calculatelevelof Detail (DirectX HLSL Texture-Objekt)</span><span class="sxs-lookup"><span data-stu-id="c9d2a-103">CalculateLevelOfDetail (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="c9d2a-104">Berechnet den Detailgrad.</span><span class="sxs-lookup"><span data-stu-id="c9d2a-104">Calculates the level of detail.</span></span>



|                                                                 |
|-----------------------------------------------------------------|
| <span data-ttu-id="c9d2a-105">Ret Object. calculatelevelof Detail (Sampler \_ State S, float x);</span><span class="sxs-lookup"><span data-stu-id="c9d2a-105">ret Object.CalculateLevelOfDetail( sampler\_state S, float x );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="c9d2a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9d2a-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9d2a-107">Element</span><span class="sxs-lookup"><span data-stu-id="c9d2a-107">Item</span></span></th>
<th><span data-ttu-id="c9d2a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9d2a-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9d2a-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="c9d2a-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="c9d2a-110">Ein beliebiger <a href="dx-graphics-hlsl-to-type.md">Textur Objekttyp</a> (mit Ausnahme von Texture2DMS und Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="c9d2a-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9d2a-111"><span id="S"></span><span id="s"></span><em>Hymnen</em></span><span class="sxs-lookup"><span data-stu-id="c9d2a-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="c9d2a-112">in Ein <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">samplerzustand</a>.</span><span class="sxs-lookup"><span data-stu-id="c9d2a-112">[in] A <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Sampler state</a>.</span></span> <span data-ttu-id="c9d2a-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="c9d2a-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9d2a-114"><span id="x"></span><span id="X"></span><em>Stuben</em></span><span class="sxs-lookup"><span data-stu-id="c9d2a-114"><span id="x"></span><span id="X"></span><em>x</em></span></span><br/></td>
<td><span data-ttu-id="c9d2a-115">in Der lineare Interpolations Wert oder die Werte, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt.</span><span class="sxs-lookup"><span data-stu-id="c9d2a-115">[in] The linear interpolation value or values, which is a floating-point number between 0.0 and 1.0 inclusive.</span></span> <span data-ttu-id="c9d2a-116">Die Anzahl der Komponenten ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="c9d2a-116">The number of components is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c9d2a-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="c9d2a-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="c9d2a-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="c9d2a-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9d2a-119">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c9d2a-119">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="c9d2a-120">float1</span><span class="sxs-lookup"><span data-stu-id="c9d2a-120">float1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9d2a-121">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c9d2a-121">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="c9d2a-122">float2</span><span class="sxs-lookup"><span data-stu-id="c9d2a-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9d2a-123">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="c9d2a-123">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="c9d2a-124">float3</span><span class="sxs-lookup"><span data-stu-id="c9d2a-124">float3</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="c9d2a-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9d2a-125">Return Value</span></span>

<span data-ttu-id="c9d2a-126">Gibt die berechnete Lod zurück, einen einzelnen Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="c9d2a-126">Returns the calculated LOD, a single floating-point value.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c9d2a-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c9d2a-127">Minimum Shader Model</span></span>

<span data-ttu-id="c9d2a-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9d2a-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c9d2a-129">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c9d2a-129">vs\_4\_0</span></span> | <span data-ttu-id="c9d2a-130">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c9d2a-130">vs\_4\_1</span></span>  | <span data-ttu-id="c9d2a-131">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c9d2a-131">ps\_4\_0</span></span> | <span data-ttu-id="c9d2a-132">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c9d2a-132">ps\_4\_1</span></span>  | <span data-ttu-id="c9d2a-133">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c9d2a-133">gs\_4\_0</span></span> | <span data-ttu-id="c9d2a-134">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c9d2a-134">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | <span data-ttu-id="c9d2a-135">x</span><span class="sxs-lookup"><span data-stu-id="c9d2a-135">x</span></span>         |          |           |



 

1.  <span data-ttu-id="c9d2a-136">Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c9d2a-136">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="c9d2a-137">Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c9d2a-137">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9d2a-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9d2a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9d2a-139">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="c9d2a-139">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

