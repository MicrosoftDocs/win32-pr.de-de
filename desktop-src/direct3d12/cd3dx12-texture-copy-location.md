---
title: CD3DX12_TEXTURE_COPY_LOCATION-Struktur (D3dx12. h)
description: Eine hilfsstruktur, mit der die einfache Initialisierung einer D3D12- \_ Textur \_ Kopie- \_ Speicherort Struktur aktiviert werden kann.
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- CD3DX12_TEXTURE_COPY_LOCATION Struktur
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5143137f92e38662660588dd89a527f59644126
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365073"
---
# <a name="cd3dx12_texture_copy_location-structure"></a><span data-ttu-id="be7e7-104">\_Struktur des CD3DX12-Textur \_ Kopier \_ Orts</span><span class="sxs-lookup"><span data-stu-id="be7e7-104">CD3DX12\_TEXTURE\_COPY\_LOCATION structure</span></span>

<span data-ttu-id="be7e7-105">Eine hilfsstruktur, mit der die einfache Initialisierung einer [**D3D12- \_ Textur Kopie- \_ \_ Speicherort**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) Struktur aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="be7e7-105">A helper structure to enable easy initialization of a [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7e7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="be7e7-106">Syntax</span></span>


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a><span data-ttu-id="be7e7-107">Member</span><span class="sxs-lookup"><span data-stu-id="be7e7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="be7e7-108">**Speicherort der CD3DX12- \_ Textur \_ Kopie \_ ()**</span><span class="sxs-lookup"><span data-stu-id="be7e7-108">**CD3DX12\_TEXTURE\_COPY\_LOCATION()**</span></span>
</dt> <dd>

<span data-ttu-id="be7e7-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ Textur \_ Kopier Speicher \_ Orts.</span><span class="sxs-lookup"><span data-stu-id="be7e7-109">Creates a new, uninitialized, instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION.</span></span>

</dd> <dt>

<span data-ttu-id="be7e7-110">**expliziter CD3DX12 \_ Textur \_ Kopier \_ Speicherort (konstant D3D12 \_ Textur \_ Kopier \_ Speicherort &o)**</span><span class="sxs-lookup"><span data-stu-id="be7e7-110">**explicit CD3DX12\_TEXTURE\_COPY\_LOCATION(const D3D12\_TEXTURE\_COPY\_LOCATION &o)**</span></span>
</dt> <dd>

<span data-ttu-id="be7e7-111">Erstellt eine neue Instanz eines CD3DX12- \_ Textur \_ Kopier Speicher \_ Orts, der mit dem Inhalt einer anderen [**D3D12- \_ Textur Kopie- \_ \_ Speicherort**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="be7e7-111">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initialized with the contents of another [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

</dd> <dt>

<span data-ttu-id="be7e7-112">**Speicherort der CD3DX12- \_ Textur \_ Kopie \_ (ID3D12Resource \* pRes)**</span><span class="sxs-lookup"><span data-stu-id="be7e7-112">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes)**</span></span>
</dt> <dd>

<span data-ttu-id="be7e7-113">Erstellt eine neue Instanz eines CD3DX12- \_ Textur \_ Kopier Speicher \_ Orts und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="be7e7-113">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="be7e7-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Prä</span><span class="sxs-lookup"><span data-stu-id="be7e7-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

</dd> <dt>

<span data-ttu-id="be7e7-115">**Speicherort der CD3DX12- \_ Textur \_ Kopie \_ (ID3D12Resource \* pRes, D3D12 Speicherort der unter \_ \_ Quelle \_& Speicherbedarf)**</span><span class="sxs-lookup"><span data-stu-id="be7e7-115">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT const& Footprint)**</span></span>
</dt> <dd>

<span data-ttu-id="be7e7-116">Erstellt eine neue Instanz eines CD3DX12- \_ Textur \_ Kopier Speicher \_ Orts und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="be7e7-116">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="be7e7-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Prä</span><span class="sxs-lookup"><span data-stu-id="be7e7-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="be7e7-118">[**D3D12 \_ Der \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) Speicherplatz der untergeordneten Quelle& Speicherbedarf.</span><span class="sxs-lookup"><span data-stu-id="be7e7-118">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) const& Footprint</span></span>

</dd> <dt>

<span data-ttu-id="be7e7-119">**Speicherort der CD3DX12- \_ Textur \_ Kopie \_ (ID3D12Resource \* pRes, uint Sub)**</span><span class="sxs-lookup"><span data-stu-id="be7e7-119">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, UINT Sub)**</span></span>
</dt> <dd>

<span data-ttu-id="be7e7-120">Erstellt eine neue Instanz eines CD3DX12- \_ Textur \_ Kopier Speicher \_ Orts und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="be7e7-120">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="be7e7-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Prä</span><span class="sxs-lookup"><span data-stu-id="be7e7-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="be7e7-122">Uint Sub</span><span class="sxs-lookup"><span data-stu-id="be7e7-122">UINT Sub</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be7e7-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be7e7-123">Requirements</span></span>



| <span data-ttu-id="be7e7-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be7e7-124">Requirement</span></span> | <span data-ttu-id="be7e7-125">Wert</span><span class="sxs-lookup"><span data-stu-id="be7e7-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="be7e7-126">Header</span><span class="sxs-lookup"><span data-stu-id="be7e7-126">Header</span></span><br/> | <dl> <span data-ttu-id="be7e7-127"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="be7e7-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be7e7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be7e7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7e7-129">**Speicherort der D3D12- \_ Textur \_ Kopie \_**</span><span class="sxs-lookup"><span data-stu-id="be7e7-129">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[<span data-ttu-id="be7e7-130">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="be7e7-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





