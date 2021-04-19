---
description: Erstellt ein Mesh-Objekt mit einem Deklarator.
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: D3DXCreateMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cfb56fe5c52d2726dff0877522b6f72f70437552
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355824"
---
# <a name="d3dxcreatemesh-function"></a><span data-ttu-id="b65de-103">D3DXCreateMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="b65de-103">D3DXCreateMesh function</span></span>

<span data-ttu-id="b65de-104">Erstellt ein Mesh-Objekt mit einem Deklarator.</span><span class="sxs-lookup"><span data-stu-id="b65de-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="b65de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b65de-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMesh(
  _In_        DWORD               NumFaces,
  _In_        DWORD               NumVertices,
  _In_        DWORD               Options,
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _In_        LPDIRECT3DDEVICE9   pD3DDevice,
  _Out_       LPD3DXMESH          *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="b65de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b65de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b65de-107">*Numerische Werte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b65de-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b65de-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b65de-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b65de-109">Anzahl der Flächen für das Mesh.</span><span class="sxs-lookup"><span data-stu-id="b65de-109">Number of faces for the mesh.</span></span> <span data-ttu-id="b65de-110">Der gültige Bereich für diese Zahl ist größer als 0 und ein kleiner als der maximale DWORD-Wert (in der Regel 65534), da der letzte Index reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="b65de-110">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b65de-111">*Numvertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b65de-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b65de-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b65de-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b65de-113">Anzahl der Scheitel Punkte für das Mesh.</span><span class="sxs-lookup"><span data-stu-id="b65de-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="b65de-114">Dieser Parameter muss größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="b65de-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="b65de-115">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b65de-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b65de-116">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b65de-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b65de-117">Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Optionen für das Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="b65de-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b65de-118">*pdeclaration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b65de-118">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b65de-119">Typ: **Konstanten [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="b65de-119">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="b65de-120">Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, das das Scheitelpunkt Format für das zurückgegebene Mesh beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b65de-120">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="b65de-121">Dieser Parameter muss einem flexiblen Scheitelpunkt Format (FVF) direkt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b65de-121">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="b65de-122">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b65de-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b65de-123">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b65de-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b65de-124">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das Geräte Objekt, das dem Mesh zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b65de-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b65de-125">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b65de-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b65de-126">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="b65de-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="b65de-127">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das erstellte Mesh-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b65de-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b65de-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b65de-128">Return value</span></span>

<span data-ttu-id="b65de-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b65de-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b65de-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b65de-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b65de-131">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="b65de-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b65de-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b65de-132">Requirements</span></span>



| <span data-ttu-id="b65de-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b65de-133">Requirement</span></span> | <span data-ttu-id="b65de-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b65de-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b65de-135">Header</span><span class="sxs-lookup"><span data-stu-id="b65de-135">Header</span></span><br/>  | <dl> <span data-ttu-id="b65de-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b65de-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b65de-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b65de-137">Library</span></span><br/> | <dl> <span data-ttu-id="b65de-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b65de-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b65de-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b65de-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b65de-140">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="b65de-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="b65de-141">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="b65de-141">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
