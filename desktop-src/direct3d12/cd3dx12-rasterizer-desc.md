---
title: CD3DX12_RASTERIZER_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Rasterizer- \_ DESC-Struktur zu ermöglichen.
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- CD3DX12_RASTERIZER_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078b9e92d25cb5309b4cd97d35586192a37eed90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364347"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a><span data-ttu-id="acf1c-104">CD3DX12 \_ Rasterizer- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="acf1c-104">CD3DX12\_RASTERIZER\_DESC structure</span></span>

<span data-ttu-id="acf1c-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Rasterizer- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="acf1c-105">A helper structure to enable easy initialization of a [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf1c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="acf1c-106">Syntax</span></span>


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="acf1c-107">Member</span><span class="sxs-lookup"><span data-stu-id="acf1c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="acf1c-108">**CD3DX12 \_ Rasterizer \_ deaktiviert ()**</span><span class="sxs-lookup"><span data-stu-id="acf1c-108">**CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="acf1c-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Rasterizer-Moduls \_ .</span><span class="sxs-lookup"><span data-stu-id="acf1c-109">Creates a new, uninitialized, instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="acf1c-110">**explizites CD3DX12 \_ Rasterizer-Element \_ (konstant D3D12 \_ Rasterizer- \_& o)**</span><span class="sxs-lookup"><span data-stu-id="acf1c-110">**explicit CD3DX12\_RASTERIZER\_DESC(const D3D12\_RASTERIZER\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="acf1c-111">Erstellt eine neue Instanz eines CD3DX12 \_ Rasterizer-Moduls \_ , das mit dem Inhalt einer anderen [**D3D12 \_ Rasterizer \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) -Erstellungs Struktur initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="acf1c-111">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with the contents of another [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="acf1c-112">**explizites CD3DX12 \_ Rasterizer-Element \_ (CD3DX12- \_ Standard)**</span><span class="sxs-lookup"><span data-stu-id="acf1c-112">**explicit CD3DX12\_RASTERIZER\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="acf1c-113">Erstellt eine neue Instanz eines CD3DX12 \_ Rasterizer- \_ DESC, initialisiert mit Standardparametern.</span><span class="sxs-lookup"><span data-stu-id="acf1c-113">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with default parameters.</span></span>

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

<span data-ttu-id="acf1c-114">**explizites CD3DX12 \_ Rasterizer \_ DESC (D3D12 \_ Fill \_ Mode FillMode, D3D12 \_ cull \_ Mode CullMode, bool frontcounteruhrzeiger Sinn, int depthbias, float depthbiasclamp, float slopescaleddepthbias, bool depthclipenable, bool multisampleenable, bool antialiasedlineenable, uint forcedsamplecount, D3D12 \_ konservative \_ rasterisierungsmodus \_ conservativeraster)**</span><span class="sxs-lookup"><span data-stu-id="acf1c-114">**explicit CD3DX12\_RASTERIZER\_DESC(D3D12\_FILL\_MODE fillMode, D3D12\_CULL\_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE conservativeRaster)**</span></span>
</dt> <dd>

<span data-ttu-id="acf1c-115">Erstellt eine neue Instanz eines CD3DX12 \_ Rasterizer- \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="acf1c-115">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="acf1c-116">[**D3D12 \_ Füllmodus für Füll \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode)</span><span class="sxs-lookup"><span data-stu-id="acf1c-116">[**D3D12\_FILL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode</span></span>

<span data-ttu-id="acf1c-117">[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) CullMode im cull-Modus</span><span class="sxs-lookup"><span data-stu-id="acf1c-117">[**D3D12\_CULL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode</span></span>

<span data-ttu-id="acf1c-118">Bool frontcounteruhrzeiger Sinn</span><span class="sxs-lookup"><span data-stu-id="acf1c-118">BOOL frontCounterClockwise</span></span>

<span data-ttu-id="acf1c-119">INT depthbias</span><span class="sxs-lookup"><span data-stu-id="acf1c-119">INT depthBias</span></span>

<span data-ttu-id="acf1c-120">FLOAT depthbiasclamp</span><span class="sxs-lookup"><span data-stu-id="acf1c-120">FLOAT depthBiasClamp</span></span>

<span data-ttu-id="acf1c-121">FLOAT slopescaleddepthbias</span><span class="sxs-lookup"><span data-stu-id="acf1c-121">FLOAT slopeScaledDepthBias</span></span>

<span data-ttu-id="acf1c-122">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="acf1c-122">BOOL depthClipEnable</span></span>

<span data-ttu-id="acf1c-123">Bool multisampleenable</span><span class="sxs-lookup"><span data-stu-id="acf1c-123">BOOL multisampleEnable</span></span>

<span data-ttu-id="acf1c-124">Bool antialiasedlineenable</span><span class="sxs-lookup"><span data-stu-id="acf1c-124">BOOL antialiasedLineEnable</span></span>

<span data-ttu-id="acf1c-125">Uint forcedsamplecount</span><span class="sxs-lookup"><span data-stu-id="acf1c-125">UINT forcedSampleCount</span></span>

<span data-ttu-id="acf1c-126">[**D3D12 \_ Konservativer \_ rasterisierungsmodus \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeraster</span><span class="sxs-lookup"><span data-stu-id="acf1c-126">[**D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span></span>

</dd> <dt>

<span data-ttu-id="acf1c-127">**~ CD3DX12 \_ Rasterizer- \_ Decoder ()**</span><span class="sxs-lookup"><span data-stu-id="acf1c-127">**~CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="acf1c-128">Zerstört eine Instanz eines CD3DX12 \_ Rasterizer-Moduls \_ .</span><span class="sxs-lookup"><span data-stu-id="acf1c-128">Destroys an instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="acf1c-129">**Operator Konstanten D3D12 \_ Rasterizer- \_& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="acf1c-129">**operator const D3D12\_RASTERIZER\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="acf1c-130">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="acf1c-130">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="acf1c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acf1c-131">Requirements</span></span>



| <span data-ttu-id="acf1c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acf1c-132">Requirement</span></span> | <span data-ttu-id="acf1c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="acf1c-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="acf1c-134">Header</span><span class="sxs-lookup"><span data-stu-id="acf1c-134">Header</span></span><br/> | <dl> <span data-ttu-id="acf1c-135"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="acf1c-135"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acf1c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acf1c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf1c-137">**D3D12 \_ Rasterizer- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="acf1c-137">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[<span data-ttu-id="acf1c-138">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="acf1c-138">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





