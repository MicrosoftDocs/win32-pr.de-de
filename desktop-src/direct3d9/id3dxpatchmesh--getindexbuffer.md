---
description: Ruft den Mesh-Index Puffer ab.
ms.assetid: d9152f3b-c8e6-4def-8cf1-a517ca4d34e7
title: 'ID3DXPatchMesh:: getindexbuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2730b90f77d33db519d2231a68ab7fdc2b520fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353397"
---
# <a name="id3dxpatchmeshgetindexbuffer-method"></a><span data-ttu-id="f72bc-103">ID3DXPatchMesh:: getindexbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="f72bc-103">ID3DXPatchMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="f72bc-104">Ruft den Mesh-Index Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="f72bc-104">Gets the mesh index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f72bc-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="f72bc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f72bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f72bc-107">*ppib* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f72bc-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f72bc-108">Typ: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="f72bc-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="f72bc-109">Zeiger auf den Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="f72bc-109">Pointer to the index buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f72bc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f72bc-110">Return value</span></span>

<span data-ttu-id="f72bc-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f72bc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f72bc-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f72bc-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f72bc-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="f72bc-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f72bc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f72bc-114">Remarks</span></span>

<span data-ttu-id="f72bc-115">Der Index Puffer enthält die Scheitelpunkt Reihenfolge im Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="f72bc-115">The index buffer contains the vertex ordering in the vertex buffer.</span></span> <span data-ttu-id="f72bc-116">Der Index Puffer wird für den Zugriff auf den Scheitelpunkt Puffer verwendet, wenn das Mesh gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="f72bc-116">The index buffer is used to access the vertex buffer when the mesh is rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="f72bc-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f72bc-117">Requirements</span></span>



| <span data-ttu-id="f72bc-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f72bc-118">Requirement</span></span> | <span data-ttu-id="f72bc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f72bc-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f72bc-120">Header</span><span class="sxs-lookup"><span data-stu-id="f72bc-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f72bc-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f72bc-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f72bc-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f72bc-122">Library</span></span><br/> | <dl> <span data-ttu-id="f72bc-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f72bc-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f72bc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f72bc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72bc-125">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="f72bc-125">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
