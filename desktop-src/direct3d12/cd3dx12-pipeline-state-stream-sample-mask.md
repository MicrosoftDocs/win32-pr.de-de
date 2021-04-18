---
title: CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um eine Beispiel Maske als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: 20116DA1-F56D-42CA-A846-42509FAF88C1
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a498bec1bbf8c4f55f320765272d04cbdd81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365345"
---
# <a name="cd3dx12_pipeline_state_stream_sample_mask-structure"></a><span data-ttu-id="27a33-104">CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ Mask-Struktur</span><span class="sxs-lookup"><span data-stu-id="27a33-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK structure</span></span>

<span data-ttu-id="27a33-105">Eine hilfsstruktur, die verwendet wird, um eine Beispiel Maske als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="27a33-105">A helper structure used to describe a sample mask as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="27a33-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="27a33-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK operator=(UINT const& i);
                                            operator UINT() const;
};
```



## <a name="members"></a><span data-ttu-id="27a33-107">Member</span><span class="sxs-lookup"><span data-stu-id="27a33-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="27a33-108">**CD3DX12 \_ Pipeline \_ State \_ Stream- \_ Beispiel \_ Maske**</span><span class="sxs-lookup"><span data-stu-id="27a33-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>
</dt> <dd>

<span data-ttu-id="27a33-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ Mask.</span><span class="sxs-lookup"><span data-stu-id="27a33-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK.</span></span>

</dd> <dt>

<span data-ttu-id="27a33-110">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ Mask (uint Konstanten &i)**</span><span class="sxs-lookup"><span data-stu-id="27a33-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK(UINT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="27a33-111">Erstellt eine neue Instanz einer CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ Mask, initialisiert mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ subbobject \_ Type \_ Sample \_ Mask** und unter Objekt Data from *i*, a **uint** Sample Mask.</span><span class="sxs-lookup"><span data-stu-id="27a33-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_MASK** and subobject data copied from *i*, a **UINT** sample mask.</span></span>

</dd> <dt>

<span data-ttu-id="27a33-112">**Operator = (uint Konstanten& i)**</span><span class="sxs-lookup"><span data-stu-id="27a33-112">**operator=(UINT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="27a33-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="27a33-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="27a33-114">**Operator uint () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="27a33-114">**operator UINT() const**</span></span>
</dt> <dd>

<span data-ttu-id="27a33-115">Implizite Konvertierung in eine **uint** -Beispiel Maske.</span><span class="sxs-lookup"><span data-stu-id="27a33-115">Implicit conversion to a **UINT** sample mask.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27a33-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27a33-116">Remarks</span></span>

<span data-ttu-id="27a33-117">CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ Mask ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="27a33-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
          
```



## <a name="requirements"></a><span data-ttu-id="27a33-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27a33-118">Requirements</span></span>



| <span data-ttu-id="27a33-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27a33-119">Requirement</span></span> | <span data-ttu-id="27a33-120">Wert</span><span class="sxs-lookup"><span data-stu-id="27a33-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="27a33-121">Header</span><span class="sxs-lookup"><span data-stu-id="27a33-121">Header</span></span><br/> | <dl> <span data-ttu-id="27a33-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="27a33-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27a33-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27a33-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a33-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="27a33-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="27a33-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="27a33-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="27a33-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="27a33-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

