---
description: 'D3DXUVAtlasPartition-Funktion: Erstellen sie einen UV-Atlas für ein Gitternetz.'
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: D3DXUVAtlasPartition-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 63df6bbcc1b811b9617796bc6e7e51af2dfdca56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117798"
---
# <a name="d3dxuvatlaspartition-function"></a><span data-ttu-id="c65bc-103">D3DXUVAtlasPartition-Funktion</span><span class="sxs-lookup"><span data-stu-id="c65bc-103">D3DXUVAtlasPartition function</span></span>

<span data-ttu-id="c65bc-104">Erstellen Sie einen UV-Atlas für ein Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="c65bc-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="c65bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c65bc-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="c65bc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c65bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c65bc-107">*pMesh* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="c65bc-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="c65bc-109">Zeiger auf ein Eingabegittermodell (siehe [**ID3DXMesh),**](id3dxmesh.md)das die Objektgeometrie zum Berechnen des Atlas enthält.</span><span class="sxs-lookup"><span data-stu-id="c65bc-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) that contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="c65bc-110">Das Gitternetz muss mindestens Positionsdaten und 2D-Texturkoordinaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="c65bc-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-111">*dwMaxChartNumber* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-112">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c65bc-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c65bc-113">Die maximale Anzahl von Diagrammen, in die das Gitternetz partitioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c65bc-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="c65bc-114">Weitere Informationen finden Sie in den Hinweisen zu den Partitionierungsmodi.</span><span class="sxs-lookup"><span data-stu-id="c65bc-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="c65bc-115">Verwenden Sie 0, um D3DX mitzuteilen, dass der Atlas basierend auf Stretch parametrisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c65bc-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-116">*fMaxStretch* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c65bc-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c65bc-118">Die zulässige Menge an Stretching.</span><span class="sxs-lookup"><span data-stu-id="c65bc-118">The amount of stretching allowed.</span></span> <span data-ttu-id="c65bc-119">0 bedeutet, dass kein Stretching zulässig ist, 1 bedeutet, dass eine beliebige Menge an Stretching verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c65bc-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-120">*dwTextureIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-120">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-121">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c65bc-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c65bc-122">Nullbasierter Texturkoordinatenindex, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c65bc-122">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-123">*pdwAdjacency* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-123">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-124">Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c65bc-124">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c65bc-125">Ein Zeiger auf ein Array von Adjacency-Daten mit 3 DWORDs pro Gesicht, der angibt, welche Dreiecke nebeneinander liegen (siehe [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="c65bc-125">A pointer to an array of adjacency data with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-126">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="c65bc-126">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="c65bc-127">Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c65bc-127">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c65bc-128">Ein Array mit 3 DWORDS pro Gesicht.</span><span class="sxs-lookup"><span data-stu-id="c65bc-128">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="c65bc-129">Jedes Gesicht gibt an, ob ein Rand false ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="c65bc-129">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="c65bc-130">Ein nicht falscher Rand wird durch -1 angegeben, ein falscher Rand wird durch einen anderen Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="c65bc-130">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="c65bc-131">Dies ermöglicht die Parametrisierung eines Gitters von Quadern, bei dem die Ränder in der Mitte jedes Quader nicht ausgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="c65bc-131">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-132">*pfIMTArray* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-132">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-133">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c65bc-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c65bc-134">Ein Zeiger auf ein Array integrierter Metriktensoren, der beschreibt, wie ein Dreieck gestreckt wird (siehe [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="c65bc-134">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-135">*pCallback* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-135">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-136">Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="c65bc-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="c65bc-137">Ein Zeiger auf eine Rückruffunktion (siehe [LPD3DXUVATLASCB),](lpd3dxuvatlascb.md)die für die Überwachung des Fortschritts nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="c65bc-137">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-138">*fCallbackFrequency* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-138">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-139">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c65bc-139">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c65bc-140">Geben Sie an, wie oft D3DX den Rückruf aufruft. Ein angemessener Standardwert ist 0,0001f.</span><span class="sxs-lookup"><span data-stu-id="c65bc-140">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-141">*pUserContent* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-141">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-142">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c65bc-142">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c65bc-143">Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird; wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c65bc-143">Pointer to a user-defined value that is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-144">*dwOptions* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-144">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-145">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c65bc-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c65bc-146">Geben Sie die Qualität der Diagramme an, die durch Kombinieren eines oder mehrerer [**D3DXUVATLAS-Flags**](./d3dxuvatlas.md) generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c65bc-146">Specify the quality of the charts generated by combining one or more [**D3DXUVATLAS**](./d3dxuvatlas.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-147">*ppMeshOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-147">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-148">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="c65bc-148">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="c65bc-149">Zeiger auf das erstellte Gitternetz mit dem Atlas (siehe [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="c65bc-149">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-150">*pFacePartitioning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-150">*pFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-151">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="c65bc-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="c65bc-152">Ein Zeiger auf ein Array der endgültigen Gesichtspartitionierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="c65bc-152">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="c65bc-153">Jedes Element enthält ein DWORD pro Gesicht (siehe [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="c65bc-153">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-154">*ppVertexRemapArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-154">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-155">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c65bc-155">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c65bc-156">Ein Zeiger auf ein Array neu zugeordneter Scheitelpunkte.</span><span class="sxs-lookup"><span data-stu-id="c65bc-156">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="c65bc-157">Jedes Arrayelement identifiziert den ursprünglichen Scheitelpunkt, von dem jeder letzte Scheitelpunkt stammt (wenn der Scheitelpunkt während der Neuzuordnung geteilt wurde).</span><span class="sxs-lookup"><span data-stu-id="c65bc-157">Each array element identifies the original vertex each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="c65bc-158">Jedes Arrayelement enthält ein DWORD pro Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="c65bc-158">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-159">*ppPartitionResultAdjaency*</span><span class="sxs-lookup"><span data-stu-id="c65bc-159">*ppPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="c65bc-160">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c65bc-160">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c65bc-161">Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle.**](id3dxbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="c65bc-161">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="c65bc-162">Dieser Puffer enthält ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Ausgabegitternetz angeben.</span><span class="sxs-lookup"><span data-stu-id="c65bc-162">This buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="c65bc-163">Dieser Parameter darf nicht **NULL sein,** da der nachfolgende Aufruf von D3DXUVAtlasPack() dies erfordert.</span><span class="sxs-lookup"><span data-stu-id="c65bc-163">This parameter must not be **NULL**, because the subsequent call to D3DXUVAtlasPack() requires it.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-164">*pfMaxStretchOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-164">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-165">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c65bc-165">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c65bc-166">Ein Zeiger auf den maximalen Streckungswert, der vom Atlas-Algorithmus generiert wird.</span><span class="sxs-lookup"><span data-stu-id="c65bc-166">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="c65bc-167">Der Bereich liegt zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="c65bc-167">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="c65bc-168">*pdwNumChartsOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c65bc-168">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c65bc-169">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c65bc-169">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c65bc-170">Ein Zeiger auf die Anzahl von Diagrammen, die vom Atlas-Algorithmus erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c65bc-170">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="c65bc-171">Wenn dwMaxChartNumber zu niedrig ist, gibt dieser Parameter die Mindestanzahl von Diagrammen zurück, die zum Erstellen eines Atlas erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c65bc-171">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c65bc-172">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c65bc-172">Return value</span></span>

<span data-ttu-id="c65bc-173">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c65bc-173">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c65bc-174">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D OK, andernfalls ist der Wert \_ D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c65bc-174">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c65bc-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c65bc-175">Remarks</span></span>

<span data-ttu-id="c65bc-176">D3DXUVAtlasPartition ähnelt [**D3DXUVAtlasCreate,**](d3dxuvatlascreate.md)mit der Ausnahme, dass D3DXUVAtlasPartition den letzten Füllschritt nicht übernimmt.</span><span class="sxs-lookup"><span data-stu-id="c65bc-176">D3DXUVAtlasPartition is similar to [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), except that D3DXUVAtlasPartition does not performing the final packing step.</span></span>

## <a name="requirements"></a><span data-ttu-id="c65bc-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c65bc-177">Requirements</span></span>



| <span data-ttu-id="c65bc-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c65bc-178">Requirement</span></span> | <span data-ttu-id="c65bc-179">Wert</span><span class="sxs-lookup"><span data-stu-id="c65bc-179">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c65bc-180">Header</span><span class="sxs-lookup"><span data-stu-id="c65bc-180">Header</span></span><br/>  | <dl> <span data-ttu-id="c65bc-181"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="c65bc-181"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c65bc-182">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c65bc-182">Library</span></span><br/> | <dl> <span data-ttu-id="c65bc-183"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c65bc-183"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c65bc-184">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c65bc-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c65bc-185">UVAtlas-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c65bc-185">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="c65bc-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="c65bc-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
