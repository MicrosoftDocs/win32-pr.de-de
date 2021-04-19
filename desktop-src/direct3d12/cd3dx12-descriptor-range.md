---
title: CD3DX12_DESCRIPTOR_RANGE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12- \_ deskriptorbereichstruktur ermöglicht \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- CD3DX12_DESCRIPTOR_RANGE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b511af1766daaefa7f92d33b71841b3a69c99927
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350664"
---
# <a name="cd3dx12_descriptor_range-structure"></a><span data-ttu-id="321ad-104">CD3DX12- \_ \_ deskriptorbereichstruktur</span><span class="sxs-lookup"><span data-stu-id="321ad-104">CD3DX12\_DESCRIPTOR\_RANGE structure</span></span>

<span data-ttu-id="321ad-105">Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12- \_ \_ deskriptorbereichstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="321ad-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="321ad-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="321ad-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="321ad-107">Member</span><span class="sxs-lookup"><span data-stu-id="321ad-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="321ad-108">**CD3DX12- \_ \_ Deskriptorbereich ()**</span><span class="sxs-lookup"><span data-stu-id="321ad-108">**CD3DX12\_DESCRIPTOR\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="321ad-109">Erstellt eine neue, nicht initialisierte Instanz eines D3DX12- \_ \_ Deskriptorbereichs.</span><span class="sxs-lookup"><span data-stu-id="321ad-109">Creates a new, uninitialized, instance of a D3DX12\_DESCRIPTOR\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="321ad-110">**expliziter CD3DX12- \_ \_ Deskriptorbereich (konstant D3D12 \_ \_ Deskriptorbereich &o)**</span><span class="sxs-lookup"><span data-stu-id="321ad-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE(const D3D12\_DESCRIPTOR\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="321ad-111">Erstellt eine neue Instanz eines D3DX12- \_ \_ Deskriptorbereichs, der mit dem Inhalt einer anderen [**D3D12- \_ \_ deskriptorbereichstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="321ad-111">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="321ad-112">**CD3DX12 \_ Descriptor \_ Range (D3D12 \_ deskriptorbereichstyp \_ \_ RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Append)**</span><span class="sxs-lookup"><span data-stu-id="321ad-112">**CD3DX12\_DESCRIPTOR\_RANGE(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="321ad-113">Erstellt eine neue Instanz eines D3DX12- \_ \_ Deskriptorbereichs und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="321ad-113">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="321ad-114">[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"</span><span class="sxs-lookup"><span data-stu-id="321ad-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="321ad-115">Uint-numdeskriptors</span><span class="sxs-lookup"><span data-stu-id="321ad-115">UINT numDescriptors</span></span>

<span data-ttu-id="321ad-116">Uint baseshaderregister</span><span class="sxs-lookup"><span data-stu-id="321ad-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="321ad-117">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="321ad-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="321ad-118">Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen</span><span class="sxs-lookup"><span data-stu-id="321ad-118">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="321ad-119">**Inline-init (D3D12 \_ Descriptor \_ Range \_ Type RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, uint offsetindescriptorsfromtablestart = D3D12 \_ Descriptor \_ Range \_ Offset \_ Append)**</span><span class="sxs-lookup"><span data-stu-id="321ad-119">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="321ad-120">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="321ad-120">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="321ad-121">[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"</span><span class="sxs-lookup"><span data-stu-id="321ad-121">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="321ad-122">Uint-numdeskriptors</span><span class="sxs-lookup"><span data-stu-id="321ad-122">UINT numDescriptors</span></span>

<span data-ttu-id="321ad-123">Uint baseshaderregister</span><span class="sxs-lookup"><span data-stu-id="321ad-123">UINT baseShaderRegister</span></span>

<span data-ttu-id="321ad-124">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="321ad-124">UINT registerSpace = 0</span></span>

<span data-ttu-id="321ad-125">Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen</span><span class="sxs-lookup"><span data-stu-id="321ad-125">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="321ad-126">**static Inline init (D3D12 \_ Descriptor \_ Range &Range, D3D12 \_ Descriptor \_ Range \_ Type RangeType, uint numdescriptors, uint baseshaderregister, uint registerspace = 0, uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Append)**</span><span class="sxs-lookup"><span data-stu-id="321ad-126">**static inline Init(D3D12\_DESCRIPTOR\_RANGE &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="321ad-127">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="321ad-127">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="321ad-128">[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &Bereich</span><span class="sxs-lookup"><span data-stu-id="321ad-128">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &range</span></span>

<span data-ttu-id="321ad-129">[**D3D12 \_ \_ \_ Deskriptorbereichstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) "RangeType"</span><span class="sxs-lookup"><span data-stu-id="321ad-129">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="321ad-130">Uint-numdeskriptors</span><span class="sxs-lookup"><span data-stu-id="321ad-130">UINT numDescriptors</span></span>

<span data-ttu-id="321ad-131">Uint baseshaderregister</span><span class="sxs-lookup"><span data-stu-id="321ad-131">UINT baseShaderRegister</span></span>

<span data-ttu-id="321ad-132">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="321ad-132">UINT registerSpace = 0</span></span>

<span data-ttu-id="321ad-133">Uint offsetindescriptorsfromtablestart = D3D12 \_ \_ deskriptorrange \_ Offset \_ Anfügen</span><span class="sxs-lookup"><span data-stu-id="321ad-133">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="321ad-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="321ad-134">Requirements</span></span>



| <span data-ttu-id="321ad-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="321ad-135">Requirement</span></span> | <span data-ttu-id="321ad-136">Wert</span><span class="sxs-lookup"><span data-stu-id="321ad-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="321ad-137">Header</span><span class="sxs-lookup"><span data-stu-id="321ad-137">Header</span></span><br/> | <dl> <span data-ttu-id="321ad-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="321ad-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="321ad-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="321ad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321ad-140">**D3D12- \_ \_ Deskriptorbereich**</span><span class="sxs-lookup"><span data-stu-id="321ad-140">**D3D12\_DESCRIPTOR\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[<span data-ttu-id="321ad-141">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="321ad-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





