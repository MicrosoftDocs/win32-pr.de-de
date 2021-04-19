---
description: Führt die Software in einem Array von Vertices aus.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: ID3DX10SkinInfo::D osoftwareskinning-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54dfe909e36be0273e0679a824ff0674b0e3b38c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363142"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a><span data-ttu-id="d9d79-103">ID3DX10SkinInfo::D osoftwareskinning-Methode</span><span class="sxs-lookup"><span data-stu-id="d9d79-103">ID3DX10SkinInfo::DoSoftwareSkinning method</span></span>

<span data-ttu-id="d9d79-104">Führt die Software in einem Array von Vertices aus.</span><span class="sxs-lookup"><span data-stu-id="d9d79-104">Do software skinning on an array of vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9d79-105">Syntax</span></span>


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a><span data-ttu-id="d9d79-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9d79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9d79-107">*StartVertex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-107">*StartVertex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9d79-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9d79-109">Ein 0-basierter Index in psrcvertices.</span><span class="sxs-lookup"><span data-stu-id="d9d79-109">A 0-based index into pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="d9d79-110">*VertexCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-110">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9d79-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9d79-112">Anzahl der zu transformierenden Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="d9d79-112">Number of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="d9d79-113">*psrcvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-113">*pSrcVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-114">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="d9d79-114">Type: **void\***</span></span>

<span data-ttu-id="d9d79-115">Zeiger auf ein Array von Vertices, die transformiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d9d79-115">Pointer to an array of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="d9d79-116">*Srcstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-116">*SrcStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9d79-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9d79-118">Die Größe eines Scheitel Punkts in psrcvertices (in Byte).</span><span class="sxs-lookup"><span data-stu-id="d9d79-118">The size, in bytes, of a vertex in pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="d9d79-119">*pdestvertices* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-119">*pDestVertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-120">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="d9d79-120">Type: **void\***</span></span>

<span data-ttu-id="d9d79-121">Zeiger auf ein Array von Vertices, das mit den transformierten Scheitel Punkten gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="d9d79-121">Pointer to an array of vertices, which will be filled with the transformed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d9d79-122">*Deststride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-122">*DestStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9d79-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9d79-124">Die Größe eines Scheitel Punkts in pdestvertices (in Byte).</span><span class="sxs-lookup"><span data-stu-id="d9d79-124">The size, in bytes, of a vertex in pDestVertices.</span></span>

</dd> <dt>

<span data-ttu-id="d9d79-125">*pbonematrices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-125">*pBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-126">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9d79-126">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d9d79-127">Ein Array von Matrizen, das verwendet wird, um die jedem Knochen zugeordneten Punkte zu transformieren, sodass die dem "Bone i" zugeordneten Scheitel Punkte \[ \] von pbonematrices i transformiert werden \[ \] .</span><span class="sxs-lookup"><span data-stu-id="d9d79-127">An array of matrices that will be used to transform the points mapped to each bone, such that the vertices mapped to bone\[i\] will be transformed by pBoneMatrices\[i\].</span></span> <span data-ttu-id="d9d79-128">Dieses Array wird nur verwendet, um die Matrizen zu transformieren, wenn der isnormal-Wert in pchanneldescs auf **false** festgelegt ist, andernfalls wird pinversetransposebonematrices verwendet.</span><span class="sxs-lookup"><span data-stu-id="d9d79-128">This array will be used to transform the matrices only if the IsNormal value in pChannelDescs is set to **FALSE**, otherwise pInverseTransposeBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="d9d79-129">*pinverabversieinbonematrices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-129">*pInverseTransposeBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-130">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9d79-130">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d9d79-131">Wenn dieser Wert **null** ist, wird er auf pbonematrices festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9d79-131">If this value is **NULL**, it will be set equal to pBoneMatrices.</span></span> <span data-ttu-id="d9d79-132">Dieses Array von Matrizen wird nur verwendet, um die Scheitel Punkte zu transformieren, wenn der isnormal-Wert in pchanneldescs auf **true** festgelegt ist, andernfalls wird pbonematrices verwendet.</span><span class="sxs-lookup"><span data-stu-id="d9d79-132">This array of matrices will be used to transform the vertices only if the IsNormal value in pChannelDescs is set to **TRUE**, otherwise pBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="d9d79-133">*pchanneldescs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-133">*pChannelDescs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-134">Type: **[ **d3dx10 \_ Skinning \_ Channel**](d3dx10-skinning-channel.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9d79-134">Type: **[**D3DX10\_SKINNING\_CHANNEL**](d3dx10-skinning-channel.md)\***</span></span>

<span data-ttu-id="d9d79-135">Zeiger auf eine d3dx10 \_ SKINNING \_ Channel-Struktur, die den Member der Vertex-decl bestimmt, auf der das softwareskinning ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9d79-135">Pointer to a D3DX10\_SKINNING\_CHANNEL structure, which determines the member of the vertex decl the software skinning will be done on.</span></span>

</dd> <dt>

<span data-ttu-id="d9d79-136">*Numchannels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-136">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-137">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9d79-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9d79-138">Die Anzahl der d3dx10 \_ Skinning \_ Channel-Strukturen in pchanneldescs.</span><span class="sxs-lookup"><span data-stu-id="d9d79-138">The number of D3DX10\_SKINNING\_CHANNEL structures in pChannelDescs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9d79-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9d79-139">Return value</span></span>

<span data-ttu-id="d9d79-140">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9d79-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9d79-141">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d9d79-141">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d9d79-142">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg.</span><span class="sxs-lookup"><span data-stu-id="d9d79-142">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d79-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9d79-143">Remarks</span></span>

<span data-ttu-id="d9d79-144">Im folgenden finden Sie ein Beispiel für die Verwendung der softwareskinning:</span><span class="sxs-lookup"><span data-stu-id="d9d79-144">Here is an example of how to use software skinning:</span></span>


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



## <a name="requirements"></a><span data-ttu-id="d9d79-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9d79-145">Requirements</span></span>



| <span data-ttu-id="d9d79-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9d79-146">Requirement</span></span> | <span data-ttu-id="d9d79-147">Wert</span><span class="sxs-lookup"><span data-stu-id="d9d79-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d79-148">Header</span><span class="sxs-lookup"><span data-stu-id="d9d79-148">Header</span></span><br/>  | <dl> <span data-ttu-id="d9d79-149"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9d79-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9d79-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9d79-150">Library</span></span><br/> | <dl> <span data-ttu-id="d9d79-151"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9d79-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9d79-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9d79-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9d79-153">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="d9d79-153">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="d9d79-154">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d9d79-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
