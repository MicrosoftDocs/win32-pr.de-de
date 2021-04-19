---
description: Erstellen Sie einen UV-Atlas für ein Mesh.
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: D3DXUVAtlasPartition-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 707a503832a4fd66ab2e8d9346587d11544a885c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361861"
---
# <a name="d3dxuvatlaspartition-function"></a><span data-ttu-id="0b7fd-103">D3DXUVAtlasPartition-Funktion</span><span class="sxs-lookup"><span data-stu-id="0b7fd-103">D3DXUVAtlasPartition function</span></span>

<span data-ttu-id="0b7fd-104">Erstellen Sie einen UV-Atlas für ein Mesh.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b7fd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b7fd-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0b7fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b7fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b7fd-107">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="0b7fd-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="0b7fd-109">Zeiger auf ein Eingabe Mesh (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des Atlas enthält.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) that contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="0b7fd-110">Das Mesh muss mindestens Positionsdaten und 2D-Texturkoordinaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-111">*dwmaxchartnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b7fd-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b7fd-113">Die maximale Anzahl von Diagrammen, in die das Mesh partitioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="0b7fd-114">Siehe Hinweise zu den Partitionierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="0b7fd-115">Verwenden Sie 0, um D3DX zu sagen, dass der Atlas auf der Grundlage von Stretch parametrisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-116">*"f"* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b7fd-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b7fd-118">Der Umfang der zulässigen Streckung.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-118">The amount of stretching allowed.</span></span> <span data-ttu-id="0b7fd-119">0 bedeutet, dass keine Streckung zulässig ist, 1 bedeutet, dass eine beliebige Streckung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-120">*dwtextureindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-120">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-121">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b7fd-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b7fd-122">NULL basierter Texturkoordinaten Index, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-122">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-123">*PDW-ency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-123">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-124">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0b7fd-124">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b7fd-125">Ein Zeiger auf ein Array von Ereignisdaten mit 3 DWords pro Gesicht, das angibt, welche Dreiecke nebeneinander zueinander stehen (siehe [**ID3DXBaseMesh:: generatefaceency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="0b7fd-125">A pointer to an array of adjacency data with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-126">*pdwfalseedges*</span><span class="sxs-lookup"><span data-stu-id="0b7fd-126">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="0b7fd-127">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0b7fd-127">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b7fd-128">Ein Array mit 3 DWords pro Gesicht.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-128">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="0b7fd-129">Jedes Gesicht gibt an, ob ein Rand false ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-129">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="0b7fd-130">Ein nicht-false-Rand wird durch-1 angegeben. ein falscher Rand wird durch einen beliebigen anderen Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-130">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="0b7fd-131">Dies ermöglicht die Parametrisierung eines Netzes von Quads, bei dem die Ränder in der Mitte der einzelnen Quad nicht abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-131">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-132">*pfimtarray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-132">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-133">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7fd-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b7fd-134">Ein Zeiger auf ein Array von integrierten metriktensoren, das beschreibt, wie ein Dreieck gestreckt wird (siehe [integratedmetrictensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="0b7fd-134">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-135">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-135">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-136">Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="0b7fd-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="0b7fd-137">Ein Zeiger auf eine Rückruffunktion (siehe [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)), die zum Überwachen des Fortschritts nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-137">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-138">" *schcallbackfrequency* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-138">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-139">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b7fd-139">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b7fd-140">Geben Sie an, wie oft D3DX den Rückruf aufruft. ein angemessener Standardwert ist 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-140">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-141">*pusercontent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-141">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-142">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b7fd-142">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b7fd-143">Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übermittelt wird. wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-143">Pointer to a user-defined value that is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-144">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-144">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-145">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b7fd-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b7fd-146">Geben Sie die Qualität der Diagramme an, die durch Kombinieren von mindestens einem [**D3DXUVATLAS**](./d3dxuvatlas.md) -Flags generiert werden.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-146">Specify the quality of the charts generated by combining one or more [**D3DXUVATLAS**](./d3dxuvatlas.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-147">*ppmeshout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-147">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-148">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7fd-148">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="0b7fd-149">Zeiger auf das erstellte Mesh mit dem Atlas (siehe [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="0b7fd-149">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-150">*pfacepartitionierung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-150">*pFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-151">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="0b7fd-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="0b7fd-152">Ein Zeiger auf ein Array der letzten Gesichts Partitionierungs Daten.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-152">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="0b7fd-153">Jedes Element enthält ein DWORD pro Gesicht (siehe [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="0b7fd-153">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-154">*ppvertexrematexray* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-154">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-155">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7fd-155">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0b7fd-156">Ein Zeiger auf ein Array von neu zugeordnete Vertices.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-156">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="0b7fd-157">Jedes Array Element identifiziert den ursprünglichen Vertex, von dem jeder abschließende Scheitelpunkt stammt (wenn der Scheitelpunkt während der Neuzuordnung aufgeteilt wurde).</span><span class="sxs-lookup"><span data-stu-id="0b7fd-157">Each array element identifies the original vertex each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="0b7fd-158">Jedes Array Element enthält ein DWORD pro Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-158">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-159">*pppartitionresultadjacency*</span><span class="sxs-lookup"><span data-stu-id="0b7fd-159">*ppPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="0b7fd-160">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7fd-160">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0b7fd-161">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-161">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="0b7fd-162">Dieser Puffer enthält ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Ausgabe Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-162">This buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="0b7fd-163">Dieser Parameter darf nicht **null** sein, da er für den nachfolgenden Aufrufen von D3DXUVAtlasPack () erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-163">This parameter must not be **NULL**, because the subsequent call to D3DXUVAtlasPack() requires it.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-164">*pfmaxstretchout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-164">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-165">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7fd-165">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b7fd-166">Ein Zeiger auf den maximalen streckungs Wert, der vom Atlas-Algorithmus generiert wird.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-166">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="0b7fd-167">Der Bereich liegt zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-167">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="0b7fd-168">*pdwnumcharout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0b7fd-168">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fd-169">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7fd-169">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b7fd-170">Ein Zeiger auf die Anzahl der Diagramme, die vom Atlas-Algorithmus erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-170">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="0b7fd-171">Wenn dwmaxchartnumber zu niedrig ist, gibt dieser Parameter die Mindestanzahl von Diagrammen zurück, die zum Erstellen eines Atlas erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-171">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b7fd-172">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b7fd-172">Return value</span></span>

<span data-ttu-id="0b7fd-173">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b7fd-173">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b7fd-174">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK; andernfalls ist der Wert D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-174">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b7fd-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b7fd-175">Remarks</span></span>

<span data-ttu-id="0b7fd-176">D3DXUVAtlasPartition ähnelt [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), mit der Ausnahme, dass D3DXUVAtlasPartition den abschließenden Verpackungs Schritt nicht ausführt.</span><span class="sxs-lookup"><span data-stu-id="0b7fd-176">D3DXUVAtlasPartition is similar to [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), except that D3DXUVAtlasPartition does not performing the final packing step.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b7fd-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b7fd-177">Requirements</span></span>



| <span data-ttu-id="0b7fd-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b7fd-178">Requirement</span></span> | <span data-ttu-id="0b7fd-179">Wert</span><span class="sxs-lookup"><span data-stu-id="0b7fd-179">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b7fd-180">Header</span><span class="sxs-lookup"><span data-stu-id="0b7fd-180">Header</span></span><br/>  | <dl> <span data-ttu-id="0b7fd-181"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b7fd-181"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0b7fd-182">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b7fd-182">Library</span></span><br/> | <dl> <span data-ttu-id="0b7fd-183"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b7fd-183"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0b7fd-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b7fd-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b7fd-185">Uvatlas-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0b7fd-185">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="0b7fd-186">[Command-Line Tool für UV-Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="0b7fd-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
