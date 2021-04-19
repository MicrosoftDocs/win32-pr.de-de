---
title: CD3DX12_SUBRESOURCE_FOOTPRINT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12-unter Ressourcen-Speicherplatz \_ \_ Struktur ermöglicht.
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- CD3DX12_SUBRESOURCE_FOOTPRINT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370402"
---
# <a name="cd3dx12_subresource_footprint-structure"></a><span data-ttu-id="492d3-104">CD3DX12 unter Ressourcen-Speicherplatz \_ \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="492d3-104">CD3DX12\_SUBRESOURCE\_FOOTPRINT structure</span></span>

<span data-ttu-id="492d3-105">Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) -unter Ressourcen-Speicherplatz Struktur ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="492d3-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="492d3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="492d3-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a><span data-ttu-id="492d3-107">Member</span><span class="sxs-lookup"><span data-stu-id="492d3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="492d3-108">**CD3DX12 Ressourcen \_ \_ Bedarf ()**</span><span class="sxs-lookup"><span data-stu-id="492d3-108">**CD3DX12\_SUBRESOURCE\_FOOTPRINT()**</span></span>
</dt> <dd>

<span data-ttu-id="492d3-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12-Ressourcen Speicherplatzes \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="492d3-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT.</span></span>

</dd> <dt>

<span data-ttu-id="492d3-110">**expliziter CD3DX12 Ressourcen \_ \_ Bedarf (konstant D3D12 Ressourcenbedarf bei der unter Quelle \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="492d3-110">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_SUBRESOURCE\_FOOTPRINT &o)**</span></span>
</dt> <dd>

<span data-ttu-id="492d3-111">Erstellt eine neue Instanz eines CD3DX12-Speicherplatzes \_ \_ , der mit dem Inhalt einer anderen [**D3D12 \_ subresource \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) -Speicherplatz Struktur initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="492d3-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initialized with the contents of another [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

</dd> <dt>

<span data-ttu-id="492d3-112">**CD3DX12 \_ subresource-Speicher \_ Bedarf (DXGI- \_ Format Format, uint-Breite, uint-Höhe, uint-Tiefe, uint-rowpitch)**</span><span class="sxs-lookup"><span data-stu-id="492d3-112">**CD3DX12\_SUBRESOURCE\_FOOTPRINT(DXGI\_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="492d3-113">Erstellt eine neue Instanz eines CD3DX12-Speicherplatzes für \_ die unter Quelle \_ und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="492d3-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="492d3-114">[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format</span><span class="sxs-lookup"><span data-stu-id="492d3-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="492d3-115">Uint-Breite</span><span class="sxs-lookup"><span data-stu-id="492d3-115">UINT width</span></span>

<span data-ttu-id="492d3-116">Uint-Höhe</span><span class="sxs-lookup"><span data-stu-id="492d3-116">UINT height</span></span>

<span data-ttu-id="492d3-117">Uint-Tiefe</span><span class="sxs-lookup"><span data-stu-id="492d3-117">UINT depth</span></span>

<span data-ttu-id="492d3-118">Uint-rowpitch</span><span class="sxs-lookup"><span data-stu-id="492d3-118">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="492d3-119">**expliziter CD3DX12- \_ \_ Ressourcenbedarf (konstant D3D12 \_ Ressourcen- \_& resdesc, uint rowpitch)**</span><span class="sxs-lookup"><span data-stu-id="492d3-119">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_RESOURCE\_DESC& resDesc, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="492d3-120">Erstellt eine neue Instanz eines CD3DX12-Speicherplatzes für \_ die unter Quelle \_ und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="492d3-120">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="492d3-121">[**D3D12 \_ Ressourcen \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) -& resdesc</span><span class="sxs-lookup"><span data-stu-id="492d3-121">[**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc</span></span>

<span data-ttu-id="492d3-122">Uint-rowpitch</span><span class="sxs-lookup"><span data-stu-id="492d3-122">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="492d3-123">**Operator Konstanten D3D12 Ressourcenbedarf für unter Ressourcen \_ \_& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="492d3-123">**operator const D3D12\_SUBRESOURCE\_FOOTPRINT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="492d3-124">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="492d3-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="492d3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="492d3-125">Requirements</span></span>



| <span data-ttu-id="492d3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="492d3-126">Requirement</span></span> | <span data-ttu-id="492d3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="492d3-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="492d3-128">Header</span><span class="sxs-lookup"><span data-stu-id="492d3-128">Header</span></span><br/> | <dl> <span data-ttu-id="492d3-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="492d3-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="492d3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="492d3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="492d3-131">**D3D12 Ressourcen \_ \_ Bedarf**</span><span class="sxs-lookup"><span data-stu-id="492d3-131">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[<span data-ttu-id="492d3-132">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="492d3-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

