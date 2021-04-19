---
title: CD3DX12_PACKED_MIP_INFO-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ gepackten \_ MIP Info-Struktur zu ermöglichen \_ .
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- CD3DX12_PACKED_MIP_INFO Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357223"
---
# <a name="cd3dx12_packed_mip_info-structure"></a><span data-ttu-id="e7138-104">CD3DX12- \_ gepackte \_ MIP- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="e7138-104">CD3DX12\_PACKED\_MIP\_INFO structure</span></span>

<span data-ttu-id="e7138-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ gepackten \_ MIP \_ Info**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e7138-105">A helper structure to enable easy initialization of a [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7138-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7138-106">Syntax</span></span>


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="e7138-107">Member</span><span class="sxs-lookup"><span data-stu-id="e7138-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e7138-108">**CD3DX12- \_ gepackte \_ MIP- \_ Informationen ()**</span><span class="sxs-lookup"><span data-stu-id="e7138-108">**CD3DX12\_PACKED\_MIP\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="e7138-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ gepackten \_ MIP- \_ Info.</span><span class="sxs-lookup"><span data-stu-id="e7138-109">Creates a new, uninitialized, instance of a CD3DX12\_PACKED\_MIP\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="e7138-110">**explizites CD3DX12 \_ gepackte \_ MIP- \_ Informationen (konstant D3D12 \_ gepackte \_ MIP \_ Info &o)**</span><span class="sxs-lookup"><span data-stu-id="e7138-110">**explicit CD3DX12\_PACKED\_MIP\_INFO(const D3D12\_PACKED\_MIP\_INFO &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e7138-111">Erstellt eine neue Instanz einer CD3DX12- \_ gepackten \_ MIP- \_ Info, die mit dem Inhalt einer anderen [**D3D12- \_ gepackten \_ MIP \_ Info**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e7138-111">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initialized with the contents of another [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e7138-112">**CD3DX12- \_ gepackte \_ MIP- \_ Informationen (Uint8 numstandardmips, Uint8 numpackedmips, uint numtilesforpackedmips, uint starttileindexinoverallresource)**</span><span class="sxs-lookup"><span data-stu-id="e7138-112">**CD3DX12\_PACKED\_MIP\_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="e7138-113">Erstellt eine neue Instanz einer CD3DX12- \_ gepackten \_ MIP- \_ Info und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="e7138-113">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="e7138-114">Uint8 numstandardmips</span><span class="sxs-lookup"><span data-stu-id="e7138-114">UINT8 numStandardMips</span></span>

<span data-ttu-id="e7138-115">Uint8 numpackedmips</span><span class="sxs-lookup"><span data-stu-id="e7138-115">UINT8 numPackedMips</span></span>

<span data-ttu-id="e7138-116">Uint numtilesforpackedmips</span><span class="sxs-lookup"><span data-stu-id="e7138-116">UINT numTilesForPackedMips</span></span>

<span data-ttu-id="e7138-117">Uint starttileingede xinoverallresource</span><span class="sxs-lookup"><span data-stu-id="e7138-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="e7138-118">**Operator konstant D3D12 \_ gepackte \_ MIP- \_ Info& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="e7138-118">**operator const D3D12\_PACKED\_MIP\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="e7138-119">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="e7138-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7138-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7138-120">Requirements</span></span>



| <span data-ttu-id="e7138-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7138-121">Requirement</span></span> | <span data-ttu-id="e7138-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e7138-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e7138-123">Header</span><span class="sxs-lookup"><span data-stu-id="e7138-123">Header</span></span><br/> | <dl> <span data-ttu-id="e7138-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7138-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7138-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7138-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7138-126">**D3D12- \_ gepackte \_ MIP- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="e7138-126">**D3D12\_PACKED\_MIP\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[<span data-ttu-id="e7138-127">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="e7138-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





