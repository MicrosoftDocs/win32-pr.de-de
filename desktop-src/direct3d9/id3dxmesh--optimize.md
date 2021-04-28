---
description: 'ID3DXMesh::Optimize-Methode: Generiert ein neues Gitternetz mit neu angeordneten Gesichtern und Scheitelungen, um die Zeichnungsleistung zu optimieren.'
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: ID3DXMesh::Optimize-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: debec1c0ee54e612ab0de832dbc5c2481dcefad8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093308"
---
# <a name="id3dxmeshoptimize-method"></a><span data-ttu-id="34e30-103">ID3DXMesh::Optimize-Methode</span><span class="sxs-lookup"><span data-stu-id="34e30-103">ID3DXMesh::Optimize method</span></span>

<span data-ttu-id="34e30-104">Generiert ein neues Gitternetz mit neu angeordneten Gesichtern und Scheitelungen, um die Zeichnungsleistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="34e30-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e30-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34e30-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="34e30-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34e30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e30-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="34e30-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e30-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34e30-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34e30-109">Gibt den Typ der durchzuführenden Optimierung an.</span><span class="sxs-lookup"><span data-stu-id="34e30-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="34e30-110">Dieser Parameter kann auf eine Kombination aus mindestens einem Flag von [**D3DXMESHOPT**](./d3dxmeshopt.md) und [**D3DXMESH**](./d3dxmesh.md) festgelegt werden (außer D3DXMESH \_ 32BIT, D3DXMESH \_ IB WRITEONLY und \_ D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="34e30-110">This parameter can be set to a combination of one or more flags from [**D3DXMESHOPT**](./d3dxmeshopt.md) and [**D3DXMESH**](./d3dxmesh.md) (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="34e30-111">*pAdjacencyIn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="34e30-111">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e30-112">Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="34e30-112">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="34e30-113">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Quellgitter angibt.</span><span class="sxs-lookup"><span data-stu-id="34e30-113">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="34e30-114">Wenn der Rand keine angrenzenden Gesichter hat, wird der Wert 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="34e30-114">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="34e30-115">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="34e30-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="34e30-116">*pAdjacencyOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="34e30-116">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="34e30-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="34e30-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="34e30-118">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im optimierten Gitter angibt.</span><span class="sxs-lookup"><span data-stu-id="34e30-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="34e30-119">Wenn der Rand keine angrenzenden Gesichter hat, wird der Wert 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="34e30-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="34e30-120">*pFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="34e30-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="34e30-121">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="34e30-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="34e30-122">Ein Array von DWORDs pro Gesicht, das das ursprüngliche Gitternetzgesicht identifiziert, das jedem Gesicht im optimierten Gitter entspricht.</span><span class="sxs-lookup"><span data-stu-id="34e30-122">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="34e30-123">Wenn der für dieses Argument angegebene Wert **NULL ist,** werden keine Gesichtszuordnungsdaten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34e30-123">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="34e30-124">*ppVertexRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="34e30-124">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34e30-125">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="34e30-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="34e30-126">Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle,**](id3dxbuffer.md) die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitelpunkte den alten Scheitelpunkten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="34e30-126">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="34e30-127">Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunktzuordnung ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="34e30-127">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> <dt>

<span data-ttu-id="34e30-128">*ppOptMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="34e30-128">*ppOptMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34e30-129">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="34e30-129">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="34e30-130">Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das optimierte Gitternetz darstellt.</span><span class="sxs-lookup"><span data-stu-id="34e30-130">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the optimized mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e30-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34e30-131">Return value</span></span>

<span data-ttu-id="34e30-132">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="34e30-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="34e30-133">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="34e30-133">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="34e30-134">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="34e30-134">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="34e30-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34e30-135">Remarks</span></span>

<span data-ttu-id="34e30-136">Diese Methode generiert ein neues Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="34e30-136">This method generates a new mesh.</span></span> <span data-ttu-id="34e30-137">Vor dem Ausführen von Optimize muss eine Anwendung einen Adjazenzpuffer generieren, indem [**ID3DXBaseMesh::GenerateAdjaency**](id3dxbasemesh--generateadjacency.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="34e30-137">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="34e30-138">Der Adjazenzpuffer enthält Adjazenzdaten, z. B. eine Liste von Kanten und den nebeneinander liegenden Gesichtern.</span><span class="sxs-lookup"><span data-stu-id="34e30-138">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="34e30-139">Diese Methode ist der [**ID3DXBaseMesh::CloneMesh-Methode**](id3dxbasemesh--clonemesh.md) sehr ähnlich, mit der Ausnahme, dass sie beim Generieren des neuen Klons des Gitternetzes Optimierungen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="34e30-139">This method is very similar to the [**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="34e30-140">Das Ausgabegitternetz erbt alle Erstellungsparameter des Eingabegitters.</span><span class="sxs-lookup"><span data-stu-id="34e30-140">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="34e30-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34e30-141">Requirements</span></span>



| <span data-ttu-id="34e30-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34e30-142">Requirement</span></span> | <span data-ttu-id="34e30-143">Wert</span><span class="sxs-lookup"><span data-stu-id="34e30-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34e30-144">Header</span><span class="sxs-lookup"><span data-stu-id="34e30-144">Header</span></span><br/>  | <dl> <span data-ttu-id="34e30-145"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="34e30-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="34e30-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34e30-146">Library</span></span><br/> | <dl> <span data-ttu-id="34e30-147"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="34e30-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="34e30-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="34e30-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e30-149">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="34e30-149">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="34e30-150">**ID3DXMesh::OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="34e30-150">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
