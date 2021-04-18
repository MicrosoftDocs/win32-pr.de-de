---
title: CD3DX12_ROOT_DESCRIPTOR_TABLE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12 \_ - \_ stammdeskriptortabellenstruktur ermöglicht \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- CD3DX12_ROOT_DESCRIPTOR_TABLE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354350"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a><span data-ttu-id="c15a7-104">CD3DX12 \_ - \_ stammdeskriptortabellenstruktur \_</span><span class="sxs-lookup"><span data-stu-id="c15a7-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE structure</span></span>

<span data-ttu-id="c15a7-105">Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12 \_ - \_ stammdeskriptortabellenstruktur \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c15a7-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c15a7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c15a7-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="c15a7-107">Member</span><span class="sxs-lookup"><span data-stu-id="c15a7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c15a7-108">**CD3DX12 \_ - \_ stammdeskriptortabelle \_ ()**</span><span class="sxs-lookup"><span data-stu-id="c15a7-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE()**</span></span>
</dt> <dd>

<span data-ttu-id="c15a7-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ \_ stammdeskriptortabelle \_ .</span><span class="sxs-lookup"><span data-stu-id="c15a7-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE.</span></span>

</dd> <dt>

<span data-ttu-id="c15a7-110">**explizite CD3DX12 \_ - \_ stammdeskriptortabelle \_ (konstant D3D12 \_ \_ stammdeskriptortabelle \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="c15a7-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(const D3D12\_ROOT\_DESCRIPTOR\_TABLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="c15a7-111">Erstellt eine neue Instanz einer CD3DX12- \_ \_ \_ stammdeskriptortabelle, die mit dem Inhalt einer anderen [**D3D12- \_ \_ stammdeskriptortabellenstruktur \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c15a7-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c15a7-112">**CD3DX12 \_ root \_ Descriptor \_ Table (uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Range \* \_ pdescriptorranges)**</span><span class="sxs-lookup"><span data-stu-id="c15a7-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="c15a7-113">Erstellt eine neue Instanz einer CD3DX12- \_ \_ \_ stammdeskriptortabelle und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="c15a7-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initializing the following parameters:</span></span>

<span data-ttu-id="c15a7-114">Uint numdescriptor Ranges</span><span class="sxs-lookup"><span data-stu-id="c15a7-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="c15a7-115">[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) " \* \_ pdescriptorranges"</span><span class="sxs-lookup"><span data-stu-id="c15a7-115">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="c15a7-116">**Inline-init (uint numdescriptorranges, Konstanten D3D12 \_ \_ Deskriptorbereich \* \_ pdescriptorranges)**</span><span class="sxs-lookup"><span data-stu-id="c15a7-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="c15a7-117">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="c15a7-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="c15a7-118">Uint numdescriptor Ranges</span><span class="sxs-lookup"><span data-stu-id="c15a7-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="c15a7-119">[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) " \* \_ pdescriptorranges"</span><span class="sxs-lookup"><span data-stu-id="c15a7-119">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="c15a7-120">**static Inline init (D3D12 \_ root \_ Descriptor- \_ Tabelle &rootdescriptortable, uint numdescriptorranges, Konstanten D3D12 \_ \_ deskriptorrange \* \_ pdescriptorranges)**</span><span class="sxs-lookup"><span data-stu-id="c15a7-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="c15a7-121">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="c15a7-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="c15a7-122">[**D3D12 \_ \_ \_ Stammdeskriptortabelle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootdescriptortable</span><span class="sxs-lookup"><span data-stu-id="c15a7-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span></span>

<span data-ttu-id="c15a7-123">Uint numdescriptor Ranges</span><span class="sxs-lookup"><span data-stu-id="c15a7-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="c15a7-124">[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) " \* \_ pdescriptorranges"</span><span class="sxs-lookup"><span data-stu-id="c15a7-124">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c15a7-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c15a7-125">Requirements</span></span>



| <span data-ttu-id="c15a7-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c15a7-126">Requirement</span></span> | <span data-ttu-id="c15a7-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c15a7-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c15a7-128">Header</span><span class="sxs-lookup"><span data-stu-id="c15a7-128">Header</span></span><br/> | <dl> <span data-ttu-id="c15a7-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c15a7-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c15a7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c15a7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c15a7-131">**D3D12 \_ - \_ stammdeskriptortabelle \_**</span><span class="sxs-lookup"><span data-stu-id="c15a7-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[<span data-ttu-id="c15a7-132">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="c15a7-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





