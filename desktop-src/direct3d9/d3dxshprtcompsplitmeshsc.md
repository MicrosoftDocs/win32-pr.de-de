---
description: Wird mit komprimierten Ergebnissen der vertexversion des PRT-Simulators (preberechneten Radiance Transfer) verwendet.
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: D3DXSHPRTCompSplitMeshSC-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 18742d12b6e1ae106dcf832baccccb2416465880
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394098"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a><span data-ttu-id="53efb-103">D3DXSHPRTCompSplitMeshSC-Funktion</span><span class="sxs-lookup"><span data-stu-id="53efb-103">D3DXSHPRTCompSplitMeshSC function</span></span>

<span data-ttu-id="53efb-104">Wird mit komprimierten Ergebnissen der vertexversion des PRT-Simulators (preberechneten Radiance Transfer) verwendet.</span><span class="sxs-lookup"><span data-stu-id="53efb-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="53efb-105">Nachdem [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) aufgerufen wurde, kann diese Funktion verwendet werden, um das Mesh in eine Gruppe von Gesichtern/Scheitel Punkten pro Super Cluster aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="53efb-105">After [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) has been called, this function can be used to split the mesh into a group of faces/vertices per super cluster.</span></span> <span data-ttu-id="53efb-106">Jeder Super Cluster enthält alle Gesichter, die alle in einem ihrer Cluster klassifizierten Scheitel Punkte enthalten.</span><span class="sxs-lookup"><span data-stu-id="53efb-106">Each super cluster contains all of the faces that contain any vertex classified in one of its clusters.</span></span> <span data-ttu-id="53efb-107">Alle Scheitel Punkte, die mit dieser Gruppe von Gesichtern verbunden sind, sind auch im zurückgegebenen Array ppvertstatus enthalten, das angibt, ob der Scheitelpunkt zu dem Super Cluster gehört.</span><span class="sxs-lookup"><span data-stu-id="53efb-107">All of the vertices connected to this set of faces are also included with the returned array ppVertStatus indicating whether or not the vertex belongs to the super cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="53efb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="53efb-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="53efb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="53efb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53efb-110">*pclusterids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53efb-110">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-111">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53efb-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53efb-112">*Numvertices* Cluster-IDs (aus einem komprimierten Puffer extrahiert)</span><span class="sxs-lookup"><span data-stu-id="53efb-112">*NumVertices* cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="53efb-113">*Numvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53efb-113">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53efb-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53efb-115">Anzahl der Scheitel Punkte im ursprünglichen Mesh.</span><span class="sxs-lookup"><span data-stu-id="53efb-115">Number of vertices in original mesh.</span></span>

</dd> <dt>

<span data-ttu-id="53efb-116">*Numcs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53efb-116">*NumCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53efb-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53efb-118">Anzahl von Clustern (Eingabeparameter für die Komprimierung.)</span><span class="sxs-lookup"><span data-stu-id="53efb-118">Number of clusters (input parameter to compression.)</span></span>

</dd> <dt>

<span data-ttu-id="53efb-119">*psclusterids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53efb-119">*pSClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-120">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53efb-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53efb-121">Array von Größen- *numcs* , das Super Cluster-IDs enthalten wird.</span><span class="sxs-lookup"><span data-stu-id="53efb-121">Array of size *NumCs* that will contain super cluster IDs.</span></span>

</dd> <dt>

<span data-ttu-id="53efb-122">*Numscs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53efb-122">*NumSCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53efb-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53efb-124">Anzahl der in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md)zugeordneten Super Cluster.</span><span class="sxs-lookup"><span data-stu-id="53efb-124">Number of super clusters allocated in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span></span>

</dd> <dt>

<span data-ttu-id="53efb-125">*pinputib* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53efb-125">*pInputIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-126">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53efb-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53efb-127">Unformatierten Index Puffer für Mesh.</span><span class="sxs-lookup"><span data-stu-id="53efb-127">Raw index buffer for mesh.</span></span> <span data-ttu-id="53efb-128">Das Format ist abhängig von *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="53efb-128">The format depends on *InputIBIs32Bit*.</span></span>

</dd> <dt>

<span data-ttu-id="53efb-129">*InputIBIs32Bit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53efb-129">*InputIBIs32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-130">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53efb-130">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53efb-131">**True** gibt an, dass der Index Puffer auf 32 Bit festgelegt ist. Andernfalls 16 Bit.</span><span class="sxs-lookup"><span data-stu-id="53efb-131">If **TRUE**, the index buffer is set to 32 bit; otherwise, 16 bit.</span></span>

</dd> <dt>

<span data-ttu-id="53efb-132">*Numerische Werte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53efb-132">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-133">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53efb-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53efb-134">Anzahl der Gesichter im ursprünglichen Mesh (*pinputib* ist dreimal so lang).</span><span class="sxs-lookup"><span data-stu-id="53efb-134">Number of faces in the original mesh (*pInputIB* is 3 times this length.)</span></span>

</dd> <dt>

<span data-ttu-id="53efb-135">*ppibdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53efb-135">*ppIBData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-136">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="53efb-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="53efb-137">Unformatierten Index Puffer, der die sich ergebenden geteilten Gesichter enthält.</span><span class="sxs-lookup"><span data-stu-id="53efb-137">Raw index buffer that will contain the resulting split faces.</span></span> <span data-ttu-id="53efb-138">Das von *InputIBIs32Bit* festgelegte Format.</span><span class="sxs-lookup"><span data-stu-id="53efb-138">Format determined by *InputIBIs32Bit*.</span></span> <span data-ttu-id="53efb-139">Zugeordnet von Funktion.</span><span class="sxs-lookup"><span data-stu-id="53efb-139">Allocated by function.</span></span>

</dd> <dt>

<span data-ttu-id="53efb-140">*pibdatalength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53efb-140">*pIBDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-141">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53efb-141">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53efb-142">Länge der in der Funktion zugewiesenen *ppibdata*.</span><span class="sxs-lookup"><span data-stu-id="53efb-142">Length of *ppIBData*, assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="53efb-143">*OutputIBIs32Bit* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53efb-143">*OutputIBIs32Bit* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-144">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53efb-144">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53efb-145">Wenn **true**, wird ein ganzzahliges Array ohne Vorzeichen zugeordnet. Andernfalls weist ein unsigniertes kurzes Array zu.</span><span class="sxs-lookup"><span data-stu-id="53efb-145">If **TRUE**, allocates an unsigned integer array; otherwise, allocates an unsigned short array.</span></span>

</dd> <dt>

<span data-ttu-id="53efb-146">*ppfakeremap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53efb-146">*ppFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-147">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="53efb-147">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="53efb-148">Zuordnung von jedem Gesicht in *ppibdata* zu ursprünglichen Gesichtern.</span><span class="sxs-lookup"><span data-stu-id="53efb-148">Mapping of each face in *ppIBData* to original faces.</span></span> <span data-ttu-id="53efb-149">Länge ist \* *pibdatalength*/3.</span><span class="sxs-lookup"><span data-stu-id="53efb-149">Length is \**pIBDataLength*/3.</span></span>

</dd> <dt>

<span data-ttu-id="53efb-150">*ppvertdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53efb-150">*ppVertData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-151">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="53efb-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="53efb-152">Neue Vertex-Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="53efb-152">New vertex data structure.</span></span> <span data-ttu-id="53efb-153">Größe von *pvertdatalength*.</span><span class="sxs-lookup"><span data-stu-id="53efb-153">Size of *pVertDataLength*.</span></span>

</dd> <dt>

<span data-ttu-id="53efb-154">*pvertdatalength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53efb-154">*pVertDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-155">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53efb-155">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53efb-156">Anzahl der neuen Scheitel Punkte in geteiltem Mesh.</span><span class="sxs-lookup"><span data-stu-id="53efb-156">Number of new vertices in split mesh.</span></span> <span data-ttu-id="53efb-157">Zugewiesen in-Funktion.</span><span class="sxs-lookup"><span data-stu-id="53efb-157">Assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="53efb-158">*pscclusterlist* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53efb-158">*pSCClusterList* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-159">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53efb-159">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53efb-160">Ein Array von Längen- *numcs* , in das *pscdata* indiziert (*pclusterids* - \* Felder) für jeden Supercluster, enthält nach Supercluster sortierte Cluster.</span><span class="sxs-lookup"><span data-stu-id="53efb-160">Array of length *NumCs* which *pSCData* indexes into (*pClusterIDs*\* fields) for each supercluster, contains clusters sorted by supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="53efb-161">*pscdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53efb-161">*pSCData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53efb-162">Typ: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span><span class="sxs-lookup"><span data-stu-id="53efb-162">Type: **[**D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span></span>

<span data-ttu-id="53efb-163">Struktur pro Super Cluster.</span><span class="sxs-lookup"><span data-stu-id="53efb-163">Structure per super cluster.</span></span> <span data-ttu-id="53efb-164">Enthält Indizes in " *ppibdata*", " *pscclusterlist*" und " *ppvertdata*".</span><span class="sxs-lookup"><span data-stu-id="53efb-164">Contains indices into *ppIBData*, *pSCClusterList*, and *ppVertData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53efb-165">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53efb-165">Return value</span></span>

<span data-ttu-id="53efb-166">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53efb-166">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53efb-167">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="53efb-167">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="53efb-168">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="53efb-168">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="53efb-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53efb-169">Requirements</span></span>



| <span data-ttu-id="53efb-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53efb-170">Requirement</span></span> | <span data-ttu-id="53efb-171">Wert</span><span class="sxs-lookup"><span data-stu-id="53efb-171">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53efb-172">Header</span><span class="sxs-lookup"><span data-stu-id="53efb-172">Header</span></span><br/>  | <dl> <span data-ttu-id="53efb-173"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="53efb-173"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="53efb-174">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="53efb-174">Library</span></span><br/> | <dl> <span data-ttu-id="53efb-175"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53efb-175"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="53efb-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53efb-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53efb-177">Voraus berechnete Strahlungs Übertragungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="53efb-177">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
