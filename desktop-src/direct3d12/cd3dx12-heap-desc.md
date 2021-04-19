---
title: CD3DX12_HEAP_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ Heap- \_ DESC-Struktur zu ermöglichen.
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- CD3DX12_HEAP_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b2537d2571355f26c46f03aed3489fb2b6069
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355787"
---
# <a name="cd3dx12_heap_desc-structure"></a><span data-ttu-id="7b55a-104">CD3DX12- \_ Heap- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="7b55a-104">CD3DX12\_HEAP\_DESC structure</span></span>

<span data-ttu-id="7b55a-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Heap- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7b55a-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b55a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b55a-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="7b55a-107">Member</span><span class="sxs-lookup"><span data-stu-id="7b55a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b55a-108">**CD3DX12 \_ Heap- \_ Debugheap ()**</span><span class="sxs-lookup"><span data-stu-id="7b55a-108">**CD3DX12\_HEAP\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="7b55a-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12-Heaps \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b55a-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="7b55a-110">**expliziter CD3DX12 \_ Heap- \_ Debugheap (konstant D3D12 \_ Heap- \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="7b55a-110">**explicit CD3DX12\_HEAP\_DESC(const D3D12\_HEAP\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="7b55a-111">Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ decoens, der mit dem Inhalt einer anderen [**D3D12 \_ Heap- \_ debugerenstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7b55a-111">Creates a new instance of a CD3DX12\_HEAP\_DESC, initialized with the contents of another [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b55a-112">**CD3DX12 \_ Heap Debug \_ (UINT64 Size, D3D12 \_ Heap \_ Properties Properties, UINT64 Alignment = 0, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="7b55a-112">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_PROPERTIES properties, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="7b55a-113">Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="7b55a-113">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="7b55a-114">UINT64-Größe</span><span class="sxs-lookup"><span data-stu-id="7b55a-114">UINT64 size</span></span>

<span data-ttu-id="7b55a-115">[**D3D12 \_ Eigenschaften von Heap \_ Eigenschaften**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)</span><span class="sxs-lookup"><span data-stu-id="7b55a-115">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="7b55a-116">Opt UINT64 Alignment = 0</span><span class="sxs-lookup"><span data-stu-id="7b55a-116">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="7b55a-117">Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="7b55a-117">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="7b55a-118">**CD3DX12 \_ Heap \_ DESC (UINT64 Size, D3D12 \_ Heap \_ Type type, UINT64 Alignment = 0, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="7b55a-118">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_TYPE type, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="7b55a-119">Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="7b55a-119">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="7b55a-120">UINT64-Größe</span><span class="sxs-lookup"><span data-stu-id="7b55a-120">UINT64 size</span></span>

<span data-ttu-id="7b55a-121">[**D3D12 \_ Typ des Heap \_ Typs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="7b55a-121">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="7b55a-122">Opt UINT64 Alignment = 0</span><span class="sxs-lookup"><span data-stu-id="7b55a-122">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="7b55a-123">Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="7b55a-123">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="7b55a-124">**CD3DX12 \_ Heap \_ DESC (UINT64 Size, D3D12 \_ CPU \_ Page \_ Property cpupageproperty, D3D12 \_ Speicher \_ Pool memorypoolpreference, UINT64 Alignment = 0, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="7b55a-124">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="7b55a-125">Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="7b55a-125">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="7b55a-126">UINT64-Größe</span><span class="sxs-lookup"><span data-stu-id="7b55a-126">UINT64 size</span></span>

<span data-ttu-id="7b55a-127">[**D3D12 \_ CPU \_ - \_ Seiteneigenschaft**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpupageproperty</span><span class="sxs-lookup"><span data-stu-id="7b55a-127">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="7b55a-128">[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) Memorypoolpreference für Speicher Pool</span><span class="sxs-lookup"><span data-stu-id="7b55a-128">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="7b55a-129">Opt UINT64 Alignment = 0</span><span class="sxs-lookup"><span data-stu-id="7b55a-129">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="7b55a-130">Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="7b55a-130">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="7b55a-131">**CD3DX12 \_ Heap \_ DESC (Zuordnungs \_ Informationen für Ressourcen \_ Zuordnungen \_& resallocinfo, D3D12 \_ Heap \_ Eigenschaften Eigenschaften, D3D12 Heap Kennzeichen \_ \_ Flags = D3D12 \_ Heap \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="7b55a-131">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_PROPERTIES properties, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="7b55a-132">Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="7b55a-132">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="7b55a-133">[**D3D12 \_ \_ \_ Informationen zur Ressourcenzuweisung**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resallocinfo</span><span class="sxs-lookup"><span data-stu-id="7b55a-133">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="7b55a-134">[**D3D12 \_ Eigenschaften von Heap \_ Eigenschaften**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)</span><span class="sxs-lookup"><span data-stu-id="7b55a-134">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="7b55a-135">Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="7b55a-135">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="7b55a-136">**CD3DX12 \_ Heap \_ DESC (Informationen zur Ressourcenzuweisung für "" \_ \_ \_ )& resallocinfo, D3D12 \_ Heap \_ Type type, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="7b55a-136">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_TYPE type, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="7b55a-137">Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="7b55a-137">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="7b55a-138">[**D3D12 \_ \_ \_ Informationen zur Ressourcenzuweisung**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resallocinfo</span><span class="sxs-lookup"><span data-stu-id="7b55a-138">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="7b55a-139">[**D3D12 \_ Typ des Heap \_ Typs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="7b55a-139">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="7b55a-140">Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="7b55a-140">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="7b55a-141">**CD3DX12 \_ Heap \_ DESC (konstant D3D12 \_ Ressourcen \_ Zuordnungs \_ Info& resallocinfo, D3D12 \_ CPU \_ Page \_ Property cpupageproperty, D3D12 \_ Memory \_ Pool memorypoolpreference, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="7b55a-141">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="7b55a-142">Erstellt eine neue Instanz eines CD3DX12- \_ Heap- \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="7b55a-142">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="7b55a-143">[**D3D12 \_ \_ \_ Informationen zur Ressourcenzuweisung**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resallocinfo</span><span class="sxs-lookup"><span data-stu-id="7b55a-143">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="7b55a-144">[**D3D12 \_ CPU \_ - \_ Seiteneigenschaft**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpupageproperty</span><span class="sxs-lookup"><span data-stu-id="7b55a-144">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="7b55a-145">[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) Memorypoolpreference für Speicher Pool</span><span class="sxs-lookup"><span data-stu-id="7b55a-145">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="7b55a-146">Opt [**D3D12 \_ Heap \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Kennzeichen Flags = D3D12 \_ Heap \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="7b55a-146">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="7b55a-147">**Operator Konstanten D3D12 \_ Heap- \_& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="7b55a-147">**operator const D3D12\_HEAP\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="7b55a-148">Definiert den & Operator "Pass-by-Reference" für den CD3DX12 \_ Heap \_ DESC-Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="7b55a-148">Defines the & pass-by-reference operator for the CD3DX12\_HEAP\_DESC structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b55a-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b55a-149">Requirements</span></span>



| <span data-ttu-id="7b55a-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b55a-150">Requirement</span></span> | <span data-ttu-id="7b55a-151">Wert</span><span class="sxs-lookup"><span data-stu-id="7b55a-151">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7b55a-152">Header</span><span class="sxs-lookup"><span data-stu-id="7b55a-152">Header</span></span><br/> | <dl> <span data-ttu-id="7b55a-153"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b55a-153"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b55a-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b55a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b55a-155">**D3D12 \_ Heap- \_ Debugheap**</span><span class="sxs-lookup"><span data-stu-id="7b55a-155">**D3D12\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[<span data-ttu-id="7b55a-156">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="7b55a-156">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





