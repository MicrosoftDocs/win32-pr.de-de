---
description: Entsperren Sie den Index Puffer.
ms.assetid: de3d0893-1596-42df-b049-6574c58ffa8d
title: 'ID3DXPatchMesh:: unlockindexbuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9bae54c6c4477682422328410558f1b405eb2677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363156"
---
# <a name="id3dxpatchmeshunlockindexbuffer-method"></a><span data-ttu-id="862c8-103">ID3DXPatchMesh:: unlockindexbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="862c8-103">ID3DXPatchMesh::UnlockIndexBuffer method</span></span>

<span data-ttu-id="862c8-104">Entsperren Sie den Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="862c8-104">Unlock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="862c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="862c8-105">Syntax</span></span>


```C++
HRESULT UnlockIndexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="862c8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="862c8-106">Parameters</span></span>

<span data-ttu-id="862c8-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="862c8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="862c8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="862c8-108">Return value</span></span>

<span data-ttu-id="862c8-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="862c8-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="862c8-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="862c8-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="862c8-111">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="862c8-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="862c8-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="862c8-112">Remarks</span></span>

<span data-ttu-id="862c8-113">Der Index Puffer ist in der Regel gesperrt, in geschrieben und dann zum Lesen entsperrt.</span><span class="sxs-lookup"><span data-stu-id="862c8-113">The index buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="862c8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="862c8-114">Requirements</span></span>



| <span data-ttu-id="862c8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="862c8-115">Requirement</span></span> | <span data-ttu-id="862c8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="862c8-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="862c8-117">Header</span><span class="sxs-lookup"><span data-stu-id="862c8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="862c8-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="862c8-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="862c8-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="862c8-119">Library</span></span><br/> | <dl> <span data-ttu-id="862c8-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="862c8-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="862c8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="862c8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="862c8-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="862c8-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




