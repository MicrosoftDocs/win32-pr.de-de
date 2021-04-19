---
title: CD3DX12_RESOURCE_BARRIER-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12- \_ Ressourcen \_ Barriere ermöglicht.
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- CD3DX12_RESOURCE_BARRIER Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361900"
---
# <a name="cd3dx12_resource_barrier-structure"></a><span data-ttu-id="4a351-104">CD3DX12 \_ \_ ressourcensperrenstruktur</span><span class="sxs-lookup"><span data-stu-id="4a351-104">CD3DX12\_RESOURCE\_BARRIER structure</span></span>

<span data-ttu-id="4a351-105">Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12- \_ Ressourcen \_ Barriere**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="4a351-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a351-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a351-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a><span data-ttu-id="4a351-107">Member</span><span class="sxs-lookup"><span data-stu-id="4a351-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a351-108">**CD3DX12- \_ Ressourcen \_ Barriere ()**</span><span class="sxs-lookup"><span data-stu-id="4a351-108">**CD3DX12\_RESOURCE\_BARRIER()**</span></span>
</dt> <dd>

<span data-ttu-id="4a351-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Ressourcen \_ Barriere.</span><span class="sxs-lookup"><span data-stu-id="4a351-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_BARRIER.</span></span>

</dd> <dt>

<span data-ttu-id="4a351-110">**explizites CD3DX12 \_ Ressourcen \_ Barriere (konstant D3D12 \_ Ressourcen \_ Barriere &o)**</span><span class="sxs-lookup"><span data-stu-id="4a351-110">**explicit CD3DX12\_RESOURCE\_BARRIER(const D3D12\_RESOURCE\_BARRIER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="4a351-111">Erstellt eine neue Instanz einer CD3DX12- \_ Ressourcen \_ Barriere, die mit dem Inhalt einer anderen [**D3D12- \_ Ressourcen \_ Barriere**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="4a351-111">Creates a new instance of a CD3DX12\_RESOURCE\_BARRIER, initialized with the contents of another [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span></span>

</dd> <dt>

<span data-ttu-id="4a351-112">**statischer Inline Übergang ("ID3D12Resource \* presource", "D3D12 \_ Resource \_ States statebefore", "D3D12 \_ Resource \_ States stateafter", "uint subresource = D3D12 \_ Resource \_ Barrier \_ All \_ subresources", "D3D12 \_ Resource \_ Barrier \_ Flags Flags = D3D12 \_ Resource \_ Barrier \_ Flag \_ None")**</span><span class="sxs-lookup"><span data-stu-id="4a351-112">**static inline Transition(ID3D12Resource\* pResource, D3D12\_RESOURCE\_STATES stateBefore, D3D12\_RESOURCE\_STATES stateAfter, UINT subresource = D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES, D3D12\_RESOURCE\_BARRIER\_FLAGS flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="4a351-113">Übergänge zwischen Ressourcen Zuständen mit den folgenden Parametern:</span><span class="sxs-lookup"><span data-stu-id="4a351-113">Transitions between resource states, using the following parameters:</span></span>

<span data-ttu-id="4a351-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* vorab Quelle</span><span class="sxs-lookup"><span data-stu-id="4a351-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

<span data-ttu-id="4a351-115">[**D3D12 \_ Ressourcen \_ Zustände**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) statebefore</span><span class="sxs-lookup"><span data-stu-id="4a351-115">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore</span></span>

<span data-ttu-id="4a351-116">[**D3D12 \_ Ressourcen \_ Zustände**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateafter</span><span class="sxs-lookup"><span data-stu-id="4a351-116">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter</span></span>

<span data-ttu-id="4a351-117">Opt Uint subresource = [ **D3D12 \_ Ressourcen \_ Barriere \_ alle \_ unter Ressourcen**](constants.md)</span><span class="sxs-lookup"><span data-stu-id="4a351-117">(opt) UINT subresource = [**D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES**](constants.md)</span></span>

<span data-ttu-id="4a351-118">Opt [**D3D12 \_ \_ \_ Ressourcensperrungsflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) = \_ D3D12 \_ ressourcensperrungsflag " \_ \_ None"</span><span class="sxs-lookup"><span data-stu-id="4a351-118">(opt) [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="4a351-119">**statisches Inline Aliasing (ID3D12Resource \* presourcebefore, ID3D12Resource \* presourceafter)**</span><span class="sxs-lookup"><span data-stu-id="4a351-119">**static inline Aliasing(ID3D12Resource\* pResourceBefore, ID3D12Resource\* pResourceAfter)**</span></span>
</dt> <dd>

<span data-ttu-id="4a351-120">Erstellt Aliase für die Ressource vor und nach dem Sperr Übergang.</span><span class="sxs-lookup"><span data-stu-id="4a351-120">Creates aliases for the resource before and after the barrier transition.</span></span> <span data-ttu-id="4a351-121">Parameter:</span><span class="sxs-lookup"><span data-stu-id="4a351-121">Parameters:</span></span>

<span data-ttu-id="4a351-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* presourcebefore</span><span class="sxs-lookup"><span data-stu-id="4a351-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceBefore</span></span>

<span data-ttu-id="4a351-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* presourceafter</span><span class="sxs-lookup"><span data-stu-id="4a351-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceAfter</span></span>

</dd> <dt>

<span data-ttu-id="4a351-124">**statische Inline-UAV (ID3D12Resource \* presource)**</span><span class="sxs-lookup"><span data-stu-id="4a351-124">**static inline UAV(ID3D12Resource\* pResource)**</span></span>
</dt> <dd>

<span data-ttu-id="4a351-125">Erstellt eine ungeordnete Zugriffs Ansicht (UAV) für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="4a351-125">Creates an unordered-access-view (UAV) for the resource.</span></span> <span data-ttu-id="4a351-126">Parameter:</span><span class="sxs-lookup"><span data-stu-id="4a351-126">Parameters:</span></span>

<span data-ttu-id="4a351-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* vorab Quelle</span><span class="sxs-lookup"><span data-stu-id="4a351-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

</dd> <dt>

<span data-ttu-id="4a351-128">**Operator konstant D3D12 \_ Ressourcen \_ Barriere& () konstant**</span><span class="sxs-lookup"><span data-stu-id="4a351-128">**operator const D3D12\_RESOURCE\_BARRIER&() const**</span></span>
</dt> <dd>

<span data-ttu-id="4a351-129">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="4a351-129">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a351-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a351-130">Requirements</span></span>



| <span data-ttu-id="4a351-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a351-131">Requirement</span></span> | <span data-ttu-id="4a351-132">Wert</span><span class="sxs-lookup"><span data-stu-id="4a351-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4a351-133">Header</span><span class="sxs-lookup"><span data-stu-id="4a351-133">Header</span></span><br/> | <dl> <span data-ttu-id="4a351-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a351-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a351-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a351-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a351-136">**D3D12 \_ Ressourcen \_ Barriere**</span><span class="sxs-lookup"><span data-stu-id="4a351-136">**D3D12\_RESOURCE\_BARRIER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[<span data-ttu-id="4a351-137">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="4a351-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





