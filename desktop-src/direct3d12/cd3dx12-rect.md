---
title: CD3DX12_RECT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Rect-Struktur zu ermöglichen.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- CD3DX12_RECT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351929"
---
# <a name="cd3dx12_rect-structure"></a><span data-ttu-id="16a33-104">CD3DX12 \_ Rect-Struktur</span><span class="sxs-lookup"><span data-stu-id="16a33-104">CD3DX12\_RECT structure</span></span>

<span data-ttu-id="16a33-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Rect**](d3d12-rect.md) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="16a33-105">A helper structure to enable easy initialization of a [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a33-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="16a33-106">Syntax</span></span>


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a><span data-ttu-id="16a33-107">Member</span><span class="sxs-lookup"><span data-stu-id="16a33-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="16a33-108">**CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="16a33-108">**CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="16a33-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Rect.</span><span class="sxs-lookup"><span data-stu-id="16a33-109">Creates a new, uninitialized, instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="16a33-110">**explizites CD3DX12 \_ Rect (konstant D3D12 \_ Rect& o)**</span><span class="sxs-lookup"><span data-stu-id="16a33-110">**explicit CD3DX12\_RECT(const D3D12\_RECT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="16a33-111">Erstellt eine neue Instanz eines CD3DX12 \_ Rect, das mit dem Inhalt einer anderen [**D3D12 \_ Rect**](d3d12-rect.md) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="16a33-111">Creates a new instance of a CD3DX12\_RECT, initialized with the contents of another [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="16a33-112">**explizites CD3DX12 \_ Rect (Long Left, Long Top, Long right, Long Bottom)**</span><span class="sxs-lookup"><span data-stu-id="16a33-112">**explicit CD3DX12\_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="16a33-113">Erstellt eine neue Instanz eines CD3DX12 \_ Rect und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="16a33-113">Creates a new instance of a CD3DX12\_RECT, initializing the following parameters:</span></span>

<span data-ttu-id="16a33-114">Long Left</span><span class="sxs-lookup"><span data-stu-id="16a33-114">LONG Left</span></span>

<span data-ttu-id="16a33-115">Langer Anfang</span><span class="sxs-lookup"><span data-stu-id="16a33-115">LONG Top</span></span>

<span data-ttu-id="16a33-116">Long right</span><span class="sxs-lookup"><span data-stu-id="16a33-116">LONG Right</span></span>

<span data-ttu-id="16a33-117">Long-Bottom</span><span class="sxs-lookup"><span data-stu-id="16a33-117">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="16a33-118">**~ CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="16a33-118">**~CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="16a33-119">Zerstört eine Instanz eines CD3DX12 \_ Rect.</span><span class="sxs-lookup"><span data-stu-id="16a33-119">Destroys an instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="16a33-120">**Operator Konstanten D3D12 \_ Rect& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="16a33-120">**operator const D3D12\_RECT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="16a33-121">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="16a33-121">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16a33-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16a33-122">Requirements</span></span>



| <span data-ttu-id="16a33-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16a33-123">Requirement</span></span> | <span data-ttu-id="16a33-124">Wert</span><span class="sxs-lookup"><span data-stu-id="16a33-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="16a33-125">Header</span><span class="sxs-lookup"><span data-stu-id="16a33-125">Header</span></span><br/> | <dl> <span data-ttu-id="16a33-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="16a33-126"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16a33-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16a33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a33-128">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="16a33-128">**D3D12\_RECT**</span></span>](d3d12-rect.md)
</dt> <dt>

[<span data-ttu-id="16a33-129">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="16a33-129">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





