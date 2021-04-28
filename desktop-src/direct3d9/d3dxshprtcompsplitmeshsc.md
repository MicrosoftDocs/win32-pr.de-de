---
description: 'D3DXSHPRTCompSplitMeshSC-Funktion: Wird mit komprimierten Ergebnissen der Scheitelpunktversion des PRT-Simulators (Precomputed Radiance Transfer) verwendet.'
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: D3DXSHPRTCompSplitMeshSC-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e51a86ec9b12992d49364d3a7c614751dacafac3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093898"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a><span data-ttu-id="616da-103">D3DXSHPRTCompSplitMeshSC-Funktion</span><span class="sxs-lookup"><span data-stu-id="616da-103">D3DXSHPRTCompSplitMeshSC function</span></span>

<span data-ttu-id="616da-104">Wird mit komprimierten Ergebnissen der Scheitelpunktversion des PRT-Simulators (Precomputed Radiance Transfer) verwendet.</span><span class="sxs-lookup"><span data-stu-id="616da-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="616da-105">Nachdem [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) aufgerufen wurde, kann diese Funktion verwendet werden, um das Gitternetz in eine Gruppe von Gesichtern/Scheitelpunkten pro Supercluster aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="616da-105">After [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) has been called, this function can be used to split the mesh into a group of faces/vertices per super cluster.</span></span> <span data-ttu-id="616da-106">Jeder Supercluster enthält alle Gesichter, die einen beliebigen Scheitelpunkt enthalten, der in einem seiner Cluster klassifiziert ist.</span><span class="sxs-lookup"><span data-stu-id="616da-106">Each super cluster contains all of the faces that contain any vertex classified in one of its clusters.</span></span> <span data-ttu-id="616da-107">Alle Scheitelpunkte, die mit dieser Gruppe von Gesichtern verbunden sind, sind auch im zurückgegebenen Array ppVertStatus enthalten, das angibt, ob der Scheitelpunkt zum Supercluster gehört.</span><span class="sxs-lookup"><span data-stu-id="616da-107">All of the vertices connected to this set of faces are also included with the returned array ppVertStatus indicating whether or not the vertex belongs to the super cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="616da-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="616da-108">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a><span data-ttu-id="616da-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="616da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="616da-110">*pClusterIDs* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="616da-110">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="616da-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="616da-112">*NumVertices-Cluster-IDs* (aus einem komprimierten Puffer extrahiert)</span><span class="sxs-lookup"><span data-stu-id="616da-112">*NumVertices* cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="616da-113">*NumVertices* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="616da-113">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="616da-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="616da-115">Anzahl der Scheitelpunkte im ursprünglichen Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="616da-115">Number of vertices in original mesh.</span></span>

</dd> <dt>

<span data-ttu-id="616da-116">*NumCs* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="616da-116">*NumCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="616da-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="616da-118">Anzahl von Clustern (Eingabeparameter für Komprimierung))</span><span class="sxs-lookup"><span data-stu-id="616da-118">Number of clusters (input parameter to compression.)</span></span>

</dd> <dt>

<span data-ttu-id="616da-119">*pSClusterIDs* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="616da-119">*pSClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-120">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="616da-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="616da-121">Array von *NumCs* der Größe, die Supercluster-IDs enthalten.</span><span class="sxs-lookup"><span data-stu-id="616da-121">Array of size *NumCs* that will contain super cluster IDs.</span></span>

</dd> <dt>

<span data-ttu-id="616da-122">*NumSCs* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="616da-122">*NumSCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-123">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="616da-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="616da-124">Anzahl von Superclustern, die in [**D3DXSHPRTCompSuperCluster zugeordnet sind.**](d3dxshprtcompsupercluster.md)</span><span class="sxs-lookup"><span data-stu-id="616da-124">Number of super clusters allocated in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span></span>

</dd> <dt>

<span data-ttu-id="616da-125">*pInputIB* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="616da-125">*pInputIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-126">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="616da-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="616da-127">Unformatierter Indexpuffer für Mesh.</span><span class="sxs-lookup"><span data-stu-id="616da-127">Raw index buffer for mesh.</span></span> <span data-ttu-id="616da-128">Das Format hängt von *InputIBIs32Bit ab.*</span><span class="sxs-lookup"><span data-stu-id="616da-128">The format depends on *InputIBIs32Bit*.</span></span>

</dd> <dt>

<span data-ttu-id="616da-129">*InputIBIs32Bit* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="616da-129">*InputIBIs32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-130">Typ: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="616da-130">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="616da-131">True **gibt an,** dass der Indexpuffer auf 32 Bit festgelegt ist. andernfalls 16 Bit.</span><span class="sxs-lookup"><span data-stu-id="616da-131">If **TRUE**, the index buffer is set to 32 bit; otherwise, 16 bit.</span></span>

</dd> <dt>

<span data-ttu-id="616da-132">*NumFaces* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="616da-132">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-133">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="616da-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="616da-134">Anzahl der Gesichter im ursprünglichen Gitter (*pInputIB* ist das 3-fache dieser Länge.)</span><span class="sxs-lookup"><span data-stu-id="616da-134">Number of faces in the original mesh (*pInputIB* is 3 times this length.)</span></span>

</dd> <dt>

<span data-ttu-id="616da-135">*ppIBData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="616da-135">*ppIBData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-136">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="616da-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="616da-137">Unformatierter Indexpuffer, der die resultierenden geteilten Gesichter enthält.</span><span class="sxs-lookup"><span data-stu-id="616da-137">Raw index buffer that will contain the resulting split faces.</span></span> <span data-ttu-id="616da-138">Format, das von *InputIBIs32Bit bestimmt wird.*</span><span class="sxs-lookup"><span data-stu-id="616da-138">Format determined by *InputIBIs32Bit*.</span></span> <span data-ttu-id="616da-139">Zugeordnet nach Funktion.</span><span class="sxs-lookup"><span data-stu-id="616da-139">Allocated by function.</span></span>

</dd> <dt>

<span data-ttu-id="616da-140">*pIBDataLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="616da-140">*pIBDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-141">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="616da-141">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="616da-142">Länge von *ppIBData,* zugewiesen in funktion.</span><span class="sxs-lookup"><span data-stu-id="616da-142">Length of *ppIBData*, assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="616da-143">*OutputIBIs32Bit* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="616da-143">*OutputIBIs32Bit* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-144">Typ: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="616da-144">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="616da-145">True gibt an, dass ein Ganzzahlarray ohne Vorzeichen zuordnet. andernfalls ordnet ein short-Array ohne Vorzeichen zu.</span><span class="sxs-lookup"><span data-stu-id="616da-145">If **TRUE**, allocates an unsigned integer array; otherwise, allocates an unsigned short array.</span></span>

</dd> <dt>

<span data-ttu-id="616da-146">*ppFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="616da-146">*ppFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-147">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="616da-147">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="616da-148">Zuordnung jedes Gesichts in *ppIBData* zu ursprünglichen Gesichtern.</span><span class="sxs-lookup"><span data-stu-id="616da-148">Mapping of each face in *ppIBData* to original faces.</span></span> <span data-ttu-id="616da-149">Die Länge ist \* *pIBDataLength*/3.</span><span class="sxs-lookup"><span data-stu-id="616da-149">Length is \**pIBDataLength*/3.</span></span>

</dd> <dt>

<span data-ttu-id="616da-150">*ppVertData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="616da-150">*ppVertData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-151">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="616da-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="616da-152">Neue Scheitelpunktdatenstruktur.</span><span class="sxs-lookup"><span data-stu-id="616da-152">New vertex data structure.</span></span> <span data-ttu-id="616da-153">Größe von *pVertDataLength.*</span><span class="sxs-lookup"><span data-stu-id="616da-153">Size of *pVertDataLength*.</span></span>

</dd> <dt>

<span data-ttu-id="616da-154">*pVertDataLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="616da-154">*pVertDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-155">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="616da-155">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="616da-156">Anzahl der neuen Scheitelpunkte im geteilten Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="616da-156">Number of new vertices in split mesh.</span></span> <span data-ttu-id="616da-157">In Funktion zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="616da-157">Assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="616da-158">*pSCClusterList* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="616da-158">*pSCClusterList* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-159">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="616da-159">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="616da-160">Ein Array mit *NumCs* der Länge, in das *pSCData* für jeden Supercluster indiziert *(pClusterIDs-Felder),* \* enthält Cluster, die nach Supercluster sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="616da-160">Array of length *NumCs* which *pSCData* indexes into (*pClusterIDs*\* fields) for each supercluster, contains clusters sorted by supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="616da-161">*pSCData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="616da-161">*pSCData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="616da-162">Typ: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span><span class="sxs-lookup"><span data-stu-id="616da-162">Type: **[**D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span></span>

<span data-ttu-id="616da-163">Struktur pro Supercluster.</span><span class="sxs-lookup"><span data-stu-id="616da-163">Structure per super cluster.</span></span> <span data-ttu-id="616da-164">Enthält Indizes in *ppIBData,* *pSCClusterList* und *ppVertData.*</span><span class="sxs-lookup"><span data-stu-id="616da-164">Contains indices into *ppIBData*, *pSCClusterList*, and *ppVertData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="616da-165">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="616da-165">Return value</span></span>

<span data-ttu-id="616da-166">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="616da-166">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="616da-167">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="616da-167">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="616da-168">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="616da-168">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="616da-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="616da-169">Requirements</span></span>



| <span data-ttu-id="616da-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="616da-170">Requirement</span></span> | <span data-ttu-id="616da-171">Wert</span><span class="sxs-lookup"><span data-stu-id="616da-171">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="616da-172">Header</span><span class="sxs-lookup"><span data-stu-id="616da-172">Header</span></span><br/>  | <dl> <span data-ttu-id="616da-173"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="616da-173"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="616da-174">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="616da-174">Library</span></span><br/> | <dl> <span data-ttu-id="616da-175"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="616da-175"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="616da-176">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="616da-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="616da-177">Vorausberechnungsfunktionen für die Übertragung von Radiance</span><span class="sxs-lookup"><span data-stu-id="616da-177">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
