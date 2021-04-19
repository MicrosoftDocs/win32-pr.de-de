---
title: CD3DX12_RESOURCE_ALLOCATION_INFO-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ Ressourcen \_ Zuordnungs Info-Struktur zu ermöglichen \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- CD3DX12_RESOURCE_ALLOCATION_INFO Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350662"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a><span data-ttu-id="5905a-104">CD3DX12 \_ \_ ressourcenzuordnungs- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="5905a-104">CD3DX12\_RESOURCE\_ALLOCATION\_INFO structure</span></span>

<span data-ttu-id="5905a-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Ressourcen \_ Zuordnungs \_ Info**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5905a-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5905a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5905a-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="5905a-107">Member</span><span class="sxs-lookup"><span data-stu-id="5905a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5905a-108">**CD3DX12 \_ Ressourcen \_ Zuordnungs \_ Informationen ()**</span><span class="sxs-lookup"><span data-stu-id="5905a-108">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="5905a-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Ressourcen \_ Zuordnungs \_ Informationen.</span><span class="sxs-lookup"><span data-stu-id="5905a-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="5905a-110">**explizite CD3DX12 \_ Ressourcen \_ Zuordnungs \_ Informationen (konstant D3D12 \_ Ressourcen \_ Zuordnungs \_ Informationen& o)**</span><span class="sxs-lookup"><span data-stu-id="5905a-110">**explicit CD3DX12\_RESOURCE\_ALLOCATION\_INFO(const D3D12\_RESOURCE\_ALLOCATION\_INFO& o)**</span></span>
</dt> <dd>

<span data-ttu-id="5905a-111">Erstellt eine neue Instanz der CD3DX12- \_ Ressourcen \_ Zuordnungs \_ Informationen, die mit dem Inhalt einer anderen [**D3D12 \_ Resource \_ Allocation \_ Info**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) -Struktur initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5905a-111">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initialized with the contents of another [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5905a-112">**CD3DX12 \_ Ressourcen \_ Zuordnungs \_ Informationen (UINT64 Size, UINT64 Alignment)**</span><span class="sxs-lookup"><span data-stu-id="5905a-112">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO(UINT64 size, UINT64 alignment)**</span></span>
</dt> <dd>

<span data-ttu-id="5905a-113">Erstellt eine neue Instanz der CD3DX12- \_ Ressourcen \_ Zuordnungs \_ Informationen und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="5905a-113">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="5905a-114">UINT64-Größe</span><span class="sxs-lookup"><span data-stu-id="5905a-114">UINT64 size</span></span>

<span data-ttu-id="5905a-115">UINT64-Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="5905a-115">UINT64 alignment</span></span>

</dd> <dt>

<span data-ttu-id="5905a-116">**Operator Konstanten D3D12 \_ Ressourcen \_ Zuordnungs \_ Informationen& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="5905a-116">**operator const D3D12\_RESOURCE\_ALLOCATION\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="5905a-117">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="5905a-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5905a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5905a-118">Requirements</span></span>



| <span data-ttu-id="5905a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5905a-119">Requirement</span></span> | <span data-ttu-id="5905a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5905a-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5905a-121">Header</span><span class="sxs-lookup"><span data-stu-id="5905a-121">Header</span></span><br/> | <dl> <span data-ttu-id="5905a-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5905a-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5905a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5905a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5905a-124">**D3D12 \_ Ressourcen \_ Zuordnungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="5905a-124">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[<span data-ttu-id="5905a-125">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="5905a-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





