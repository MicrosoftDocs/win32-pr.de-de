---
description: Sperrt einen Scheitelpunkt Puffer und erhält einen Zeiger auf den Vertex-Pufferspeicher.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'ID3DXBaseMesh:: lockvertexbuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e93e59715d9f262d7693f2bef652f8be63337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357240"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a><span data-ttu-id="4a4f1-103">ID3DXBaseMesh:: lockvertexbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="4a4f1-103">ID3DXBaseMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="4a4f1-104">Sperrt einen Scheitelpunkt Puffer und erhält einen Zeiger auf den Vertex-Pufferspeicher.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-104">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4f1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a4f1-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="4a4f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a4f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a4f1-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4a4f1-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4f1-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a4f1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a4f1-109">Kombination von 0 (null) oder mehreren Sperr Flags, die den Typ der auszuführenden Sperre beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="4a4f1-110">Für diese Methode sind die gültigen Flags:</span><span class="sxs-lookup"><span data-stu-id="4a4f1-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="4a4f1-111">D3DLOCK \_ verwerfen</span><span class="sxs-lookup"><span data-stu-id="4a4f1-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="4a4f1-112">D3DLOCK \_ kein \_ Dirty \_ Update</span><span class="sxs-lookup"><span data-stu-id="4a4f1-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="4a4f1-113">D3DLOCK \_ nosyslock</span><span class="sxs-lookup"><span data-stu-id="4a4f1-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="4a4f1-114">D3DLOCK \_ schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4a4f1-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="4a4f1-115">D3DLOCK \_ noüberschreibung</span><span class="sxs-lookup"><span data-stu-id="4a4f1-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="4a4f1-116">Eine Beschreibung der Flags finden Sie unter [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="4a4f1-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a4f1-117">*ppData* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4a4f1-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4f1-118">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a4f1-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4a4f1-119">VOID- \* Zeiger auf einen Puffer, der die Scheitelpunkt Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-119">VOID\* pointer to a buffer containing the vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a4f1-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a4f1-120">Return value</span></span>

<span data-ttu-id="4a4f1-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4a4f1-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4a4f1-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4a4f1-123">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a4f1-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a4f1-124">Remarks</span></span>

<span data-ttu-id="4a4f1-125">Wenn Sie mit Scheitelpunkt Puffern arbeiten, können Sie mehrere Sperr Aufrufe durchführen. Sie müssen jedoch sicherstellen, dass die Anzahl der Sperr Aufrufe mit der Anzahl der entsperrungs Aufrufe identisch ist.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-125">When working with vertex buffers, you are allowed to make multiple lock calls; however, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="4a4f1-126">Bei drawprimitive-aufrufen gibt es keine ausstehenden Sperr Zähler für einen aktuell festgelegten Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-126">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set vertex buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a4f1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a4f1-127">Requirements</span></span>



| <span data-ttu-id="4a4f1-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a4f1-128">Requirement</span></span> | <span data-ttu-id="4a4f1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4a4f1-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4f1-130">Header</span><span class="sxs-lookup"><span data-stu-id="4a4f1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4a4f1-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a4f1-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4a4f1-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4a4f1-132">Library</span></span><br/> | <dl> <span data-ttu-id="4a4f1-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a4f1-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4a4f1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a4f1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4f1-135">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="4a4f1-135">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
