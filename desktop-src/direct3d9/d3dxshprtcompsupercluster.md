---
description: 'D3DXSHPRTCompSuperCluster-Funktion: Wird mit komprimierten Ergebnissen der Scheitelpunktversion des PRT-Simulators (Precomputed Radiance Transfer) verwendet.'
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: D3DXSHPRTCompSuperCluster-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: 0c22c8a3a14fd8af3e9104889b421068c7ff1457
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117858"
---
# <a name="d3dxshprtcompsupercluster-function"></a><span data-ttu-id="f04c3-103">D3DXSHPRTCompSuperCluster-Funktion</span><span class="sxs-lookup"><span data-stu-id="f04c3-103">D3DXSHPRTCompSuperCluster function</span></span>

<span data-ttu-id="f04c3-104">Wird mit komprimierten Ergebnissen der Scheitelpunktversion des PRT-Simulators (Precomputed Radiance Transfer) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f04c3-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="f04c3-105">Generiert "Supercluster", bei denen es sich um Gruppen von Clustern handelt, die im gleichen Zeichnen-Aufruf gezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="f04c3-105">Generates "superclusters," which are groups of clusters that can be drawn in the same draw call.</span></span> <span data-ttu-id="f04c3-106">Ein gieriger Algorithmus, der die Überzeichnung minimiert, wird verwendet, um die Cluster zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="f04c3-106">A greedy algorithm that minimizes overdraw is used to group the clusters.</span></span>

## <a name="syntax"></a><span data-ttu-id="f04c3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f04c3-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f04c3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f04c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f04c3-109">*pClusterIDs* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f04c3-109">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04c3-110">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f04c3-110">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f04c3-111">Zeiger auf numVerts-Cluster-IDs (extrahiert aus einem komprimierten Puffer)</span><span class="sxs-lookup"><span data-stu-id="f04c3-111">Pointer to a NumVerts cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="f04c3-112">*pScene* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f04c3-112">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04c3-113">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f04c3-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="f04c3-114">Zeiger auf ein Gitternetz, das eine zusammengesetzte Szene darstellt, die an den Simulator übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f04c3-114">Pointer to a mesh that represents composite scene passed to the simulator.</span></span> <span data-ttu-id="f04c3-115">Siehe [**ID3DXMesh.**](id3dxmesh.md)</span><span class="sxs-lookup"><span data-stu-id="f04c3-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="f04c3-116">*MaxNumClusters* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f04c3-116">*MaxNumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04c3-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f04c3-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f04c3-118">Maximale Anzahl von Clustern, die pro Supercluster zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f04c3-118">Maximum number of clusters allocated per super cluster.</span></span>

</dd> <dt>

<span data-ttu-id="f04c3-119">*NumClusters* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f04c3-119">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04c3-120">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f04c3-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f04c3-121">Anzahl der im Simulator berechneten Cluster.</span><span class="sxs-lookup"><span data-stu-id="f04c3-121">Number of clusters computed in the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="f04c3-122">*pSClusterIDs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f04c3-122">*pSClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f04c3-123">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f04c3-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f04c3-124">Zeiger auf ein Array der Länge *NumClusters*.</span><span class="sxs-lookup"><span data-stu-id="f04c3-124">Pointer to an array of length *NumClusters*.</span></span> <span data-ttu-id="f04c3-125">Enthält den Index des Superclusters, dem der entsprechende Cluster zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="f04c3-125">Contains the index of the super cluster to which the corresponding cluster was assigned.</span></span>

</dd> <dt>

<span data-ttu-id="f04c3-126">*pNumSCs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f04c3-126">*pNumSCs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f04c3-127">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f04c3-127">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f04c3-128">Anzahl der zugeordneten Supercluster.</span><span class="sxs-lookup"><span data-stu-id="f04c3-128">Number of super clusters allocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f04c3-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f04c3-129">Return value</span></span>

<span data-ttu-id="f04c3-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f04c3-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f04c3-131">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f04c3-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f04c3-132">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f04c3-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f04c3-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f04c3-133">Requirements</span></span>



| <span data-ttu-id="f04c3-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f04c3-134">Requirement</span></span> | <span data-ttu-id="f04c3-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f04c3-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f04c3-136">Header</span><span class="sxs-lookup"><span data-stu-id="f04c3-136">Header</span></span><br/>  | <dl> <span data-ttu-id="f04c3-137"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="f04c3-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f04c3-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f04c3-138">Library</span></span><br/> | <dl> <span data-ttu-id="f04c3-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f04c3-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f04c3-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f04c3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f04c3-141">Vorausberechnungsfunktionen für die Übertragung von Radiance</span><span class="sxs-lookup"><span data-stu-id="f04c3-141">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
