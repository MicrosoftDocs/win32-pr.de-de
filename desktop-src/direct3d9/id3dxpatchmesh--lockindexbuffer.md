---
description: Sperren Sie den Index Puffer.
ms.assetid: b68aff75-9ba6-4088-b35f-f56d700d1aff
title: 'ID3DXPatchMesh:: LockIndexBuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81dc410262ff21ea972d4c501ac3b5d26a361642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531082"
---
# <a name="id3dxpatchmeshlockindexbuffer-method"></a><span data-ttu-id="6ad95-103">ID3DXPatchMesh:: LockIndexBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="6ad95-103">ID3DXPatchMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="6ad95-104">Sperren Sie den Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="6ad95-104">Lock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad95-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ad95-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="6ad95-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ad95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ad95-107">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ad95-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad95-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ad95-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ad95-109">Kombination von 0 (null) oder mehreren Sperr Flags, die den Typ der auszuführenden Sperre beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6ad95-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="6ad95-110">Für diese Methode sind die gültigen Flags:</span><span class="sxs-lookup"><span data-stu-id="6ad95-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="6ad95-111">D3DLOCK \_ verwerfen</span><span class="sxs-lookup"><span data-stu-id="6ad95-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="6ad95-112">D3DLOCK \_ kein \_ Dirty \_ Update</span><span class="sxs-lookup"><span data-stu-id="6ad95-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="6ad95-113">D3DLOCK \_ nosyslock</span><span class="sxs-lookup"><span data-stu-id="6ad95-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="6ad95-114">D3DLOCK \_ schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ad95-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="6ad95-115">Eine Beschreibung der Flags finden Sie unter [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="6ad95-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ad95-116">*ppData* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6ad95-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad95-117">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ad95-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6ad95-118">VOID- \* Zeiger auf einen Arbeitsspeicher Puffer, der die zurückgegebenen Indexdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="6ad95-118">VOID\* pointer to a memory buffer containing the returned index data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ad95-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ad95-119">Return value</span></span>

<span data-ttu-id="6ad95-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6ad95-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6ad95-121">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ad95-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6ad95-122">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="6ad95-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ad95-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ad95-123">Remarks</span></span>

<span data-ttu-id="6ad95-124">Der Index Puffer ist in der Regel gesperrt, in geschrieben und dann zum Lesen entsperrt.</span><span class="sxs-lookup"><span data-stu-id="6ad95-124">The index buffer is usually locked, written to, and then unlocked for reading.</span></span> <span data-ttu-id="6ad95-125">Patchmesh-Index Puffer sind 16-Bit-Puffer.</span><span class="sxs-lookup"><span data-stu-id="6ad95-125">Patch mesh index buffers are 16-bit buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad95-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ad95-126">Requirements</span></span>



| <span data-ttu-id="6ad95-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ad95-127">Requirement</span></span> | <span data-ttu-id="6ad95-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6ad95-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad95-129">Header</span><span class="sxs-lookup"><span data-stu-id="6ad95-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6ad95-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ad95-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6ad95-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6ad95-131">Library</span></span><br/> | <dl> <span data-ttu-id="6ad95-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ad95-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ad95-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ad95-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad95-134">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="6ad95-134">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="6ad95-135">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="6ad95-135">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
