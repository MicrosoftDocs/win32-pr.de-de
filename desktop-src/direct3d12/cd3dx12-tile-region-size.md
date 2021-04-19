---
title: CD3DX12_TILE_REGION_SIZE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Tile- \_ Regions \_ Größen Struktur zu ermöglichen.
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- CD3DX12_TILE_REGION_SIZE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353701"
---
# <a name="cd3dx12_tile_region_size-structure"></a><span data-ttu-id="abab6-104">Struktur der CD3DX12- \_ Kachel \_ Regions \_ Größe</span><span class="sxs-lookup"><span data-stu-id="abab6-104">CD3DX12\_TILE\_REGION\_SIZE structure</span></span>

<span data-ttu-id="abab6-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Tile- \_ Regions \_ Größen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="abab6-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="abab6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="abab6-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a><span data-ttu-id="abab6-107">Member</span><span class="sxs-lookup"><span data-stu-id="abab6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="abab6-108">**CD3DX12 \_ Tile- \_ Regions \_ Größe ()**</span><span class="sxs-lookup"><span data-stu-id="abab6-108">**CD3DX12\_TILE\_REGION\_SIZE()**</span></span>
</dt> <dd>

<span data-ttu-id="abab6-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Kachel \_ Bereichs \_ Größe.</span><span class="sxs-lookup"><span data-stu-id="abab6-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_REGION\_SIZE.</span></span>

</dd> <dt>

<span data-ttu-id="abab6-110">**explizite CD3DX12- \_ Kachel \_ Regions \_ Größe (konstant D3D12 \_ Kachel \_ Regions \_ Größe &o)**</span><span class="sxs-lookup"><span data-stu-id="abab6-110">**explicit CD3DX12\_TILE\_REGION\_SIZE(const D3D12\_TILE\_REGION\_SIZE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="abab6-111">Erstellt eine neue Instanz einer CD3DX12- \_ Kachel \_ Regions \_ Größe, die mit dem Inhalt einer anderen [**D3D12 \_ Tile- \_ Regions \_ Größen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="abab6-111">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initialized with the contents of another [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

</dd> <dt>

<span data-ttu-id="abab6-112">**CD3DX12 \_ Tile \_ Regions \_ size (uint numtiles, bool usebox, uint Width, UInt16 Height, UInt16 Tiefe)**</span><span class="sxs-lookup"><span data-stu-id="abab6-112">**CD3DX12\_TILE\_REGION\_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth)**</span></span>
</dt> <dd>

<span data-ttu-id="abab6-113">Erstellt eine neue Instanz einer CD3DX12- \_ Kachel \_ Regions \_ Größe und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="abab6-113">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initializing the following parameters:</span></span>

<span data-ttu-id="abab6-114">Uint-numtiles</span><span class="sxs-lookup"><span data-stu-id="abab6-114">UINT numTiles</span></span>

<span data-ttu-id="abab6-115">Boolesche usebox</span><span class="sxs-lookup"><span data-stu-id="abab6-115">BOOL useBox</span></span>

<span data-ttu-id="abab6-116">Uint-Breite</span><span class="sxs-lookup"><span data-stu-id="abab6-116">UINT width</span></span>

<span data-ttu-id="abab6-117">UInt16-Höhe</span><span class="sxs-lookup"><span data-stu-id="abab6-117">UINT16 height</span></span>

<span data-ttu-id="abab6-118">UInt16 Tiefe</span><span class="sxs-lookup"><span data-stu-id="abab6-118">UINT16 depth</span></span>

</dd> <dt>

<span data-ttu-id="abab6-119">**Operator Konstanten D3D12 \_ Kachel \_ Regions \_ Größe& () konstant**</span><span class="sxs-lookup"><span data-stu-id="abab6-119">**operator const D3D12\_TILE\_REGION\_SIZE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="abab6-120">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="abab6-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abab6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abab6-121">Requirements</span></span>



| <span data-ttu-id="abab6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abab6-122">Requirement</span></span> | <span data-ttu-id="abab6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="abab6-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="abab6-124">Header</span><span class="sxs-lookup"><span data-stu-id="abab6-124">Header</span></span><br/> | <dl> <span data-ttu-id="abab6-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="abab6-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abab6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abab6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abab6-127">**D3D12 \_ Tile- \_ Regions \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="abab6-127">**D3D12\_TILE\_REGION\_SIZE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[<span data-ttu-id="abab6-128">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="abab6-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





