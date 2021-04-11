---
description: Diese Schnittstelle wird von der Anwendung implementiert, um Frame-und Mesh-Containerobjekte zuzuordnen oder freizugeben. Methoden für diese werden beim Laden und zerstören von Frame Hierarchien aufgerufen.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: ID3DXAllocateHierarchy-Schnittstelle (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050926"
---
# <a name="id3dxallocatehierarchy-interface"></a><span data-ttu-id="1776f-104">ID3DXAllocateHierarchy-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1776f-104">ID3DXAllocateHierarchy interface</span></span>

<span data-ttu-id="1776f-105">Diese Schnittstelle wird von der Anwendung implementiert, um Frame-und Mesh-Containerobjekte zuzuordnen oder freizugeben.</span><span class="sxs-lookup"><span data-stu-id="1776f-105">This interface is implemented by the application to allocate or free frame and mesh container objects.</span></span> <span data-ttu-id="1776f-106">Methoden für diese werden beim Laden und zerstören von Frame Hierarchien aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1776f-106">Methods on this are called during loading and destroying frame hierarchies.</span></span>

## <a name="members"></a><span data-ttu-id="1776f-107">Member</span><span class="sxs-lookup"><span data-stu-id="1776f-107">Members</span></span>

<span data-ttu-id="1776f-108">Die **ID3DXAllocateHierarchy** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1776f-108">The **ID3DXAllocateHierarchy** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1776f-109">**ID3DXAllocateHierarchy** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1776f-109">**ID3DXAllocateHierarchy** also has these types of members:</span></span>

-   [<span data-ttu-id="1776f-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="1776f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1776f-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="1776f-111">Methods</span></span>

<span data-ttu-id="1776f-112">Die **ID3DXAllocateHierarchy** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1776f-112">The **ID3DXAllocateHierarchy** interface has these methods.</span></span>



| <span data-ttu-id="1776f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="1776f-113">Method</span></span>                                                                       | <span data-ttu-id="1776f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1776f-114">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="1776f-115">**CreateFrame**</span><span class="sxs-lookup"><span data-stu-id="1776f-115">**CreateFrame**</span></span>](id3dxallocatehierarchy--createframe.md)                   | <span data-ttu-id="1776f-116">Fordert die Zuordnung eines Frame Objekts an.</span><span class="sxs-lookup"><span data-stu-id="1776f-116">Requests allocation of a frame object.</span></span><br/>            |
| [<span data-ttu-id="1776f-117">**"Kreatemeschcontainer"**</span><span class="sxs-lookup"><span data-stu-id="1776f-117">**CreateMeshContainer**</span></span>](id3dxallocatehierarchy--createmeshcontainer.md)   | <span data-ttu-id="1776f-118">Fordert die Zuordnung eines Mesh-Container Objekts an.</span><span class="sxs-lookup"><span data-stu-id="1776f-118">Requests allocation of a mesh container object.</span></span><br/>   |
| [<span data-ttu-id="1776f-119">**Destroyframe**</span><span class="sxs-lookup"><span data-stu-id="1776f-119">**DestroyFrame**</span></span>](id3dxallocatehierarchy--destroyframe.md)                 | <span data-ttu-id="1776f-120">Fordert die Aufhebung der Zuordnung eines Frame Objekts an.</span><span class="sxs-lookup"><span data-stu-id="1776f-120">Requests deallocation of a frame object.</span></span><br/>          |
| [<span data-ttu-id="1776f-121">**Destroymeschcontainer**</span><span class="sxs-lookup"><span data-stu-id="1776f-121">**DestroyMeshContainer**</span></span>](id3dxallocatehierarchy--destroymeshcontainer.md) | <span data-ttu-id="1776f-122">Fordert die Aufhebung der Zuordnung eines Mesh-Container Objekts an.</span><span class="sxs-lookup"><span data-stu-id="1776f-122">Requests deallocation of a mesh container object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1776f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1776f-123">Remarks</span></span>

<span data-ttu-id="1776f-124">Der LPD3DXALLOCATEHIERARCHY-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="1776f-124">The LPD3DXALLOCATEHIERARCHY type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a><span data-ttu-id="1776f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1776f-125">Requirements</span></span>



| <span data-ttu-id="1776f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1776f-126">Requirement</span></span> | <span data-ttu-id="1776f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1776f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1776f-128">Header</span><span class="sxs-lookup"><span data-stu-id="1776f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1776f-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1776f-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1776f-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1776f-130">Library</span></span><br/> | <dl> <span data-ttu-id="1776f-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1776f-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1776f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1776f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1776f-133">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1776f-133">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
