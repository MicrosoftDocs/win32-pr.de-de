---
description: Nimmt ein Mesh an und gibt ein neues Mesh mit pro-vertexblend-Gewichtungen und einer Tabelle mit einer Kombination aus der Tabelle zurück In der Tabelle ist beschrieben, welche Knochen welche Teilmengen des Netzes beeinflussen.
ms.assetid: c26a9e84-5731-4394-a047-5f1ffe7688d9
title: 'ID3DXSkinInfo:: convertdeblendedmesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 051c51291416dd7e190c83433a9bf84baeb92957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363182"
---
# <a name="id3dxskininfoconverttoblendedmesh-method"></a><span data-ttu-id="8cb28-104">ID3DXSkinInfo:: convertdeblendedmesh-Methode</span><span class="sxs-lookup"><span data-stu-id="8cb28-104">ID3DXSkinInfo::ConvertToBlendedMesh method</span></span>

<span data-ttu-id="8cb28-105">Nimmt ein Mesh an und gibt ein neues Mesh mit pro-vertexblend-Gewichtungen und einer Tabelle mit einer Kombination aus der Tabelle zurück</span><span class="sxs-lookup"><span data-stu-id="8cb28-105">Takes a mesh and returns a new mesh with per-vertex blend weights and a bone combination table.</span></span> <span data-ttu-id="8cb28-106">In der Tabelle ist beschrieben, welche Knochen welche Teilmengen des Netzes beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="8cb28-106">The table describes which bones affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cb28-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cb28-107">Syntax</span></span>


```C++
HRESULT ConvertToBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
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



## <a name="parameters"></a><span data-ttu-id="8cb28-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cb28-109">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cb28-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb28-110">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="8cb28-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="8cb28-111">Eingabe Gitter.</span><span class="sxs-lookup"><span data-stu-id="8cb28-111">Input mesh.</span></span> <span data-ttu-id="8cb28-112">Siehe [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="8cb28-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cb28-113">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cb28-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb28-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cb28-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cb28-115">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8cb28-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="8cb28-116">*padjackocyin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cb28-116">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb28-117">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8cb28-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8cb28-118">Informationen zur Eingabe Gitter Informationen.</span><span class="sxs-lookup"><span data-stu-id="8cb28-118">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="8cb28-119">*padjacumcyout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cb28-119">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb28-120">Typ: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cb28-120">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cb28-121">Informationen zur Ausgabe Gitter Informationen.</span><span class="sxs-lookup"><span data-stu-id="8cb28-121">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="8cb28-122">*pfakeremap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8cb28-122">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb28-123">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cb28-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8cb28-124">Ein Array von DWords, eines pro Gesicht, das die ursprüngliche Gitterfläche angibt, die den einzelnen Flächen im gemischten Mesh entspricht.</span><span class="sxs-lookup"><span data-stu-id="8cb28-124">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="8cb28-125">Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Gesichts Umwandlungs Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8cb28-125">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="8cb28-126">*ppvertexremap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8cb28-126">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb28-127">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cb28-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8cb28-128">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitel Punkten den alten Scheitel Punkten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8cb28-128">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="8cb28-129">Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunkt Zuordnung ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="8cb28-129">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="8cb28-130">Dieser Parameter ist optional. **Null** kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cb28-130">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="8cb28-131">*pmaxvertexinfl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8cb28-131">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb28-132">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cb28-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8cb28-133">Ein Zeiger auf ein DWORD-Wert, der die maximale Anzahl der für den Scheitelpunkt für diese Skinning-Methode erforderlichen Knochen Einflüsse enthält.</span><span class="sxs-lookup"><span data-stu-id="8cb28-133">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="8cb28-134">*pnumbonekombinationen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8cb28-134">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb28-135">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cb28-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8cb28-136">Ein Zeiger auf die Anzahl der Knochen in der Tabelle mit der Knochen Kombination.</span><span class="sxs-lookup"><span data-stu-id="8cb28-136">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="8cb28-137">*ppbonecombinationtable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8cb28-137">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb28-138">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cb28-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8cb28-139">Zeiger auf die Tabelle mit der Knochen Kombination.</span><span class="sxs-lookup"><span data-stu-id="8cb28-139">Pointer to the bone combination table.</span></span> <span data-ttu-id="8cb28-140">Die Daten werden in einer [**D3DXBONECOMBINATION**](d3dxbonecombination.md) -Struktur organisiert.</span><span class="sxs-lookup"><span data-stu-id="8cb28-140">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8cb28-141">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8cb28-141">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb28-142">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cb28-142">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="8cb28-143">Zeiger auf das neue Mesh.</span><span class="sxs-lookup"><span data-stu-id="8cb28-143">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cb28-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cb28-144">Return value</span></span>

<span data-ttu-id="8cb28-145">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8cb28-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8cb28-146">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8cb28-146">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8cb28-147">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="8cb28-147">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cb28-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cb28-148">Remarks</span></span>

<span data-ttu-id="8cb28-149">Jedes Element im Umwandlungs-Array gibt den vorherigen Index für diese Position an.</span><span class="sxs-lookup"><span data-stu-id="8cb28-149">Each element in the remap array specifies the previous index for that position.</span></span> <span data-ttu-id="8cb28-150">Wenn sich z. b. ein Scheitelpunkt an Position 3, aber an Position 5 neu zugeordnet wurde, enthält das fünfte Element von pvertexremap 3.</span><span class="sxs-lookup"><span data-stu-id="8cb28-150">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="8cb28-151">Diese Methode kann nicht auf Hardware ausgeführt werden, die eine Scheitelpunkt Mischung mit fester Funktion nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cb28-151">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cb28-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cb28-152">Requirements</span></span>



| <span data-ttu-id="8cb28-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cb28-153">Requirement</span></span> | <span data-ttu-id="8cb28-154">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb28-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb28-155">Header</span><span class="sxs-lookup"><span data-stu-id="8cb28-155">Header</span></span><br/>  | <dl> <span data-ttu-id="8cb28-156"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cb28-156"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8cb28-157">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8cb28-157">Library</span></span><br/> | <dl> <span data-ttu-id="8cb28-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cb28-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8cb28-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cb28-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cb28-160">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="8cb28-160">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
