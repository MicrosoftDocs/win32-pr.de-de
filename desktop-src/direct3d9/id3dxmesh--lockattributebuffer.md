---
description: Sperrt den Gitter Puffer, der die Daten des Mesh-Attributs enthält, und gibt einen Zeiger darauf zurück.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'ID3DXMesh:: LockAttributeBuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 901cb98a9d75d08b6412d6fdca841d403064354b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370410"
---
# <a name="id3dxmeshlockattributebuffer-method"></a><span data-ttu-id="af49d-103">ID3DXMesh:: LockAttributeBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="af49d-103">ID3DXMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="af49d-104">Sperrt den Gitter Puffer, der die Daten des Mesh-Attributs enthält, und gibt einen Zeiger darauf zurück.</span><span class="sxs-lookup"><span data-stu-id="af49d-104">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="af49d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="af49d-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="af49d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="af49d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af49d-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="af49d-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af49d-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af49d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af49d-109">Kombination von 0 (null) oder mehreren Sperr Flags, die den Typ der auszuführenden Sperre beschreiben.</span><span class="sxs-lookup"><span data-stu-id="af49d-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="af49d-110">Für diese Methode sind die gültigen Flags:</span><span class="sxs-lookup"><span data-stu-id="af49d-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="af49d-111">D3DLOCK \_ verwerfen</span><span class="sxs-lookup"><span data-stu-id="af49d-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="af49d-112">D3DLOCK \_ kein \_ Dirty \_ Update</span><span class="sxs-lookup"><span data-stu-id="af49d-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="af49d-113">D3DLOCK \_ nosyslock</span><span class="sxs-lookup"><span data-stu-id="af49d-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="af49d-114">D3DLOCK \_ schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af49d-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="af49d-115">Eine Beschreibung der Flags finden Sie unter [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="af49d-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="af49d-116">*ppData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="af49d-116">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af49d-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="af49d-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="af49d-118">Adresse eines Zeigers auf einen Puffer, der ein DWORD für jedes Gesicht im Mesh enthält.</span><span class="sxs-lookup"><span data-stu-id="af49d-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af49d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af49d-119">Return value</span></span>

<span data-ttu-id="af49d-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af49d-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af49d-121">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af49d-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="af49d-122">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="af49d-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="af49d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af49d-123">Remarks</span></span>

<span data-ttu-id="af49d-124">Wenn [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md) aufgerufen wurde, verfügt das Mesh auch über eine Attribut Tabelle, auf die mithilfe der [**ID3DXBaseMesh:: GetAttributeTable**](id3dxbasemesh--getattributetable.md) -Methode zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="af49d-124">If [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) has been called, the mesh will also have an attribute table that can be accessed using the [**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="af49d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af49d-125">Requirements</span></span>



| <span data-ttu-id="af49d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af49d-126">Requirement</span></span> | <span data-ttu-id="af49d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="af49d-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af49d-128">Header</span><span class="sxs-lookup"><span data-stu-id="af49d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="af49d-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="af49d-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="af49d-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="af49d-130">Library</span></span><br/> | <dl> <span data-ttu-id="af49d-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af49d-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af49d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af49d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af49d-133">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="af49d-133">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="af49d-134">**ID3DXMesh:: UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="af49d-134">**ID3DXMesh::UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="af49d-135">**ID3DXBaseMesh:: GetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="af49d-135">**ID3DXBaseMesh::GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[<span data-ttu-id="af49d-136">**ID3DXMesh:: Einstellungs Tabelle**</span><span class="sxs-lookup"><span data-stu-id="af49d-136">**ID3DXMesh::SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
