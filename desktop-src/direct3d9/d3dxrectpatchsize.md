---
description: Ruft die Größe des Rechteck Patches ab.
ms.assetid: d25373ef-789d-4515-83da-7049f040c9a4
title: D3DXRectPatchSize-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRectPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5770e05493164db9da75fb38fa1e41594bfae8f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353351"
---
# <a name="d3dxrectpatchsize-function"></a><span data-ttu-id="5d4f7-103">D3DXRectPatchSize-Funktion</span><span class="sxs-lookup"><span data-stu-id="5d4f7-103">D3DXRectPatchSize function</span></span>

<span data-ttu-id="5d4f7-104">Ruft die Größe des Rechteck Patches ab.</span><span class="sxs-lookup"><span data-stu-id="5d4f7-104">Gets the size of the rectangle patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d4f7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d4f7-105">Syntax</span></span>


```C++
HRESULT D3DXRectPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pwdVertices
);
```



## <a name="parameters"></a><span data-ttu-id="5d4f7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d4f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d4f7-107">*pfnumungsgs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d4f7-107">*pfNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4f7-108">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5d4f7-108">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5d4f7-109">Anzahl der Segmente pro Rand bis Mosaik.</span><span class="sxs-lookup"><span data-stu-id="5d4f7-109">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="5d4f7-110">*pdwdreiecke* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5d4f7-110">*pdwTriangles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4f7-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d4f7-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5d4f7-112">Zeiger auf ein DWORD, das die Anzahl der Dreiecke im Patch enthält.</span><span class="sxs-lookup"><span data-stu-id="5d4f7-112">Pointer to a DWORD that contains the number of triangles in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="5d4f7-113">*pwdvertices* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5d4f7-113">*pwdVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d4f7-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d4f7-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5d4f7-115">Zeiger auf ein DWORD, das die Anzahl der Scheitel Punkte im Patch enthält.</span><span class="sxs-lookup"><span data-stu-id="5d4f7-115">Pointer to a DWORD that contains the number of vertices in the patch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d4f7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d4f7-116">Return value</span></span>

<span data-ttu-id="5d4f7-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d4f7-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d4f7-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5d4f7-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5d4f7-119">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="5d4f7-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d4f7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d4f7-120">Requirements</span></span>



| <span data-ttu-id="5d4f7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d4f7-121">Requirement</span></span> | <span data-ttu-id="5d4f7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5d4f7-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d4f7-123">Header</span><span class="sxs-lookup"><span data-stu-id="5d4f7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5d4f7-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d4f7-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5d4f7-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5d4f7-125">Library</span></span><br/> | <dl> <span data-ttu-id="5d4f7-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d4f7-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d4f7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d4f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d4f7-128">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5d4f7-128">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="5d4f7-129">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="5d4f7-129">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
