---
title: CD3DX12_DEPTH_STENCIL_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ tiefen \_ Schablone- \_ DESC-Struktur zu ermöglichen.
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- CD3DX12_DEPTH_STENCIL_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367350"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a><span data-ttu-id="a26e4-104">CD3DX12 \_ Tiefe Schablone-Struktur-Debug- \_ \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="a26e4-104">CD3DX12\_DEPTH\_STENCIL\_DESC structure</span></span>

<span data-ttu-id="a26e4-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ tiefen \_ Schablone- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a26e4-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a26e4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a26e4-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="a26e4-107">Member</span><span class="sxs-lookup"><span data-stu-id="a26e4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a26e4-108">**CD3DX12 \_ tiefen \_ Schablone \_ ()**</span><span class="sxs-lookup"><span data-stu-id="a26e4-108">**CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="a26e4-109">Erstellt eine neue, nicht initialisierte Instanz einer D3DX12- \_ tiefen \_ Schablone \_ .</span><span class="sxs-lookup"><span data-stu-id="a26e4-109">Creates a new, uninitialized, instance of a D3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="a26e4-110">**explizites CD3DX12 \_ tiefen \_ Schablone \_ (konstant D3D12 \_ tiefen Schablone- \_ \_& o)**</span><span class="sxs-lookup"><span data-stu-id="a26e4-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="a26e4-111">Erstellt eine neue Instanz einer D3DX12- \_ tiefen \_ Schablone \_ , die mit dem Inhalt einer anderen [**D3D12- \_ tiefen \_ Schablone \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) -Erstellungs Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a26e4-111">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with the contents of another [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a26e4-112">**explizites CD3DX12 \_ tiefen \_ Schablone \_ (CD3DX12 \_ Standard)**</span><span class="sxs-lookup"><span data-stu-id="a26e4-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="a26e4-113">Erstellt eine neue Instanz einer D3DX12- \_ tiefen \_ Schablone \_ DESC, die mit Standardparametern initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a26e4-113">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with default parameters.</span></span>

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

<span data-ttu-id="a26e4-114">**explizites CD3DX12 \_ tiefen \_ Schablone \_ DESC (bool depthenable, D3D12 \_ Tiefe \_ Write \_ Mask depthschreitemask, D3D12 \_ COMPARISON \_ Func depthfunc, bool stencilenable, Uint8 stencilread Mask, Uint8 stencilbeschreib temask, D3D12 \_ Stencil \_ op frontstencilfailop, D3D12 \_ Stencil \_ op frontstencildepthfailop, D3D12 \_ Stencil \_ op frontstencilpassop, D3D12 \_ COMPARISON \_ Func frontstencilfunc, D3D12 \_ Stencil \_ op backstencilfailop, D3D12 \_ Stencil op \_ backstencildepthfailop, D3D12 \_ Stencil \_ op backstencilpassop, D3D12 \_ Comparison \_ Func backstencilfunc)**</span><span class="sxs-lookup"><span data-stu-id="a26e4-114">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc)**</span></span>
</dt> <dd>

<span data-ttu-id="a26e4-115">Erstellt eine neue Instanz einer D3DX12- \_ tiefen \_ Schablone- \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="a26e4-115">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="a26e4-116">Bool depthenable</span><span class="sxs-lookup"><span data-stu-id="a26e4-116">BOOL depthEnable</span></span>

<span data-ttu-id="a26e4-117">[**D3D12 \_ "Tiefe \_ Schreib \_ Maske**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) " depthschreitemask</span><span class="sxs-lookup"><span data-stu-id="a26e4-117">[**D3D12\_DEPTH\_WRITE\_MASK**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span></span>

<span data-ttu-id="a26e4-118">[**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) -depthfunc</span><span class="sxs-lookup"><span data-stu-id="a26e4-118">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc</span></span>

<span data-ttu-id="a26e4-119">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="a26e4-119">BOOL stencilEnable</span></span>

<span data-ttu-id="a26e4-120">Uint8 stencillesmaske</span><span class="sxs-lookup"><span data-stu-id="a26e4-120">UINT8 stencilReadMask</span></span>

<span data-ttu-id="a26e4-121">Uint8 stencilschreitefrage</span><span class="sxs-lookup"><span data-stu-id="a26e4-121">UINT8 stencilWriteMask</span></span>

<span data-ttu-id="a26e4-122">[**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontstencilfailop</span><span class="sxs-lookup"><span data-stu-id="a26e4-122">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp</span></span>

<span data-ttu-id="a26e4-123">[**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontstencildepthfailop</span><span class="sxs-lookup"><span data-stu-id="a26e4-123">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp</span></span>

<span data-ttu-id="a26e4-124">[**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontstencilpassop</span><span class="sxs-lookup"><span data-stu-id="a26e4-124">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp</span></span>

<span data-ttu-id="a26e4-125">[**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontstencilfunc</span><span class="sxs-lookup"><span data-stu-id="a26e4-125">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc</span></span>

<span data-ttu-id="a26e4-126">[**D3D12 \_ Stencil \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backstencilfailop</span><span class="sxs-lookup"><span data-stu-id="a26e4-126">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp</span></span>

<span data-ttu-id="a26e4-127">[**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backstencildepthfailop</span><span class="sxs-lookup"><span data-stu-id="a26e4-127">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp</span></span>

<span data-ttu-id="a26e4-128">[**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backstencilpassop</span><span class="sxs-lookup"><span data-stu-id="a26e4-128">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp</span></span>

<span data-ttu-id="a26e4-129">[**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) -backstencilfunc</span><span class="sxs-lookup"><span data-stu-id="a26e4-129">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc</span></span>

</dd> <dt>

<span data-ttu-id="a26e4-130">**~ CD3DX12 \_ tiefen \_ Schablone \_ ()**</span><span class="sxs-lookup"><span data-stu-id="a26e4-130">**~CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="a26e4-131">Zerstört eine Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ .</span><span class="sxs-lookup"><span data-stu-id="a26e4-131">Destroys an instance of a CD3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="a26e4-132">**Operator Konstanten D3D12 \_ tiefen \_ Schablone \_& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="a26e4-132">**operator const D3D12\_DEPTH\_STENCIL\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="a26e4-133">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="a26e4-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a26e4-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a26e4-134">Requirements</span></span>



| <span data-ttu-id="a26e4-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a26e4-135">Requirement</span></span> | <span data-ttu-id="a26e4-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a26e4-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a26e4-137">Header</span><span class="sxs-lookup"><span data-stu-id="a26e4-137">Header</span></span><br/> | <dl> <span data-ttu-id="a26e4-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a26e4-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a26e4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a26e4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a26e4-140">**D3D12 \_ tiefen \_ Schablone-Schablone \_**</span><span class="sxs-lookup"><span data-stu-id="a26e4-140">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[<span data-ttu-id="a26e4-141">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="a26e4-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





