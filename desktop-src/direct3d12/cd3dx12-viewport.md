---
title: CD3DX12_VIEWPORT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Viewport-Struktur zu ermöglichen.
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- CD3DX12_VIEWPORT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354409"
---
# <a name="cd3dx12_viewport-structure"></a><span data-ttu-id="b243d-104">CD3DX12 \_ Viewport-Struktur</span><span class="sxs-lookup"><span data-stu-id="b243d-104">CD3DX12\_VIEWPORT structure</span></span>

<span data-ttu-id="b243d-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b243d-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b243d-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="b243d-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b243d-107">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Viewport**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b243d-107">A helper structure to enable easy initialization of a [**D3D12\_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b243d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b243d-108">Syntax</span></span>


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a><span data-ttu-id="b243d-109">Member</span><span class="sxs-lookup"><span data-stu-id="b243d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b243d-110">**CD3DX12 \_ Viewport ()**</span><span class="sxs-lookup"><span data-stu-id="b243d-110">**CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="b243d-111">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Viewports.</span><span class="sxs-lookup"><span data-stu-id="b243d-111">Creates a new, uninitialized, instance of a CD3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="b243d-112">**expliziter CD3DX12 \_ Viewport (konstant D3D12 \_ Viewport& o)**</span><span class="sxs-lookup"><span data-stu-id="b243d-112">**explicit CD3DX12\_VIEWPORT(const D3D12\_VIEWPORT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="b243d-113">Erstellt eine neue Instanz eines CD3DX12 \_ Viewports und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="b243d-113">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="b243d-114">Konstanten D3D12 \_ Viewport& o</span><span class="sxs-lookup"><span data-stu-id="b243d-114">const D3D12\_VIEWPORT& o</span></span>

</dd> <dt>

<span data-ttu-id="b243d-115">**expliziter CD3DX12 \_ Viewport (float-topleftx, float-toplefty, float-Breite, float-Höhe, float mintiefe = D3D12 \_ minimale \_ Tiefe, float maxtiefe = D3D12 \_ Max. \_ Tiefe)**</span><span class="sxs-lookup"><span data-stu-id="b243d-115">**explicit CD3DX12\_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="b243d-116">Erstellt eine neue Instanz eines CD3DX12 \_ Viewports und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="b243d-116">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="b243d-117">FLOAT-topleftx</span><span class="sxs-lookup"><span data-stu-id="b243d-117">FLOAT topLeftX</span></span>

<span data-ttu-id="b243d-118">FLOAT-toplefty</span><span class="sxs-lookup"><span data-stu-id="b243d-118">FLOAT topLeftY</span></span>

<span data-ttu-id="b243d-119">Gleit Komma Breite</span><span class="sxs-lookup"><span data-stu-id="b243d-119">FLOAT width</span></span>

<span data-ttu-id="b243d-120">FLOAT-Höhe</span><span class="sxs-lookup"><span data-stu-id="b243d-120">FLOAT height</span></span>

<span data-ttu-id="b243d-121">FLOAT mintiefe = D3D12 \_ minimale \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="b243d-121">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="b243d-122">FLOAT maxtiefe = D3D12 \_ Maximale \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="b243d-122">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="b243d-123">**expliziter CD3DX12 \_ Viewport (ID3D12Resource \* presource, uint mipslice = 0, float topleftx = 0,0 f, float toplefty = 0,0 f, float mintiefe = D3D12 \_ minimale \_ Tiefe, float maxtiefe = D3D12 \_ Maximale \_ Tiefe)**</span><span class="sxs-lookup"><span data-stu-id="b243d-123">**explicit CD3DX12\_VIEWPORT(ID3D12Resource\* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="b243d-124">Erstellt eine neue Instanz eines CD3DX12 \_ Viewports und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="b243d-124">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="b243d-125">ID3D12Resource- \* präsource</span><span class="sxs-lookup"><span data-stu-id="b243d-125">ID3D12Resource\* pResource</span></span>

<span data-ttu-id="b243d-126">Uint mipslice = 0</span><span class="sxs-lookup"><span data-stu-id="b243d-126">UINT mipSlice = 0</span></span>

<span data-ttu-id="b243d-127">FLOAT topleftx = 0,0 f</span><span class="sxs-lookup"><span data-stu-id="b243d-127">FLOAT topLeftX = 0.0f</span></span>

<span data-ttu-id="b243d-128">FLOAT toplefty = 0,0 f</span><span class="sxs-lookup"><span data-stu-id="b243d-128">FLOAT topLeftY = 0.0f</span></span>

<span data-ttu-id="b243d-129">FLOAT mintiefe = D3D12 \_ minimale \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="b243d-129">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="b243d-130">FLOAT maxtiefe = D3D12 \_ Maximale \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="b243d-130">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="b243d-131">**~ CD3DX12 \_ Viewport ()**</span><span class="sxs-lookup"><span data-stu-id="b243d-131">**~CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="b243d-132">Zerstört eine Instanz eines D3DX12 \_ Viewports.</span><span class="sxs-lookup"><span data-stu-id="b243d-132">Destroys an instance of a D3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="b243d-133">**Operator Konstanten D3D12 \_ Viewport& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="b243d-133">**operator const D3D12\_VIEWPORT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="b243d-134">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="b243d-134">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b243d-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b243d-135">Requirements</span></span>



| <span data-ttu-id="b243d-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b243d-136">Requirement</span></span> | <span data-ttu-id="b243d-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b243d-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b243d-138">Header</span><span class="sxs-lookup"><span data-stu-id="b243d-138">Header</span></span><br/> | <dl> <span data-ttu-id="b243d-139"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b243d-139"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b243d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b243d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b243d-141">**D3D12 \_ Viewport**</span><span class="sxs-lookup"><span data-stu-id="b243d-141">**D3D12\_VIEWPORT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[<span data-ttu-id="b243d-142">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="b243d-142">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





