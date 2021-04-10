---
description: Generiert ein neues Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'ID3DXMesh:: optimiert-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7752e08236094d7038a5e77ac1a679f787305022
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961770"
---
# <a name="id3dxmeshoptimize-method"></a><span data-ttu-id="78dff-103">ID3DXMesh:: optimiert-Methode</span><span class="sxs-lookup"><span data-stu-id="78dff-103">ID3DXMesh::Optimize method</span></span>

<span data-ttu-id="78dff-104">Generiert ein neues Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="78dff-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="78dff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78dff-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a><span data-ttu-id="78dff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78dff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78dff-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="78dff-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78dff-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78dff-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78dff-109">Gibt den Typ der auszuführenden Optimierung an.</span><span class="sxs-lookup"><span data-stu-id="78dff-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="78dff-110">Dieser Parameter kann auf eine Kombination aus einem oder mehreren Flags aus [**D3DXMESHOPT**](./d3dxmeshopt.md) und [**D3DXMESH**](./d3dxmesh.md) festgelegt werden (mit Ausnahme von D3DXMESH \_ 32 Bit, D3DXMESH \_ IB \_ Write only und D3DXMESH \_ Write).</span><span class="sxs-lookup"><span data-stu-id="78dff-110">This parameter can be set to a combination of one or more flags from [**D3DXMESHOPT**](./d3dxmeshopt.md) and [**D3DXMESH**](./d3dxmesh.md) (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="78dff-111">*padjackocyin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78dff-111">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78dff-112">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="78dff-112">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78dff-113">Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im quellmesh angibt.</span><span class="sxs-lookup"><span data-stu-id="78dff-113">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="78dff-114">Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="78dff-114">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="78dff-115">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="78dff-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="78dff-116">*padjacumcyout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="78dff-116">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78dff-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78dff-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78dff-118">Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im optimierten Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="78dff-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="78dff-119">Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="78dff-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="78dff-120">*pfakeremap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="78dff-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78dff-121">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78dff-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78dff-122">Ein Array von DWords, eines pro Gesicht, das die ursprüngliche Gitterfläche angibt, die den einzelnen Flächen im optimierten Mesh entspricht.</span><span class="sxs-lookup"><span data-stu-id="78dff-122">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="78dff-123">Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Gesichts Umwandlungs Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78dff-123">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="78dff-124">*ppvertexremap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="78dff-124">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78dff-125">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="78dff-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="78dff-126">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitel Punkten den alten Scheitel Punkten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="78dff-126">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="78dff-127">Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunkt Zuordnung ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="78dff-127">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> <dt>

<span data-ttu-id="78dff-128">*ppoptmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="78dff-128">*ppOptMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78dff-129">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="78dff-129">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="78dff-130">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das optimierte Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="78dff-130">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the optimized mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78dff-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78dff-131">Return value</span></span>

<span data-ttu-id="78dff-132">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78dff-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78dff-133">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="78dff-133">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="78dff-134">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="78dff-134">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="78dff-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78dff-135">Remarks</span></span>

<span data-ttu-id="78dff-136">Diese Methode generiert ein neues Mesh.</span><span class="sxs-lookup"><span data-stu-id="78dff-136">This method generates a new mesh.</span></span> <span data-ttu-id="78dff-137">Bevor Sie optimieren ausführen, muss eine Anwendung durch Aufrufen von [**ID3DXBaseMesh:: generateency**](id3dxbasemesh--generateadjacency.md)einen Ereignis Puffer generieren.</span><span class="sxs-lookup"><span data-stu-id="78dff-137">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="78dff-138">Der zutreffende Puffer enthält Informationen zu den Daten, z. b. eine Liste der Kanten und die Gesichter, die nebeneinander angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="78dff-138">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="78dff-139">Diese Methode ähnelt der [**ID3DXBaseMesh:: clonemesh**](id3dxbasemesh--clonemesh.md) -Methode, mit der Ausnahme, dass Sie beim Erzeugen des neuen Klon des Netzes eine Optimierung durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="78dff-139">This method is very similar to the [**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="78dff-140">Das Ausgabe Mesh erbt alle Erstellungs Parameter des eingabemesh.</span><span class="sxs-lookup"><span data-stu-id="78dff-140">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="78dff-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78dff-141">Requirements</span></span>



| <span data-ttu-id="78dff-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78dff-142">Requirement</span></span> | <span data-ttu-id="78dff-143">Wert</span><span class="sxs-lookup"><span data-stu-id="78dff-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78dff-144">Header</span><span class="sxs-lookup"><span data-stu-id="78dff-144">Header</span></span><br/>  | <dl> <span data-ttu-id="78dff-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="78dff-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="78dff-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78dff-146">Library</span></span><br/> | <dl> <span data-ttu-id="78dff-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78dff-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78dff-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78dff-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78dff-149">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="78dff-149">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="78dff-150">**ID3DXMesh:: optimizeingeplace**</span><span class="sxs-lookup"><span data-stu-id="78dff-150">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
