---
description: Führt Tangens-Frame Berechnungen in einem Mesh aus. Tangens, Binormale und optional normale Vektoren werden generiert. Singularitäten werden nach Bedarf durch Gruppierung von Rändern und Aufteilen von Scheitel Punkten behandelt.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: D3DXComputeTangentFrameEx-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58c7e8a1f1f7247d6a3ecc92d5771d68c9c3e5a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365294"
---
# <a name="d3dxcomputetangentframeex-function"></a><span data-ttu-id="614dc-105">D3DXComputeTangentFrameEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="614dc-105">D3DXComputeTangentFrameEx function</span></span>

<span data-ttu-id="614dc-106">Führt Tangens-Frame Berechnungen in einem Mesh aus.</span><span class="sxs-lookup"><span data-stu-id="614dc-106">Performs tangent frame computations on a mesh.</span></span> <span data-ttu-id="614dc-107">Tangens, Binormale und optional normale Vektoren werden generiert.</span><span class="sxs-lookup"><span data-stu-id="614dc-107">Tangent, binormal, and optionally normal vectors are generated.</span></span> <span data-ttu-id="614dc-108">Singularitäten werden nach Bedarf durch Gruppierung von Rändern und Aufteilen von Scheitel Punkten behandelt.</span><span class="sxs-lookup"><span data-stu-id="614dc-108">Singularities are handled as required by grouping edges and splitting vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="614dc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="614dc-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a><span data-ttu-id="614dc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="614dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="614dc-111">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-111">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-112">Typ: **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="614dc-112">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="614dc-113">Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Eingabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="614dc-113">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-114">*dwtextureinsemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-114">*dwTextureInSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-115">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-116">Gibt die Eingabe Semantik der Textur Koordinate an.</span><span class="sxs-lookup"><span data-stu-id="614dc-116">Specifies the texture coordinate input semantic.</span></span> <span data-ttu-id="614dc-117">Wenn D3DX \_ Default ist, geht die Funktion davon aus, dass keine Texturkoordinaten vorhanden sind, und die Funktion schlägt fehl, es sei denn, die normale Vektor Berechnung wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="614dc-117">If D3DX\_DEFAULT, the function assumes that there are no texture coordinates, and the function will fail unless normal vector calculation is specified.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-118">*dwtextureinindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-118">*dwTextureInIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-119">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-120">Wenn ein Mesh über mehrere Texturkoordinaten verfügt, gibt die Textur Koordinate an, die für die Tangens-Frame-Berechnungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="614dc-120">If a mesh has multiple texture coordinates, specifies the texture coordinate to use for the tangent frame computations.</span></span> <span data-ttu-id="614dc-121">Wenn der Wert NULL ist, verfügt das Mesh nur über eine einzelne Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="614dc-121">If zero, the mesh has only a single texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-122">*dwupartialoutsemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-122">*dwUPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-123">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-124">Gibt die Ausgabe Semantik für den Typ an, üblicherweise D3DDECLUSAGE \_ Tangens, der beschreibt, wo die partielle Ableitung in Bezug auf die U-Textur Koordinate gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="614dc-124">Specifies the output semantic for the type, typically D3DDECLUSAGE\_TANGENT, that describes where the partial derivative with respect to the U texture coordinate will be stored.</span></span> <span data-ttu-id="614dc-125">Wenn D3DX den \_ Standardwert hat, wird diese partielle Ableitung nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="614dc-125">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-126">*dwupartialoutindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-126">*dwUPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-127">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-128">Gibt den semantischen Index an, bei dem die partielle Ableitung in Bezug auf die U-Textur Koordinate gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="614dc-128">Specifies the semantic index at which to store the partial derivative with respect to the U texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-129">*dwvpartialoutsemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-129">*dwVPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-130">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-131">Gibt den [**D3DDECLUSAGE**](./d3ddeclusage.md) -Typ an, in der Regel D3DDECLUSAGE \_ Binormal, der beschreibt, wo die partielle Ableitung in Bezug auf die V-Textur Koordinate gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="614dc-131">Specifies the [**D3DDECLUSAGE**](./d3ddeclusage.md) type, typically D3DDECLUSAGE\_BINORMAL, that describes where the partial derivative with respect to the V texture coordinate will be stored.</span></span> <span data-ttu-id="614dc-132">Wenn D3DX den \_ Standardwert hat, wird diese partielle Ableitung nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="614dc-132">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-133">*dwvpartialoutindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-133">*dwVPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-134">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-135">Gibt den semantischen Index an, bei dem die partielle Ableitung in Bezug auf die V-Textur Koordinate gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="614dc-135">Specifies the semantic index at which to store the partial derivative with respect to the V texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-136">*dwnormaloutsemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-136">*dwNormalOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-137">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-138">Gibt die normale Semantik der Ausgabe an (normalerweise D3DDECLUSAGE normal), die \_ beschreibt, wo der normale Vektor bei jedem Scheitelpunkt gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="614dc-138">Specifies the output normal semantic, typically D3DDECLUSAGE\_NORMAL, that describes where the normal vector at each vertex will be stored.</span></span> <span data-ttu-id="614dc-139">Wenn D3DX den \_ Standardwert hat, wird dieser normale Vektor nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="614dc-139">If D3DX\_DEFAULT, then this normal vector will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-140">*dwnormaloutindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-140">*dwNormalOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-141">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-142">Gibt den semantischen Index an, bei dem der normale Vektor in jedem Scheitelpunkt gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="614dc-142">Specifies the semantic index at which to store the normal vector at each vertex.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-143">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-143">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-144">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-145">Eine Kombination aus einem oder mehreren [**D3DXTANGENT**](./d3dxtangent.md) -Flags, die Optionen für die Tangens Frame Berechnung angeben.</span><span class="sxs-lookup"><span data-stu-id="614dc-145">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags that specify tangent frame computation options.</span></span> <span data-ttu-id="614dc-146">Wenn der Wert **null** ist, werden die folgenden Optionen angegeben:</span><span class="sxs-lookup"><span data-stu-id="614dc-146">If **NULL**, the following options will be specified:</span></span>



| <span data-ttu-id="614dc-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="614dc-147">Description</span></span>                                                                                              | <span data-ttu-id="614dc-148">[**D3DXTANGENT**](./d3dxtangent.md) Flagwert</span><span class="sxs-lookup"><span data-stu-id="614dc-148">[**D3DXTANGENT**](./d3dxtangent.md) Flag Value</span></span>                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="614dc-149">Gewichtung der normalen Vektor Länge um den Winkel im Bogenmaße, der von den beiden Kanten, die den Scheitelpunkt hinterlassen, untergeordneter Länge liegt.</span><span class="sxs-lookup"><span data-stu-id="614dc-149">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span> | <span data-ttu-id="614dc-150">&! (D3DXTANGENT \_ Gewichtung \_ nach \_ Bereich \| D3DXTANGENT \_ Gewichtung \_ gleich)</span><span class="sxs-lookup"><span data-stu-id="614dc-150">& !( D3DXTANGENT\_WEIGHT\_BY\_AREA \| D3DXTANGENT\_WEIGHT\_EQUAL )</span></span>                |
| <span data-ttu-id="614dc-151">Berechnen Sie orthogonale kartesische Koordinaten von Texturkoordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="614dc-151">Compute orthogonal Cartesian coordinates from texture coordinates (u, v).</span></span> <span data-ttu-id="614dc-152">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="614dc-152">See Remarks.</span></span>                   | <span data-ttu-id="614dc-153">&! (D3DXTANGENT \_ Orthogonalize \_ from \_ U \| D3DXTANGENT \_ orthogonalize \_ from \_ V)</span><span class="sxs-lookup"><span data-stu-id="614dc-153">& !( D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U \| D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V )</span></span> |
| <span data-ttu-id="614dc-154">Texturen sind weder in der u-noch in der v-Richtung umschließt</span><span class="sxs-lookup"><span data-stu-id="614dc-154">Textures are not wrapped in either u or v directions</span></span>                                                     | <span data-ttu-id="614dc-155">&! (D3DXTANGENT \_ Wrapper \_ -UV)</span><span class="sxs-lookup"><span data-stu-id="614dc-155">& !( D3DXTANGENT\_WRAP\_UV )</span></span>                                                      |
| <span data-ttu-id="614dc-156">Partielle Ableitungen in Bezug auf Texturkoordinaten werden normalisiert.</span><span class="sxs-lookup"><span data-stu-id="614dc-156">Partial derivatives with respect to texture coordinates are normalized.</span></span>                                  | <span data-ttu-id="614dc-157">&! (D3DXTANGENT \_ \_ \_ partitionale nicht normalisieren</span><span class="sxs-lookup"><span data-stu-id="614dc-157">& !( D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS )</span></span>                                     |
| <span data-ttu-id="614dc-158">Vertices werden um jedes Dreieck in der Richtung gegen den Uhrzeigersinn angeordnet.</span><span class="sxs-lookup"><span data-stu-id="614dc-158">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>                               | <span data-ttu-id="614dc-159">&! (D3DXTANGENT \_ Wind- \_ CW)</span><span class="sxs-lookup"><span data-stu-id="614dc-159">& !( D3DXTANGENT\_WIND\_CW )</span></span>                                                      |
| <span data-ttu-id="614dc-160">Verwenden Sie die pro-Vertex-normal Vektoren, die bereits im Eingabe Mesh vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="614dc-160">Use per-vertex normal vectors already present in the input mesh.</span></span>                                         | <span data-ttu-id="614dc-161">&! (D3DXTANGENT \_ \_normale berechnen)</span><span class="sxs-lookup"><span data-stu-id="614dc-161">& !( D3DXTANGENT\_CALCULATE\_NORMALS )</span></span>                                            |



 

<span data-ttu-id="614dc-162">Wenn D3DXTANGENT \_ Generate \_ on \_ Place nicht festgelegt ist, wird das eingabemesh geklont.</span><span class="sxs-lookup"><span data-stu-id="614dc-162">If D3DXTANGENT\_GENERATE\_IN\_PLACE is not set, the input mesh is cloned.</span></span> <span data-ttu-id="614dc-163">Das ursprüngliche Mesh muss daher über ausreichend Speicherplatz verfügen, um den berechneten normalen Vektor und teilweise abgeleitete Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="614dc-163">The original mesh must therefore have sufficient space to store the computed normal vector and partial derivative data.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-164">*PDW-ency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-164">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-165">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="614dc-165">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="614dc-166">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="614dc-166">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="614dc-167">Die Anzahl der Bytes in diesem Array muss mindestens 3 \* [**getnumgesichter**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) betragen.</span><span class="sxs-lookup"><span data-stu-id="614dc-167">The number of bytes in this array must be at least 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="614dc-168">*' f '* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-168">*fPartialEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-169">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-169">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-170">Gibt den maximalen Kosinus des Winkels an, bei dem zwei partielle Ableitungen als nicht kompatibel eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="614dc-170">Specifies the maximum cosine of the angle at which two partial derivatives are deemed to be incompatible with each other.</span></span> <span data-ttu-id="614dc-171">Wenn das Punktprodukt der Richtung der beiden partiellen Ableitungen in angrenzenden Dreiecken kleiner oder gleich diesem Schwellenwert ist, werden die Scheitel Punkte, die von diesen Dreiecken gemeinsam genutzt werden, aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="614dc-171">If the dot product of the direction of the two partial derivatives in adjacent triangles is less than or equal to this threshold, then the vertices shared between these triangles will be split.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-172">*' f ' (' f '* \[ ) in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-172">*fSingularPointThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-173">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-173">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-174">Gibt die maximale Größe einer partiellen Ableitung an, bei der ein Scheitelpunkt als Singular eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="614dc-174">Specifies the maximum magnitude of a partial derivative at which a vertex will be deemed singular.</span></span> <span data-ttu-id="614dc-175">Da mehrere Dreiecke an einem Punkt mit nahe gelegenen Tangenten Frames, aber vollständig abgebrochen werden (z. b. am oberen Rand einer Kugel), wird die Größe der partiellen Ableitung verringert.</span><span class="sxs-lookup"><span data-stu-id="614dc-175">As multiple triangles are incident on a point that have nearby tangent frames, but altogether cancel each other out (such as at the top of a sphere), the magnitude of the partial derivative will decrease.</span></span> <span data-ttu-id="614dc-176">Wenn die Größe kleiner oder gleich diesem Schwellenwert ist, wird der Scheitelpunkt für jedes Dreieck aufgeteilt, das es enthält.</span><span class="sxs-lookup"><span data-stu-id="614dc-176">If the magnitude is less than or equal to this threshold, then the vertex will be split for every triangle that contains it.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-177">" *Wert* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="614dc-177">*fNormalEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-178">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="614dc-178">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="614dc-179">Ähnlich wie bei fpartialedgethreshold gibt den maximalen Kosinus des Winkels zwischen zwei normalen an, bei denen es sich um einen Schwellenwert handelt, über den die von Dreiecken gemeinsam genutzten Scheitel Punkte aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="614dc-179">Similar to fPartialEdgeThreshold, specifies the maximum cosine of the angle between two normals that is a threshold beyond which vertices shared between triangles will be split.</span></span> <span data-ttu-id="614dc-180">Wenn das Punktprodukt der beiden normale kleiner als der Schwellenwert ist, werden die freigegebenen Scheitel Punkte aufgeteilt und bilden einen festen Rand zwischen benachbarten Dreiecken.</span><span class="sxs-lookup"><span data-stu-id="614dc-180">If the dot product of the two normals is less than the threshold, the shared vertices will be split, forming a hard edge between neighboring triangles.</span></span> <span data-ttu-id="614dc-181">Wenn das Punktprodukt den Schwellenwert überschreitet, werden die normalen der benachbarten Dreiecke interpoliert.</span><span class="sxs-lookup"><span data-stu-id="614dc-181">If the dot product is more than the threshold, neighboring triangles will have their normals interpolated.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-182">*ppmeshout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="614dc-182">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-183">Typ: **[ **ID3DXMesh**](id3dxmesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="614dc-183">Type: **[**ID3DXMesh**](id3dxmesh.md)\*\***</span></span>

<span data-ttu-id="614dc-184">Adresse eines Zeigers auf ein Output [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekt, das die berechneten Tangens-, Binormale-und normal Vektordaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="614dc-184">Address of a pointer to an output [**ID3DXMesh**](id3dxmesh.md) mesh object that receives the computed tangent, binormal, and normal vector data.</span></span>

</dd> <dt>

<span data-ttu-id="614dc-185">*ppvertexmapping* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="614dc-185">*ppVertexMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="614dc-186">Typ: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="614dc-186">Type: **[**ID3DXBuffer**](id3dxbuffer.md)\*\***</span></span>

<span data-ttu-id="614dc-187">Adresse eines Zeigers auf ein [**ID3DXBuffer**](id3dxbuffer.md) -Ausgabepuffer Objekt, das eine Zuordnung von neuen Scheitel Punkten empfängt, die von dieser Methode in den ursprünglichen Scheitel Punkten berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="614dc-187">Address of a pointer to an output [**ID3DXBuffer**](id3dxbuffer.md) buffer object that receives a mapping of new vertices computed by this method to the original vertices.</span></span> <span data-ttu-id="614dc-188">Der Puffer ist ein Array von DWords, wobei die Array Größe als Anzahl von Vertices in ppmeshout definiert ist.</span><span class="sxs-lookup"><span data-stu-id="614dc-188">The buffer is an array of DWORDs, with the array size defined as the number of vertices in ppMeshOut.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="614dc-189">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="614dc-189">Return value</span></span>

<span data-ttu-id="614dc-190">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="614dc-190">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="614dc-191">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="614dc-191">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="614dc-192">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="614dc-192">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="614dc-193">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="614dc-193">Remarks</span></span>

<span data-ttu-id="614dc-194">Eine vereinfachte Version dieser Funktion ist als [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="614dc-194">A simplified version of this function is available as [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span></span>

<span data-ttu-id="614dc-195">Der berechnete normale Vektor bei jedem Scheitelpunkt wird immer normalisiert, sodass er über eine Einheitslänge verfügt.</span><span class="sxs-lookup"><span data-stu-id="614dc-195">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="614dc-196">Die stabilste Lösung für die Berechnung von orthogonalen kartesischen Koordinaten ist das Festlegen von Flags D3DXTANGENT \_ orthogonalize \_ von \_ Ihnen und D3DXTANGENT \_ orthogonalize \_ von \_ v, sodass orthogonale Koordinaten sowohl aus den Texturkoordinaten Sie als auch mit v berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="614dc-196">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both texture coordinates u and v.</span></span> <span data-ttu-id="614dc-197">Wenn in diesem Fall jedoch entweder "u" oder "v" gleich NULL ist, berechnet die Funktion orthogonale Koordinaten mithilfe von D3DXTANGENT \_ orthogonalize \_ von \_ v bzw \_ . D3DXTANGENT orthogonalize \_ von \_ u bzw..</span><span class="sxs-lookup"><span data-stu-id="614dc-197">However, in this case, if either u or v is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="614dc-198">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="614dc-198">Requirements</span></span>



| <span data-ttu-id="614dc-199">Anforderung</span><span class="sxs-lookup"><span data-stu-id="614dc-199">Requirement</span></span> | <span data-ttu-id="614dc-200">Wert</span><span class="sxs-lookup"><span data-stu-id="614dc-200">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="614dc-201">Header</span><span class="sxs-lookup"><span data-stu-id="614dc-201">Header</span></span><br/>  | <dl> <span data-ttu-id="614dc-202"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="614dc-202"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="614dc-203">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="614dc-203">Library</span></span><br/> | <dl> <span data-ttu-id="614dc-204"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="614dc-204"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="614dc-205">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="614dc-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="614dc-206">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="614dc-206">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="614dc-207">**D3DXComputeTangentFrame**</span><span class="sxs-lookup"><span data-stu-id="614dc-207">**D3DXComputeTangentFrame**</span></span>](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
