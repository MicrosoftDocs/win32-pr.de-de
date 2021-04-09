---
description: Mosaik Elemente in einem Dreiecks Gitter, das eine eckige Oberfläche für eine höhere Ordnung ist.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: D3DXTessellateTriPatch-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61d5a426f9fe3331b85c4a881219319622283820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762018"
---
# <a name="d3dxtessellatetripatch-function"></a><span data-ttu-id="bfaa7-103">D3DXTessellateTriPatch-Funktion</span><span class="sxs-lookup"><span data-stu-id="bfaa7-103">D3DXTessellateTriPatch function</span></span>

<span data-ttu-id="bfaa7-104">Mosaik Elemente in einem Dreiecks Gitter, das eine eckige Oberfläche für eine höhere Ordnung ist.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-104">Tessellates a triangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfaa7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfaa7-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="bfaa7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfaa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfaa7-107">*PVB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfaa7-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfaa7-108">Typ: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="bfaa7-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="bfaa7-109">Vertex-Puffer, der die Patchdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="bfaa7-110">*pnumsek* \[ . in\]</span><span class="sxs-lookup"><span data-stu-id="bfaa7-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfaa7-111">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="bfaa7-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bfaa7-112">Ein Zeiger auf ein Array von drei Gleit Komma Werten, die die Anzahl der Segmente identifizieren, in denen die einzelnen Kanten des Dreiecks Patches bei einem Mosaik Prozess aufgeteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-112">Pointer to an array of three floating-point values that identify the number of segments into which each edge of the triangle patch should be divided when tessellated.</span></span> <span data-ttu-id="bfaa7-113">Siehe [**D3DTRIPATCH \_ Info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="bfaa7-113">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfaa7-114">*pindecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfaa7-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfaa7-115">Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="bfaa7-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="bfaa7-116">Vertex-Deklarations Struktur, die die Scheitelpunkt Daten definiert.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="bfaa7-117">Siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="bfaa7-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfaa7-118">*pzpatchinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfaa7-118">*pTriPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfaa7-119">Type: **[**D3TRIPATCH \_ Info**](d3dtripatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="bfaa7-119">Type: **const [**D3TRIPATCH\_INFO**](d3dtripatch-info.md)\***</span></span>

<span data-ttu-id="bfaa7-120">Beschreibt einen Dreiecks Patch.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-120">Describes a triangle patch.</span></span> <span data-ttu-id="bfaa7-121">Siehe [**D3DTRIPATCH \_ Info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="bfaa7-121">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfaa7-122">*pmesh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bfaa7-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfaa7-123">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="bfaa7-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="bfaa7-124">Zeiger auf das erstellte Mesh.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-124">Pointer to the created mesh.</span></span> <span data-ttu-id="bfaa7-125">Siehe [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="bfaa7-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfaa7-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfaa7-126">Return value</span></span>

<span data-ttu-id="bfaa7-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bfaa7-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bfaa7-128">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bfaa7-129">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfaa7-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfaa7-130">Remarks</span></span>

<span data-ttu-id="bfaa7-131">Verwenden Sie [**D3DXTriPatchSize**](d3dxtripatchsize.md) , um die Anzahl der Ausgabe Scheitel Punkte und Indizes zu erhalten, die von der Mosaik Funktion benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="bfaa7-131">Use [**D3DXTriPatchSize**](d3dxtripatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfaa7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfaa7-132">Requirements</span></span>



| <span data-ttu-id="bfaa7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfaa7-133">Requirement</span></span> | <span data-ttu-id="bfaa7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="bfaa7-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfaa7-135">Header</span><span class="sxs-lookup"><span data-stu-id="bfaa7-135">Header</span></span><br/>  | <dl> <span data-ttu-id="bfaa7-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfaa7-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bfaa7-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bfaa7-137">Library</span></span><br/> | <dl> <span data-ttu-id="bfaa7-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfaa7-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bfaa7-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfaa7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfaa7-140">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="bfaa7-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="bfaa7-141">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="bfaa7-141">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
