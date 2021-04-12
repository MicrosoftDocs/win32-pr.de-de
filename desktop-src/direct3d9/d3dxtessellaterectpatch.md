---
description: Mosaik einen rechteckigen Patch für eine höhere Ordnung in einem Dreiecks Gitter.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: D3DXTessellateRectPatch-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219493"
---
# <a name="d3dxtessellaterectpatch-function"></a><span data-ttu-id="dcc30-103">D3DXTessellateRectPatch-Funktion</span><span class="sxs-lookup"><span data-stu-id="dcc30-103">D3DXTessellateRectPatch function</span></span>

<span data-ttu-id="dcc30-104">Mosaik einen rechteckigen Patch für eine höhere Ordnung in einem Dreiecks Gitter.</span><span class="sxs-lookup"><span data-stu-id="dcc30-104">Tessellates a rectangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc30-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcc30-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="dcc30-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcc30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcc30-107">*PVB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcc30-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc30-108">Typ: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="dcc30-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="dcc30-109">Vertex-Puffer, der die Patchdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="dcc30-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="dcc30-110">*pnumsek* \[ . in\]</span><span class="sxs-lookup"><span data-stu-id="dcc30-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc30-111">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dcc30-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dcc30-112">Ein Zeiger auf ein Array von vier Gleit Komma Werten, die die Anzahl der Segmente angeben, in die die einzelnen Kanten des Rechteck Patches bei einem Mosaik Prozess aufgeteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dcc30-112">Pointer to an array of four floating-point values that identify the number of segments into which each edge of the rectangle patch should be divided when tessellated.</span></span> <span data-ttu-id="dcc30-113">Siehe [**D3DRECTPATCH \_ Info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="dcc30-113">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcc30-114">*pindecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcc30-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc30-115">Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="dcc30-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="dcc30-116">Vertex-Deklarations Struktur, die die Scheitelpunkt Daten definiert.</span><span class="sxs-lookup"><span data-stu-id="dcc30-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="dcc30-117">Siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="dcc30-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcc30-118">*prectpatchinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcc30-118">*pRectPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc30-119">Type: **[**D3DRECTPATCH \_ Info**](d3drectpatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="dcc30-119">Type: **const [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md)\***</span></span>

<span data-ttu-id="dcc30-120">Beschreibt einen rechteckigen Patch.</span><span class="sxs-lookup"><span data-stu-id="dcc30-120">Describes a rectangular patch.</span></span> <span data-ttu-id="dcc30-121">Siehe [**D3DRECTPATCH \_ Info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="dcc30-121">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcc30-122">*pmesh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dcc30-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc30-123">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="dcc30-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="dcc30-124">Zeiger auf das erstellte Mesh.</span><span class="sxs-lookup"><span data-stu-id="dcc30-124">Pointer to the created mesh.</span></span> <span data-ttu-id="dcc30-125">Siehe [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="dcc30-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcc30-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dcc30-126">Return value</span></span>

<span data-ttu-id="dcc30-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dcc30-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dcc30-128">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dcc30-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dcc30-129">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="dcc30-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcc30-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcc30-130">Remarks</span></span>

<span data-ttu-id="dcc30-131">Verwenden Sie [**D3DXRectPatchSize**](d3dxrectpatchsize.md) , um die Anzahl der Ausgabe Scheitel Punkte und Indizes zu erhalten, die von der Mosaik Funktion benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="dcc30-131">Use [**D3DXRectPatchSize**](d3dxrectpatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc30-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcc30-132">Requirements</span></span>



| <span data-ttu-id="dcc30-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcc30-133">Requirement</span></span> | <span data-ttu-id="dcc30-134">Wert</span><span class="sxs-lookup"><span data-stu-id="dcc30-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc30-135">Header</span><span class="sxs-lookup"><span data-stu-id="dcc30-135">Header</span></span><br/>  | <dl> <span data-ttu-id="dcc30-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcc30-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dcc30-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dcc30-137">Library</span></span><br/> | <dl> <span data-ttu-id="dcc30-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcc30-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dcc30-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcc30-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc30-140">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="dcc30-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="dcc30-141">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="dcc30-141">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
