---
title: CD3DX12_ROOT_DESCRIPTOR_TABLE1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-Stamm \_ \_ Deskriptor Table1-Struktur zu ermöglichen \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354410"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a><span data-ttu-id="7122f-104">CD3DX12 \_ root \_ Descriptor \_ Table1-Struktur</span><span class="sxs-lookup"><span data-stu-id="7122f-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1 structure</span></span>

<span data-ttu-id="7122f-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12-Stamm \_ \_ Deskriptor \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7122f-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7122f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7122f-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="7122f-107">Member</span><span class="sxs-lookup"><span data-stu-id="7122f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7122f-108">**CD3DX12 \_ root \_ Descriptor \_ Table1 ()**</span><span class="sxs-lookup"><span data-stu-id="7122f-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1()**</span></span>
</dt> <dd>

<span data-ttu-id="7122f-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12-Stamm \_ \_ Deskriptors \_ Table1.</span><span class="sxs-lookup"><span data-stu-id="7122f-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1.</span></span>

</dd> <dt>

<span data-ttu-id="7122f-110">**expliziter CD3DX12-Stamm \_ \_ Deskriptor \_ Table1 (konstant D3D12 Stamm \_ \_ Deskriptor \_ Table1 &o)**</span><span class="sxs-lookup"><span data-stu-id="7122f-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(const D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="7122f-111">Erstellt eine neue Instanz eines CD3DX12 \_ root \_ Descriptor \_ Table1, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ root \_ Descriptor \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7122f-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7122f-112">**CD3DX12 \_ root \_ Descriptor \_ Table1 (uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Bereich1 \* \_ pdescriptorranges)**</span><span class="sxs-lookup"><span data-stu-id="7122f-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="7122f-113">Erstellt eine neue Instanz eines CD3DX12 \_ root \_ Descriptor \_ Table1 und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="7122f-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initializing the following parameters:</span></span>

<span data-ttu-id="7122f-114">Uint numdescriptor Ranges</span><span class="sxs-lookup"><span data-stu-id="7122f-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="7122f-115">Konstanten [**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pdescriptorranges</span><span class="sxs-lookup"><span data-stu-id="7122f-115">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="7122f-116">**Inline-init (uint numdescriptorranges, Konstanten D3D12 \_ Deskriptor \_ Bereich1 \* \_ pdescriptorranges)**</span><span class="sxs-lookup"><span data-stu-id="7122f-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="7122f-117">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="7122f-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7122f-118">Uint numdescriptor Ranges</span><span class="sxs-lookup"><span data-stu-id="7122f-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="7122f-119">Konstanten [**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pdescriptorranges</span><span class="sxs-lookup"><span data-stu-id="7122f-119">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="7122f-120">**static Inline init (D3D12 \_ root \_ Descriptor \_ Table1 &rootdescriptortable, uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Bereich1 \* \_ pdescriptorranges)**</span><span class="sxs-lookup"><span data-stu-id="7122f-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="7122f-121">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="7122f-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7122f-122">[**D3D12 \_ Stamm \_ Deskriptor \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootdescriptortable</span><span class="sxs-lookup"><span data-stu-id="7122f-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span></span>

<span data-ttu-id="7122f-123">Uint numdescriptor Ranges</span><span class="sxs-lookup"><span data-stu-id="7122f-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="7122f-124">Konstanten [**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pdescriptorranges</span><span class="sxs-lookup"><span data-stu-id="7122f-124">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7122f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7122f-125">Requirements</span></span>



| <span data-ttu-id="7122f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7122f-126">Requirement</span></span> | <span data-ttu-id="7122f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7122f-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7122f-128">Header</span><span class="sxs-lookup"><span data-stu-id="7122f-128">Header</span></span><br/> | <dl> <span data-ttu-id="7122f-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7122f-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7122f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7122f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7122f-131">**D3D12-Stamm \_ \_ Deskriptor \_ Table1**</span><span class="sxs-lookup"><span data-stu-id="7122f-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[<span data-ttu-id="7122f-132">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="7122f-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





