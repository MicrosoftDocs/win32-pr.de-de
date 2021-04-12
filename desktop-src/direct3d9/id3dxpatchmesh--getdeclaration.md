---
description: Ruft die Vertex-Deklaration ab.
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'ID3DXPatchMesh:: getDeclaration-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 7d2d39192368fdca8ccaba7c51e64f60ea030568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356086"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a><span data-ttu-id="6ea6c-103">ID3DXPatchMesh:: getDeclaration-Methode</span><span class="sxs-lookup"><span data-stu-id="6ea6c-103">ID3DXPatchMesh::GetDeclaration method</span></span>

<span data-ttu-id="6ea6c-104">Ruft die Vertex-Deklaration ab.</span><span class="sxs-lookup"><span data-stu-id="6ea6c-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea6c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ea6c-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="6ea6c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ea6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ea6c-107">*pdeclaration* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6ea6c-107">*pDeclaration* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea6c-108">Typ: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="6ea6c-108">Type: **[**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="6ea6c-109">Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, die das Scheitelpunkt Format der Mesh-Scheitel Punkte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6ea6c-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="6ea6c-110">Die Dimension dieses deklaratorarrays ist die [**Maximale Anzahl von \_ SVF- \_ decls \_**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="6ea6c-110">The dimension of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="6ea6c-111">Das Vertex-Element Array endet mit dem [**D3DDECL \_ End**](d3ddecl-end.md) -Makro.</span><span class="sxs-lookup"><span data-stu-id="6ea6c-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ea6c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ea6c-112">Return value</span></span>

<span data-ttu-id="6ea6c-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6ea6c-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6ea6c-114">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ea6c-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6ea6c-115">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="6ea6c-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ea6c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ea6c-116">Remarks</span></span>

<span data-ttu-id="6ea6c-117">Das Array von-Elementen enthält das [**D3DDECL \_ End**](d3ddecl-end.md) -Makro, das die Deklaration beendet.</span><span class="sxs-lookup"><span data-stu-id="6ea6c-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ea6c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ea6c-118">Requirements</span></span>



| <span data-ttu-id="6ea6c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ea6c-119">Requirement</span></span> | <span data-ttu-id="6ea6c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6ea6c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea6c-121">Header</span><span class="sxs-lookup"><span data-stu-id="6ea6c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6ea6c-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ea6c-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6ea6c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6ea6c-123">Library</span></span><br/> | <dl> <span data-ttu-id="6ea6c-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ea6c-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ea6c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ea6c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ea6c-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="6ea6c-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
