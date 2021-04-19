---
description: Informationen zu den Eigenschaften eines Anzeigemodus.
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: D3DDISPLAYMODEEX-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5906b6b23cc83e6d2379f0c5923b08b220285708
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373498"
---
# <a name="d3ddisplaymodeex-structure"></a><span data-ttu-id="ba889-103">D3DDISPLAYMODEEX-Struktur</span><span class="sxs-lookup"><span data-stu-id="ba889-103">D3DDISPLAYMODEEX structure</span></span>

<span data-ttu-id="ba889-104">Informationen zu den Eigenschaften eines Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="ba889-104">Information about the properties of a display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba889-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba889-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a><span data-ttu-id="ba889-106">Member</span><span class="sxs-lookup"><span data-stu-id="ba889-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba889-107">**Größe**</span><span class="sxs-lookup"><span data-stu-id="ba889-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="ba889-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba889-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba889-109">Die Größe dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="ba889-109">The size of this structure.</span></span> <span data-ttu-id="ba889-110">Diese sollte immer auf sizeof (D3DDISPLAYMODEEX) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ba889-110">This should always be set to sizeof(D3DDISPLAYMODEEX).</span></span>

</dd> <dt>

<span data-ttu-id="ba889-111">**Width**</span><span class="sxs-lookup"><span data-stu-id="ba889-111">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="ba889-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba889-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba889-113">Breite des Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="ba889-113">Width of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="ba889-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="ba889-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="ba889-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba889-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba889-116">Die Höhe des Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="ba889-116">Height of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="ba889-117">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="ba889-117">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="ba889-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba889-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba889-119">Aktualisierungsrate des Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="ba889-119">Refresh rate of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="ba889-120">**Format**</span><span class="sxs-lookup"><span data-stu-id="ba889-120">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="ba889-121">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ba889-121">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba889-122">Das Format des Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="ba889-122">Format of the display mode.</span></span> <span data-ttu-id="ba889-123">Siehe [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="ba889-123">See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba889-124">**Scanlineorder**</span><span class="sxs-lookup"><span data-stu-id="ba889-124">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="ba889-125">Typ: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="ba889-125">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba889-126">Gibt an, ob die Scanline-Reihenfolge progressiv oder mit Zeilen Sprung ist.</span><span class="sxs-lookup"><span data-stu-id="ba889-126">Indicates whether the scanline order is progressive or interlaced.</span></span> <span data-ttu-id="ba889-127">Siehe [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="ba889-127">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba889-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba889-128">Remarks</span></span>

<span data-ttu-id="ba889-129">Diese Struktur wird in verschiedenen Methoden verwendet, um Direct3D 9Ex-Geräte ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) und SwapChain ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)) zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ba889-129">This structure is used in various methods to create and manage Direct3D 9Ex devices ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) and swapchains ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba889-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba889-130">Requirements</span></span>



| <span data-ttu-id="ba889-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba889-131">Requirement</span></span> | <span data-ttu-id="ba889-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ba889-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba889-133">Header</span><span class="sxs-lookup"><span data-stu-id="ba889-133">Header</span></span><br/> | <dl> <span data-ttu-id="ba889-134"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba889-134"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba889-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba889-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba889-136">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ba889-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
