---
description: Ruft die Vertex-Deklaration ab.
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: 'ID3DXSkinInfo:: getDeclaration-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de80694bbbb6eea29f391b3b39cff9caacd4791c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354066"
---
# <a name="id3dxskininfogetdeclaration-method"></a><span data-ttu-id="9db7f-103">ID3DXSkinInfo:: getDeclaration-Methode</span><span class="sxs-lookup"><span data-stu-id="9db7f-103">ID3DXSkinInfo::GetDeclaration method</span></span>

<span data-ttu-id="9db7f-104">Ruft die Vertex-Deklaration ab.</span><span class="sxs-lookup"><span data-stu-id="9db7f-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db7f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9db7f-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="9db7f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9db7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db7f-107">*Deklaration* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9db7f-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9db7f-108">Typ: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="9db7f-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="9db7f-109">Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, die das Scheitelpunkt Format der Mesh-Scheitel Punkte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9db7f-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="9db7f-110">Die Obergrenze dieses deklaratorarrays ist [**Max \_ \_ \_**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="9db7f-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="9db7f-111">Das Vertex-Element Array endet mit dem [**D3DDECL \_ End**](d3ddecl-end.md) -Makro.</span><span class="sxs-lookup"><span data-stu-id="9db7f-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db7f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9db7f-112">Return value</span></span>

<span data-ttu-id="9db7f-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9db7f-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9db7f-114">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9db7f-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9db7f-115">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="9db7f-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9db7f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9db7f-116">Remarks</span></span>

<span data-ttu-id="9db7f-117">Das Array von-Elementen enthält das [**D3DDECL \_ End**](d3ddecl-end.md) -Makro, das die Deklaration beendet.</span><span class="sxs-lookup"><span data-stu-id="9db7f-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db7f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9db7f-118">Requirements</span></span>



| <span data-ttu-id="9db7f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9db7f-119">Requirement</span></span> | <span data-ttu-id="9db7f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9db7f-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9db7f-121">Header</span><span class="sxs-lookup"><span data-stu-id="9db7f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9db7f-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9db7f-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9db7f-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9db7f-123">Library</span></span><br/> | <dl> <span data-ttu-id="9db7f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9db7f-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9db7f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9db7f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db7f-126">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="9db7f-126">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="9db7f-127">**ID3DXSkinInfo:: setdeclaration**</span><span class="sxs-lookup"><span data-stu-id="9db7f-127">**ID3DXSkinInfo::SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
