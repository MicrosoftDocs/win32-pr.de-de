---
description: 'ID3DXSkinInfo::GetDeclaration-Methode: Ruft die Scheitelpunktdeklaration ab.'
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: ID3DXSkinInfo::GetDeclaration-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: 83554b13fe8e20890b1edecd690c540c2e14d4d7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093138"
---
# <a name="id3dxskininfogetdeclaration-method"></a><span data-ttu-id="14c17-103">ID3DXSkinInfo::GetDeclaration-Methode</span><span class="sxs-lookup"><span data-stu-id="14c17-103">ID3DXSkinInfo::GetDeclaration method</span></span>

<span data-ttu-id="14c17-104">Ruft die Scheitelpunktdeklaration ab.</span><span class="sxs-lookup"><span data-stu-id="14c17-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c17-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14c17-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="14c17-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14c17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c17-107">*Deklaration* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="14c17-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="14c17-108">Typ: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="14c17-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="14c17-109">Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) die das Scheitelpunktformat der Gitternetzvertices beschreiben.</span><span class="sxs-lookup"><span data-stu-id="14c17-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="14c17-110">Die Obergrenze dieses Deklaratorarrays ist [**MAX \_ FVF \_ DECL \_ SIZE.**](./max-fvf-decl-size.md)</span><span class="sxs-lookup"><span data-stu-id="14c17-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="14c17-111">Das Vertexelementarray endet mit dem [**D3DDECL \_ END-Makro.**](d3ddecl-end.md)</span><span class="sxs-lookup"><span data-stu-id="14c17-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c17-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14c17-112">Return value</span></span>

<span data-ttu-id="14c17-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14c17-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14c17-114">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="14c17-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="14c17-115">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="14c17-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="14c17-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14c17-116">Remarks</span></span>

<span data-ttu-id="14c17-117">Das Array von Elementen enthält das [**D3DDECL \_ END-Makro,**](d3ddecl-end.md) das die Deklaration beendet.</span><span class="sxs-lookup"><span data-stu-id="14c17-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="14c17-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14c17-118">Requirements</span></span>



| <span data-ttu-id="14c17-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14c17-119">Requirement</span></span> | <span data-ttu-id="14c17-120">Wert</span><span class="sxs-lookup"><span data-stu-id="14c17-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14c17-121">Header</span><span class="sxs-lookup"><span data-stu-id="14c17-121">Header</span></span><br/>  | <dl> <span data-ttu-id="14c17-122"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="14c17-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="14c17-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14c17-123">Library</span></span><br/> | <dl> <span data-ttu-id="14c17-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="14c17-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="14c17-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14c17-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c17-126">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="14c17-126">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="14c17-127">**ID3DXSkinInfo::SetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="14c17-127">**ID3DXSkinInfo::SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
