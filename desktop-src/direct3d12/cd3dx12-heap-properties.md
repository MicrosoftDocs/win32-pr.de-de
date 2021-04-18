---
title: CD3DX12_HEAP_PROPERTIES-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ Heap \_ Eigenschaften Struktur zu ermöglichen.
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- CD3DX12_HEAP_PROPERTIES Struktur
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354351"
---
# <a name="cd3dx12_heap_properties-structure"></a><span data-ttu-id="26ae3-104">Struktur der CD3DX12- \_ Heap \_ Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26ae3-104">CD3DX12\_HEAP\_PROPERTIES structure</span></span>

<span data-ttu-id="26ae3-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Heap \_ Eigenschaften**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="26ae3-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ae3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="26ae3-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a><span data-ttu-id="26ae3-107">Member</span><span class="sxs-lookup"><span data-stu-id="26ae3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="26ae3-108">**CD3DX12 \_ Heap- \_ Eigenschaften ()**</span><span class="sxs-lookup"><span data-stu-id="26ae3-108">**CD3DX12\_HEAP\_PROPERTIES()**</span></span>
</dt> <dd>

<span data-ttu-id="26ae3-109">Erstellt eine neue, nicht initialisierte Instanz von CD3DX12 \_ Heap \_ Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="26ae3-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_PROPERTIES.</span></span>

</dd> <dt>

<span data-ttu-id="26ae3-110">**explizite CD3DX12 \_ Heap \_ Eigenschaften (Konstanten D3D12 \_ Heap \_ Eigenschaften &o)**</span><span class="sxs-lookup"><span data-stu-id="26ae3-110">**explicit CD3DX12\_HEAP\_PROPERTIES(const D3D12\_HEAP\_PROPERTIES &o)**</span></span>
</dt> <dd>

<span data-ttu-id="26ae3-111">Erstellt eine neue Instanz einer CD3DX12- \_ Heap Eigenschaft \_ , die mit dem Inhalt einer anderen [**D3D12 \_ Heap \_ Properties**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="26ae3-111">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initialized with the contents of another [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

</dd> <dt>

<span data-ttu-id="26ae3-112">**CD3DX12 \_ Heap- \_ Eigenschaften (D3D12 \_ CPU \_ Page \_ Property cpupageproperty, D3D12 \_ Memory \_ Pool memorypoolpreference, uint anationnodemask = 1, uint nodemask = 1)**</span><span class="sxs-lookup"><span data-stu-id="26ae3-112">**CD3DX12\_HEAP\_PROPERTIES(D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="26ae3-113">Erstellt eine neue Instanz der CD3DX12- \_ Heap \_ Eigenschaften und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="26ae3-113">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="26ae3-114">[**D3D12 \_ CPU \_ - \_ Seiteneigenschaft**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpupageproperty</span><span class="sxs-lookup"><span data-stu-id="26ae3-114">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="26ae3-115">[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) Memorypoolpreference für Speicher Pool</span><span class="sxs-lookup"><span data-stu-id="26ae3-115">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="26ae3-116">Opt Uint-kreationnodemask = 1</span><span class="sxs-lookup"><span data-stu-id="26ae3-116">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="26ae3-117">Opt Uint nodemask = 1</span><span class="sxs-lookup"><span data-stu-id="26ae3-117">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="26ae3-118">**explizite CD3DX12 \_ Heap- \_ Eigenschaften (D3D12 \_ Heap \_ Type type, uint kreationnodemask = 1, uint nodemask = 1)**</span><span class="sxs-lookup"><span data-stu-id="26ae3-118">**explicit CD3DX12\_HEAP\_PROPERTIES(D3D12\_HEAP\_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="26ae3-119">Erstellt eine neue Instanz der CD3DX12- \_ Heap \_ Eigenschaften und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="26ae3-119">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="26ae3-120">[**D3D12 \_ Typ des Heap \_ Typs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="26ae3-120">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="26ae3-121">Opt Uint-kreationnodemask = 1</span><span class="sxs-lookup"><span data-stu-id="26ae3-121">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="26ae3-122">Opt Uint nodemask = 1</span><span class="sxs-lookup"><span data-stu-id="26ae3-122">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="26ae3-123">**Operator Konstanten D3D12 \_ Heap \_ Eigenschaften& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="26ae3-123">**operator const D3D12\_HEAP\_PROPERTIES&() const**</span></span>
</dt> <dd>

<span data-ttu-id="26ae3-124">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="26ae3-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="26ae3-125">**Inline Operator = = (Konstanten D3D12 \_ Heap \_ Eigenschaften& l, Konstanten D3D12 \_ Heap \_ Eigenschaften& r)**</span><span class="sxs-lookup"><span data-stu-id="26ae3-125">**inline operator==( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="26ae3-126">Testet basierend auf der Gleichheit aller Element Felder auf Gleichheit zwischen den angegebenen D3D12 \_ Heap- \_ Eigenschaften Instanzen.</span><span class="sxs-lookup"><span data-stu-id="26ae3-126">Tests for equality between the specified D3D12\_HEAP\_PROPERTIES instances, based on equality of all member fields.</span></span>

</dd> <dt>

<span data-ttu-id="26ae3-127">**Inline Operator! = (Konstanten D3D12 \_ Heap \_ Eigenschaften& l, Konstanten D3D12 \_ Heap \_ Eigenschaften& r)**</span><span class="sxs-lookup"><span data-stu-id="26ae3-127">**inline operator!=( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="26ae3-128">Prüft auf Ungleichheit zwischen den angegebenen D3D12 \_ Heap- \_ Eigenschaften Instanzen.</span><span class="sxs-lookup"><span data-stu-id="26ae3-128">Tests for inequality between the specified D3D12\_HEAP\_PROPERTIES instances.</span></span> <span data-ttu-id="26ae3-129">Wird durch die Umkehrung des **Operators = =** implementiert.</span><span class="sxs-lookup"><span data-stu-id="26ae3-129">Implemented by taking the inverse of the **operator==** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26ae3-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26ae3-130">Requirements</span></span>



| <span data-ttu-id="26ae3-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26ae3-131">Requirement</span></span> | <span data-ttu-id="26ae3-132">Wert</span><span class="sxs-lookup"><span data-stu-id="26ae3-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="26ae3-133">Header</span><span class="sxs-lookup"><span data-stu-id="26ae3-133">Header</span></span><br/> | <dl> <span data-ttu-id="26ae3-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="26ae3-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ae3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26ae3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ae3-136">**D3D12- \_ Heap \_ Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="26ae3-136">**D3D12\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[<span data-ttu-id="26ae3-137">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="26ae3-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





