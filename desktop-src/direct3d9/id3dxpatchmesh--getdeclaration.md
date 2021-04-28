---
description: 'ID3DXPatchMesh::GetDeclaration-Methode: Ruft die Scheitelpunktdeklaration ab.'
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: ID3DXPatchMesh::GetDeclaration-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0fde070b1b013e651c84ffea7098eb8225aed8f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093298"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a><span data-ttu-id="b183d-103">ID3DXPatchMesh::GetDeclaration-Methode</span><span class="sxs-lookup"><span data-stu-id="b183d-103">ID3DXPatchMesh::GetDeclaration method</span></span>

<span data-ttu-id="b183d-104">Ruft die Scheitelpunktdeklaration ab.</span><span class="sxs-lookup"><span data-stu-id="b183d-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="b183d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b183d-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="b183d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b183d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b183d-107">*pDeclaration* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b183d-107">*pDeclaration* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b183d-108">Typ: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="b183d-108">Type: **[**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="b183d-109">Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) die das Scheitelpunktformat der Gitternetzvertices beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b183d-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="b183d-110">Die Dimension dieses Deklaratorarrays ist [**MAX \_ FVF \_ DECL \_ SIZE.**](./max-fvf-decl-size.md)</span><span class="sxs-lookup"><span data-stu-id="b183d-110">The dimension of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="b183d-111">Das Vertexelementarray endet mit dem [**D3DDECL-END-Makro. \_**](d3ddecl-end.md)</span><span class="sxs-lookup"><span data-stu-id="b183d-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b183d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b183d-112">Return value</span></span>

<span data-ttu-id="b183d-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b183d-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b183d-114">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b183d-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b183d-115">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b183d-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b183d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b183d-116">Remarks</span></span>

<span data-ttu-id="b183d-117">Das Array von Elementen enthält das [**D3DDECL-END-Makro, \_**](d3ddecl-end.md) das die Deklaration beendet.</span><span class="sxs-lookup"><span data-stu-id="b183d-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b183d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b183d-118">Requirements</span></span>



| <span data-ttu-id="b183d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b183d-119">Requirement</span></span> | <span data-ttu-id="b183d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b183d-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b183d-121">Header</span><span class="sxs-lookup"><span data-stu-id="b183d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b183d-122"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="b183d-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b183d-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b183d-123">Library</span></span><br/> | <dl> <span data-ttu-id="b183d-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b183d-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b183d-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b183d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b183d-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="b183d-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
