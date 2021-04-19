---
description: Erstellen Sie einen UV-Atlas für ein Mesh.
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: D3DXUVAtlasCreate-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 814f213b0195b0922270d0548d8b5fd4c48fb3e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373502"
---
# <a name="d3dxuvatlascreate-function"></a><span data-ttu-id="8ae70-103">D3DXUVAtlasCreate-Funktion</span><span class="sxs-lookup"><span data-stu-id="8ae70-103">D3DXUVAtlasCreate function</span></span>

<span data-ttu-id="8ae70-104">Erstellen Sie einen UV-Atlas für ein Mesh.</span><span class="sxs-lookup"><span data-stu-id="8ae70-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae70-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ae70-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="8ae70-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ae70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae70-107">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="8ae70-109">Zeiger auf ein Eingabe Mesh (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des Atlas enthält.</span><span class="sxs-lookup"><span data-stu-id="8ae70-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="8ae70-110">Das Mesh muss mindestens Positionsdaten und 2D-Texturkoordinaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="8ae70-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-111">*dwmaxchartnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ae70-113">Die maximale Anzahl von Diagrammen, in die das Mesh partitioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ae70-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="8ae70-114">Siehe Hinweise zu den Partitionierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="8ae70-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="8ae70-115">Verwenden Sie 0, um D3DX zu sagen, dass der Atlas auf der Grundlage von Stretch parametrisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ae70-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-116">*"f"* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ae70-118">Der Umfang der zulässigen Streckung.</span><span class="sxs-lookup"><span data-stu-id="8ae70-118">The amount of stretching allowed.</span></span> <span data-ttu-id="8ae70-119">0 bedeutet, dass keine Streckung zulässig ist, 1 bedeutet, dass eine beliebige Streckung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ae70-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-120">*dwwidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-120">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-121">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ae70-122">Textur Breite.</span><span class="sxs-lookup"><span data-stu-id="8ae70-122">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-123">*dwheight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-123">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-124">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ae70-125">Textur Höhe.</span><span class="sxs-lookup"><span data-stu-id="8ae70-125">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-126">nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-126">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-127">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ae70-128">Der Mindestabstand in texeln zwischen zwei Diagrammen im Atlas.</span><span class="sxs-lookup"><span data-stu-id="8ae70-128">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="8ae70-129">Der bundbundwert wird immer durch die Breite skaliert. Wenn also ein bundbundwert von 2,5 für eine 512 x 512-Textur verwendet wird, ist der minimale Abstand zwischen zwei Diagrammen 2,5/512,0 Texels.</span><span class="sxs-lookup"><span data-stu-id="8ae70-129">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-130">*dwtextureindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-130">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ae70-132">NULL basierter Texturkoordinaten Index, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ae70-132">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-133">*PDW-ency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-133">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-134">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ae70-134">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ae70-135">Ein Zeiger auf ein Array von-Daten.</span><span class="sxs-lookup"><span data-stu-id="8ae70-135">A pointer to an array of adjacency data.</span></span> <span data-ttu-id="8ae70-136">mit 3 DWords pro Gesicht, das angibt, welche Dreiecke nebeneinander zueinander liegen (siehe [**ID3DXBaseMesh:: generatefaceency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="8ae70-136">with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-137">*pdwfalseedges*</span><span class="sxs-lookup"><span data-stu-id="8ae70-137">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae70-138">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ae70-138">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ae70-139">Ein Array mit 3 DWords pro Gesicht.</span><span class="sxs-lookup"><span data-stu-id="8ae70-139">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="8ae70-140">Jedes Gesicht gibt an, ob ein Rand false ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="8ae70-140">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="8ae70-141">Ein nicht-false-Rand wird durch-1 angegeben. ein falscher Rand wird durch einen beliebigen anderen Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="8ae70-141">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="8ae70-142">Dies ermöglicht die Parametrisierung eines Netzes von Quads, bei dem die Ränder in der Mitte der einzelnen Quad nicht abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="8ae70-142">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-143">*pfimtarray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-143">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-144">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ae70-144">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ae70-145">Ein Zeiger auf ein Array von integrierten metriktensoren, das beschreibt, wie ein Dreieck gestreckt wird (siehe [integratedmetrictensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="8ae70-145">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-146">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-146">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-147">Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-147">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="8ae70-148">Ein Zeiger auf eine Rückruffunktion (siehe [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)), die zum Überwachen des Fortschritts nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="8ae70-148">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-149">" *schcallbackfrequency* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-149">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-150">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-150">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ae70-151">Geben Sie an, wie oft D3DX den Rückruf aufruft. ein angemessener Standardwert ist 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="8ae70-151">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-152">*pusercontent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-152">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-153">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-153">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ae70-154">Ein Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übermittelt wird. wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ae70-154">Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-155">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-155">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-156">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ae70-157">Geben Sie die Qualität der generierten Diagramme an.</span><span class="sxs-lookup"><span data-stu-id="8ae70-157">Specify the quality of the charts generated.</span></span> <span data-ttu-id="8ae70-158">Siehe [**D3DXUVATLAS**](./d3dxuvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="8ae70-158">See [**D3DXUVATLAS**](./d3dxuvatlas.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-159">*ppmeshout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-159">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-160">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ae70-160">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="8ae70-161">Zeiger auf das erstellte Mesh mit dem Atlas (siehe [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="8ae70-161">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-162">*ppfacepartitionierung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-162">*ppFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-163">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ae70-163">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8ae70-164">Ein Zeiger auf ein Array der letzten Gesichts Partitionierungs Daten.</span><span class="sxs-lookup"><span data-stu-id="8ae70-164">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="8ae70-165">Jedes Element enthält ein DWORD pro Gesicht (siehe [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="8ae70-165">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-166">*ppvertexrematexray* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-166">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-167">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ae70-167">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8ae70-168">Ein Zeiger auf ein Array von neu zugeordnete Vertices.</span><span class="sxs-lookup"><span data-stu-id="8ae70-168">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="8ae70-169">Jedes Array Element identifiziert den ursprünglichen Vertex, von dem jeder abschließende Scheitelpunkt stammt (wenn der Scheitelpunkt während der Neuzuordnung aufgeteilt wurde).</span><span class="sxs-lookup"><span data-stu-id="8ae70-169">Each array element identifies the original vertex that each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="8ae70-170">Jedes Array Element enthält ein DWORD pro Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="8ae70-170">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-171">*pfmaxstretchout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-171">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-172">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ae70-172">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ae70-173">Ein Zeiger auf den maximalen streckungs Wert, der vom Atlas-Algorithmus generiert wird.</span><span class="sxs-lookup"><span data-stu-id="8ae70-173">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="8ae70-174">Der Bereich liegt zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="8ae70-174">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="8ae70-175">*pdwnumcharout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8ae70-175">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae70-176">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ae70-176">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ae70-177">Ein Zeiger auf die Anzahl der Diagramme, die vom Atlas-Algorithmus erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="8ae70-177">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="8ae70-178">Wenn dwmaxchartnumber zu niedrig ist, gibt dieser Parameter die Mindestanzahl von Diagrammen zurück, die zum Erstellen eines Atlas erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8ae70-178">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae70-179">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ae70-179">Return value</span></span>

<span data-ttu-id="8ae70-180">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ae70-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ae70-181">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK; andernfalls ist der Wert D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="8ae70-181">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ae70-182">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ae70-182">Remarks</span></span>

<span data-ttu-id="8ae70-183">D3DXUVAtlasCreate kann Mesh-Geometrie auf zwei Arten partitionieren:</span><span class="sxs-lookup"><span data-stu-id="8ae70-183">D3DXUVAtlasCreate can partition mesh geometry two ways:</span></span>

-   <span data-ttu-id="8ae70-184">Basierend auf der Anzahl der Diagramme</span><span class="sxs-lookup"><span data-stu-id="8ae70-184">Based on the number of charts</span></span>
-   <span data-ttu-id="8ae70-185">Basierend auf der maximal zulässigen Streckung.</span><span class="sxs-lookup"><span data-stu-id="8ae70-185">Based on the maximum allowed stretch.</span></span> <span data-ttu-id="8ae70-186">Wenn die maximal zulässige Streckung 0 beträgt, befindet sich jedes Dreieck wahrscheinlich in einem eigenen Diagramm.</span><span class="sxs-lookup"><span data-stu-id="8ae70-186">If the maximum allowed stretch is 0, each triangle will likely be in its own chart.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae70-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ae70-187">Requirements</span></span>



| <span data-ttu-id="8ae70-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ae70-188">Requirement</span></span> | <span data-ttu-id="8ae70-189">Wert</span><span class="sxs-lookup"><span data-stu-id="8ae70-189">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae70-190">Header</span><span class="sxs-lookup"><span data-stu-id="8ae70-190">Header</span></span><br/>  | <dl> <span data-ttu-id="8ae70-191"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ae70-191"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8ae70-192">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ae70-192">Library</span></span><br/> | <dl> <span data-ttu-id="8ae70-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ae70-193"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ae70-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ae70-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae70-195">Uvatlas-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8ae70-195">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="8ae70-196">[Command-Line Tool für UV-Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="8ae70-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
