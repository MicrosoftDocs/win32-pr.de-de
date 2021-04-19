---
title: CD3DX12_DESCRIPTOR_RANGE1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Descriptor \_ Bereich1-Struktur zu ermöglichen.
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- CD3DX12_DESCRIPTOR_RANGE1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373490"
---
# <a name="cd3dx12_descriptor_range1-structure"></a><span data-ttu-id="7d93e-104">CD3DX12 \_ Descriptor \_ Bereich1-Struktur</span><span class="sxs-lookup"><span data-stu-id="7d93e-104">CD3DX12\_DESCRIPTOR\_RANGE1 structure</span></span>

<span data-ttu-id="7d93e-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Descriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7d93e-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d93e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d93e-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="7d93e-107">Member</span><span class="sxs-lookup"><span data-stu-id="7d93e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d93e-108">**CD3DX12 \_ Descriptor \_ Bereich1 ()**</span><span class="sxs-lookup"><span data-stu-id="7d93e-108">**CD3DX12\_DESCRIPTOR\_RANGE1()**</span></span>
</dt> <dd>

<span data-ttu-id="7d93e-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ Deskriptors \_ Bereich1.</span><span class="sxs-lookup"><span data-stu-id="7d93e-109">Creates a new, uninitialized, instance of a CD3DX12\_DESCRIPTOR\_RANGE1.</span></span>

</dd> <dt>

<span data-ttu-id="7d93e-110">**expliziter CD3DX12- \_ Deskriptor \_ Bereich1 (konstant D3D12 \_ Deskriptor \_ Bereich1 &o)**</span><span class="sxs-lookup"><span data-stu-id="7d93e-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE1(const D3D12\_DESCRIPTOR\_RANGE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="7d93e-111">Erstellt eine neue Instanz eines CD3DX12 \_ Deskriptors \_ Bereich1, die mit dem Inhalt einer anderen [**D3D12 \_ Descriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7d93e-111">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7d93e-112">**CD3DX12 \_ Descriptor \_ Bereich1 (D3D12 \_ deskriptorbereichstyp \_ \_ RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, D3D12 \_ deskriptorbereichsflags \_ \_ = D3D12 \_ deskriptorbereichsflag \_ \_ \_ None, uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Append)**</span><span class="sxs-lookup"><span data-stu-id="7d93e-112">**CD3DX12\_DESCRIPTOR\_RANGE1(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="7d93e-113">Erstellt eine neue Instanz eines CD3DX12 \_ Deskriptors \_ Bereich1 und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="7d93e-113">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initializing the following parameters:</span></span>

<span data-ttu-id="7d93e-114">[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"</span><span class="sxs-lookup"><span data-stu-id="7d93e-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="7d93e-115">Uint-numdeskriptors</span><span class="sxs-lookup"><span data-stu-id="7d93e-115">UINT numDescriptors</span></span>

<span data-ttu-id="7d93e-116">Uint baseshaderregister</span><span class="sxs-lookup"><span data-stu-id="7d93e-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="7d93e-117">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="7d93e-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="7d93e-118">[**D3D12 \_ Deskriptorbereichsflags \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) -Flags = D3D12 \_ deskriptorbereichsflag " \_ \_ \_ None"</span><span class="sxs-lookup"><span data-stu-id="7d93e-118">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="7d93e-119">Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen</span><span class="sxs-lookup"><span data-stu-id="7d93e-119">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="7d93e-120">**Inline-init (D3D12 \_ Descriptor \_ Range \_ Type RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, D3D12 \_ Descriptor \_ Range \_ Flags Flags = D3D12 \_ Descriptor \_ Range \_ Flag \_ None, uint offsetindescriptorsfromtablestart = D3D12 \_ Descriptor \_ Range \_ Offset \_ Append)**</span><span class="sxs-lookup"><span data-stu-id="7d93e-120">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="7d93e-121">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="7d93e-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7d93e-122">[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"</span><span class="sxs-lookup"><span data-stu-id="7d93e-122">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="7d93e-123">Uint-numdeskriptors</span><span class="sxs-lookup"><span data-stu-id="7d93e-123">UINT numDescriptors</span></span>

<span data-ttu-id="7d93e-124">Uint baseshaderregister</span><span class="sxs-lookup"><span data-stu-id="7d93e-124">UINT baseShaderRegister</span></span>

<span data-ttu-id="7d93e-125">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="7d93e-125">UINT registerSpace = 0</span></span>

<span data-ttu-id="7d93e-126">[**D3D12 \_ Deskriptorbereichsflags \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) -Flags = D3D12 \_ deskriptorbereichsflag " \_ \_ \_ None"</span><span class="sxs-lookup"><span data-stu-id="7d93e-126">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="7d93e-127">Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen</span><span class="sxs-lookup"><span data-stu-id="7d93e-127">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="7d93e-128">**static Inline init (D3D12 \_ Descriptor \_ Bereich1 &Range, D3D12 \_ Descriptor \_ Range \_ Type RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, D3D12 \_ Descriptor \_ Range \_ Flags Flags = D3D12 \_ Descriptor \_ Range \_ Flag \_ None, uint offsetindescriptorsfromtablestart = D3D12 \_ Descriptor \_ Range \_ Offset \_ Append)**</span><span class="sxs-lookup"><span data-stu-id="7d93e-128">**static inline Init(D3D12\_DESCRIPTOR\_RANGE1 &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="7d93e-129">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="7d93e-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7d93e-130">[**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &Bereich</span><span class="sxs-lookup"><span data-stu-id="7d93e-130">[**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &range</span></span>

<span data-ttu-id="7d93e-131">[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"</span><span class="sxs-lookup"><span data-stu-id="7d93e-131">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="7d93e-132">Uint-numdeskriptors</span><span class="sxs-lookup"><span data-stu-id="7d93e-132">UINT numDescriptors</span></span>

<span data-ttu-id="7d93e-133">Uint baseshaderregister</span><span class="sxs-lookup"><span data-stu-id="7d93e-133">UINT baseShaderRegister</span></span>

<span data-ttu-id="7d93e-134">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="7d93e-134">UINT registerSpace = 0</span></span>

<span data-ttu-id="7d93e-135">[**D3D12 \_ Deskriptorbereichsflags \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) -Flags = D3D12 \_ deskriptorbereichsflag " \_ \_ \_ None"</span><span class="sxs-lookup"><span data-stu-id="7d93e-135">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="7d93e-136">Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen</span><span class="sxs-lookup"><span data-stu-id="7d93e-136">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d93e-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d93e-137">Requirements</span></span>



| <span data-ttu-id="7d93e-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d93e-138">Requirement</span></span> | <span data-ttu-id="7d93e-139">Wert</span><span class="sxs-lookup"><span data-stu-id="7d93e-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7d93e-140">Header</span><span class="sxs-lookup"><span data-stu-id="7d93e-140">Header</span></span><br/> | <dl> <span data-ttu-id="7d93e-141"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d93e-141"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d93e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d93e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d93e-143">**D3D12- \_ Deskriptor \_ Bereich1**</span><span class="sxs-lookup"><span data-stu-id="7d93e-143">**D3D12\_DESCRIPTOR\_RANGE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[<span data-ttu-id="7d93e-144">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="7d93e-144">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





