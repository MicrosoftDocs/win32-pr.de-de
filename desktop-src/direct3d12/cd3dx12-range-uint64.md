---
title: CD3DX12_RANGE_UINT64-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Range \_ UINT64-Struktur zu ermöglichen.
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- CD3DX12_RANGE_UINT64 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365344"
---
# <a name="cd3dx12_range_uint64-structure"></a><span data-ttu-id="46e65-104">CD3DX12 \_ Range \_ UINT64-Struktur</span><span class="sxs-lookup"><span data-stu-id="46e65-104">CD3DX12\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="46e65-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Range \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="46e65-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e65-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e65-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="46e65-107">Member</span><span class="sxs-lookup"><span data-stu-id="46e65-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="46e65-108">**CD3DX12 \_ Range \_ UINT64 ()**</span><span class="sxs-lookup"><span data-stu-id="46e65-108">**CD3DX12\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="46e65-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Range \_ UINT64.</span><span class="sxs-lookup"><span data-stu-id="46e65-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="46e65-110">**expliziter CD3DX12 \_ Range \_ UINT64 (konstant D3D12 \_ Bereich \_ UINT64 &o)**</span><span class="sxs-lookup"><span data-stu-id="46e65-110">**explicit CD3DX12\_RANGE\_UINT64(const D3D12\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="46e65-111">Erstellt eine neue Instanz eines CD3DX12 \_ Range \_ UINT64, das mit Werten initialisiert wird, die aus einer [**D3D12 \_ Range \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) -Struktur kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="46e65-111">Creates a new instance of a CD3DX12\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="46e65-112">**CD3DX12 \_ Range \_ UINT64 (UINT64 BEGIN, UINT64 End)**</span><span class="sxs-lookup"><span data-stu-id="46e65-112">**CD3DX12\_RANGE\_UINT64(UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="46e65-113">Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit den in der Parameterliste übergebenen Werten initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="46e65-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="46e65-114">**Operator konstant D3D12 \_ Range \_ UINT64& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="46e65-114">**operator const D3D12\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="46e65-115">Implizite Konvertierung in eine D3D12 \_ Range \_ UINT64-Struktur.</span><span class="sxs-lookup"><span data-stu-id="46e65-115">Implicit conversion to a D3D12\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="46e65-116">Da D3D12 \_ Range \_ UINT64 der zugrunde liegende Typ von CD3DX12 \_ Range \_ UINT64 ist, wird das Objekt einfach als konstanter D3D12 \_ Range UINT64- \_ Verweis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46e65-116">Because D3D12\_RANGE\_UINT64 is the underlying type of CD3DX12\_RANGE\_UINT64, the object is simply returned as a const D3D12\_RANGE\_UINT64 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46e65-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46e65-117">Requirements</span></span>



| <span data-ttu-id="46e65-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46e65-118">Requirement</span></span> | <span data-ttu-id="46e65-119">Wert</span><span class="sxs-lookup"><span data-stu-id="46e65-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46e65-120">Header</span><span class="sxs-lookup"><span data-stu-id="46e65-120">Header</span></span><br/> | <dl> <span data-ttu-id="46e65-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="46e65-121"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46e65-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46e65-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e65-123">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="46e65-123">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="46e65-124">**D3D12 \_ Range \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="46e65-124">**D3D12\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





