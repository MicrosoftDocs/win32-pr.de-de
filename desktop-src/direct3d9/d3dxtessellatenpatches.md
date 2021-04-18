---
description: Erstellt das angegebene Mesh mit dem N-Patch-Mosaik Schema.
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: D3DXTessellateNPatches-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c8811816447deb858b5c8b42d651d219f06fef5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365302"
---
# <a name="d3dxtessellatenpatches-function"></a><span data-ttu-id="f9b9f-103">D3DXTessellateNPatches-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9b9f-103">D3DXTessellateNPatches function</span></span>

<span data-ttu-id="f9b9f-104">Erstellt das angegebene Mesh mit dem N-Patch-Mosaik Schema.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-104">Tessellates the given mesh using the N-patch tessellation scheme.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b9f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9b9f-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a><span data-ttu-id="f9b9f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9b9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9b9f-107">*pmeshat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9b9f-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b9f-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f9b9f-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="f9b9f-109">Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das zu Mosaik Ende Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="f9b9f-110">*padjackocyin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9b9f-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b9f-111">Typ: Konstante Konstante **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="f9b9f-111">Type: **const CONST DWORD\***</span></span>

<span data-ttu-id="f9b9f-112">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im quellmesh angibt.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="f9b9f-113">Dieser Parameter kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-113">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f9b9f-114">*Numungsgs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9b9f-114">*NumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b9f-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9b9f-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9b9f-116">Anzahl der Segmente pro Rand bis Mosaik.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-116">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="f9b9f-117">*Quadraticinterpnormals* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9b9f-117">*QuadraticInterpNormals* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b9f-118">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9b9f-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9b9f-119">Auf **true** festgelegt, um quadratische Interpolationen für normale zu verwenden; Legen Sie für die lineare interpolung auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-119">Set to **TRUE** to use quadratic interpolation for normals; set to **FALSE** for linear interpolation.</span></span>

</dd> <dt>

<span data-ttu-id="f9b9f-120">*ppmeshout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f9b9f-120">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b9f-121">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="f9b9f-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="f9b9f-122">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das zurückgegebene Mosaik Gitter darstellt.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-122">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned tessellated mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f9b9f-123">*ppyouts-cyout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f9b9f-123">*ppAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b9f-124">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f9b9f-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f9b9f-125">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="f9b9f-126">Wenn der Wert dieses Parameters nicht auf **null** festgelegt ist, enthält dieser Puffer ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Ausgabe Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-126">If the value of this parameter is not set to **NULL**, this buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="f9b9f-127">Dieser Parameter kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-127">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9b9f-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9b9f-128">Return value</span></span>

<span data-ttu-id="f9b9f-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f9b9f-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f9b9f-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f9b9f-131">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-131">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9b9f-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9b9f-132">Remarks</span></span>

<span data-ttu-id="f9b9f-133">Diese Funktion verwendet den N-Patch-Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="f9b9f-133">This function tessellates by using the N-patch algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9b9f-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9b9f-134">Requirements</span></span>



| <span data-ttu-id="f9b9f-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9b9f-135">Requirement</span></span> | <span data-ttu-id="f9b9f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="f9b9f-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b9f-137">Header</span><span class="sxs-lookup"><span data-stu-id="f9b9f-137">Header</span></span><br/>  | <dl> <span data-ttu-id="f9b9f-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9b9f-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f9b9f-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9b9f-139">Library</span></span><br/> | <dl> <span data-ttu-id="f9b9f-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9b9f-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f9b9f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9b9f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b9f-142">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f9b9f-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
