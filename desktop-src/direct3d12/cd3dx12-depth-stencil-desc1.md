---
title: CD3DX12_DEPTH_STENCIL_DESC1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ tiefen \_ Schablone \_ DESC1-Struktur zu ermöglichen.
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- CD3DX12_DEPTH_STENCIL_DESC1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354990"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a><span data-ttu-id="7c612-104">CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 Struktur</span><span class="sxs-lookup"><span data-stu-id="7c612-104">CD3DX12\_DEPTH\_STENCIL\_DESC1 structure</span></span>

<span data-ttu-id="7c612-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ tiefen \_ Schablone \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7c612-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c612-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c612-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="7c612-107">Member</span><span class="sxs-lookup"><span data-stu-id="7c612-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c612-108">**CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="7c612-108">**CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1.</span><span class="sxs-lookup"><span data-stu-id="7c612-109">Creates a new, uninitialized, instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="7c612-110">**explizite CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 (konstant D3D12 \_ Tiefe \_ Schablone \_ DESC1& o)**</span><span class="sxs-lookup"><span data-stu-id="7c612-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC1& o)**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-111">Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit Werten initialisiert wird, die aus einer [**D3D12- \_ tiefen \_ Schablone \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) -Struktur kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7c612-111">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7c612-112">**explizite CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 (konstant D3D12 \_ tiefen \_ Schablone \_& o)**</span><span class="sxs-lookup"><span data-stu-id="7c612-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-113">Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit Werten initialisiert wird, die aus einer [**D3D12- \_ tiefen Schablone- \_ \_ decoderstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="7c612-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure</span></span>

<span data-ttu-id="7c612-114">und der zusätzliche **depthboundstestenable** -Member ist auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c612-114">and the additional **DepthBoundsTestEnable** member set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7c612-115">**explizite CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 (CD3DX12- \_ Standard)**</span><span class="sxs-lookup"><span data-stu-id="7c612-115">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-116">Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit dem von D3DX12 vorgeschriebenen Standardzustand initialisiert wird:</span><span class="sxs-lookup"><span data-stu-id="7c612-116">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the default state prescribed by D3DX12:</span></span>

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

<span data-ttu-id="7c612-117">**explizite CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 (bool depthenable, D3D12- \_ Tiefe \_ Schreib \_ Maske depthschreitemask, D3D12 \_ COMPARISON \_ Func depthfunc, bool stencilenable, Uint8 stencilread Mask, Uint8 stencilschreitemask, D3D12 \_ Stencil \_ op frontstencilfailop, D3D12 \_ Stencil \_ op frontstencildepthfailop, D3D12 \_ Stencil \_ op frontstencilpassop, D3D12 \_ Comparison \_ Func frontstencilfunc, D3D12 \_ Stencil \_ op backstencilfailop, D3D12 \_ Stencil \_ op backstencildepthfailop, D3D12 \_ Stencil \_ op backstencilpassop, D3D12 \_ COMPARISON \_ Func backstencilfunc, bool depthboundstestenable)**</span><span class="sxs-lookup"><span data-stu-id="7c612-117">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc, BOOL depthBoundsTestEnable)**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-118">Erstellt eine neue Instanz einer CD3DX12- \_ tiefen \_ Schablone \_ DESC1, die mit den in der Parameterliste übergebenen Werten initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7c612-118">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="7c612-119">**~ CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="7c612-119">**~CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-120">Zerstört eine Instanz einer D3DX12- \_ tiefen \_ Schablone \_ DESC1.</span><span class="sxs-lookup"><span data-stu-id="7c612-120">Destroys an instance of a D3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="7c612-121">**Operator Konstanten D3D12 \_ tiefen \_ Schablone \_ DESC1& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="7c612-121">**operator const D3D12\_DEPTH\_STENCIL\_DESC1&() const**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-122">Implizite Konvertierung in eine D3D12 \_ Tiefe \_ Schablone \_ DESC1-Struktur.</span><span class="sxs-lookup"><span data-stu-id="7c612-122">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC1 structure.</span></span> <span data-ttu-id="7c612-123">Da D3D12 \_ Tiefe \_ Schablone \_ DESC1 der zugrunde liegende Typ von CD3DX12 \_ Tiefe \_ Schablone DESC1 ist \_ , wird das Objekt einfach als eine Konstante D3D12-tiefen Schablone zurückgegeben \_ \_ \_ DESC1 Verweis auf sich selbst.</span><span class="sxs-lookup"><span data-stu-id="7c612-123">Because D3D12\_DEPTH\_STENCIL\_DESC1 is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> <dt>

<span data-ttu-id="7c612-124">**Operator Konstanten D3D12 \_ tiefen \_ Schablone \_ () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="7c612-124">**operator const D3D12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-125">Implizite Konvertierung in den Wert einer D3D12- \_ tiefen \_ Schablone- \_ Struktur.</span><span class="sxs-lookup"><span data-stu-id="7c612-125">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC structure value.</span></span> <span data-ttu-id="7c612-126">Da \_ die D3D12 \_ -tiefen Schablone \_ DESC nicht der zugrunde liegende Typ der \_ CD3DX12 \_ -tiefen Schablone \_ DESC1 ist, wird eine neue D3D12 \_ \_ -tiefen Schablone \_ -DESC-Instanz erstellt und als Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c612-126">Because D3D12\_DEPTH\_STENCIL\_DESC is not the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, a new D3D12\_DEPTH\_STENCIL\_DESC instance is created and returned by value.</span></span> <span data-ttu-id="7c612-127">Beachten Sie, dass die D3D12- \_ tiefen \_ Schablone \_ DESC nicht den **depthboundstestenable** -Member enthält, sodass dieser Wert bei der Konvertierung verloren geht.</span><span class="sxs-lookup"><span data-stu-id="7c612-127">Note that D3D12\_DEPTH\_STENCIL\_DESC does not include the **DepthBoundsTestEnable** member, so this value is lost in the conversion.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c612-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c612-128">Requirements</span></span>



| <span data-ttu-id="7c612-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c612-129">Requirement</span></span> | <span data-ttu-id="7c612-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7c612-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7c612-131">Header</span><span class="sxs-lookup"><span data-stu-id="7c612-131">Header</span></span><br/> | <dl> <span data-ttu-id="7c612-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c612-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c612-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c612-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c612-134">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="7c612-134">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="7c612-135">**D3D12 \_ Tiefe \_ Schablone \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="7c612-135">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[<span data-ttu-id="7c612-136">**D3D12 \_ tiefen \_ Schablone-Schablone \_**</span><span class="sxs-lookup"><span data-stu-id="7c612-136">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





