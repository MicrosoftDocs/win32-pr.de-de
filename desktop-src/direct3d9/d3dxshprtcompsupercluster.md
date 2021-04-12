---
description: Wird mit komprimierten Ergebnissen der vertexversion des PRT-Simulators (preberechneten Radiance Transfer) verwendet.
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: D3DXSHPRTCompSuperCluster-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1daf25dddfaf738ecc2fed9605429a19170177ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354707"
---
# <a name="d3dxshprtcompsupercluster-function"></a><span data-ttu-id="fdb3f-103">D3DXSHPRTCompSuperCluster-Funktion</span><span class="sxs-lookup"><span data-stu-id="fdb3f-103">D3DXSHPRTCompSuperCluster function</span></span>

<span data-ttu-id="fdb3f-104">Wird mit komprimierten Ergebnissen der vertexversion des PRT-Simulators (preberechneten Radiance Transfer) verwendet.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="fdb3f-105">Generiert "Super Cluster", bei denen es sich um Gruppen von Clustern handelt, die im selben zeichnen-Befehl gezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-105">Generates "superclusters," which are groups of clusters that can be drawn in the same draw call.</span></span> <span data-ttu-id="fdb3f-106">Ein gieriger Algorithmus, der Alphablendings minimiert, wird zum Gruppieren der Cluster verwendet.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-106">A greedy algorithm that minimizes overdraw is used to group the clusters.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb3f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdb3f-107">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a><span data-ttu-id="fdb3f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdb3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdb3f-109">*pclusterids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fdb3f-109">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb3f-110">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdb3f-110">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fdb3f-111">Zeiger auf eine num}-Cluster-IDs (aus einem komprimierten Puffer extrahiert)</span><span class="sxs-lookup"><span data-stu-id="fdb3f-111">Pointer to a NumVerts cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="fdb3f-112">*pscene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fdb3f-112">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb3f-113">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb3f-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="fdb3f-114">Ein Zeiger auf ein Mesh, das die an den Simulator übergebenen Verbund Szene darstellt.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-114">Pointer to a mesh that represents composite scene passed to the simulator.</span></span> <span data-ttu-id="fdb3f-115">Siehe [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="fdb3f-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="fdb3f-116">*Maxnumclusters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fdb3f-116">*MaxNumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb3f-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb3f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb3f-118">Maximale Anzahl von Clustern, die pro Super Cluster zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-118">Maximum number of clusters allocated per super cluster.</span></span>

</dd> <dt>

<span data-ttu-id="fdb3f-119">*Numclusters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fdb3f-119">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb3f-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb3f-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb3f-121">Anzahl der Cluster, die im Simulator berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-121">Number of clusters computed in the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="fdb3f-122">*psclusterids* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fdb3f-122">*pSClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb3f-123">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdb3f-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fdb3f-124">Zeiger auf ein Array der Länge *numclusters*.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-124">Pointer to an array of length *NumClusters*.</span></span> <span data-ttu-id="fdb3f-125">Enthält den Index des Super Clusters, dem der entsprechende Cluster zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-125">Contains the index of the super cluster to which the corresponding cluster was assigned.</span></span>

</dd> <dt>

<span data-ttu-id="fdb3f-126">*pnumscs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fdb3f-126">*pNumSCs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb3f-127">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdb3f-127">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fdb3f-128">Anzahl der zugewiesenen Super Cluster.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-128">Number of super clusters allocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdb3f-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fdb3f-129">Return value</span></span>

<span data-ttu-id="fdb3f-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fdb3f-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fdb3f-131">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fdb3f-132">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdb3f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdb3f-133">Requirements</span></span>



| <span data-ttu-id="fdb3f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fdb3f-134">Requirement</span></span> | <span data-ttu-id="fdb3f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="fdb3f-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb3f-136">Header</span><span class="sxs-lookup"><span data-stu-id="fdb3f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="fdb3f-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdb3f-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fdb3f-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fdb3f-138">Library</span></span><br/> | <dl> <span data-ttu-id="fdb3f-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdb3f-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fdb3f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdb3f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb3f-141">Voraus berechnete Strahlungs Übertragungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="fdb3f-141">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
