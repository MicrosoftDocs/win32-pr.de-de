---
title: CD3DX12_ROOT_SIGNATURE_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-Stamm \_ \_ Signatur \_ DESC-Struktur zu ermöglichen.
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- CD3DX12_ROOT_SIGNATURE_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f89f9cd0f5ad9be08af1fa9c2556ebfbd4fcff1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361899"
---
# <a name="cd3dx12_root_signature_desc-structure"></a><span data-ttu-id="2fa88-104">CD3DX12-Struktur der Stamm \_ \_ Signatur \_ DESC</span><span class="sxs-lookup"><span data-stu-id="2fa88-104">CD3DX12\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="2fa88-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12-Stamm \_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2fa88-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa88-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fa88-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_SIGNATURE_DESC  : public D3D12_ROOT_SIGNATURE_DESC{
       CD3DX12_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       CD3DX12_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init(D3D12_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="2fa88-107">Member</span><span class="sxs-lookup"><span data-stu-id="2fa88-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2fa88-108">**CD3DX12 \_ Stamm \_ Signatur \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="2fa88-108">**CD3DX12\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="2fa88-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ root \_ Signature \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="2fa88-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="2fa88-110">**explizit CD3DX12 \_ Stamm \_ Signatur \_ DESC (konstant D3D12 Stamm \_ \_ Signatur \_ DESC &o)**</span><span class="sxs-lookup"><span data-stu-id="2fa88-110">**explicit CD3DX12\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="2fa88-111">Erstellt eine neue Instanz einer CD3DX12 \_ root \_ Signature \_ DESC, die mit dem Inhalt einer anderen [**D3D12 \_ root \_ Signature \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2fa88-111">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with the contents of another [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2fa88-112">**CD3DX12 \_ root \_ Signature \_ DESC (uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ static \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="2fa88-112">**CD3DX12\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="2fa88-113">Erstellt eine neue Instanz einer CD3DX12 \_ root \_ Signature \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="2fa88-113">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="2fa88-114">Uint numparameters</span><span class="sxs-lookup"><span data-stu-id="2fa88-114">UINT numParameters</span></span>

<span data-ttu-id="2fa88-115">[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Pparameters-Stamm Parameter \* \_</span><span class="sxs-lookup"><span data-stu-id="2fa88-115">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="2fa88-116">Opt Uint numstaticsamplers = 0</span><span class="sxs-lookup"><span data-stu-id="2fa88-116">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="2fa88-117">Opt [**D3D12 \_ Statischer \_ Sampler- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="2fa88-117">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="2fa88-118">Opt [**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="2fa88-118">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="2fa88-119">**CD3DX12 \_ root \_ Signature \_ DESC (CD3DX12 \_ Standard)**</span><span class="sxs-lookup"><span data-stu-id="2fa88-119">**CD3DX12\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="2fa88-120">Erstellt eine neue Instanz einer CD3DX12 \_ root \_ Signature \_ DESC, die mit Standardparametern initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2fa88-120">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with default parameters.</span></span>

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

<span data-ttu-id="2fa88-121">**Inline-init (uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ static \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="2fa88-121">**inline Init(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="2fa88-122">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="2fa88-122">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2fa88-123">Uint numparameters</span><span class="sxs-lookup"><span data-stu-id="2fa88-123">UINT numParameters</span></span>

<span data-ttu-id="2fa88-124">[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Pparameters-Stamm Parameter \* \_</span><span class="sxs-lookup"><span data-stu-id="2fa88-124">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="2fa88-125">Opt Uint numstaticsamplers = 0</span><span class="sxs-lookup"><span data-stu-id="2fa88-125">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="2fa88-126">Opt [**D3D12 \_ Statischer \_ Sampler- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="2fa88-126">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="2fa88-127">Opt [**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="2fa88-127">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="2fa88-128">**static Inline init (D3D12 \_ root \_ Signature \_ DESC &DESC, uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ static \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="2fa88-128">**static inline Init(D3D12\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="2fa88-129">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="2fa88-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2fa88-130">[**D3D12 \_ Stamm \_ Signatur \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="2fa88-130">[**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &desc</span></span>

<span data-ttu-id="2fa88-131">Uint numparameters</span><span class="sxs-lookup"><span data-stu-id="2fa88-131">UINT numParameters</span></span>

<span data-ttu-id="2fa88-132">[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Pparameters-Stamm Parameter \* \_</span><span class="sxs-lookup"><span data-stu-id="2fa88-132">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="2fa88-133">Opt Uint numstaticsamplers = 0</span><span class="sxs-lookup"><span data-stu-id="2fa88-133">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="2fa88-134">Opt [**D3D12 \_ Statischer \_ Sampler- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="2fa88-134">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="2fa88-135">Opt [**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="2fa88-135">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fa88-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fa88-136">Requirements</span></span>



| <span data-ttu-id="2fa88-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fa88-137">Requirement</span></span> | <span data-ttu-id="2fa88-138">Wert</span><span class="sxs-lookup"><span data-stu-id="2fa88-138">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa88-139">Header</span><span class="sxs-lookup"><span data-stu-id="2fa88-139">Header</span></span><br/> | <dl> <span data-ttu-id="2fa88-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fa88-140"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa88-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fa88-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa88-142">**D3D12 \_ Stamm \_ Signatur \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="2fa88-142">**D3D12\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="2fa88-143">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="2fa88-143">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





