---
description: Compute Tangens, Binormale und normale Vektoren für ein Mesh.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: D3DXComputeTangentFrame-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353761"
---
# <a name="d3dxcomputetangentframe-function"></a><span data-ttu-id="ed82b-103">D3DXComputeTangentFrame-Funktion</span><span class="sxs-lookup"><span data-stu-id="ed82b-103">D3DXComputeTangentFrame function</span></span>

<span data-ttu-id="ed82b-104">Compute Tangens, Binormale und normale Vektoren für ein Mesh.</span><span class="sxs-lookup"><span data-stu-id="ed82b-104">Compute tangent, binormal, and normal vectors for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed82b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed82b-105">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a><span data-ttu-id="ed82b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed82b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed82b-107">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed82b-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed82b-108">Typ: **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed82b-108">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="ed82b-109">Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Eingabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="ed82b-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="ed82b-110">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed82b-110">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed82b-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed82b-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed82b-112">Kombination von mindestens einem [**D3DXTANGENT**](./d3dxtangent.md) -Flags.</span><span class="sxs-lookup"><span data-stu-id="ed82b-112">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags.</span></span>

<span data-ttu-id="ed82b-113">Verwenden Sie **null** , um die folgenden Optionen anzugeben:</span><span class="sxs-lookup"><span data-stu-id="ed82b-113">Use **NULL** to specify the following options:</span></span>

-   <span data-ttu-id="ed82b-114">Gewichtung der normalen Vektor Länge um den Winkel im Bogenmaße, der von den beiden Kanten, die den Scheitelpunkt hinterlassen, untergeordneter Länge liegt.</span><span class="sxs-lookup"><span data-stu-id="ed82b-114">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span>
-   <span data-ttu-id="ed82b-115">Berechnen Sie orthogonale kartesische Koordinaten aus den UV-Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="ed82b-115">Compute orthogonal Cartesian coordinates from the UV texture coordinates.</span></span>
-   <span data-ttu-id="ed82b-116">Texturen sind weder in der U-noch in der V-Richtung umschließt</span><span class="sxs-lookup"><span data-stu-id="ed82b-116">Textures are not wrapped in either U or V directions</span></span>
-   <span data-ttu-id="ed82b-117">Partielle Ableitungen in Bezug auf Texturkoordinaten werden normalisiert.</span><span class="sxs-lookup"><span data-stu-id="ed82b-117">Partial derivatives with respect to texture coordinates are normalized.</span></span>
-   <span data-ttu-id="ed82b-118">Vertices werden um jedes Dreieck in der Richtung gegen den Uhrzeigersinn angeordnet.</span><span class="sxs-lookup"><span data-stu-id="ed82b-118">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>
-   <span data-ttu-id="ed82b-119">Verwenden Sie die pro-Vertex-normal Vektoren, die bereits im Eingabe Mesh vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ed82b-119">Use per-vertex normal vectors already present in the input mesh.</span></span>
-   <span data-ttu-id="ed82b-120">Die Ergebnisse werden im ursprünglichen Eingabe Mesh gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ed82b-120">The results will be stored in the original input mesh.</span></span> <span data-ttu-id="ed82b-121">Die Funktion schlägt fehl, wenn neue Vertices erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ed82b-121">The function will fail if new vertices need to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed82b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed82b-122">Return value</span></span>

<span data-ttu-id="ed82b-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed82b-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed82b-124">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed82b-124">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ed82b-125">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="ed82b-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed82b-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed82b-126">Remarks</span></span>

<span data-ttu-id="ed82b-127">Diese Funktion ruft einfach [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) mit den folgenden Eingabe Parametern auf:</span><span class="sxs-lookup"><span data-stu-id="ed82b-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



<span data-ttu-id="ed82b-128">Singularitäten werden nach Bedarf durch Gruppierung von Rändern und Aufteilen von Scheitel Punkten behandelt.</span><span class="sxs-lookup"><span data-stu-id="ed82b-128">Singularities are handled as required by grouping edges and splitting vertices.</span></span> <span data-ttu-id="ed82b-129">Wenn Vertices aufgeteilt werden müssen, schlägt die Funktion fehl.</span><span class="sxs-lookup"><span data-stu-id="ed82b-129">If any vertices need to be split, the function will fail.</span></span> <span data-ttu-id="ed82b-130">Der berechnete normale Vektor bei jedem Scheitelpunkt wird immer normalisiert, sodass er über eine Einheitslänge verfügt.</span><span class="sxs-lookup"><span data-stu-id="ed82b-130">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="ed82b-131">Die stabilste Lösung für die Berechnung von orthogonalen kartesischen Koordinaten ist das Festlegen von Flags D3DXTANGENT \_ orthogonalize \_ von \_ Ihnen und D3DXTANGENT \_ orthogonalize \_ von \_ V, sodass orthogonale Koordinaten aus beiden UV-Texturkoordinaten berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="ed82b-131">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both UV texture coordinates.</span></span> <span data-ttu-id="ed82b-132">Wenn in diesem Fall jedoch entweder "U" oder "V" gleich NULL ist, berechnet die Funktion orthogonale Koordinaten mithilfe von D3DXTANGENT \_ orthogonalize \_ von \_ V bzw \_ . D3DXTANGENT orthogonalize \_ von \_ U bzw..</span><span class="sxs-lookup"><span data-stu-id="ed82b-132">However, in this case, if either U or V is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed82b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed82b-133">Requirements</span></span>



| <span data-ttu-id="ed82b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed82b-134">Requirement</span></span> | <span data-ttu-id="ed82b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ed82b-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed82b-136">Header</span><span class="sxs-lookup"><span data-stu-id="ed82b-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ed82b-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed82b-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ed82b-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ed82b-138">Library</span></span><br/> | <dl> <span data-ttu-id="ed82b-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed82b-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed82b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed82b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed82b-141">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ed82b-141">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="ed82b-142">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="ed82b-142">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> <dt>

[<span data-ttu-id="ed82b-143">**D3DXTANGENT**</span><span class="sxs-lookup"><span data-stu-id="ed82b-143">**D3DXTANGENT**</span></span>](./d3dxtangent.md)
</dt> </dl>

 

 
