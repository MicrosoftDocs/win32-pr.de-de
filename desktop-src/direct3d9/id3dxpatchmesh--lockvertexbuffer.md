---
description: Sperren Sie den Scheitelpunkt Puffer.
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: 'ID3DXPatchMesh:: lockvertexbuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d88d8a1da7ae544c5647fc844cda4966cfee7b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870151"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a><span data-ttu-id="3d99f-103">ID3DXPatchMesh:: lockvertexbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="3d99f-103">ID3DXPatchMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="3d99f-104">Sperren Sie den Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="3d99f-104">Lock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d99f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d99f-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="3d99f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d99f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d99f-107">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d99f-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d99f-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d99f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3d99f-109">Kombination von 0 (null) oder mehreren Sperr Flags, die den Typ der auszuführenden Sperre beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3d99f-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="3d99f-110">Für diese Methode sind die gültigen Flags:</span><span class="sxs-lookup"><span data-stu-id="3d99f-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="3d99f-111">D3DLOCK \_ verwerfen</span><span class="sxs-lookup"><span data-stu-id="3d99f-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="3d99f-112">D3DLOCK \_ kein \_ Dirty \_ Update</span><span class="sxs-lookup"><span data-stu-id="3d99f-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="3d99f-113">D3DLOCK \_ nosyslock</span><span class="sxs-lookup"><span data-stu-id="3d99f-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="3d99f-114">D3DLOCK \_ schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3d99f-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="3d99f-115">D3DLOCK \_ noüberschreibung</span><span class="sxs-lookup"><span data-stu-id="3d99f-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="3d99f-116">Eine Beschreibung der Flags finden Sie unter [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="3d99f-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d99f-117">*ppData* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3d99f-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3d99f-118">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d99f-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3d99f-119">VOID- \* Zeiger auf einen Arbeitsspeicher Puffer, der die zurückgegebenen Vertex-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="3d99f-119">VOID\* pointer to a memory buffer containing the returned vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d99f-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d99f-120">Return value</span></span>

<span data-ttu-id="3d99f-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3d99f-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3d99f-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3d99f-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3d99f-123">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="3d99f-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d99f-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d99f-124">Remarks</span></span>

<span data-ttu-id="3d99f-125">Der Vertex-Puffer ist in der Regel gesperrt, in geschrieben und dann zum Lesen entsperrt.</span><span class="sxs-lookup"><span data-stu-id="3d99f-125">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

<span data-ttu-id="3d99f-126">Patchnetze verwenden 16-Bit-Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="3d99f-126">Patch meshes use 16-bit index buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d99f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d99f-127">Requirements</span></span>



| <span data-ttu-id="3d99f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d99f-128">Requirement</span></span> | <span data-ttu-id="3d99f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3d99f-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d99f-130">Header</span><span class="sxs-lookup"><span data-stu-id="3d99f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3d99f-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d99f-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3d99f-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3d99f-132">Library</span></span><br/> | <dl> <span data-ttu-id="3d99f-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d99f-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3d99f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d99f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d99f-135">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="3d99f-135">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
