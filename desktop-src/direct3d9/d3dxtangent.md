---
description: Definiert Einstellungen, die für Gitter Tangens-Frame Berechnungen verwendet werden.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: D3DXTANGENT-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371908"
---
# <a name="d3dxtangent-enumeration"></a><span data-ttu-id="4f777-103">D3DXTANGENT-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4f777-103">D3DXTANGENT enumeration</span></span>

<span data-ttu-id="4f777-104">Definiert Einstellungen, die für Gitter Tangens-Frame Berechnungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f777-104">Defines settings used for mesh tangent frame computations.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f777-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f777-105">Syntax</span></span>


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a><span data-ttu-id="4f777-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="4f777-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4f777-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ Wrap \_ U**</span><span class="sxs-lookup"><span data-stu-id="4f777-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-108">Texturkoordinaten Werte in der u-Richtung liegen zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="4f777-108">Texture coordinate values in the u direction are between 0 and 1.</span></span> <span data-ttu-id="4f777-109">In diesem Fall wird ein Texturkoordinaten Satz ausgewählt, der den Umkreis des Dreiecks minimiert.</span><span class="sxs-lookup"><span data-stu-id="4f777-109">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="4f777-110">Weitere Informationen finden Sie unter [Textur Wrapping (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="4f777-110">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f777-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ Wrap \_ V**</span><span class="sxs-lookup"><span data-stu-id="4f777-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-112">Texturkoordinaten Werte in der v-Richtung liegen zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="4f777-112">Texture coordinate values in the v direction are between 0 and 1.</span></span> <span data-ttu-id="4f777-113">In diesem Fall wird ein Texturkoordinaten Satz ausgewählt, der den Umkreis des Dreiecks minimiert.</span><span class="sxs-lookup"><span data-stu-id="4f777-113">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="4f777-114">Weitere Informationen finden Sie unter [Textur Wrapping (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="4f777-114">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f777-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ Wrap \_ -UV**</span><span class="sxs-lookup"><span data-stu-id="4f777-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-116">Die Texturkoordinaten Werte in der Richtung und der v-Richtung liegen zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="4f777-116">Texture coordinate values in both u and v directions are between 0 and 1.</span></span> <span data-ttu-id="4f777-117">In diesem Fall wird ein Texturkoordinaten Satz ausgewählt, der den Umkreis des Dreiecks minimiert.</span><span class="sxs-lookup"><span data-stu-id="4f777-117">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="4f777-118">Weitere Informationen finden Sie unter [Textur Wrapping (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="4f777-118">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f777-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ keine \_ \_ partitionale normalisieren**</span><span class="sxs-lookup"><span data-stu-id="4f777-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-120">Partielle Ableitungen sollten nicht in Bezug auf Texturkoordinaten normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4f777-120">Do not normalize partial derivatives with respect to texture coordinates.</span></span> <span data-ttu-id="4f777-121">Wenn nicht normalisiert, ist die Skala der partiellen Ableitungen proportional zur Skala des 3D-Modells dividiert durch die Skala des Dreiecks im (u, v)-Raum.</span><span class="sxs-lookup"><span data-stu-id="4f777-121">If not normalized, the scale of the partial derivatives is proportional to the scale of the 3D model divided by the scale of the triangle in (u, v) space.</span></span> <span data-ttu-id="4f777-122">Dieser Skalierungs Wert gibt an, wie weit die Textur in eine bestimmte Richtung gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="4f777-122">This scale value provides a measure of how much the texture is stretched in a given direction.</span></span> <span data-ttu-id="4f777-123">Die resultierende Vektor Länge ist eine gewichtete Summe der Längen der partiellen Ableitungen.</span><span class="sxs-lookup"><span data-stu-id="4f777-123">The resulting vector length is a weighted sum of the lengths of the partial derivatives.</span></span>

</dd> <dt>

<span data-ttu-id="4f777-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ nicht \_ orthogonalize**</span><span class="sxs-lookup"><span data-stu-id="4f777-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT\_DONT\_ORTHOGONALIZE**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-125">Transformieren Sie keine Texturkoordinaten in orthogonale kartesische Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="4f777-125">Do not transform texture coordinates to orthogonal Cartesian coordinates.</span></span> <span data-ttu-id="4f777-126">Schließen Sie sich mit D3DXTANGENT \_ orthogonalize \_ von \_ Ihnen und D3DXTANGENT \_ orthogonalize \_ von \_ V gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="4f777-126">Mutually exclusive with D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="4f777-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ orthogonalize \_ von \_ V**</span><span class="sxs-lookup"><span data-stu-id="4f777-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-128">Berechnen Sie die partielle Ableitung in Bezug auf die Texturkoordinaten v unabhängig für jeden Scheitelpunkt, und berechnen Sie dann die partielle Ableitung in Bezug auf das Kreuz Produkt der partiellen Ableitung in Bezug auf v und den normalen Vektor.</span><span class="sxs-lookup"><span data-stu-id="4f777-128">Compute the partial derivative with respect to texture coordinate v independently for each vertex, and then compute the partial derivative with respect to u as the cross product of the partial derivative with respect to v and the normal vector.</span></span> <span data-ttu-id="4f777-129">Schließen Sie sich mit D3DXTANGENT \_ dont \_ orthogonalize und D3DXTANGENT \_ orthogonalize aus U gegenseitig \_ aus \_ .</span><span class="sxs-lookup"><span data-stu-id="4f777-129">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U.</span></span>

</dd> <dt>

<span data-ttu-id="4f777-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ orthogonalize \_ von \_ U**</span><span class="sxs-lookup"><span data-stu-id="4f777-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-131">Berechnen Sie die partielle Ableitung in Bezug auf die Textur Koordinate u unabhängig für jeden Scheitelpunkt, und berechnen Sie dann die partielle Ableitung in Bezug auf v als Kreuz Produkt des normalen Vektors und die partielle Ableitung in Bezug auf Sie.</span><span class="sxs-lookup"><span data-stu-id="4f777-131">Compute the partial derivative with respect to texture coordinate u independently for each vertex, and then compute the partial derivative with respect to v as the cross product of the normal vector and the partial derivative with respect to u.</span></span> <span data-ttu-id="4f777-132">Schließen Sie sich mit D3DXTANGENT \_ dont \_ orthogonalize und D3DXTANGENT \_ orthogonalize aus V gegenseitig \_ aus \_ .</span><span class="sxs-lookup"><span data-stu-id="4f777-132">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="4f777-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT \_ Gewichtung \_ nach \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="4f777-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT\_WEIGHT\_BY\_AREA**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-134">Gewichtet die Richtung des berechneten pro-Vertex-normalen oder partiellen Ableitung-Vektors gemäß den Bereichen der Dreiecke, die an diesen Scheitelpunkt angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="4f777-134">Weight the direction of the computed per-vertex normal or partial derivative vector according to the areas of triangles attached to that vertex.</span></span> <span data-ttu-id="4f777-135">Schließen Sie sich mit D3DXTANGENT Weight gleich gegenseitig aus \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4f777-135">Mutually exclusive with D3DXTANGENT\_WEIGHT\_EQUAL.</span></span>

</dd> <dt>

<span data-ttu-id="4f777-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT \_ Gewichtung \_ gleich**</span><span class="sxs-lookup"><span data-stu-id="4f777-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT\_WEIGHT\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-137">Berechnen Sie für jedes Dreieck des Eingabe Netzes einen normalen Vektor mit Einheiten Länge.</span><span class="sxs-lookup"><span data-stu-id="4f777-137">Compute a unit-length normal vector for each triangle of the input mesh.</span></span> <span data-ttu-id="4f777-138">Schließen Sie sich mit D3DXTANGENT \_ Weight \_ by Area gegenseitig aus \_ .</span><span class="sxs-lookup"><span data-stu-id="4f777-138">Mutually exclusive with D3DXTANGENT\_WEIGHT\_BY\_AREA.</span></span>

</dd> <dt>

<span data-ttu-id="4f777-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ Wind \_ CW**</span><span class="sxs-lookup"><span data-stu-id="4f777-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT\_WIND\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-140">Vertices werden um jedes Dreieck in einer Richtung im Uhrzeigersinn angeordnet.</span><span class="sxs-lookup"><span data-stu-id="4f777-140">Vertices are ordered in a clockwise direction around each triangle.</span></span> <span data-ttu-id="4f777-141">Die berechnete normale Vektor Richtung wird aus der Richtung, die mithilfe der Vertex-Reihenfolge gegen den Uhrzeigersinn berechnet wurde, um 180 Grad</span><span class="sxs-lookup"><span data-stu-id="4f777-141">The computed normal vector direction is therefore inverted 180 degrees from the direction computed using counterclockwise vertex ordering.</span></span>

</dd> <dt>

<span data-ttu-id="4f777-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ Berechnen von \_ normalen**</span><span class="sxs-lookup"><span data-stu-id="4f777-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT\_CALCULATE\_NORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-143">Berechnen Sie den normalen Vertex-Vektor für jedes Dreieck des Eingabe Netzes, und ignorieren Sie alle normalen Vektoren, die bereits im eingabemesh vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4f777-143">Compute the per-vertex normal vector for each triangle of the input mesh, and ignore any normal vectors already in the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="4f777-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT- \_ Generierung direkt generieren \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f777-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT\_GENERATE\_IN\_PLACE**</span></span>
</dt> <dd>

<span data-ttu-id="4f777-145">Die Ergebnisse werden im ursprünglichen eingabemesh gespeichert, und das Ausgabe Mesh wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f777-145">The results are stored in the original input mesh, and the output mesh is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f777-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f777-146">Requirements</span></span>



| <span data-ttu-id="4f777-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f777-147">Requirement</span></span> | <span data-ttu-id="4f777-148">Wert</span><span class="sxs-lookup"><span data-stu-id="4f777-148">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f777-149">Header</span><span class="sxs-lookup"><span data-stu-id="4f777-149">Header</span></span><br/> | <dl> <span data-ttu-id="4f777-150"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f777-150"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f777-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f777-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f777-152">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4f777-152">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="4f777-153">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="4f777-153">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




