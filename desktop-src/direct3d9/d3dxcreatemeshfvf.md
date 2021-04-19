---
description: Erstellt ein Mesh-Objekt mithilfe eines FVF-Codes (Flexible Vertex-Format).
ms.assetid: 4681f181-8a16-42d4-bbfa-bdee5ed69fd3
title: D3DXCreateMeshFVF-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMeshFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9d5589b0f02bfcb85f9c0f0dc4dc5de69e2fb23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360237"
---
# <a name="d3dxcreatemeshfvf-function"></a><span data-ttu-id="6ea9c-103">D3DXCreateMeshFVF-Funktion</span><span class="sxs-lookup"><span data-stu-id="6ea9c-103">D3DXCreateMeshFVF function</span></span>

<span data-ttu-id="6ea9c-104">Erstellt ein Mesh-Objekt mithilfe eines FVF-Codes (Flexible Vertex-Format).</span><span class="sxs-lookup"><span data-stu-id="6ea9c-104">Creates a mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea9c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ea9c-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMeshFVF(
  _In_  DWORD             NumFaces,
  _In_  DWORD             NumVertices,
  _In_  DWORD             Options,
  _In_  DWORD             FVF,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="6ea9c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ea9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ea9c-107">*Numerische Werte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ea9c-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea9c-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ea9c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ea9c-109">Anzahl der Flächen für das Mesh.</span><span class="sxs-lookup"><span data-stu-id="6ea9c-109">Number of faces for the mesh.</span></span> <span data-ttu-id="6ea9c-110">Der gültige Bereich für diese Zahl ist größer als 0 (null) und ein kleiner als der Max DWORD-Wert (in der Regel 2 ³ ²-1), da der letzte Index reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="6ea9c-110">The valid range for this number is greater than 0, and one less than the max DWORD value, typically 2³² - 1, because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6ea9c-111">*Numvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ea9c-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea9c-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ea9c-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ea9c-113">Anzahl der Scheitel Punkte für das Mesh.</span><span class="sxs-lookup"><span data-stu-id="6ea9c-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="6ea9c-114">Dieser Parameter muss größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="6ea9c-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="6ea9c-115">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ea9c-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea9c-116">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ea9c-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ea9c-117">Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Erstellungs Optionen für das Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="6ea9c-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6ea9c-118">*F-VF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ea9c-118">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea9c-119">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ea9c-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ea9c-120">Eine Kombination aus [D3DFVF](d3dfvf.md) , die das Vertex-Format für das zurückgegebene Mesh beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6ea9c-120">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned mesh.</span></span> <span data-ttu-id="6ea9c-121">Diese Funktion unterstützt D3DFVF \_ xyzrhw nicht.</span><span class="sxs-lookup"><span data-stu-id="6ea9c-121">This function does not support D3DFVF\_XYZRHW.</span></span>

</dd> <dt>

<span data-ttu-id="6ea9c-122">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ea9c-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea9c-123">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6ea9c-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6ea9c-124">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das Geräte Objekt, das dem Mesh zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ea9c-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6ea9c-125">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6ea9c-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea9c-126">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ea9c-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="6ea9c-127">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das erstellte Mesh-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ea9c-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ea9c-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ea9c-128">Return value</span></span>

<span data-ttu-id="6ea9c-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6ea9c-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6ea9c-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ea9c-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6ea9c-131">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="6ea9c-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ea9c-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ea9c-132">Requirements</span></span>



| <span data-ttu-id="6ea9c-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ea9c-133">Requirement</span></span> | <span data-ttu-id="6ea9c-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6ea9c-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea9c-135">Header</span><span class="sxs-lookup"><span data-stu-id="6ea9c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="6ea9c-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ea9c-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6ea9c-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6ea9c-137">Library</span></span><br/> | <dl> <span data-ttu-id="6ea9c-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ea9c-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ea9c-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ea9c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ea9c-140">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="6ea9c-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="6ea9c-141">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="6ea9c-141">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
