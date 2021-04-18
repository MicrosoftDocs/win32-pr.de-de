---
title: CD3DX12_SUBRESOURCE_RANGE_UINT64-Struktur (D3dx12. h)
description: Eine hilfsstruktur, mit der die einfache Initialisierung einer D3D12-unter \_ \_ Bereichs UINT64-Struktur aktiviert werden kann \_ .
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- CD3DX12_SUBRESOURCE_RANGE_UINT64 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351927"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a><span data-ttu-id="71dec-104">CD3DX12 \_ subresource- \_ Bereich \_ UINT64 Struktur</span><span class="sxs-lookup"><span data-stu-id="71dec-104">CD3DX12\_SUBRESOURCE\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="71dec-105">Eine hilfsstruktur, mit der die einfache Initialisierung einer D3D12-unter [**\_ \_ Bereichs \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) -Struktur aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="71dec-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="71dec-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="71dec-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="71dec-107">Member</span><span class="sxs-lookup"><span data-stu-id="71dec-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="71dec-108">**CD3DX12 \_ subresource- \_ Bereich \_ UINT64 ()**</span><span class="sxs-lookup"><span data-stu-id="71dec-108">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="71dec-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ subresource- \_ Bereichs \_ UINT64.</span><span class="sxs-lookup"><span data-stu-id="71dec-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="71dec-110">**expliziter CD3DX12-unter \_ \_ Bereichs Bereich \_ UINT64 (konstant D3D12 unter \_ \_ Bereichs Quelle \_ UINT64 &o)**</span><span class="sxs-lookup"><span data-stu-id="71dec-110">**explicit CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(const D3D12\_SUBRESOURCE\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="71dec-111">Erstellt eine neue Instanz eines CD3DX12 \_ subresource- \_ Bereichs \_ UINT64, initialisiert mit Werten, die aus einem D3D12-unter [**\_ \_ Bereich \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) -Struktur kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="71dec-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="71dec-112">**CD3DX12 \_ subresource \_ Range \_ UINT64 (uint subresource, Konstanten D3D12 \_ Range \_ UINT64& Range)**</span><span class="sxs-lookup"><span data-stu-id="71dec-112">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, const D3D12\_RANGE\_UINT64& range)**</span></span>
</dt> <dd>

<span data-ttu-id="71dec-113">Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit den in der Parameterliste übergebenen Werten initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="71dec-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="71dec-114">**CD3DX12 \_ subresource \_ Range \_ UINT64 (uint subresource, UINT64 BEGIN, UINT64 End)**</span><span class="sxs-lookup"><span data-stu-id="71dec-114">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="71dec-115">Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit den in der Parameterliste übergebenen Werten initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="71dec-115">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="71dec-116">**Operator Konstanten D3D12 \_ subresource- \_ Bereich \_ UINT64& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="71dec-116">**operator const D3D12\_SUBRESOURCE\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="71dec-117">Implizite Konvertierung in eine D3D12 \_ subresource \_ Range \_ UINT64-Struktur.</span><span class="sxs-lookup"><span data-stu-id="71dec-117">Implicit conversion to a D3D12\_SUBRESOURCE\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="71dec-118">Da D3D12 \_ subresource \_ Range \_ UINT64 der zugrunde liegende Typ von CD3DX12 \_ subresource \_ Range \_ UINT64 ist, wird das Objekt einfach als Konstante D3D12-tiefen Schablone zurückgegeben, \_ \_ \_ DESC1 Verweis auf sich selbst.</span><span class="sxs-lookup"><span data-stu-id="71dec-118">Because D3D12\_SUBRESOURCE\_RANGE\_UINT64 is the underlying type of CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71dec-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71dec-119">Requirements</span></span>



| <span data-ttu-id="71dec-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71dec-120">Requirement</span></span> | <span data-ttu-id="71dec-121">Wert</span><span class="sxs-lookup"><span data-stu-id="71dec-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="71dec-122">Header</span><span class="sxs-lookup"><span data-stu-id="71dec-122">Header</span></span><br/> | <dl> <span data-ttu-id="71dec-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="71dec-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71dec-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71dec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71dec-125">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="71dec-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="71dec-126">**D3D12 \_ subresource- \_ Bereich \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="71dec-126">**D3D12\_SUBRESOURCE\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





