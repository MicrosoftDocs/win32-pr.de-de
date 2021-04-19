---
description: Sperrt den Attribut Puffer.
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: 'ID3DXPatchMesh:: LockAttributeBuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71e50fdc27f3f50b560324c74f5a1609f900772d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367502"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a><span data-ttu-id="80355-103">ID3DXPatchMesh:: LockAttributeBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="80355-103">ID3DXPatchMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="80355-104">Sperrt den Attribut Puffer.</span><span class="sxs-lookup"><span data-stu-id="80355-104">Locks the attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="80355-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="80355-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]          DWORD flags,
  [out, retval] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="80355-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="80355-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80355-107">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80355-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80355-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80355-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80355-109">Kombination von 0 (null) oder mehreren Sperr Flags, die den Typ der auszuführenden Sperre beschreiben.</span><span class="sxs-lookup"><span data-stu-id="80355-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="80355-110">Für diese Methode sind die gültigen Flags:</span><span class="sxs-lookup"><span data-stu-id="80355-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="80355-111">D3DLOCK \_ verwerfen</span><span class="sxs-lookup"><span data-stu-id="80355-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="80355-112">D3DLOCK \_ kein \_ Dirty \_ Update</span><span class="sxs-lookup"><span data-stu-id="80355-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="80355-113">D3DLOCK \_ nosyslock</span><span class="sxs-lookup"><span data-stu-id="80355-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="80355-114">D3DLOCK \_ schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80355-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="80355-115">Eine Beschreibung der Flags finden Sie unter [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="80355-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="80355-116">*ppData* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="80355-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="80355-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="80355-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="80355-118">Adresse eines Zeigers auf einen Puffer, der ein DWORD für jedes Gesicht im Mesh enthält.</span><span class="sxs-lookup"><span data-stu-id="80355-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80355-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80355-119">Return value</span></span>

<span data-ttu-id="80355-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80355-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80355-121">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80355-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="80355-122">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="80355-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="80355-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80355-123">Remarks</span></span>

<span data-ttu-id="80355-124">Der Attribut Puffer ist in der Regel gesperrt, in geschrieben und dann zum Lesen entsperrt.</span><span class="sxs-lookup"><span data-stu-id="80355-124">The attribute buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="80355-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80355-125">Requirements</span></span>



| <span data-ttu-id="80355-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80355-126">Requirement</span></span> | <span data-ttu-id="80355-127">Wert</span><span class="sxs-lookup"><span data-stu-id="80355-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80355-128">Header</span><span class="sxs-lookup"><span data-stu-id="80355-128">Header</span></span><br/>  | <dl> <span data-ttu-id="80355-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="80355-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="80355-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="80355-130">Library</span></span><br/> | <dl> <span data-ttu-id="80355-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80355-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80355-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80355-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80355-133">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="80355-133">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
