---
description: Sperrt einen Index Puffer und erhält einen Zeiger auf den Speicher des Index Puffers.
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: 'ID3DXBaseMesh:: LockIndexBuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 388915d0d11ff910c19a2c70b305597a79cd04bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050832"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a><span data-ttu-id="67669-103">ID3DXBaseMesh:: LockIndexBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="67669-103">ID3DXBaseMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="67669-104">Sperrt einen Index Puffer und erhält einen Zeiger auf den Speicher des Index Puffers.</span><span class="sxs-lookup"><span data-stu-id="67669-104">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="67669-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="67669-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="67669-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="67669-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67669-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="67669-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67669-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67669-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67669-109">Kombination von 0 (null) oder mehreren Sperr Flags, die den Typ der auszuführenden Sperre beschreiben.</span><span class="sxs-lookup"><span data-stu-id="67669-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="67669-110">Für diese Methode sind die gültigen Flags:</span><span class="sxs-lookup"><span data-stu-id="67669-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="67669-111">D3DLOCK \_ verwerfen</span><span class="sxs-lookup"><span data-stu-id="67669-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="67669-112">D3DLOCK \_ kein \_ Dirty \_ Update</span><span class="sxs-lookup"><span data-stu-id="67669-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="67669-113">D3DLOCK \_ nosyslock</span><span class="sxs-lookup"><span data-stu-id="67669-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="67669-114">D3DLOCK \_ schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67669-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="67669-115">Eine Beschreibung der Flags finden Sie unter [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="67669-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="67669-116">*ppData* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="67669-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="67669-117">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="67669-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="67669-118">VOID- \* Zeiger auf einen Puffer, der die Indexdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="67669-118">VOID\* pointer to a buffer containing the index data.</span></span> <span data-ttu-id="67669-119">Die Anzahl der Indizes in diesem Puffer ist gleich [**ID3DXBaseMesh:: getnumgesichter**](id3dxbasemesh--getnumfaces.md) \* 3.</span><span class="sxs-lookup"><span data-stu-id="67669-119">The count of indices in this buffer will be equal to [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67669-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67669-120">Return value</span></span>

<span data-ttu-id="67669-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="67669-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="67669-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="67669-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="67669-123">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="67669-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="67669-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67669-124">Remarks</span></span>

<span data-ttu-id="67669-125">Beim Arbeiten mit Index Puffern können Sie mehrere Sperr Aufrufe durchführen.</span><span class="sxs-lookup"><span data-stu-id="67669-125">When working with index buffers, you are allowed to make multiple lock calls.</span></span> <span data-ttu-id="67669-126">Sie müssen jedoch sicherstellen, dass die Anzahl der Sperr Aufrufe mit der Anzahl der entsperrungs Aufrufe identisch ist.</span><span class="sxs-lookup"><span data-stu-id="67669-126">However, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="67669-127">Drawprimitive-Aufrufe können nicht mit einer ausstehenden Sperr Anzahl für einen aktuell festgelegten Index Puffer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="67669-127">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set index buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="67669-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67669-128">Requirements</span></span>



| <span data-ttu-id="67669-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67669-129">Requirement</span></span> | <span data-ttu-id="67669-130">Wert</span><span class="sxs-lookup"><span data-stu-id="67669-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67669-131">Header</span><span class="sxs-lookup"><span data-stu-id="67669-131">Header</span></span><br/>  | <dl> <span data-ttu-id="67669-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="67669-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="67669-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="67669-133">Library</span></span><br/> | <dl> <span data-ttu-id="67669-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67669-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="67669-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67669-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67669-136">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="67669-136">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
