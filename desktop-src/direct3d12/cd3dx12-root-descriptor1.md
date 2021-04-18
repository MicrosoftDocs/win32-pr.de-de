---
title: CD3DX12_ROOT_DESCRIPTOR1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ root \_ DESCRIPTOR1-Struktur zu ermöglichen.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- CD3DX12_ROOT_DESCRIPTOR1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361244"
---
# <a name="cd3dx12_root_descriptor1-structure"></a><span data-ttu-id="5b51f-104">CD3DX12 \_ root \_ DESCRIPTOR1-Struktur</span><span class="sxs-lookup"><span data-stu-id="5b51f-104">CD3DX12\_ROOT\_DESCRIPTOR1 structure</span></span>

<span data-ttu-id="5b51f-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ root \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5b51f-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b51f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b51f-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="5b51f-107">Member</span><span class="sxs-lookup"><span data-stu-id="5b51f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b51f-108">**CD3DX12 \_ root \_ DESCRIPTOR1 ()**</span><span class="sxs-lookup"><span data-stu-id="5b51f-108">**CD3DX12\_ROOT\_DESCRIPTOR1()**</span></span>
</dt> <dd>

<span data-ttu-id="5b51f-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ root \_ DESCRIPTOR1.</span><span class="sxs-lookup"><span data-stu-id="5b51f-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR1.</span></span>

</dd> <dt>

<span data-ttu-id="5b51f-110">**explizites CD3DX12 \_ root \_ DESCRIPTOR1 (Konstanten D3D12 \_ root \_ DESCRIPTOR1 &o)**</span><span class="sxs-lookup"><span data-stu-id="5b51f-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR1(const D3D12\_ROOT\_DESCRIPTOR1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="5b51f-111">Erstellt eine neue Instanz eines CD3DX12 \_ root \_ DESCRIPTOR1, das mit dem Inhalt einer anderen [**D3D12 \_ root \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="5b51f-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5b51f-112">**CD3DX12 \_ root \_ DESCRIPTOR1 (uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="5b51f-112">**CD3DX12\_ROOT\_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5b51f-113">Erstellt eine neue Instanz eines CD3DX12 \_ root \_ DESCRIPTOR1 und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="5b51f-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initializing the following parameters:</span></span>

<span data-ttu-id="5b51f-114">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="5b51f-114">UINT shaderRegister</span></span>

<span data-ttu-id="5b51f-115">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="5b51f-115">UINT registerSpace = 0</span></span>

<span data-ttu-id="5b51f-116">[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="5b51f-116">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5b51f-117">**Inline-init (uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="5b51f-117">**inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5b51f-118">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="5b51f-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="5b51f-119">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="5b51f-119">UINT shaderRegister</span></span>

<span data-ttu-id="5b51f-120">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="5b51f-120">UINT registerSpace = 0</span></span>

<span data-ttu-id="5b51f-121">[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="5b51f-121">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5b51f-122">**static Inline init (D3D12 \_ root \_ DESCRIPTOR1 &Table, uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="5b51f-122">**static inline Init(D3D12\_ROOT\_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5b51f-123">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="5b51f-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="5b51f-124">[**D3D12 \_ Stamm \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &Tabelle</span><span class="sxs-lookup"><span data-stu-id="5b51f-124">[**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &table</span></span>

<span data-ttu-id="5b51f-125">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="5b51f-125">UINT shaderRegister</span></span>

<span data-ttu-id="5b51f-126">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="5b51f-126">UINT registerSpace = 0</span></span>

<span data-ttu-id="5b51f-127">[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="5b51f-127">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b51f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b51f-128">Requirements</span></span>



| <span data-ttu-id="5b51f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b51f-129">Requirement</span></span> | <span data-ttu-id="5b51f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5b51f-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5b51f-131">Header</span><span class="sxs-lookup"><span data-stu-id="5b51f-131">Header</span></span><br/> | <dl> <span data-ttu-id="5b51f-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b51f-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b51f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b51f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b51f-134">**D3D12 \_ root \_ DESCRIPTOR1**</span><span class="sxs-lookup"><span data-stu-id="5b51f-134">**D3D12\_ROOT\_DESCRIPTOR1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[<span data-ttu-id="5b51f-135">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="5b51f-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





