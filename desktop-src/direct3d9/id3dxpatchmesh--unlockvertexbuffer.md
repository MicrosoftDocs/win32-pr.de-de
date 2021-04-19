---
description: Entsperren Sie den Vertex-Puffer.
ms.assetid: 98b82fd1-56e8-45f3-bf26-a1e3b54c2979
title: 'ID3DXPatchMesh:: unlockvertexbuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6d4b6a55281048b303733e1addf2ab4636f74ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355846"
---
# <a name="id3dxpatchmeshunlockvertexbuffer-method"></a><span data-ttu-id="50baf-103">ID3DXPatchMesh:: unlockvertexbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="50baf-103">ID3DXPatchMesh::UnlockVertexBuffer method</span></span>

<span data-ttu-id="50baf-104">Entsperren Sie den Vertex-Puffer.</span><span class="sxs-lookup"><span data-stu-id="50baf-104">Unlock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="50baf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50baf-105">Syntax</span></span>


```C++
HRESULT UnlockVertexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="50baf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50baf-106">Parameters</span></span>

<span data-ttu-id="50baf-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="50baf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50baf-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50baf-108">Return value</span></span>

<span data-ttu-id="50baf-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="50baf-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="50baf-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="50baf-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="50baf-111">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="50baf-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="50baf-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50baf-112">Remarks</span></span>

<span data-ttu-id="50baf-113">Der Vertex-Puffer ist in der Regel gesperrt, in geschrieben und dann zum Lesen entsperrt.</span><span class="sxs-lookup"><span data-stu-id="50baf-113">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="50baf-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50baf-114">Requirements</span></span>



| <span data-ttu-id="50baf-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50baf-115">Requirement</span></span> | <span data-ttu-id="50baf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="50baf-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50baf-117">Header</span><span class="sxs-lookup"><span data-stu-id="50baf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="50baf-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="50baf-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="50baf-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="50baf-119">Library</span></span><br/> | <dl> <span data-ttu-id="50baf-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50baf-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50baf-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50baf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50baf-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="50baf-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




