---
title: CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um die renderzielformate als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353340"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a><span data-ttu-id="23d3a-104">CD3DX12 \_ - \_ Struktur des Pipeline Status-Stream- \_ \_ \_ Renderziels \_</span><span class="sxs-lookup"><span data-stu-id="23d3a-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS structure</span></span>

<span data-ttu-id="23d3a-105">Eine hilfsstruktur, die verwendet wird, um die renderzielformate als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="23d3a-105">A helper structure used to describe the render target formats as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="23d3a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="23d3a-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a><span data-ttu-id="23d3a-107">Member</span><span class="sxs-lookup"><span data-stu-id="23d3a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="23d3a-108">**CD3DX12 \_ - \_ \_ \_ \_ renderzielformate des Pipeline Zustands Stroms \_**</span><span class="sxs-lookup"><span data-stu-id="23d3a-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>
</dt> <dd>

<span data-ttu-id="23d3a-109">Erstellt eine neue, nicht initialisierte Instanz von \_ \_ \_ \_ \_ renderzielformaten eines CD3DX12 Pipeline-Statusdaten Stroms \_ .</span><span class="sxs-lookup"><span data-stu-id="23d3a-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS.</span></span>

</dd> <dt>

<span data-ttu-id="23d3a-110">**CD3DX12 \_ - \_ \_ \_ renderzielformate des Pipeline Zustands Stroms \_ \_ (D3D12 \_ RT- \_ Format \_ Array konstant &i)**</span><span class="sxs-lookup"><span data-stu-id="23d3a-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS(D3D12\_RT\_FORMAT\_ARRAY const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="23d3a-111">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ State- \_ Stream \_ \_ -renderzielformats \_ , das mit einem untergeordneten Typ von **D3D12 Pipeline State-untergeordneten \_ \_ \_ \_ Typen \_ \_ renderzielformate \_** und aus *i* kopierten untergeordneten Daten, einer Array Struktur im [**D3D12 RT- \_ \_ \_ Format**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) , initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="23d3a-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_RENDER\_TARGET\_FORMATS** and subobject data copied from *i*, a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="23d3a-112">**Operator = (D3D12 \_ RT- \_ Format \_ Array konstant& i)**</span><span class="sxs-lookup"><span data-stu-id="23d3a-112">**operator=(D3D12\_RT\_FORMAT\_ARRAY const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="23d3a-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="23d3a-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="23d3a-114">**Operator D3D12 \_ RT- \_ Format \_ Array () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="23d3a-114">**operator D3D12\_RT\_FORMAT\_ARRAY() const**</span></span>
</dt> <dd>

<span data-ttu-id="23d3a-115">Implizite Konvertierung in eine [**Array Struktur im D3D12 \_ RT- \_ Format \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="23d3a-115">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23d3a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23d3a-116">Remarks</span></span>

<span data-ttu-id="23d3a-117">CD3DX12 \_ Pipeline \_ State \_ Stream \_ \_ -renderzielformate \_ ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="23d3a-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
```



## <a name="requirements"></a><span data-ttu-id="23d3a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23d3a-118">Requirements</span></span>



| <span data-ttu-id="23d3a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23d3a-119">Requirement</span></span> | <span data-ttu-id="23d3a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="23d3a-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="23d3a-121">Header</span><span class="sxs-lookup"><span data-stu-id="23d3a-121">Header</span></span><br/> | <dl> <span data-ttu-id="23d3a-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="23d3a-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23d3a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23d3a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23d3a-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="23d3a-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="23d3a-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="23d3a-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="23d3a-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="23d3a-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

