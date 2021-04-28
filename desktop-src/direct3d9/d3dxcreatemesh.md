---
description: 'D3DXCreateMesh-Funktion: Erstellt ein Gittermodellobjekt mithilfe eines Deklarators.'
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: D3DXCreateMesh-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: 1c7e1c0d626c74f5427f91a5b9eb796e3b79d5a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102758"
---
# <a name="d3dxcreatemesh-function"></a><span data-ttu-id="2ec46-103">D3DXCreateMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="2ec46-103">D3DXCreateMesh function</span></span>

<span data-ttu-id="2ec46-104">Erstellt ein Gittermodellobjekt mithilfe eines Deklarators.</span><span class="sxs-lookup"><span data-stu-id="2ec46-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ec46-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ec46-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2ec46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ec46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ec46-107">*NumFaces* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ec46-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ec46-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ec46-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ec46-109">Anzahl der Gesichter für das Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="2ec46-109">Number of faces for the mesh.</span></span> <span data-ttu-id="2ec46-110">Der gültige Bereich für diese Zahl ist größer als 0 und einer kleiner als der maximale DWORD-Wert (in der Regel 65534), da der letzte Index reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="2ec46-110">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2ec46-111">*NumVertices* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ec46-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ec46-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ec46-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ec46-113">Anzahl der Scheitelpunkte für das Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="2ec46-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="2ec46-114">Dieser Parameter muss größer als 0 sein.</span><span class="sxs-lookup"><span data-stu-id="2ec46-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="2ec46-115">*Optionen* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ec46-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ec46-116">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ec46-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ec46-117">Kombination aus einem oder mehreren Flags aus der [**D3DXMESH-Enumeration,**](./d3dxmesh.md) die Optionen für das Gitternetz angeben.</span><span class="sxs-lookup"><span data-stu-id="2ec46-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2ec46-118">*pDeclaration* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ec46-118">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ec46-119">Typ: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ec46-119">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="2ec46-120">Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) das das Scheitelpunktformat für das zurückgegebene Gitternetz beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2ec46-120">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="2ec46-121">Dieser Parameter muss direkt einem flexiblen Vertexformat (FVF) zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2ec46-121">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="2ec46-122">*pD3DDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ec46-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ec46-123">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2ec46-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2ec46-124">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das Geräteobjekt, das dem Gittermodell zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ec46-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2ec46-125">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2ec46-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ec46-126">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ec46-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="2ec46-127">Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das erstellte Gittermodellobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2ec46-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ec46-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ec46-128">Return value</span></span>

<span data-ttu-id="2ec46-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ec46-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ec46-130">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ec46-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2ec46-131">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2ec46-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ec46-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ec46-132">Requirements</span></span>



| <span data-ttu-id="2ec46-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ec46-133">Requirement</span></span> | <span data-ttu-id="2ec46-134">Wert</span><span class="sxs-lookup"><span data-stu-id="2ec46-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ec46-135">Header</span><span class="sxs-lookup"><span data-stu-id="2ec46-135">Header</span></span><br/>  | <dl> <span data-ttu-id="2ec46-136"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="2ec46-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2ec46-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ec46-137">Library</span></span><br/> | <dl> <span data-ttu-id="2ec46-138"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ec46-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2ec46-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2ec46-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ec46-140">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="2ec46-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="2ec46-141">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="2ec46-141">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
