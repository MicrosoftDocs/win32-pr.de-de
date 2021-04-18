---
title: CD3DX12_BOX-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Box-Struktur zu ermöglichen.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- CD3DX12_BOX Struktur
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371892"
---
# <a name="cd3dx12_box-structure"></a><span data-ttu-id="3667d-104">CD3DX12 \_ Box-Struktur</span><span class="sxs-lookup"><span data-stu-id="3667d-104">CD3DX12\_BOX structure</span></span>

<span data-ttu-id="3667d-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Box**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3667d-105">A helper structure to enable easy initialization of a [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3667d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3667d-106">Syntax</span></span>


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a><span data-ttu-id="3667d-107">Member</span><span class="sxs-lookup"><span data-stu-id="3667d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3667d-108">**CD3DX12 \_ Box ()**</span><span class="sxs-lookup"><span data-stu-id="3667d-108">**CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="3667d-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Box-Felds \_ .</span><span class="sxs-lookup"><span data-stu-id="3667d-109">Creates a new, uninitialized, instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="3667d-110">**explizites CD3DX12 Box-Feld \_ (konstant D3D12 \_ Box& o)**</span><span class="sxs-lookup"><span data-stu-id="3667d-110">**explicit CD3DX12\_BOX(const D3D12\_BOX& o)**</span></span>
</dt> <dd>

<span data-ttu-id="3667d-111">Erstellt eine neue Instanz eines CD3DX12-Felds \_ , das mit dem Inhalt einer anderen [**D3D12 \_ Box**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="3667d-111">Creates a new instance of a CD3DX12\_BOX, initialized with the contents of another [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3667d-112">**explizites CD3DX12 \_ Feld (Long Left, Long right)**</span><span class="sxs-lookup"><span data-stu-id="3667d-112">**explicit CD3DX12\_BOX(LONG Left, LONG Right)**</span></span>
</dt> <dd>

<span data-ttu-id="3667d-113">Erstellt eine neue Instanz eines CD3DX12 Felds \_ und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="3667d-113">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="3667d-114">Long Left</span><span class="sxs-lookup"><span data-stu-id="3667d-114">LONG Left</span></span>

<span data-ttu-id="3667d-115">Long right</span><span class="sxs-lookup"><span data-stu-id="3667d-115">LONG Right</span></span>

</dd> <dt>

<span data-ttu-id="3667d-116">**explizites CD3DX12 \_ Feld (Long Left, Long Top, Long right, Long Bottom)**</span><span class="sxs-lookup"><span data-stu-id="3667d-116">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="3667d-117">Erstellt eine neue Instanz eines CD3DX12 Felds \_ und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="3667d-117">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="3667d-118">Long Left</span><span class="sxs-lookup"><span data-stu-id="3667d-118">LONG Left</span></span>

<span data-ttu-id="3667d-119">Langer Anfang</span><span class="sxs-lookup"><span data-stu-id="3667d-119">LONG Top</span></span>

<span data-ttu-id="3667d-120">Long right</span><span class="sxs-lookup"><span data-stu-id="3667d-120">LONG Right</span></span>

<span data-ttu-id="3667d-121">Long-Bottom</span><span class="sxs-lookup"><span data-stu-id="3667d-121">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="3667d-122">**explizites CD3DX12 \_ Feld (Long Left, Long Top, Long Front, Long right, Long Bottom, Long Back)**</span><span class="sxs-lookup"><span data-stu-id="3667d-122">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back)**</span></span>
</dt> <dd>

<span data-ttu-id="3667d-123">Erstellt eine neue Instanz eines CD3DX12 Felds \_ und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="3667d-123">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="3667d-124">Long Left</span><span class="sxs-lookup"><span data-stu-id="3667d-124">LONG Left</span></span>

<span data-ttu-id="3667d-125">Langer Anfang</span><span class="sxs-lookup"><span data-stu-id="3667d-125">LONG Top</span></span>

<span data-ttu-id="3667d-126">Lange Vorderseite</span><span class="sxs-lookup"><span data-stu-id="3667d-126">LONG Front</span></span>

<span data-ttu-id="3667d-127">Long right</span><span class="sxs-lookup"><span data-stu-id="3667d-127">LONG Right</span></span>

<span data-ttu-id="3667d-128">Long-Bottom</span><span class="sxs-lookup"><span data-stu-id="3667d-128">LONG Bottom</span></span>

<span data-ttu-id="3667d-129">Lange wieder</span><span class="sxs-lookup"><span data-stu-id="3667d-129">LONG Back</span></span>

</dd> <dt>

<span data-ttu-id="3667d-130">**~ CD3DX12 \_ Box ()**</span><span class="sxs-lookup"><span data-stu-id="3667d-130">**~CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="3667d-131">Zerstört eine Instanz einer CD3DX12 \_ Box.</span><span class="sxs-lookup"><span data-stu-id="3667d-131">Destroys an instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="3667d-132">**Operator Konstanten D3D12 \_ Box& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="3667d-132">**operator const D3D12\_BOX&() const**</span></span>
</dt> <dd>

<span data-ttu-id="3667d-133">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="3667d-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3667d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3667d-134">Requirements</span></span>



| <span data-ttu-id="3667d-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3667d-135">Requirement</span></span> | <span data-ttu-id="3667d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="3667d-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3667d-137">Header</span><span class="sxs-lookup"><span data-stu-id="3667d-137">Header</span></span><br/> | <dl> <span data-ttu-id="3667d-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3667d-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3667d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3667d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3667d-140">**D3D12- \_ Feld**</span><span class="sxs-lookup"><span data-stu-id="3667d-140">**D3D12\_BOX**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[<span data-ttu-id="3667d-141">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="3667d-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





