---
description: Ruft die Größe des Dreiecks Patches ab.
ms.assetid: 3bfbed4c-59af-43eb-a462-478e89cfe9ae
title: D3DXTriPatchSize-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTriPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5ee254b12485153f4d5c5ba0843189399d1aed0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366636"
---
# <a name="d3dxtripatchsize-function"></a><span data-ttu-id="df637-103">D3DXTriPatchSize-Funktion</span><span class="sxs-lookup"><span data-stu-id="df637-103">D3DXTriPatchSize function</span></span>

<span data-ttu-id="df637-104">Ruft die Größe des Dreiecks Patches ab.</span><span class="sxs-lookup"><span data-stu-id="df637-104">Gets the size of the triangle patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="df637-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df637-105">Syntax</span></span>


```C++
HRESULT D3DXTriPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pdwVertices
);
```



## <a name="parameters"></a><span data-ttu-id="df637-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df637-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df637-107">*pfnumungsgs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df637-107">*pfNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df637-108">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="df637-108">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df637-109">Anzahl der Segmente pro Rand bis Mosaik.</span><span class="sxs-lookup"><span data-stu-id="df637-109">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="df637-110">*pdwdreiecke* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="df637-110">*pdwTriangles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df637-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="df637-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df637-112">Zeiger auf ein DWORD, das die Anzahl der Dreiecke im Patch enthält.</span><span class="sxs-lookup"><span data-stu-id="df637-112">Pointer to a DWORD that contains the number of triangles in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="df637-113">*pdwvertices* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="df637-113">*pdwVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df637-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="df637-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df637-115">Zeiger auf ein DWORD, das die Anzahl der Scheitel Punkte im Dreiecks Patch enthält.</span><span class="sxs-lookup"><span data-stu-id="df637-115">Pointer to a DWORD that contains the number of vertices in the triangle patch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df637-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df637-116">Return value</span></span>

<span data-ttu-id="df637-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df637-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df637-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="df637-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="df637-119">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="df637-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="df637-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df637-120">Requirements</span></span>



| <span data-ttu-id="df637-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df637-121">Requirement</span></span> | <span data-ttu-id="df637-122">Wert</span><span class="sxs-lookup"><span data-stu-id="df637-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df637-123">Header</span><span class="sxs-lookup"><span data-stu-id="df637-123">Header</span></span><br/>  | <dl> <span data-ttu-id="df637-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="df637-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="df637-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df637-125">Library</span></span><br/> | <dl> <span data-ttu-id="df637-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df637-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="df637-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df637-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df637-128">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="df637-128">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="df637-129">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="df637-129">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
