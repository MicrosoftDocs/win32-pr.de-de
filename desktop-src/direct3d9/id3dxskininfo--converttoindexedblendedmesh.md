---
description: Nimmt ein Mesh an und gibt ein neues Mesh mit pro-Vertex-Blend-Gewichtungen,-Indizes und einer Bone-Kombinations Tabelle zurück. In der Tabelle wird beschrieben, welche Knochen Paletten welche Teilmengen des Netzes beeinflussen.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'ID3DXSkinInfo:: convertdeindexedblendedmesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373541"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a><span data-ttu-id="80d8e-104">ID3DXSkinInfo:: convertdeindexedblendedmesh-Methode</span><span class="sxs-lookup"><span data-stu-id="80d8e-104">ID3DXSkinInfo::ConvertToIndexedBlendedMesh method</span></span>

<span data-ttu-id="80d8e-105">Nimmt ein Mesh an und gibt ein neues Mesh mit pro-Vertex-Blend-Gewichtungen,-Indizes und einer Bone-Kombinations Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="80d8e-105">Takes a mesh and returns a new mesh with per-vertex blend weights, indices, and a bone combination table.</span></span> <span data-ttu-id="80d8e-106">In der Tabelle wird beschrieben, welche Knochen Paletten welche Teilmengen des Netzes beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="80d8e-106">The table describes which bone palettes affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="80d8e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="80d8e-107">Syntax</span></span>


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="80d8e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="80d8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80d8e-109">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80d8e-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80d8e-110">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="80d8e-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="80d8e-111">Das eingabemesh.</span><span class="sxs-lookup"><span data-stu-id="80d8e-111">The input mesh.</span></span> <span data-ttu-id="80d8e-112">Siehe [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="80d8e-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="80d8e-113">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80d8e-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80d8e-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80d8e-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80d8e-115">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="80d8e-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="80d8e-116">*palettesize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80d8e-116">*paletteSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80d8e-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80d8e-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80d8e-118">Anzahl der für die Matrix Palette verfügbaren Knochen Matrizen.</span><span class="sxs-lookup"><span data-stu-id="80d8e-118">Number of bone matrices available for matrix palette skinning.</span></span>

</dd> <dt>

<span data-ttu-id="80d8e-119">*padjackocyin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80d8e-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80d8e-120">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="80d8e-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="80d8e-121">Informationen zur Eingabe Gitter Informationen.</span><span class="sxs-lookup"><span data-stu-id="80d8e-121">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="80d8e-122">*padjacumcyout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80d8e-122">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80d8e-123">Typ: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80d8e-123">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80d8e-124">Informationen zur Ausgabe Gitter Informationen.</span><span class="sxs-lookup"><span data-stu-id="80d8e-124">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="80d8e-125">*pfakeremap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80d8e-125">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80d8e-126">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="80d8e-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="80d8e-127">Ein Array von DWords, eines pro Gesicht, das die ursprüngliche Gitterfläche angibt, die den einzelnen Flächen im gemischten Mesh entspricht.</span><span class="sxs-lookup"><span data-stu-id="80d8e-127">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="80d8e-128">Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Gesichts Umwandlungs Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="80d8e-128">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="80d8e-129">*ppvertexremap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80d8e-129">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80d8e-130">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="80d8e-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="80d8e-131">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitel Punkten den alten Scheitel Punkten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="80d8e-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="80d8e-132">Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunkt Zuordnung ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="80d8e-132">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="80d8e-133">Dieser Parameter ist optional. **Null** kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80d8e-133">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="80d8e-134">*pmaxvertexinfl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80d8e-134">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80d8e-135">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="80d8e-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="80d8e-136">Ein Zeiger auf ein DWORD-Wert, der die maximale Anzahl der für den Scheitelpunkt für diese Skinning-Methode erforderlichen Knochen Einflüsse enthält.</span><span class="sxs-lookup"><span data-stu-id="80d8e-136">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="80d8e-137">*pnumbonekombinationen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80d8e-137">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80d8e-138">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="80d8e-138">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="80d8e-139">Ein Zeiger auf die Anzahl der Knochen in der Tabelle mit der Knochen Kombination.</span><span class="sxs-lookup"><span data-stu-id="80d8e-139">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="80d8e-140">*ppbonecombinationtable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80d8e-140">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80d8e-141">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="80d8e-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="80d8e-142">Zeiger auf die Tabelle mit der Knochen Kombination.</span><span class="sxs-lookup"><span data-stu-id="80d8e-142">Pointer to the bone combination table.</span></span> <span data-ttu-id="80d8e-143">Die Daten werden in einer [**D3DXBONECOMBINATION**](d3dxbonecombination.md) -Struktur organisiert.</span><span class="sxs-lookup"><span data-stu-id="80d8e-143">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="80d8e-144">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80d8e-144">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80d8e-145">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="80d8e-145">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="80d8e-146">Zeiger auf das neue Mesh.</span><span class="sxs-lookup"><span data-stu-id="80d8e-146">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80d8e-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80d8e-147">Return value</span></span>

<span data-ttu-id="80d8e-148">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80d8e-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80d8e-149">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80d8e-149">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="80d8e-150">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="80d8e-150">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="80d8e-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80d8e-151">Remarks</span></span>

<span data-ttu-id="80d8e-152">Jedes Element in den Umwandlungs-Arrays gibt den vorherigen Index für diese Position an.</span><span class="sxs-lookup"><span data-stu-id="80d8e-152">Each element in the remap arrays specifies the previous index for that position.</span></span> <span data-ttu-id="80d8e-153">Wenn sich z. b. ein Scheitelpunkt an Position 3, aber an Position 5 neu zugeordnet wurde, enthält das fünfte Element von pvertexremap 3.</span><span class="sxs-lookup"><span data-stu-id="80d8e-153">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="80d8e-154">Diese Methode kann nicht auf Hardware ausgeführt werden, die eine Scheitelpunkt Mischung mit fester Funktion nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="80d8e-154">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="80d8e-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80d8e-155">Requirements</span></span>



| <span data-ttu-id="80d8e-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80d8e-156">Requirement</span></span> | <span data-ttu-id="80d8e-157">Wert</span><span class="sxs-lookup"><span data-stu-id="80d8e-157">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80d8e-158">Header</span><span class="sxs-lookup"><span data-stu-id="80d8e-158">Header</span></span><br/>  | <dl> <span data-ttu-id="80d8e-159"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="80d8e-159"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="80d8e-160">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="80d8e-160">Library</span></span><br/> | <dl> <span data-ttu-id="80d8e-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80d8e-161"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80d8e-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80d8e-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80d8e-163">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="80d8e-163">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
