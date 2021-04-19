---
description: Erstellt ein N-patchmesh aus einem Dreiecks Gitter.
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: D3DXCreateNPatchMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateNPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ab73d1254700808bbd56b7b46f7781b27b188b7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353402"
---
# <a name="d3dxcreatenpatchmesh-function"></a><span data-ttu-id="9fd02-103">D3DXCreateNPatchMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="9fd02-103">D3DXCreateNPatchMesh function</span></span>

<span data-ttu-id="9fd02-104">Erstellt ein N-patchmesh aus einem Dreiecks Gitter.</span><span class="sxs-lookup"><span data-stu-id="9fd02-104">Creates an N-patch mesh from a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fd02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fd02-105">Syntax</span></span>


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="9fd02-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fd02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fd02-107">*pmeshsysmem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fd02-107">*pMeshSysMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fd02-108">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="9fd02-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="9fd02-109">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das Dreiecks Gitter Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9fd02-109">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represents the triangle mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="9fd02-110">*ppatchmesh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9fd02-110">*pPatchMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fd02-111">Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="9fd02-111">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="9fd02-112">Adresse eines Zeigers auf eine [**ID3DXPatchMesh**](id3dxpatchmesh.md) -Schnittstelle, die das erstellte patchmesh-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9fd02-112">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the created patch mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fd02-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fd02-113">Return value</span></span>

<span data-ttu-id="9fd02-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9fd02-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9fd02-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9fd02-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9fd02-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="9fd02-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fd02-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fd02-117">Requirements</span></span>



| <span data-ttu-id="9fd02-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fd02-118">Requirement</span></span> | <span data-ttu-id="9fd02-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9fd02-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd02-120">Header</span><span class="sxs-lookup"><span data-stu-id="9fd02-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9fd02-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fd02-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9fd02-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9fd02-122">Library</span></span><br/> | <dl> <span data-ttu-id="9fd02-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fd02-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9fd02-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fd02-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd02-125">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9fd02-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




