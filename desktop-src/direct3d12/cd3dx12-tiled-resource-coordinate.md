---
title: CD3DX12_TILED_RESOURCE_COORDINATE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ Kachel \_ Ressourcen \_ Koordinaten Struktur zu ermöglichen.
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- CD3DX12_TILED_RESOURCE_COORDINATE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354987"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a><span data-ttu-id="b2011-104">CD3DX12 \_ Kacheln der \_ Ressourcen \_ Koordinaten Struktur</span><span class="sxs-lookup"><span data-stu-id="b2011-104">CD3DX12\_TILED\_RESOURCE\_COORDINATE structure</span></span>

<span data-ttu-id="b2011-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Kachel \_ Ressourcen \_ Koordinaten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b2011-105">A helper structure to enable easy initialization of a [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2011-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2011-106">Syntax</span></span>


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a><span data-ttu-id="b2011-107">Member</span><span class="sxs-lookup"><span data-stu-id="b2011-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2011-108">**CD3DX12 \_ gekachelte \_ Ressourcen \_ Koordinate ()**</span><span class="sxs-lookup"><span data-stu-id="b2011-108">**CD3DX12\_TILED\_RESOURCE\_COORDINATE()**</span></span>
</dt> <dd>

<span data-ttu-id="b2011-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ Kachel \_ Ressourcen \_ Koordinate.</span><span class="sxs-lookup"><span data-stu-id="b2011-109">Creates a new, uninitialized, instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE.</span></span>

</dd> <dt>

<span data-ttu-id="b2011-110">**explizite CD3DX12 \_ gekachelte \_ Ressourcen \_ Koordinate (konstant D3D12 \_ gekachelte \_ Ressourcen \_ Koordinate &o)**</span><span class="sxs-lookup"><span data-stu-id="b2011-110">**explicit CD3DX12\_TILED\_RESOURCE\_COORDINATE(const D3D12\_TILED\_RESOURCE\_COORDINATE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="b2011-111">Erstellt eine neue Instanz einer \_ gekachelten \_ Ressourcen \_ Koordinate (CD3DX12), die mit dem Inhalt einer anderen [**D3D12- \_ Kachel \_ Ressourcen \_ Koordinaten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b2011-111">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initialized with the contents of another [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b2011-112">**CD3DX12 \_ gekachelte \_ Ressourcen \_ Koordinate (uint x, uint y, uint z, uint subresource)**</span><span class="sxs-lookup"><span data-stu-id="b2011-112">**CD3DX12\_TILED\_RESOURCE\_COORDINATE(UINT x, UINT y, UINT z, UINT subresource)**</span></span>
</dt> <dd>

<span data-ttu-id="b2011-113">Erstellt eine neue Instanz einer CD3DX12 \_ gekachelten \_ Ressourcen \_ Koordinate und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="b2011-113">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initializing the following parameters:</span></span>

<span data-ttu-id="b2011-114">Uint x</span><span class="sxs-lookup"><span data-stu-id="b2011-114">UINT x</span></span>

<span data-ttu-id="b2011-115">Uint y</span><span class="sxs-lookup"><span data-stu-id="b2011-115">UINT y</span></span>

<span data-ttu-id="b2011-116">Uint z</span><span class="sxs-lookup"><span data-stu-id="b2011-116">UINT z</span></span>

<span data-ttu-id="b2011-117">Uint-unter Quelle</span><span class="sxs-lookup"><span data-stu-id="b2011-117">UINT subresource</span></span>

</dd> <dt>

<span data-ttu-id="b2011-118">**Operator Konstanten D3D12 \_ \_ \_& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="b2011-118">**operator const D3D12\_TILED\_RESOURCE\_COORDINATE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="b2011-119">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="b2011-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2011-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2011-120">Requirements</span></span>



| <span data-ttu-id="b2011-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2011-121">Requirement</span></span> | <span data-ttu-id="b2011-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b2011-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b2011-123">Header</span><span class="sxs-lookup"><span data-stu-id="b2011-123">Header</span></span><br/> | <dl> <span data-ttu-id="b2011-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2011-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2011-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2011-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2011-126">**D3D12 \_ gekachelte \_ Ressourcen \_ Koordinate**</span><span class="sxs-lookup"><span data-stu-id="b2011-126">**D3D12\_TILED\_RESOURCE\_COORDINATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[<span data-ttu-id="b2011-127">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="b2011-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





