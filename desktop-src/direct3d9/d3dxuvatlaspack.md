---
description: Packen Sie Mesh-Partitionierungs Daten in einen Atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: D3DXUVAtlasPack-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31de326160120fe14a71841cb5f2d18e1c8d4e57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357234"
---
# <a name="d3dxuvatlaspack-function"></a><span data-ttu-id="e0cbf-103">D3DXUVAtlasPack-Funktion</span><span class="sxs-lookup"><span data-stu-id="e0cbf-103">D3DXUVAtlasPack function</span></span>

<span data-ttu-id="e0cbf-104">Packen Sie Mesh-Partitionierungs Daten in einen Atlas.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-104">Pack mesh partitioning data into an atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0cbf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0cbf-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a><span data-ttu-id="e0cbf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0cbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0cbf-107">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cbf-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cbf-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="e0cbf-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="e0cbf-109">Zeiger auf ein Eingabe Mesh (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des Atlas enthält.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="e0cbf-110">Das Mesh muss mindestens Positionsdaten und 2D-Texturkoordinaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="e0cbf-111">*dwwidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cbf-111">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cbf-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0cbf-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0cbf-113">Textur Breite.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-113">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="e0cbf-114">*dwheight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cbf-114">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cbf-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0cbf-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0cbf-116">Textur Höhe.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-116">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="e0cbf-117">nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cbf-117">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cbf-118">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0cbf-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0cbf-119">Der Mindestabstand in texeln zwischen zwei Diagrammen im Atlas.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-119">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="e0cbf-120">Der bundbundwert wird immer durch die Breite skaliert. Wenn also ein bundbundwert von 2,5 für eine 512 x 512-Textur verwendet wird, ist der minimale Abstand zwischen zwei Diagrammen 2,5/512,0 Texels.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-120">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="e0cbf-121">*dwtextureindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cbf-121">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cbf-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0cbf-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0cbf-123">NULL basierter Texturkoordinaten Index, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-123">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="e0cbf-124">*pdwpartitionresultadjacency*</span><span class="sxs-lookup"><span data-stu-id="e0cbf-124">*pdwPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="e0cbf-125">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e0cbf-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e0cbf-126">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="e0cbf-127">Sie sollte von der pppartitionresultadjacency abgeleitet werden, die von [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-127">It should be derived from the ppPartitionResultAdjacency returned from [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span></span> <span data-ttu-id="e0cbf-128">Dieser Wert darf nicht **null** sein, da Pack wissen muss, wo Diagramme im Partitions Schritt abgeschnitten wurden, um die Kanten der einzelnen Diagramme zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-128">This value cannot be **NULL**, because Pack needs to know where charts were cut in the partition step in order to find the edges of each chart.</span></span>

</dd> <dt>

<span data-ttu-id="e0cbf-129">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cbf-129">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cbf-130">Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="e0cbf-130">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="e0cbf-131">Ein Zeiger auf eine Rückruffunktion (siehe [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)), die zum Überwachen des Fortschritts nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-131">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="e0cbf-132">" *schcallbackfrequency* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="e0cbf-132">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cbf-133">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0cbf-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0cbf-134">Geben Sie an, wie oft D3DX den Rückruf aufruft. ein angemessener Standardwert ist 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-134">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="e0cbf-135">*pusercontent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cbf-135">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cbf-136">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0cbf-136">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0cbf-137">Ein void-Zeiger, der an die Rückruffunktion zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-137">A void pointer to be passed back to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="e0cbf-138">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cbf-138">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cbf-139">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0cbf-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0cbf-140">Dieser Optionsparameter ist derzeit reserviert.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-140">This options parameter is currently reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e0cbf-141">*pfacepartitionierung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cbf-141">*pFacePartitioning* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cbf-142">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e0cbf-142">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="e0cbf-143">Ein Zeiger auf ein [**ID3DXBuffer**](id3dxbuffer.md) -Wert, der das Array der abschließenden Gesichts Partitionierung enthält.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-143">A pointer to an [**ID3DXBuffer**](id3dxbuffer.md) containing the array of the final face-partitioning.</span></span> <span data-ttu-id="e0cbf-144">Jedes Element enthält ein DWORD pro Gesicht.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-144">Each element contains one DWORD per face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0cbf-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0cbf-145">Return value</span></span>

<span data-ttu-id="e0cbf-146">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0cbf-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0cbf-147">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK; andernfalls ist der Wert D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-147">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0cbf-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0cbf-148">Requirements</span></span>



| <span data-ttu-id="e0cbf-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0cbf-149">Requirement</span></span> | <span data-ttu-id="e0cbf-150">Wert</span><span class="sxs-lookup"><span data-stu-id="e0cbf-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0cbf-151">Header</span><span class="sxs-lookup"><span data-stu-id="e0cbf-151">Header</span></span><br/>  | <dl> <span data-ttu-id="e0cbf-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0cbf-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e0cbf-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0cbf-153">Library</span></span><br/> | <dl> <span data-ttu-id="e0cbf-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0cbf-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0cbf-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0cbf-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0cbf-156">Uvatlas-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e0cbf-156">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
