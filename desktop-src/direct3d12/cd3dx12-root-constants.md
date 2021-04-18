---
title: CD3DX12_ROOT_CONSTANTS-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-Stamm \_ \_ Konstanten Struktur zu ermöglichen.
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- CD3DX12_ROOT_CONSTANTS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365074"
---
# <a name="cd3dx12_root_constants-structure"></a><span data-ttu-id="b028f-104">CD3DX12 \_ root \_ Konstanten-Struktur</span><span class="sxs-lookup"><span data-stu-id="b028f-104">CD3DX12\_ROOT\_CONSTANTS structure</span></span>

<span data-ttu-id="b028f-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12-Stamm \_ \_ Konstanten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b028f-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b028f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b028f-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="b028f-107">Member</span><span class="sxs-lookup"><span data-stu-id="b028f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b028f-108">**CD3DX12 \_ root- \_ Konstanten ()**</span><span class="sxs-lookup"><span data-stu-id="b028f-108">**CD3DX12\_ROOT\_CONSTANTS()**</span></span>
</dt> <dd>

<span data-ttu-id="b028f-109">Erstellt eine neue, nicht initialisierte Instanz von CD3DX12 root- \_ \_ Konstanten.</span><span class="sxs-lookup"><span data-stu-id="b028f-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_CONSTANTS.</span></span>

</dd> <dt>

<span data-ttu-id="b028f-110">**explizite CD3DX12-Stamm \_ \_ Konstanten (konstant D3D12 \_ Stamm \_ Konstanten &o)**</span><span class="sxs-lookup"><span data-stu-id="b028f-110">**explicit CD3DX12\_ROOT\_CONSTANTS(const D3D12\_ROOT\_CONSTANTS &o)**</span></span>
</dt> <dd>

<span data-ttu-id="b028f-111">Erstellt eine neue Instanz einer CD3DX12 \_ root- \_ Konstante, die mit dem Inhalt einer anderen [**D3D12 \_ root \_ Constants**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b028f-111">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initialized with the contents of another [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b028f-112">**CD3DX12 \_ root \_ Konstanten (uint num32BitValues, uint shaderregister, uint registerspace = 0)**</span><span class="sxs-lookup"><span data-stu-id="b028f-112">**CD3DX12\_ROOT\_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="b028f-113">Erstellt eine neue Instanz der CD3DX12- \_ Stamm \_ Konstanten und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="b028f-113">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initializing the following parameters:</span></span>

<span data-ttu-id="b028f-114">Uint num32BitValues</span><span class="sxs-lookup"><span data-stu-id="b028f-114">UINT num32BitValues</span></span>

<span data-ttu-id="b028f-115">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="b028f-115">UINT shaderRegister</span></span>

<span data-ttu-id="b028f-116">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="b028f-116">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="b028f-117">**Inline-init (uint num32BitValues, uint shaderregister, uint registerspace = 0)**</span><span class="sxs-lookup"><span data-stu-id="b028f-117">**inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="b028f-118">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="b028f-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b028f-119">Uint num32BitValues</span><span class="sxs-lookup"><span data-stu-id="b028f-119">UINT num32BitValues</span></span>

<span data-ttu-id="b028f-120">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="b028f-120">UINT shaderRegister</span></span>

<span data-ttu-id="b028f-121">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="b028f-121">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="b028f-122">**static Inline init (D3D12 \_ root \_ Konstanten &rootkonstanten, uint num32BitValues, uint shaderregister, uint registerspace = 0)**</span><span class="sxs-lookup"><span data-stu-id="b028f-122">**static inline Init(D3D12\_ROOT\_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="b028f-123">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="b028f-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b028f-124">[**D3D12 \_ Stamm \_ Konstanten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootkonstanten</span><span class="sxs-lookup"><span data-stu-id="b028f-124">[**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span></span>

<span data-ttu-id="b028f-125">Uint num32BitValues</span><span class="sxs-lookup"><span data-stu-id="b028f-125">UINT num32BitValues</span></span>

<span data-ttu-id="b028f-126">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="b028f-126">UINT shaderRegister</span></span>

<span data-ttu-id="b028f-127">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="b028f-127">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b028f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b028f-128">Requirements</span></span>



| <span data-ttu-id="b028f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b028f-129">Requirement</span></span> | <span data-ttu-id="b028f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="b028f-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b028f-131">Header</span><span class="sxs-lookup"><span data-stu-id="b028f-131">Header</span></span><br/> | <dl> <span data-ttu-id="b028f-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b028f-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b028f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b028f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b028f-134">**D3D12 \_ root- \_ Konstanten**</span><span class="sxs-lookup"><span data-stu-id="b028f-134">**D3D12\_ROOT\_CONSTANTS**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[<span data-ttu-id="b028f-135">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="b028f-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





