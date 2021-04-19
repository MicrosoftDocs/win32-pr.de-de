---
title: CD3DX12_CLEAR_VALUE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-Clear-Value-Struktur zu ermöglichen \_ \_ .
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- CD3DX12_CLEAR_VALUE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366442"
---
# <a name="cd3dx12_clear_value-structure"></a><span data-ttu-id="b5d6e-104">CD3DX12 \_ Clear \_ value-Struktur</span><span class="sxs-lookup"><span data-stu-id="b5d6e-104">CD3DX12\_CLEAR\_VALUE structure</span></span>

<span data-ttu-id="b5d6e-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ Clear- \_ value**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b5d6e-105">A helper structure to enable easy initialization of a [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d6e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5d6e-106">Syntax</span></span>


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a><span data-ttu-id="b5d6e-107">Member</span><span class="sxs-lookup"><span data-stu-id="b5d6e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5d6e-108">**CD3DX12 \_ Clear \_ value ()**</span><span class="sxs-lookup"><span data-stu-id="b5d6e-108">**CD3DX12\_CLEAR\_VALUE()**</span></span>
</dt> <dd>

<span data-ttu-id="b5d6e-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Clear- \_ \_ Werts.</span><span class="sxs-lookup"><span data-stu-id="b5d6e-109">Creates a new, uninitialized, instance of a CD3DX12\_CLEAR\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="b5d6e-110">**expliziter CD3DX12 \_ Clear \_ value (konstant D3D12 \_ Clear \_ value &o)**</span><span class="sxs-lookup"><span data-stu-id="b5d6e-110">**explicit CD3DX12\_CLEAR\_VALUE(const D3D12\_CLEAR\_VALUE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="b5d6e-111">Erstellt eine neue Instanz eines CD3DX12 \_ Clear- \_ Werts, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ Clear \_ value**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5d6e-111">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initialized with the contents of another [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b5d6e-112">**CD3DX12 \_ Clear \_ value (DXGI \_ Format Format, Konstante float Color \[ 4 \] )**</span><span class="sxs-lookup"><span data-stu-id="b5d6e-112">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, const FLOAT color\[ 4 \])**</span></span>
</dt> <dd>

<span data-ttu-id="b5d6e-113">Erstellt eine neue Instanz eines CD3DX12 \_ Clear- \_ Werts und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="b5d6e-113">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="b5d6e-114">[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format</span><span class="sxs-lookup"><span data-stu-id="b5d6e-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="b5d6e-115">FLOAT-Farbe \[ 4 \]</span><span class="sxs-lookup"><span data-stu-id="b5d6e-115">FLOAT color\[ 4 \]</span></span>

</dd> <dt>

<span data-ttu-id="b5d6e-116">**CD3DX12 \_ Clear \_ value (DXGI- \_ Format Format, float-Tiefe, Uint8-Schablone)**</span><span class="sxs-lookup"><span data-stu-id="b5d6e-116">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, FLOAT depth, UINT8 stencil)**</span></span>
</dt> <dd>

<span data-ttu-id="b5d6e-117">Erstellt eine neue Instanz eines CD3DX12 \_ Clear- \_ Werts und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="b5d6e-117">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="b5d6e-118">[**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format</span><span class="sxs-lookup"><span data-stu-id="b5d6e-118">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="b5d6e-119">Gleit Komma Tiefe</span><span class="sxs-lookup"><span data-stu-id="b5d6e-119">FLOAT depth</span></span>

<span data-ttu-id="b5d6e-120">Uint8-Schablone</span><span class="sxs-lookup"><span data-stu-id="b5d6e-120">UINT8 stencil</span></span>

</dd> <dt>

<span data-ttu-id="b5d6e-121">**Operator Konstanten D3D12 \_ Clear \_ value& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="b5d6e-121">**operator const D3D12\_CLEAR\_VALUE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="b5d6e-122">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="b5d6e-122">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5d6e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5d6e-123">Requirements</span></span>



| <span data-ttu-id="b5d6e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5d6e-124">Requirement</span></span> | <span data-ttu-id="b5d6e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b5d6e-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d6e-126">Header</span><span class="sxs-lookup"><span data-stu-id="b5d6e-126">Header</span></span><br/> | <dl> <span data-ttu-id="b5d6e-127"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5d6e-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5d6e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5d6e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d6e-129">**D3D12 \_ - \_ Wert löschen**</span><span class="sxs-lookup"><span data-stu-id="b5d6e-129">**D3D12\_CLEAR\_VALUE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[<span data-ttu-id="b5d6e-130">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="b5d6e-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

