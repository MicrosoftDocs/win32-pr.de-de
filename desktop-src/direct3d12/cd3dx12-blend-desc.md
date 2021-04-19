---
title: CD3DX12_BLEND_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Blend- \_ DESC-Struktur zu ermöglichen.
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- CD3DX12_BLEND_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363961"
---
# <a name="cd3dx12_blend_desc-structure"></a><span data-ttu-id="65b32-104">CD3DX12 \_ Blend- \_ Entsc-Struktur</span><span class="sxs-lookup"><span data-stu-id="65b32-104">CD3DX12\_BLEND\_DESC structure</span></span>

<span data-ttu-id="65b32-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Blend- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="65b32-105">A helper structure to enable easy initialization of a [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b32-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="65b32-106">Syntax</span></span>


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="65b32-107">Member</span><span class="sxs-lookup"><span data-stu-id="65b32-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="65b32-108">**CD3DX12 \_ Blend-Debug \_ ()**</span><span class="sxs-lookup"><span data-stu-id="65b32-108">**CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="65b32-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Blend- \_ \_ Absc.</span><span class="sxs-lookup"><span data-stu-id="65b32-109">Creates a new, uninitialized, instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="65b32-110">**explizites CD3DX12 \_ Blend- \_ decod (konstant D3D12 \_ Blend- \_& o)**</span><span class="sxs-lookup"><span data-stu-id="65b32-110">**explicit CD3DX12\_BLEND\_DESC(const D3D12\_BLEND\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="65b32-111">Erstellt eine neue Instanz eines CD3DX12 \_ Blend- \_ Inhalts, das mit dem Inhalt einer anderen [**D3D12 \_ \_ Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) -Debug-Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="65b32-111">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with the contents of another [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="65b32-112">**explizites CD3DX12 Blend-Debug \_ \_ (CD3DX12- \_ Standard)**</span><span class="sxs-lookup"><span data-stu-id="65b32-112">**explicit CD3DX12\_BLEND\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="65b32-113">Erstellt eine neue Instanz eines CD3DX12 \_ Blend- \_ DESC, das mit Standardparametern initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="65b32-113">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with default parameters.</span></span>



| <span data-ttu-id="65b32-114">State</span><span class="sxs-lookup"><span data-stu-id="65b32-114">State</span></span>                                   | <span data-ttu-id="65b32-115">Standardwert</span><span class="sxs-lookup"><span data-stu-id="65b32-115">Default Value</span></span>                    |
|-----------------------------------------|----------------------------------|
| <span data-ttu-id="65b32-116">Alpha atocoverageenable</span><span class="sxs-lookup"><span data-stu-id="65b32-116">AlphaToCoverageEnable</span></span>                   | <span data-ttu-id="65b32-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="65b32-117">**FALSE**</span></span>                        |
| <span data-ttu-id="65b32-118">Independentblendenable</span><span class="sxs-lookup"><span data-stu-id="65b32-118">IndependentBlendEnable</span></span>                  | <span data-ttu-id="65b32-119">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="65b32-119">**FALSE**</span></span>                        |
| <span data-ttu-id="65b32-120">RenderTarget \[ 0 \] . Blendbar</span><span class="sxs-lookup"><span data-stu-id="65b32-120">RenderTarget\[0\].BlendEnable</span></span>           | <span data-ttu-id="65b32-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="65b32-121">**FALSE**</span></span>                        |
| <span data-ttu-id="65b32-122">RenderTarget \[ 0 \] . Logicopenable</span><span class="sxs-lookup"><span data-stu-id="65b32-122">RenderTarget\[0\].LogicOpEnable</span></span>         | <span data-ttu-id="65b32-123">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="65b32-123">**FALSE**</span></span>                        |
| <span data-ttu-id="65b32-124">RenderTarget \[ 0 \] . Srcblend</span><span class="sxs-lookup"><span data-stu-id="65b32-124">RenderTarget\[0\].SrcBlend</span></span>              | <span data-ttu-id="65b32-125">D3D12 \_ Blend \_ 1</span><span class="sxs-lookup"><span data-stu-id="65b32-125">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="65b32-126">RenderTarget \[ 0 \] . Destblend</span><span class="sxs-lookup"><span data-stu-id="65b32-126">RenderTarget\[0\].DestBlend</span></span>             | <span data-ttu-id="65b32-127">D3D12 \_ Blend \_ null</span><span class="sxs-lookup"><span data-stu-id="65b32-127">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="65b32-128">RenderTarget \[ 0 \] . Blendop</span><span class="sxs-lookup"><span data-stu-id="65b32-128">RenderTarget\[0\].BlendOp</span></span>               | <span data-ttu-id="65b32-129">D3D12 \_ Blend- \_ op- \_ Add</span><span class="sxs-lookup"><span data-stu-id="65b32-129">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="65b32-130">RenderTarget \[ 0 \] . Srcblendalpha</span><span class="sxs-lookup"><span data-stu-id="65b32-130">RenderTarget\[0\].SrcBlendAlpha</span></span>         | <span data-ttu-id="65b32-131">D3D12 \_ Blend \_ 1</span><span class="sxs-lookup"><span data-stu-id="65b32-131">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="65b32-132">RenderTarget \[ 0 \] . Destblendalpha</span><span class="sxs-lookup"><span data-stu-id="65b32-132">RenderTarget\[0\].DestBlendAlpha</span></span>        | <span data-ttu-id="65b32-133">D3D12 \_ Blend \_ null</span><span class="sxs-lookup"><span data-stu-id="65b32-133">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="65b32-134">RenderTarget \[ 0 \] . Blendopalpha</span><span class="sxs-lookup"><span data-stu-id="65b32-134">RenderTarget\[0\].BlendOpAlpha</span></span>          | <span data-ttu-id="65b32-135">D3D12 \_ Blend- \_ op- \_ Add</span><span class="sxs-lookup"><span data-stu-id="65b32-135">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="65b32-136">RenderTarget \[ 0 \] . Logicop</span><span class="sxs-lookup"><span data-stu-id="65b32-136">RenderTarget\[0\].LogicOp</span></span>               | <span data-ttu-id="65b32-137">D3D12 \_ Logic \_ op \_ NoOp</span><span class="sxs-lookup"><span data-stu-id="65b32-137">D3D12\_LOGIC\_OP\_NOOP</span></span>           |
| <span data-ttu-id="65b32-138">RenderTarget \[ 0 \] . Rendertargetschreitemask</span><span class="sxs-lookup"><span data-stu-id="65b32-138">RenderTarget\[0\].RenderTargetWriteMask</span></span> | <span data-ttu-id="65b32-139">D3D12 \_ Color \_ Write \_ \_ all aktivieren</span><span class="sxs-lookup"><span data-stu-id="65b32-139">D3D12\_COLOR\_WRITE\_ENABLE\_ALL</span></span> |



 

</dd> <dt>

<span data-ttu-id="65b32-140">**~ CD3DX12 \_ Blend-Debug \_ ()**</span><span class="sxs-lookup"><span data-stu-id="65b32-140">**~CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="65b32-141">Zerstört eine Instanz eines CD3DX12 \_ Blend- \_ Entsc.</span><span class="sxs-lookup"><span data-stu-id="65b32-141">Destroys an instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="65b32-142">**Operator Konstanten D3D12 \_ Blend- \_& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="65b32-142">**operator const D3D12\_BLEND\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="65b32-143">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="65b32-143">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65b32-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65b32-144">Requirements</span></span>



| <span data-ttu-id="65b32-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65b32-145">Requirement</span></span> | <span data-ttu-id="65b32-146">Wert</span><span class="sxs-lookup"><span data-stu-id="65b32-146">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="65b32-147">Header</span><span class="sxs-lookup"><span data-stu-id="65b32-147">Header</span></span><br/> | <dl> <span data-ttu-id="65b32-148"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="65b32-148"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b32-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65b32-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b32-150">**D3D12 \_ Blend- \_ Entsc**</span><span class="sxs-lookup"><span data-stu-id="65b32-150">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[<span data-ttu-id="65b32-151">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="65b32-151">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





