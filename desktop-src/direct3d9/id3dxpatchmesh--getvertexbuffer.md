---
description: Ruft den mesvertexpuffer ab.
ms.assetid: 4ea4e99b-5c2c-467b-8b5d-8174c446680a
title: 'ID3DXPatchMesh:: getvertexbuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b8c3bb79d4c04db072adef857de195df7a0f0fff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370474"
---
# <a name="id3dxpatchmeshgetvertexbuffer-method"></a><span data-ttu-id="a6af9-103">ID3DXPatchMesh:: getvertexbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="a6af9-103">ID3DXPatchMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="a6af9-104">Ruft den mesvertexpuffer ab.</span><span class="sxs-lookup"><span data-stu-id="a6af9-104">Gets the mesh vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6af9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6af9-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="a6af9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6af9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6af9-107">*ppvb* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a6af9-107">*ppVB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6af9-108">Typ: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="a6af9-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="a6af9-109">Zeiger auf den Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="a6af9-109">Pointer to the vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6af9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6af9-110">Return value</span></span>

<span data-ttu-id="a6af9-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6af9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6af9-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a6af9-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a6af9-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="a6af9-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6af9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6af9-114">Remarks</span></span>

<span data-ttu-id="a6af9-115">Diese Methode setzt ein einheitliches Mosaik voraus.</span><span class="sxs-lookup"><span data-stu-id="a6af9-115">This method assumes uniform tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6af9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6af9-116">Requirements</span></span>



| <span data-ttu-id="a6af9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6af9-117">Requirement</span></span> | <span data-ttu-id="a6af9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a6af9-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6af9-119">Header</span><span class="sxs-lookup"><span data-stu-id="a6af9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a6af9-120"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6af9-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a6af9-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a6af9-121">Library</span></span><br/> | <dl> <span data-ttu-id="a6af9-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6af9-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a6af9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6af9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6af9-124">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="a6af9-124">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
