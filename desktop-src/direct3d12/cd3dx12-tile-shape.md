---
title: CD3DX12_TILE_SHAPE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ Kachel \_ Form Struktur zu ermöglichen.
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- CD3DX12_TILE_SHAPE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998a14e1bd4898d83d049ea50bc056abaeb68544
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365288"
---
# <a name="cd3dx12_tile_shape-structure"></a><span data-ttu-id="342a6-104">CD3DX12 \_ Tile- \_ Shape-Struktur</span><span class="sxs-lookup"><span data-stu-id="342a6-104">CD3DX12\_TILE\_SHAPE structure</span></span>

<span data-ttu-id="342a6-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Kachel \_ Form**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="342a6-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="342a6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="342a6-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a><span data-ttu-id="342a6-107">Member</span><span class="sxs-lookup"><span data-stu-id="342a6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="342a6-108">**CD3DX12- \_ Kachel \_ Form ()**</span><span class="sxs-lookup"><span data-stu-id="342a6-108">**CD3DX12\_TILE\_SHAPE()**</span></span>
</dt> <dd>

<span data-ttu-id="342a6-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Kachel \_ Form.</span><span class="sxs-lookup"><span data-stu-id="342a6-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_SHAPE.</span></span>

</dd> <dt>

<span data-ttu-id="342a6-110">**explizite CD3DX12- \_ Kachel \_ Form (konstant D3D12 \_ Kachel \_ Form &o)**</span><span class="sxs-lookup"><span data-stu-id="342a6-110">**explicit CD3DX12\_TILE\_SHAPE(const D3D12\_TILE\_SHAPE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="342a6-111">Erstellt eine neue Instanz einer CD3DX12- \_ Kachel \_ Form, die mit dem Inhalt einer anderen [**D3D12- \_ Kachel \_ Form**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="342a6-111">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initialized with the contents of another [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

</dd> <dt>

<span data-ttu-id="342a6-112">**CD3DX12 \_ Tile- \_ Form (uint widthintexels, uint heightintexels, uint depthintexels)**</span><span class="sxs-lookup"><span data-stu-id="342a6-112">**CD3DX12\_TILE\_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels)**</span></span>
</dt> <dd>

<span data-ttu-id="342a6-113">Erstellt eine neue Instanz einer CD3DX12- \_ Kachel \_ Form und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="342a6-113">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initializing the following parameters:</span></span>

<span data-ttu-id="342a6-114">Uint widthintexels</span><span class="sxs-lookup"><span data-stu-id="342a6-114">UINT widthInTexels</span></span>

<span data-ttu-id="342a6-115">Uint-heightintexels</span><span class="sxs-lookup"><span data-stu-id="342a6-115">UINT heightInTexels</span></span>

<span data-ttu-id="342a6-116">Uint depthintexels</span><span class="sxs-lookup"><span data-stu-id="342a6-116">UINT depthInTexels</span></span>

</dd> <dt>

<span data-ttu-id="342a6-117">**Operator Konstanten D3D12 \_ Kachel \_ Form& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="342a6-117">**operator const D3D12\_TILE\_SHAPE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="342a6-118">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="342a6-118">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="342a6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="342a6-119">Requirements</span></span>



| <span data-ttu-id="342a6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="342a6-120">Requirement</span></span> | <span data-ttu-id="342a6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="342a6-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="342a6-122">Header</span><span class="sxs-lookup"><span data-stu-id="342a6-122">Header</span></span><br/> | <dl> <span data-ttu-id="342a6-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="342a6-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="342a6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="342a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="342a6-125">**D3D12- \_ Kachel \_ Form**</span><span class="sxs-lookup"><span data-stu-id="342a6-125">**D3D12\_TILE\_SHAPE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[<span data-ttu-id="342a6-126">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="342a6-126">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





