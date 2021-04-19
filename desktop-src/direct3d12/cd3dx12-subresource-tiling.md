---
title: CD3DX12_SUBRESOURCE_TILING-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-unter Berichts- \_ \_ Tick-Struktur zu ermöglichen.
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- CD3DX12_SUBRESOURCE_TILING Struktur
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364346"
---
# <a name="cd3dx12_subresource_tiling-structure"></a><span data-ttu-id="cc74b-104">CD3DX12-Struktur für unter \_ geordnete Elemente \_</span><span class="sxs-lookup"><span data-stu-id="cc74b-104">CD3DX12\_SUBRESOURCE\_TILING structure</span></span>

<span data-ttu-id="cc74b-105">Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-unter Berichts- [**\_ \_ Tick**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cc74b-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc74b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc74b-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a><span data-ttu-id="cc74b-107">Member</span><span class="sxs-lookup"><span data-stu-id="cc74b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc74b-108">**CD3DX12 \_ subresource- \_ tiult ()**</span><span class="sxs-lookup"><span data-stu-id="cc74b-108">**CD3DX12\_SUBRESOURCE\_TILING()**</span></span>
</dt> <dd>

<span data-ttu-id="cc74b-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ subresource- \_ Tick.</span><span class="sxs-lookup"><span data-stu-id="cc74b-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_TILING.</span></span>

</dd> <dt>

<span data-ttu-id="cc74b-110">**explizite CD3DX12 \_ subresource- \_ tiult (Konstanten D3D12 \_ subresource- \_ tiult &o)**</span><span class="sxs-lookup"><span data-stu-id="cc74b-110">**explicit CD3DX12\_SUBRESOURCE\_TILING(const D3D12\_SUBRESOURCE\_TILING &o)**</span></span>
</dt> <dd>

<span data-ttu-id="cc74b-111">Erstellt eine neue Instanz einer CD3DX12-untergeordneten \_ Quelle \_ , die mit dem Inhalt einer anderen [**D3D12 \_ subresource- \_ tilinger**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="cc74b-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initialized with the contents of another [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc74b-112">**CD3DX12 \_ subresource \_ tiult (uint widthintiles, UInt16 uptintiles, UInt16 depthintiles, uint starttileindexinoverallresource)**</span><span class="sxs-lookup"><span data-stu-id="cc74b-112">**CD3DX12\_SUBRESOURCE\_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="cc74b-113">Erstellt eine neue Instanz einer CD3DX12-Unterteilung \_ \_ , wobei die folgenden Parameter initialisiert werden:</span><span class="sxs-lookup"><span data-stu-id="cc74b-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initializing the following parameters:</span></span>

<span data-ttu-id="cc74b-114">Uint widthintiles</span><span class="sxs-lookup"><span data-stu-id="cc74b-114">UINT widthInTiles</span></span>

<span data-ttu-id="cc74b-115">UInt16-Höhen Kacheln</span><span class="sxs-lookup"><span data-stu-id="cc74b-115">UINT16 heightInTiles</span></span>

<span data-ttu-id="cc74b-116">UInt16 depthintiles</span><span class="sxs-lookup"><span data-stu-id="cc74b-116">UINT16 depthInTiles</span></span>

<span data-ttu-id="cc74b-117">Uint starttileingede xinoverallresource</span><span class="sxs-lookup"><span data-stu-id="cc74b-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="cc74b-118">**Operator Konstanten D3D12 Unterteilung \_ \_& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="cc74b-118">**operator const D3D12\_SUBRESOURCE\_TILING&() const**</span></span>
</dt> <dd>

<span data-ttu-id="cc74b-119">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="cc74b-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc74b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc74b-120">Requirements</span></span>



| <span data-ttu-id="cc74b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc74b-121">Requirement</span></span> | <span data-ttu-id="cc74b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="cc74b-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc74b-123">Header</span><span class="sxs-lookup"><span data-stu-id="cc74b-123">Header</span></span><br/> | <dl> <span data-ttu-id="cc74b-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc74b-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc74b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc74b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc74b-126">**D3D12-unter \_ geordnete \_ tiult**</span><span class="sxs-lookup"><span data-stu-id="cc74b-126">**D3D12\_SUBRESOURCE\_TILING**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[<span data-ttu-id="cc74b-127">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="cc74b-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





