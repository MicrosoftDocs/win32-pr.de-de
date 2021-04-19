---
title: CD3DX12_RANGE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12- \_ Bereichs Struktur ermöglicht.
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- CD3DX12_RANGE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367490"
---
# <a name="cd3dx12_range-structure"></a><span data-ttu-id="0f1ef-104">CD3DX12 \_ Range-Struktur</span><span class="sxs-lookup"><span data-stu-id="0f1ef-104">CD3DX12\_RANGE structure</span></span>

<span data-ttu-id="0f1ef-105">Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12- \_ Bereichs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) Struktur ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f1ef-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f1ef-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a><span data-ttu-id="0f1ef-107">Member</span><span class="sxs-lookup"><span data-stu-id="0f1ef-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f1ef-108">**CD3DX12 \_ Range ()**</span><span class="sxs-lookup"><span data-stu-id="0f1ef-108">**CD3DX12\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="0f1ef-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Bereichs.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="0f1ef-110">**expliziter CD3DX12 \_ Bereich (konstant D3D12 \_ Bereich &o)**</span><span class="sxs-lookup"><span data-stu-id="0f1ef-110">**explicit CD3DX12\_RANGE(const D3D12\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="0f1ef-111">Erstellt eine neue Instanz eines CD3DX12 \_ Bereichs, der mit dem Inhalt einer anderen D3D12- [**\_ Bereichs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-111">Creates a new instance of a CD3DX12\_RANGE, initialized with the contents of another [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0f1ef-112">**CD3DX12 \_ Range (size \_ t Begin, size \_ t End)**</span><span class="sxs-lookup"><span data-stu-id="0f1ef-112">**CD3DX12\_RANGE(SIZE\_T begin, SIZE\_T end)**</span></span>
</dt> <dd>

<span data-ttu-id="0f1ef-113">Erstellt eine neue Instanz eines CD3DX12 \_ Bereichs und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="0f1ef-113">Creates a new instance of a CD3DX12\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="0f1ef-114">\_Anfangs Größe</span><span class="sxs-lookup"><span data-stu-id="0f1ef-114">SIZE\_T begin</span></span>

<span data-ttu-id="0f1ef-115">Ende der Größe \_</span><span class="sxs-lookup"><span data-stu-id="0f1ef-115">SIZE\_T end</span></span>

</dd> <dt>

<span data-ttu-id="0f1ef-116">**Operator konstant D3D12 \_ Bereichs& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="0f1ef-116">**operator const D3D12\_RANGE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="0f1ef-117">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f1ef-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f1ef-118">Requirements</span></span>



| <span data-ttu-id="0f1ef-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f1ef-119">Requirement</span></span> | <span data-ttu-id="0f1ef-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0f1ef-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f1ef-121">Header</span><span class="sxs-lookup"><span data-stu-id="0f1ef-121">Header</span></span><br/> | <dl> <span data-ttu-id="0f1ef-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f1ef-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f1ef-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f1ef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f1ef-124">**D3D12 \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="0f1ef-124">**D3D12\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[<span data-ttu-id="0f1ef-125">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="0f1ef-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





