---
description: Gibt die beabsichtigte Verwendung von Vertex-Daten an.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: D3DDECLUSAGE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3997aa38a7a97455b9f36d8afbee896ca9ae937
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361853"
---
# <a name="d3ddeclusage-enumeration"></a><span data-ttu-id="e5030-103">D3DDECLUSAGE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e5030-103">D3DDECLUSAGE enumeration</span></span>

<span data-ttu-id="e5030-104">Gibt die beabsichtigte Verwendung von Vertex-Daten an.</span><span class="sxs-lookup"><span data-stu-id="e5030-104">Identifies the intended use of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5030-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5030-105">Syntax</span></span>


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a><span data-ttu-id="e5030-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e5030-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e5030-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE- \_ Position**</span><span class="sxs-lookup"><span data-stu-id="e5030-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-108">Positionieren von Daten im Bereich von (-1,-1) bis (1, 1).</span><span class="sxs-lookup"><span data-stu-id="e5030-108">Position data ranging from (-1,-1) to (1,1).</span></span> <span data-ttu-id="e5030-109">Verwenden \_ Sie die D3DDECLUSAGE-Position mit einem Nutzungs Index von 0, um eine nicht transformierte Position für die Vertex-Verarbeitung fester Funktionen und den n-Patch-Mosaik Wert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5030-109">Use D3DDECLUSAGE\_POSITION with a usage index of 0 to specify untransformed position for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="e5030-110">Verwenden \_ Sie die D3DDECLUSAGE-Position mit einem Verwendungs Index von 1, um eine nicht transformierte Position im Scheitelpunkt des fixierten Funktionen für die vertextwiening anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5030-110">Use D3DDECLUSAGE\_POSITION with a usage index of 1 to specify untransformed position in the fixed function vertex shader for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ blendweight**</span><span class="sxs-lookup"><span data-stu-id="e5030-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE\_BLENDWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-112">Mischen von Gewichtungsdaten.</span><span class="sxs-lookup"><span data-stu-id="e5030-112">Blending weight data.</span></span> <span data-ttu-id="e5030-113">Verwenden \_ Sie D3DDECLUSAGE blendweight mit einem Nutzungs Index von 0, um die Blend-Gewichtungen anzugeben, die für indizierte und nicht indizierte vertexblending verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5030-113">Use D3DDECLUSAGE\_BLENDWEIGHT with a usage index of 0 to specify the blend weights used in indexed and nonindexed vertex blending.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ blendindices**</span><span class="sxs-lookup"><span data-stu-id="e5030-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE\_BLENDINDICES**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-115">Kombination von Indizes-Daten.</span><span class="sxs-lookup"><span data-stu-id="e5030-115">Blending indices data.</span></span> <span data-ttu-id="e5030-116">Verwenden \_ Sie D3DDECLUSAGE blendindices mit einem Nutzungs Index von 0, um Matrix Indizes für indizierte palettenskinning anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5030-116">Use D3DDECLUSAGE\_BLENDINDICES with a usage index of 0 to specify matrix indices for indexed paletted skinning.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ Normal**</span><span class="sxs-lookup"><span data-stu-id="e5030-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-118">Vertex-normale Daten.</span><span class="sxs-lookup"><span data-stu-id="e5030-118">Vertex normal data.</span></span> <span data-ttu-id="e5030-119">Verwenden \_ Sie D3DDECLUSAGE normal mit einem Nutzungs Index von 0, um Vertex-Normale für die Vertex-Verarbeitung fester Funktionen und den n-Patch-Mosaik Wert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5030-119">Use D3DDECLUSAGE\_NORMAL with a usage index of 0 to specify vertex normals for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="e5030-120">Verwenden \_ Sie D3DDECLUSAGE normal mit einem Nutzungs Index von 1, um Vertex-Normale für die Vertex-Verarbeitung fester Funktionen für vertextwiening anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5030-120">Use D3DDECLUSAGE\_NORMAL with a usage index of 1 to specify vertex normals for fixed function vertex processing for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ Psize**</span><span class="sxs-lookup"><span data-stu-id="e5030-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE\_PSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-122">Daten zur Datenpunkt Größe.</span><span class="sxs-lookup"><span data-stu-id="e5030-122">Point size data.</span></span> <span data-ttu-id="e5030-123">Verwenden \_ Sie D3DDECLUSAGE Psize mit einem Nutzungs Index von 0, um das Attribut für die Punktgröße anzugeben, das vom Setup Modul des Rasterizers verwendet wird, um einen Punkt für die Punkt Sprite-Funktionalität zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="e5030-123">Use D3DDECLUSAGE\_PSIZE with a usage index of 0 to specify the point-size attribute used by the setup engine of the rasterizer to expand a point into a quad for the point-sprite functionality.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ texcoord**</span><span class="sxs-lookup"><span data-stu-id="e5030-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE\_TEXCOORD**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-125">Texturkoordinaten Daten.</span><span class="sxs-lookup"><span data-stu-id="e5030-125">Texture coordinate data.</span></span> <span data-ttu-id="e5030-126">Verwenden \_ Sie D3DDECLUSAGE texcoord, n, um Texturkoordinaten in der Vertex-Verarbeitung fester Funktionen und in Pixel-Shader vor PS \_ 3 0 anzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="e5030-126">Use D3DDECLUSAGE\_TEXCOORD, n to specify texture coordinates in fixed function vertex processing and in pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="e5030-127">Diese können verwendet werden, um benutzerdefinierte Daten zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="e5030-127">These can be used to pass user defined data.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE \_ Tangens**</span><span class="sxs-lookup"><span data-stu-id="e5030-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE\_TANGENT**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-129">Vertextangens-Daten.</span><span class="sxs-lookup"><span data-stu-id="e5030-129">Vertex tangent data.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ Binormal**</span><span class="sxs-lookup"><span data-stu-id="e5030-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE\_BINORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-131">Vertex-Binormale-Daten.</span><span class="sxs-lookup"><span data-stu-id="e5030-131">Vertex binormal data.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ Tess Factor**</span><span class="sxs-lookup"><span data-stu-id="e5030-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE\_TESSFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-133">Einzelner positiver Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="e5030-133">Single positive floating point value.</span></span> <span data-ttu-id="e5030-134">Verwenden \_ Sie D3DDECLUSAGE Tess Factor mit einem Nutzungs Index von 0, um einen Mosaik Faktor anzugeben, der in der Mosaik Einheit verwendet wird, um die Rate des Mosaik Prozesses zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e5030-134">Use D3DDECLUSAGE\_TESSFACTOR with a usage index of 0 to specify a tessellation factor used in the tessellation unit to control the rate of tessellation.</span></span> <span data-ttu-id="e5030-135">Weitere Informationen zum-Datentyp finden Sie unter D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="e5030-135">For more information about the data type, see D3DDECLTYPE\_FLOAT1.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE \_ positiont**</span><span class="sxs-lookup"><span data-stu-id="e5030-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE\_POSITIONT**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-137">Vertex-Daten enthalten transformierte Positionsdaten im Bereich von (0,0) bis (Viewportbreite, VIEWPORTHÖHE).</span><span class="sxs-lookup"><span data-stu-id="e5030-137">Vertex data contains transformed position data ranging from (0,0) to (viewport width, viewport height).</span></span> <span data-ttu-id="e5030-138">Verwenden \_ Sie D3DDECLUSAGE positiont mit einem Nutzungs Index von 0, um die transformierte Position anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5030-138">Use D3DDECLUSAGE\_POSITIONT with a usage index of 0 to specify transformed position.</span></span> <span data-ttu-id="e5030-139">Wenn eine Deklaration, die diese enthält, festgelegt ist, führt die Pipeline keine Scheitelpunkt Verarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="e5030-139">When a declaration containing this is set, the pipeline does not perform vertex processing.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE- \_ Farbe**</span><span class="sxs-lookup"><span data-stu-id="e5030-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-141">Vertex-Daten enthalten diffuses oder Glanz Farben.</span><span class="sxs-lookup"><span data-stu-id="e5030-141">Vertex data contains diffuse or specular color.</span></span> <span data-ttu-id="e5030-142">Verwenden \_ Sie die D3DDECLUSAGE-Farbe mit einem Nutzungs Index von 0, um die diffuse Farbe in den Scheitel Punkten der Fixed-Funktion und die Pixel-Shader vor PS \_ 3 0 anzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="e5030-142">Use D3DDECLUSAGE\_COLOR with a usage index of 0 to specify the diffuse color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="e5030-143">Verwenden \_ Sie die D3DDECLUSAGE-Farbe mit einem Verwendungs Index von 1, um die Glanz Farbe im Scheitelpunkt des Scheitel Punkts und die Pixel-Shader vor PS \_ 3 0 anzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="e5030-143">Use D3DDECLUSAGE\_COLOR with a usage index of 1 to specify the specular color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE- \_ Nebel**</span><span class="sxs-lookup"><span data-stu-id="e5030-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE\_FOG**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-145">Vertex-Daten enthalten Nebel Daten.</span><span class="sxs-lookup"><span data-stu-id="e5030-145">Vertex data contains fog data.</span></span> <span data-ttu-id="e5030-146">Verwenden \_ Sie D3DDECLUSAGE Fog mit einem Nutzungs Index von 0, um einen in der nach Abschluss der Pixel Schattierung verwendeten Wert für "Nebel Blend" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5030-146">Use D3DDECLUSAGE\_FOG with a usage index of 0 to specify a fog blend value used after pixel shading finishes.</span></span> <span data-ttu-id="e5030-147">Dies gilt für Pixel-Shader vor Version PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="e5030-147">This applies to pixel shaders prior to version ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE \_ Tiefe**</span><span class="sxs-lookup"><span data-stu-id="e5030-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE\_DEPTH**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-149">Vertex-Daten enthalten Tiefendaten.</span><span class="sxs-lookup"><span data-stu-id="e5030-149">Vertex data contains depth data.</span></span>

</dd> <dt>

<span data-ttu-id="e5030-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE- \_ Beispiel**</span><span class="sxs-lookup"><span data-stu-id="e5030-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE\_SAMPLE**</span></span>
</dt> <dd>

<span data-ttu-id="e5030-151">Vertex-Daten enthalten Samplingdaten.</span><span class="sxs-lookup"><span data-stu-id="e5030-151">Vertex data contains sampler data.</span></span> <span data-ttu-id="e5030-152">Verwenden \_ Sie D3DDECLUSAGE Sample mit einem Nutzungs Index von 0, um den zu über suchenden Verschiebungs Wert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5030-152">Use D3DDECLUSAGE\_SAMPLE with a usage index of 0 to specify the displacement value to look up.</span></span> <span data-ttu-id="e5030-153">Sie kann nur mit D3DDECLUSAGE \_ lookuppresampling oder D3DDECLUSAGE \_ Lookup verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5030-153">It can be used only with D3DDECLUSAGE\_LOOKUPPRESAMPLED or D3DDECLUSAGE\_LOOKUP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5030-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5030-154">Remarks</span></span>

<span data-ttu-id="e5030-155">Vertex-Daten werden mit einem Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Strukturen deklariert.</span><span class="sxs-lookup"><span data-stu-id="e5030-155">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="e5030-156">Jedes Element im Array enthält einen Verwendungstyp.</span><span class="sxs-lookup"><span data-stu-id="e5030-156">Each element in the array contains a usage type.</span></span>

<span data-ttu-id="e5030-157">Weitere Informationen zu Vertex-Deklarationen finden Sie unter [Vertex-Deklaration (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="e5030-157">For more information about vertex declarations, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5030-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5030-158">Requirements</span></span>



| <span data-ttu-id="e5030-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5030-159">Requirement</span></span> | <span data-ttu-id="e5030-160">Wert</span><span class="sxs-lookup"><span data-stu-id="e5030-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5030-161">Header</span><span class="sxs-lookup"><span data-stu-id="e5030-161">Header</span></span><br/> | <dl> <span data-ttu-id="e5030-162"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5030-162"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5030-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5030-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5030-164">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="e5030-164">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="e5030-165">Vertex-Deklaration (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e5030-165">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 




