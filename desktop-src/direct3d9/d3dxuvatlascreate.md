---
description: 'D3DXUVAtlasCreate-Funktion: Erstellen sie einen UV-Atlas für ein Gitter.'
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: D3DXUVAtlasCreate-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: 5f382e7d59f3a5b5db8ba3cfd65ba6cc1a11e86d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117828"
---
# <a name="d3dxuvatlascreate-function"></a><span data-ttu-id="d342c-103">D3DXUVAtlasCreate-Funktion</span><span class="sxs-lookup"><span data-stu-id="d342c-103">D3DXUVAtlasCreate function</span></span>

<span data-ttu-id="d342c-104">Erstellen Sie einen UV-Atlas für ein Gitter.</span><span class="sxs-lookup"><span data-stu-id="d342c-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d342c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d342c-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d342c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d342c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d342c-107">*pMesh* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="d342c-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="d342c-109">Zeiger auf ein Eingabegittermodell (siehe [**ID3DXMesh),**](id3dxmesh.md)das die Objektgeometrie zum Berechnen des Atlas enthält.</span><span class="sxs-lookup"><span data-stu-id="d342c-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="d342c-110">Das Gitternetz muss mindestens Positionsdaten und 2D-Texturkoordinaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="d342c-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-111">*dwMaxChartNumber* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-112">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d342c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d342c-113">Die maximale Anzahl von Diagrammen, in die das Gitternetz partitioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d342c-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="d342c-114">Siehe Hinweise zu den Partitionierungsmodi.</span><span class="sxs-lookup"><span data-stu-id="d342c-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="d342c-115">Verwenden Sie 0, um D3DX zu informieren, dass der Atlas basierend auf stretch parametrisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d342c-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-116">*fMaxStretch* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d342c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d342c-118">Die zulässige Stretchingmenge.</span><span class="sxs-lookup"><span data-stu-id="d342c-118">The amount of stretching allowed.</span></span> <span data-ttu-id="d342c-119">0 bedeutet, dass kein Stretching zulässig ist, 1 bedeutet, dass eine beliebige Menge an Stretching verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d342c-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-120">*dwWidth* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-120">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-121">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d342c-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d342c-122">Texturbreite.</span><span class="sxs-lookup"><span data-stu-id="d342c-122">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-123">*dwHeight* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-123">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-124">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d342c-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d342c-125">Texturhöhe.</span><span class="sxs-lookup"><span data-stu-id="d342c-125">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-126">*fGutter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-126">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-127">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d342c-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d342c-128">Der mindeste Abstand zwischen zwei Diagrammen im Atlas in Texel.</span><span class="sxs-lookup"><span data-stu-id="d342c-128">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="d342c-129">Der Bundsteg wird immer um die Breite skaliert. Wenn also ein Bundsteg von 2,5 für eine Textur mit 512 x 512 verwendet wird, beträgt der Mindestabstand zwischen zwei Diagrammen 2,5 /512,0 Texel.</span><span class="sxs-lookup"><span data-stu-id="d342c-129">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-130">*dwTextureIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-130">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d342c-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d342c-132">Nullbasierter Texturkoordinatenindex, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d342c-132">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-133">*pdwAdjazenz* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-133">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-134">Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d342c-134">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d342c-135">Ein Zeiger auf ein Array von Adjazenzdaten.</span><span class="sxs-lookup"><span data-stu-id="d342c-135">A pointer to an array of adjacency data.</span></span> <span data-ttu-id="d342c-136">mit 3 DWORDs pro Gesicht, die angeben, welche Dreiecke nebeneinander angeordnet sind (siehe [**ID3DXBaseMesh::GenerateAdencyency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="d342c-136">with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d342c-137">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="d342c-137">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="d342c-138">Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d342c-138">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d342c-139">Ein Array mit 3 DWORDS pro Gesicht.</span><span class="sxs-lookup"><span data-stu-id="d342c-139">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="d342c-140">Jedes Gesicht gibt an, ob ein Rand false ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="d342c-140">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="d342c-141">Ein nicht falscher Rand wird durch -1 angegeben, ein falscher Rand durch einen anderen Wert.</span><span class="sxs-lookup"><span data-stu-id="d342c-141">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="d342c-142">Dies ermöglicht die Parametrisierung eines Gitternetzes von Quadern, wobei die Ränder in der Mitte jedes Quaders nicht geschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="d342c-142">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-143">*pfIMTArray* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-143">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-144">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d342c-144">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d342c-145">Ein Zeiger auf ein Array integrierter Metriktensoren, der beschreibt, wie ein Dreieck gestreckt wird (siehe [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="d342c-145">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d342c-146">*pCallback* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-146">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-147">Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="d342c-147">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="d342c-148">Ein Zeiger auf eine Rückruffunktion (siehe [LPD3DXUVATLASCB),](lpd3dxuvatlascb.md)die für die Überwachung des Fortschritts nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="d342c-148">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-149">*fCallbackFrequency* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-149">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-150">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d342c-150">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d342c-151">Geben Sie an, wie oft D3DX den Rückruf aufruft. Ein angemessener Standardwert ist 0,0001f.</span><span class="sxs-lookup"><span data-stu-id="d342c-151">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-152">*pUserContent* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-152">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-153">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d342c-153">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d342c-154">Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird; Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion enthält.</span><span class="sxs-lookup"><span data-stu-id="d342c-154">Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-155">*dwOptions* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-155">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-156">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d342c-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d342c-157">Geben Sie die Qualität der generierten Diagramme an.</span><span class="sxs-lookup"><span data-stu-id="d342c-157">Specify the quality of the charts generated.</span></span> <span data-ttu-id="d342c-158">Siehe [**D3DXUVATLAS**](./d3dxuvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="d342c-158">See [**D3DXUVATLAS**](./d3dxuvatlas.md).</span></span>

</dd> <dt>

<span data-ttu-id="d342c-159">*ppMeshOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d342c-159">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-160">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d342c-160">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="d342c-161">Zeiger auf das erstellte Gitter mit dem Atlas (siehe [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="d342c-161">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d342c-162">*ppFacePartitioning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d342c-162">*ppFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-163">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d342c-163">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d342c-164">Ein Zeiger auf ein Array der endgültigen Gesichtspartitionierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="d342c-164">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="d342c-165">Jedes Element enthält ein DWORD pro Gesicht (siehe [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="d342c-165">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d342c-166">*ppVertexRemapArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d342c-166">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-167">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d342c-167">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d342c-168">Ein Zeiger auf ein Array neu zugeordneter Scheitelpunkte.</span><span class="sxs-lookup"><span data-stu-id="d342c-168">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="d342c-169">Jedes Arrayelement identifiziert den ursprünglichen Scheitelpunkt, von dem jeder letzte Scheitelpunkt stammt (wenn der Scheitelpunkt während der Neuzuordnung geteilt wurde).</span><span class="sxs-lookup"><span data-stu-id="d342c-169">Each array element identifies the original vertex that each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="d342c-170">Jedes Arrayelement enthält ein DWORD pro Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="d342c-170">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-171">*pfMaxStretchOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d342c-171">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-172">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d342c-172">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d342c-173">Ein Zeiger auf den maximalen Stretchwert, der vom Atlas-Algorithmus generiert wird.</span><span class="sxs-lookup"><span data-stu-id="d342c-173">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="d342c-174">Der Bereich liegt zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="d342c-174">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="d342c-175">*pdwNumChartsOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d342c-175">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d342c-176">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d342c-176">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d342c-177">Ein Zeiger auf die Anzahl von Diagrammen, die vom Atlas-Algorithmus erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d342c-177">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="d342c-178">Wenn dwMaxChartNumber zu niedrig ist, gibt dieser Parameter die mindest erforderliche Anzahl von Diagrammen zurück, um einen Atlas zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d342c-178">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d342c-179">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d342c-179">Return value</span></span>

<span data-ttu-id="d342c-180">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d342c-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d342c-181">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Andernfalls ist der Wert D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d342c-181">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d342c-182">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d342c-182">Remarks</span></span>

<span data-ttu-id="d342c-183">D3DXUVAtlasCreate kann die Meshgeometrie auf zwei Arten partitionieren:</span><span class="sxs-lookup"><span data-stu-id="d342c-183">D3DXUVAtlasCreate can partition mesh geometry two ways:</span></span>

-   <span data-ttu-id="d342c-184">Basierend auf der Anzahl der Diagramme</span><span class="sxs-lookup"><span data-stu-id="d342c-184">Based on the number of charts</span></span>
-   <span data-ttu-id="d342c-185">Basierend auf dem maximal zulässigen Stretching.</span><span class="sxs-lookup"><span data-stu-id="d342c-185">Based on the maximum allowed stretch.</span></span> <span data-ttu-id="d342c-186">Wenn die maximal zulässige Streckung 0 beträgt, befindet sich jedes Dreieck wahrscheinlich in einem eigenen Diagramm.</span><span class="sxs-lookup"><span data-stu-id="d342c-186">If the maximum allowed stretch is 0, each triangle will likely be in its own chart.</span></span>

## <a name="requirements"></a><span data-ttu-id="d342c-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d342c-187">Requirements</span></span>



| <span data-ttu-id="d342c-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d342c-188">Requirement</span></span> | <span data-ttu-id="d342c-189">Wert</span><span class="sxs-lookup"><span data-stu-id="d342c-189">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d342c-190">Header</span><span class="sxs-lookup"><span data-stu-id="d342c-190">Header</span></span><br/>  | <dl> <span data-ttu-id="d342c-191"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="d342c-191"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d342c-192">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d342c-192">Library</span></span><br/> | <dl> <span data-ttu-id="d342c-193"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d342c-193"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d342c-194">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d342c-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d342c-195">UVAtlas-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d342c-195">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="d342c-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="d342c-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
