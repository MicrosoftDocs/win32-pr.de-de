---
description: Teilt ein Mesh in die Netze, die kleiner als die angegebene Größe sind.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: D3DXSplitMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364362"
---
# <a name="d3dxsplitmesh-function"></a><span data-ttu-id="47c07-103">D3DXSplitMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="47c07-103">D3DXSplitMesh function</span></span>

<span data-ttu-id="47c07-104">Teilt ein Mesh in die Netze, die kleiner als die angegebene Größe sind.</span><span class="sxs-lookup"><span data-stu-id="47c07-104">Splits a mesh into meshes smaller than the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c07-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47c07-105">Syntax</span></span>


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a><span data-ttu-id="47c07-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47c07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47c07-107">*pmeshat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47c07-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c07-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="47c07-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="47c07-109">Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das quellmesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="47c07-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="47c07-110">*padjackocyin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47c07-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c07-111">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="47c07-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="47c07-112">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt, das vereinfacht werden soll.</span><span class="sxs-lookup"><span data-stu-id="47c07-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="47c07-113">*MaxSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47c07-113">*MaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c07-114">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47c07-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47c07-115">Maximale Anzahl der Scheitel Punkte im resultierenden Mesh.</span><span class="sxs-lookup"><span data-stu-id="47c07-115">Maximum number of vertices in the resulting mesh.</span></span>

</dd> <dt>

<span data-ttu-id="47c07-116">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47c07-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c07-117">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47c07-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47c07-118">Optionsflags für die neuen Netze.</span><span class="sxs-lookup"><span data-stu-id="47c07-118">Option flags for the new meshes.</span></span>

</dd> <dt>

<span data-ttu-id="47c07-119">*pmeshesout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="47c07-119">*pMeshesOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c07-120">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="47c07-120">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="47c07-121">Anzahl der zurückgegebenen Netzen.</span><span class="sxs-lookup"><span data-stu-id="47c07-121">Number of meshes returned.</span></span>

</dd> <dt>

<span data-ttu-id="47c07-122">*ppmesharrayout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="47c07-122">*ppMeshArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c07-123">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="47c07-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="47c07-124">Puffer, der ein Array von [**ID3DXMesh**](id3dxmesh.md) -Schnittstellen für die neuen Meshes enthält.</span><span class="sxs-lookup"><span data-stu-id="47c07-124">Buffer containing an array of [**ID3DXMesh**](id3dxmesh.md) interfaces for the new meshes.</span></span> <span data-ttu-id="47c07-125">Bei einem quellmesh, das in n Meshes aufgeteilt ist, ist *ppmesharrayout* ein Array von n **ID3DXMesh** -Zeigern.</span><span class="sxs-lookup"><span data-stu-id="47c07-125">For a source mesh split into n meshes, *ppMeshArrayOut* is an array of n **ID3DXMesh** pointers.</span></span>

</dd> <dt>

<span data-ttu-id="47c07-126">*ppyouts-cyarrayout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="47c07-126">*ppAdjacencyArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c07-127">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="47c07-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="47c07-128">Ein Puffer, der ein Array von annähernden Arrays (DWords) für die neuen Meshes enthält.</span><span class="sxs-lookup"><span data-stu-id="47c07-128">Buffer containing an array of adjacency arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="47c07-129">Siehe [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="47c07-129">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="47c07-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47c07-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="47c07-131">*ppfakeremaparamerayout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="47c07-131">*ppFaceRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c07-132">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="47c07-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="47c07-133">Puffer, der ein Array von Flächen Umwandlungs Arrays (DWords) für die neuen Meshes enthält.</span><span class="sxs-lookup"><span data-stu-id="47c07-133">Buffer containing an array of face remap arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="47c07-134">Siehe [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="47c07-134">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="47c07-135">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47c07-135">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="47c07-136">*ppvertremaparamerayout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="47c07-136">*ppVertRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c07-137">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="47c07-137">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="47c07-138">Ein Puffer, der ein Array von Vertex-neuumwandlungs Arrays für die neuen Meshes enthält.</span><span class="sxs-lookup"><span data-stu-id="47c07-138">Buffer containing an array of vertex remap arrays for the new meshes.</span></span> <span data-ttu-id="47c07-139">Siehe [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="47c07-139">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="47c07-140">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="47c07-140">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47c07-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47c07-141">Return value</span></span>

<span data-ttu-id="47c07-142">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47c07-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="47c07-143">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="47c07-143">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="47c07-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47c07-144">Remarks</span></span>

<span data-ttu-id="47c07-145">Diese Funktion wird häufig verwendet, um ein Mesh mit 32-Bit-Indizes (mehr als 65535 Scheitel Punkten) in mehr als ein Mesh aufzuteilen, die jeweils über 16-Bit-Indizes verfügen.</span><span class="sxs-lookup"><span data-stu-id="47c07-145">A common use of this function is to split a mesh with 32-bit indices (more than 65535 vertices) into more than one mesh, each of which has 16-bit indices.</span></span>

<span data-ttu-id="47c07-146">Die Arrays "ency", "Vertex Umwandlungs" und "Face Umwandlungs" sind Arrays sind "DWords", wobei jedes Array n DWORD-Zeiger enthält, gefolgt von den DWORD-Daten, auf die die Zeiger verweisen.</span><span class="sxs-lookup"><span data-stu-id="47c07-146">The adjacency, vertex remap and face remap arrays are arrays are DWORDs where each array contains n DWORD pointers, followed by the DWORD data referenced by the pointers.</span></span> <span data-ttu-id="47c07-147">Um z. b. die Gesichts Umwandlungs Informationen für Gesicht 3 in Mesh 2 abzurufen, könnte der folgende Code verwendet werden, vorausgesetzt, die Daten zur gleich Umgestaltung wurden in einer Variablen mit dem Namen *ppfakeremaparamerayout* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47c07-147">For example, to obtain the face remap information for face 3 in mesh 2, the following code could be used, assuming the face remap data was returned in a variable named *ppFaceRemapArrayOut*.</span></span>


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a><span data-ttu-id="47c07-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47c07-148">Requirements</span></span>



| <span data-ttu-id="47c07-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47c07-149">Requirement</span></span> | <span data-ttu-id="47c07-150">Wert</span><span class="sxs-lookup"><span data-stu-id="47c07-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47c07-151">Header</span><span class="sxs-lookup"><span data-stu-id="47c07-151">Header</span></span><br/>  | <dl> <span data-ttu-id="47c07-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="47c07-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="47c07-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47c07-153">Library</span></span><br/> | <dl> <span data-ttu-id="47c07-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47c07-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47c07-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47c07-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c07-156">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="47c07-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
