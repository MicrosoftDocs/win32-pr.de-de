---
title: CD3DX12_PIPELINE_STATE_STREAM_FLAGS-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die zum Beschreiben von Pipeline-Statusflags als einzelnes Objekt verwendet wird, das für eine streambeschreibung geeignet ist.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034f4a63c774ca41f28fbe9e6c2945fddee47c4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357280"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a><span data-ttu-id="17e7c-104">CD3DX12 \_ Pipeline \_ - \_ Stream- \_ Flags-Struktur</span><span class="sxs-lookup"><span data-stu-id="17e7c-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS structure</span></span>

<span data-ttu-id="17e7c-105">Eine hilfsstruktur, die zum Beschreiben von Pipeline-Statusflags als einzelnes Objekt verwendet wird, das für eine streambeschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="17e7c-105">A helper structure used to describe pipeline state flags as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e7c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="17e7c-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a><span data-ttu-id="17e7c-107">Member</span><span class="sxs-lookup"><span data-stu-id="17e7c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="17e7c-108">**CD3DX12 \_ - \_ Flags für Pipeline Zustandsdaten \_ Strom \_**</span><span class="sxs-lookup"><span data-stu-id="17e7c-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="17e7c-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Pipeline- \_ \_ \_ StatusStream- \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="17e7c-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="17e7c-110">**CD3DX12 \_ - \_ Flags für Pipeline Zustandsdaten \_ Strom \_ (D3D12 \_ Pipeline- \_ \_ Statusflags Konstanten &i)**</span><span class="sxs-lookup"><span data-stu-id="17e7c-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS(D3D12\_PIPELINE\_STATE\_FLAGS const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="17e7c-111">Erstellt eine neue Instanz der CD3DX12 \_ Pipeline- \_ \_ \_ Statusflags, die mit einem untergeordneten Typ von **D3D12 Pipeline State-untergeordneten \_ \_ \_ \_ typfjektflags \_** und aus *i* kopierten untergeordneten Daten, einer [**D3D12 \_ Pipeline \_ State \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) -Struktur, initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="17e7c-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_FLAGS** and subobject data copied from *i*, a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> <dt>

<span data-ttu-id="17e7c-112">**Operator = (D3D12 \_ Pipeline \_ State \_ Flags Konstanten& i)**</span><span class="sxs-lookup"><span data-stu-id="17e7c-112">**operator=(D3D12\_PIPELINE\_STATE\_FLAGS const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="17e7c-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="17e7c-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="17e7c-114">**Operator D3D12 \_ Pipeline \_ - \_ Statusflags ()**</span><span class="sxs-lookup"><span data-stu-id="17e7c-114">**operator D3D12\_PIPELINE\_STATE\_FLAGS() const**</span></span>
</dt> <dd>

<span data-ttu-id="17e7c-115">Implizite Konvertierung in eine [**D3D12 \_ Pipeline \_ State \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="17e7c-115">Implicit conversion to a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17e7c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17e7c-116">Remarks</span></span>

<span data-ttu-id="17e7c-117">CD3DX12 \_ Pipeline \_ State \_ Stream \_ Flags ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="17e7c-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
```



## <a name="requirements"></a><span data-ttu-id="17e7c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17e7c-118">Requirements</span></span>



| <span data-ttu-id="17e7c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17e7c-119">Requirement</span></span> | <span data-ttu-id="17e7c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="17e7c-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="17e7c-121">Header</span><span class="sxs-lookup"><span data-stu-id="17e7c-121">Header</span></span><br/> | <dl> <span data-ttu-id="17e7c-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="17e7c-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17e7c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17e7c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e7c-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="17e7c-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="17e7c-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="17e7c-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="17e7c-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="17e7c-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

