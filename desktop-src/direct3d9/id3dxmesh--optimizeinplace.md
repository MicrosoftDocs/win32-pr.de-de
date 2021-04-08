---
description: Generiert ein Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren. Diese Methode ordnet das vorhandene Mesh neu an.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'ID3DXMesh:: optimizzuplace-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f889e0d3754cc1321ffa59eba294038b87991489
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762303"
---
# <a name="id3dxmeshoptimizeinplace-method"></a><span data-ttu-id="8ba38-104">ID3DXMesh:: optimizzuplace-Methode</span><span class="sxs-lookup"><span data-stu-id="8ba38-104">ID3DXMesh::OptimizeInplace method</span></span>

<span data-ttu-id="8ba38-105">Generiert ein Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="8ba38-105">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="8ba38-106">Diese Methode ordnet das vorhandene Mesh neu an.</span><span class="sxs-lookup"><span data-stu-id="8ba38-106">This method reorders the existing mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba38-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ba38-107">Syntax</span></span>


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="8ba38-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ba38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba38-109">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8ba38-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba38-110">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ba38-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ba38-111">Eine Kombination aus einem oder mehreren [**D3DXMESHOPT**](./d3dxmeshopt.md) -Flags, die den Typ der auszuführenden Optimierung angibt.</span><span class="sxs-lookup"><span data-stu-id="8ba38-111">Combination of one or more [**D3DXMESHOPT**](./d3dxmeshopt.md) flags, specifying the type of optimization to perform.</span></span>

</dd> <dt>

<span data-ttu-id="8ba38-112">*padjackocyin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ba38-112">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba38-113">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ba38-113">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ba38-114">Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im quellmesh angibt.</span><span class="sxs-lookup"><span data-stu-id="8ba38-114">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="8ba38-115">Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="8ba38-115">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="8ba38-116">*padjacumcyout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8ba38-116">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba38-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ba38-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ba38-118">Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im optimierten Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="8ba38-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="8ba38-119">Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="8ba38-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="8ba38-120">Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ba38-120">If the value supplied for this argument is **NULL**, adjacency data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="8ba38-121">*pfakeremap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8ba38-121">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba38-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ba38-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ba38-123">Ein Array von DWords, eines pro Gesicht, das die ursprüngliche Gitterfläche angibt, die den einzelnen Flächen im optimierten Mesh entspricht.</span><span class="sxs-lookup"><span data-stu-id="8ba38-123">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="8ba38-124">Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Gesichts Umwandlungs Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ba38-124">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="8ba38-125">*ppvertexremap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8ba38-125">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba38-126">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ba38-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8ba38-127">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitel Punkten den alten Scheitel Punkten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8ba38-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="8ba38-128">Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunkt Zuordnung ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="8ba38-128">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="8ba38-129">Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Vertex-neuumwandlungs Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ba38-129">If the value supplied for this argument is **NULL**, vertex remap data is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba38-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ba38-130">Return value</span></span>

<span data-ttu-id="8ba38-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ba38-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ba38-132">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8ba38-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8ba38-133">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ cannotattrsort, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="8ba38-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba38-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ba38-134">Remarks</span></span>

<span data-ttu-id="8ba38-135">Vor dem Ausführen von **ID3DXMesh:: OptimizeInPlace** muss eine Anwendung durch Aufrufen von [**ID3DXBaseMesh:: generateency**](id3dxbasemesh--generateadjacency.md)einen antreffenden Puffer generieren.</span><span class="sxs-lookup"><span data-stu-id="8ba38-135">Before running **ID3DXMesh::OptimizeInplace**, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="8ba38-136">Der zutreffende Puffer enthält Informationen zu den Daten, z. b. eine Liste der Kanten und die Gesichter, die nebeneinander angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8ba38-136">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

> [!Note]  
> <span data-ttu-id="8ba38-137">Diese Methode schlägt fehl, wenn das Mesh den Vertex-Puffer mit einem anderen Mesh freigibt, es sei denn, die D3DXMESHOPT \_ ignoreverts werden in Flags festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ba38-137">This method will fail if the mesh is sharing its vertex buffer with another mesh, unless the D3DXMESHOPT\_IGNOREVERTS is set in Flags.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ba38-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ba38-138">Requirements</span></span>



| <span data-ttu-id="8ba38-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ba38-139">Requirement</span></span> | <span data-ttu-id="8ba38-140">Wert</span><span class="sxs-lookup"><span data-stu-id="8ba38-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba38-141">Header</span><span class="sxs-lookup"><span data-stu-id="8ba38-141">Header</span></span><br/>  | <dl> <span data-ttu-id="8ba38-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ba38-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8ba38-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ba38-143">Library</span></span><br/> | <dl> <span data-ttu-id="8ba38-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ba38-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ba38-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ba38-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba38-146">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="8ba38-146">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="8ba38-147">**ID3DXMesh:: optimieren**</span><span class="sxs-lookup"><span data-stu-id="8ba38-147">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> </dl>

 

 
